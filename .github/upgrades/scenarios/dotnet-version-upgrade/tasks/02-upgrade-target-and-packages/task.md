# 02-upgrade-target-and-packages: Retarget all projects to net11.0 and update packages

Update `TargetFramework` to `net11.0` in all 14 projects (Api, AppHost, Application, Domain, Infrastructure, Shared, gRPC, Proto, ServiceDefaults and the five test projects incl. IntegrationTests). Bump the ~21 packages flagged in the assessment to the exact version `11.0.0-rc.1.26425.128` wherever a .NET 11 version applies (Microsoft.Extensions.*, ASP.NET Core, EF Core, etc.); keep third-party packages unchanged unless they block restore/build. One package is flagged incompatible — see assessment/nuget/aggregate-packages.md and handle it only if it blocks.

**Done when**: all projects target net11.0, .NET-owned packages reference exactly 11.0.0-rc.1.26425.128, and `dotnet restore` succeeds for the solution.

## Research (executor)
- Verified 14 csproj, all net10.0, no Directory.Build.props/Directory.Packages.props. Exact scope: all csproj TargetFramework -> net11.0.
- Packages at 10.0.12 (Microsoft-owned) -> 11.0.0-rc.1.26425.128: AspNetCore.Authentication.JwtBearer, AspNetCore.OpenApi, EFCore(.Design/.Proxies/.Relational/.SqlServer/.Tools), Extensions.Caching.StackExchangeRedis, Extensions.Diagnostics.HealthChecks.EntityFrameworkCore, AspNetCore.Mvc.Testing.
- Microsoft.Extensions.Http.Resilience / ServiceDiscovery 10.10.0 (Extensions family, separate versioning): try exact version, keep if unavailable. MockQueryable 10.0.12 is third-party: unchanged.
- Decomposition: atomic (All-at-Once, mechanical edits).
