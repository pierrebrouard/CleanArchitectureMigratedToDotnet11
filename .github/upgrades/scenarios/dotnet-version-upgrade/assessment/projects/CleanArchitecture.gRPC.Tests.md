# CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** DotNetCoreApp
- **Dependencies**: 3
- **Dependants**: 0
- **Number of Files**: 6
- **Number of Files with Incidents**: 1
- **Lines of Code**: 235
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (3)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Application\CleanArchitecture.Application.csproj](../projects/CleanArchitecture.Application.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj](../projects/CleanArchitecture.gRPC.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["CleanArchitecture.gRPC.Tests.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.gRPC.Tests.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.gRPC.Tests.md"
    end
    subgraph downstream["Dependencies (3)"]
        P2["<b>📦&nbsp;CleanArchitecture.Application.csproj</b><br/><small>net10.0</small>"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        P9["<b>📦&nbsp;CleanArchitecture.gRPC.csproj</b><br/><small>net10.0</small>"]
        click P2 "../projects/CleanArchitecture.Application.md"
        click P3 "../projects/CleanArchitecture.Domain.md"
        click P9 "../projects/CleanArchitecture.gRPC.md"
    end
    MAIN --> P2
    MAIN --> P3
    MAIN --> P9

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 178 |  |
| ***Total APIs Analyzed*** | ***178*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| xunit | 2.9.3 | — | 🔵 Optional | Le package NuGet est déconseillé |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

