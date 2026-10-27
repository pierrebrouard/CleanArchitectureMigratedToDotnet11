# CleanArchitecture.IntegrationTests\CleanArchitecture.IntegrationTests.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** DotNetCoreApp
- **Dependencies**: 2
- **Dependants**: 0
- **Number of Files**: 22
- **Number of Files with Incidents**: 7
- **Lines of Code**: 1081
- **Estimated LOC to modify**: 15+ (at least 1,4% of the project)

## Related Projects

**Depends on (2)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Api\CleanArchitecture.Api.csproj](../projects/CleanArchitecture.Api.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj](../projects/CleanArchitecture.Infrastructure.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["CleanArchitecture.IntegrationTests.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.IntegrationTests.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.IntegrationTests.md"
    end
    subgraph downstream["Dependencies (2)"]
        P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
        P4["<b>📦&nbsp;CleanArchitecture.Infrastructure.csproj</b><br/><small>net10.0</small>"]
        click P1 "../projects/CleanArchitecture.Api.md"
        click P4 "../projects/CleanArchitecture.Infrastructure.md"
    end
    MAIN --> P1
    MAIN --> P4

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 15 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 457 |  |
| ***Total APIs Analyzed*** | ***472*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| Microsoft.AspNetCore.Mvc.Testing | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |
| Microsoft.EntityFrameworkCore.Proxies | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

