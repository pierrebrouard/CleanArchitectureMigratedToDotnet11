# Projects and dependencies analysis

This document provides a comprehensive overview of the projects and their dependencies in the context of upgrading to .NETCoreApp,Version=v11.0.

Detailed findings live alongside this file in `assessment/`. This page is the index: read it first, then open only the documents you need.

## Table of Contents

- [Executive Summary](#executive-summary)
  - [Highlevel Metrics](#highlevel-metrics)
  - [Projects Compatibility](#projects-compatibility)
  - [Package Compatibility](#package-compatibility)
  - [API Compatibility](#api-compatibility)
- [Top API Migration Challenges](#top-api-migration-challenges)
  - [Technologies and Features](#technologies-and-features)
  - [Most Frequent API Issues](#most-frequent-api-issues)
- [Detailed Reports](#detailed-reports)
  - [Projects Relationship Graph](assessment/project-graph.md)
  - [Aggregate NuGet packages details](assessment/nuget/aggregate-packages.md)
  - [Most Frequent API Issues (complete list)](assessment/api-issues/most-frequent-api-issues.md)
  - [Project Details](#project-details)

## Executive Summary

### Highlevel Metrics

| Metric | Count | Status |
| :--- | :---: | :--- |
| Total Projects | 14 | All require upgrade |
| Total NuGet Packages | 282 | 21 need upgrade |
| Total Code Files | 229 |  |
| Total Code Files with Incidents | 25 |  |
| Total Lines of Code | 11157 |  |
| Total Number of Issues | 66 |  |
| Proposed Target Framework | net11.0 |  |
| Estimated LOC to modify | 25+ | at least 0,2% of codebase |

### Projects Compatibility

| Project | Target Framework | Difficulty | Test Coverage | Package Issues | API Issues | Binding Issues | Est. LOC Impact | Description |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| [CleanArchitecture.Api\CleanArchitecture.Api.csproj](assessment/projects/CleanArchitecture.Api.md) | net10.0 | 🟢 Low | 🧪 Recommended | 6 | 5 | 0 | 5+ | AspNetCore, Sdk Style = True |
| [CleanArchitecture.AppHost\CleanArchitecture.AppHost.csproj](assessment/projects/CleanArchitecture.AppHost.md) | net10.0 | 🟢 Low | — | 5 | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.Application.Tests\CleanArchitecture.Application.Tests.csproj](assessment/projects/CleanArchitecture.Application.Tests.md) | net10.0 | 🟢 Low | — | 1 | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.Application\CleanArchitecture.Application.csproj](assessment/projects/CleanArchitecture.Application.md) | net10.0 | 🟢 Low | — | 1 | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.Domain.Tests\CleanArchitecture.Domain.Tests.csproj](assessment/projects/CleanArchitecture.Domain.Tests.md) | net10.0 | 🟢 Low | — | 1 | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](assessment/projects/CleanArchitecture.Domain.md) | net10.0 | 🟢 Low | — | 0 | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj](assessment/projects/CleanArchitecture.gRPC.Tests.md) | net10.0 | 🟢 Low | — | 1 | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj](assessment/projects/CleanArchitecture.gRPC.md) | net10.0 | 🟢 Low | — | 0 | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.Infrastructure.Tests\CleanArchitecture.Infrastructure.Tests.csproj](assessment/projects/CleanArchitecture.Infrastructure.Tests.md) | net10.0 | 🟢 Low | — | 1 | 0 | 0 |  | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj](assessment/projects/CleanArchitecture.Infrastructure.md) | net10.0 | 🟢 Low | — | 5 | 0 | 0 |  | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.IntegrationTests\CleanArchitecture.IntegrationTests.csproj](assessment/projects/CleanArchitecture.IntegrationTests.md) | net10.0 | 🟢 Low | — | 2 | 15 | 0 | 15+ | DotNetCoreApp, Sdk Style = True |
| [CleanArchitecture.Proto\CleanArchitecture.Proto.csproj](assessment/projects/CleanArchitecture.Proto.md) | net10.0 | 🟢 Low | 🧪 Recommended | 0 | 4 | 0 | 4+ | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.ServiceDefaults\CleanArchitecture.ServiceDefaults.csproj](assessment/projects/CleanArchitecture.ServiceDefaults.md) | net10.0 | 🟢 Low | 🧪 Recommended | 4 | 1 | 0 | 1+ | ClassLibrary, Sdk Style = True |
| [CleanArchitecture.Shared\CleanArchitecture.Shared.csproj](assessment/projects/CleanArchitecture.Shared.md) | net10.0 | 🟢 Low | — | 0 | 0 | 0 |  | ClassLibrary, Sdk Style = True |

