# .NET Version Upgrade Plan

## Overview

**Target**: Upgrade all projects from net10.0 to net11.0 (SDK 11.0.100-rc.1, packages 11.0.0-rc.1.26425.128)
**Scope**: 14 SDK-style projects, ~11k LOC, low difficulty everywhere; ~25 API incidents mostly behavioral

### Selected Strategy
**All-At-Once** — All projects upgraded simultaneously in a single operation.
**Rationale**: 14 projects, all on net10.0, clear shallow dependency structure.

## Upgrade Options

| Option | Selected | Why |
|--------|----------|-----|
| Upgrade Strategy | All-at-Once | ≤15 modern SDK-style projects, low complexity |
| Test Coverage | Skip | Default for non-interactive run |

## Tasks

### 01-prerequisites: Verify SDK and toolchain

Confirm the .NET 11 SDK (11.0.100-rc.1) is resolved through the existing `global.json` and that restore works against the required feeds. `global.json` is a local setup file and must not be modified or committed; nothing is installed globally. If the SDK is missing, report it rather than altering the environment.

**Done when**: `dotnet --version` resolves to the 11.0.100-rc.1 SDK using the unchanged `global.json`, and `global.json` has no diff.

---

### 02-upgrade-target-and-packages: Retarget all projects to net11.0 and update packages

Update `TargetFramework` to `net11.0` in all 14 projects (Api, AppHost, Application, Domain, Infrastructure, Shared, gRPC, Proto, ServiceDefaults and the five test projects incl. IntegrationTests). Bump the ~21 packages flagged in the assessment to the exact version `11.0.0-rc.1.26425.128` wherever a .NET 11 version applies (Microsoft.Extensions.*, ASP.NET Core, EF Core, etc.); keep third-party packages unchanged unless they block restore/build. One package is flagged incompatible — see assessment/nuget/aggregate-packages.md and handle it only if it blocks.

**Done when**: all projects target net11.0, .NET-owned packages reference exactly 11.0.0-rc.1.26425.128, and `dotnet restore` succeeds for the solution.

---

### 03-build-fixes-and-validation: Fix build issues and validate the solution

Run a single bounded build-and-fix pass. Known items: source-incompatible `String.Concat(ReadOnlySpan<string>)` (4 uses), binary-incompatible `ConfigurationBinder.GetValue<T>` (ServiceDefaults/Api), and Proto/IntegrationTests API notices. Behavioral notices (HttpContent, Uri, SetEnvironmentVariable, AddSimpleConsole) are advisory; address only with evidence of impact.

**Done when**: the whole solution builds with 0 errors (including CleanArchitecture.IntegrationTests, validated by build only since it needs containers), and all other test projects (Domain, Application, Infrastructure, gRPC tests) pass. No commits made.