🧪 **Test Coverage** — projects risky enough to add behavior-locking tests before upgrading, to catch regressions the upgrade may introduce. Requires the **dotnet-test** plugin.

### Package Compatibility

| Status | Count | Percentage |
| :--- | :---: | :---: |
| ✅ Compatible | 261 | 92,6% |
| ⚠️ Incompatible | 1 | 0,4% |
| 🔄 Upgrade Recommended | 20 | 7,1% |
| ***Total NuGet Packages*** | ***282*** | ***100%*** |

### API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 1 | High - Require code changes |
| 🟡 Source Incompatible | 4 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 20 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 5531 |  |
| ***Total APIs Analyzed*** | ***5556*** |  |

## Top API Migration Challenges

### Technologies and Features

| Technology | Issues | Percentage | Migration Path |
| :--- | :---: | :---: | :--- |

### Most Frequent API Issues

| API | Count | Percentage | Category |
| :--- | :---: | :---: | :--- |
| T:System.Net.Http.HttpContent | 13 | 52,0% | Behavioral Change |
| M:System.String.Concat(System.ReadOnlySpan{System.String}) | 4 | 16,0% | Source Incompatible |
| M:System.Environment.SetEnvironmentVariable(System.String,System.String) | 2 | 8,0% | Behavioral Change |
| M:System.Uri.#ctor(System.String) | 2 | 8,0% | Behavioral Change |
| T:System.Uri | 2 | 8,0% | Behavioral Change |
| M:Microsoft.Extensions.Configuration.ConfigurationBinder.GetValue''1(Microsoft.Extensions.Configuration.IConfiguration,System.String) | 1 | 4,0% | Binary Incompatible |
| M:Microsoft.Extensions.Logging.ConsoleLoggerExtensions.AddSimpleConsole(Microsoft.Extensions.Logging.ILoggingBuilder,System.Action{Microsoft.Extensions.Logging.Console.SimpleConsoleFormatterOptions}) | 1 | 4,0% | Behavioral Change |

The table above is the top 10. See [the complete list](assessment/api-issues/most-frequent-api-issues.md) for every affected API.

## Detailed Reports

- [Projects Relationship Graph](assessment/project-graph.md)
- [Aggregate NuGet packages details](assessment/nuget/aggregate-packages.md)
- [Most Frequent API Issues (complete list)](assessment/api-issues/most-frequent-api-issues.md)

### Project Details

- [CleanArchitecture.Api\CleanArchitecture.Api.csproj](assessment/projects/CleanArchitecture.Api.md)
- [CleanArchitecture.AppHost\CleanArchitecture.AppHost.csproj](assessment/projects/CleanArchitecture.AppHost.md)
- [CleanArchitecture.Application.Tests\CleanArchitecture.Application.Tests.csproj](assessment/projects/CleanArchitecture.Application.Tests.md)
- [CleanArchitecture.Application\CleanArchitecture.Application.csproj](assessment/projects/CleanArchitecture.Application.md)
- [CleanArchitecture.Domain.Tests\CleanArchitecture.Domain.Tests.csproj](assessment/projects/CleanArchitecture.Domain.Tests.md)
- [CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](assessment/projects/CleanArchitecture.Domain.md)
- [CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj](assessment/projects/CleanArchitecture.gRPC.Tests.md)
- [CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj](assessment/projects/CleanArchitecture.gRPC.md)
- [CleanArchitecture.Infrastructure.Tests\CleanArchitecture.Infrastructure.Tests.csproj](assessment/projects/CleanArchitecture.Infrastructure.Tests.md)
- [CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj](assessment/projects/CleanArchitecture.Infrastructure.md)
- [CleanArchitecture.IntegrationTests\CleanArchitecture.IntegrationTests.csproj](assessment/projects/CleanArchitecture.IntegrationTests.md)
- [CleanArchitecture.Proto\CleanArchitecture.Proto.csproj](assessment/projects/CleanArchitecture.Proto.md)
- [CleanArchitecture.ServiceDefaults\CleanArchitecture.ServiceDefaults.csproj](assessment/projects/CleanArchitecture.ServiceDefaults.md)
- [CleanArchitecture.Shared\CleanArchitecture.Shared.csproj](assessment/projects/CleanArchitecture.Shared.md)


