# CleanArchitecture.Application.Tests\CleanArchitecture.Application.Tests.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** DotNetCoreApp
- **Dependencies**: 2
- **Dependants**: 0
- **Number of Files**: 11
- **Number of Files with Incidents**: 1
- **Lines of Code**: 461
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (2)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Application\CleanArchitecture.Application.csproj](../projects/CleanArchitecture.Application.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["CleanArchitecture.Application.Tests.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Application.Tests.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Application.Tests.md"
    end
    subgraph downstream["Dependencies (2)"]
        P2["<b>📦&nbsp;CleanArchitecture.Application.csproj</b><br/><small>net10.0</small>"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        click P2 "../projects/CleanArchitecture.Application.md"
        click P3 "../projects/CleanArchitecture.Domain.md"
    end
    MAIN --> P2
    MAIN --> P3

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 161 |  |
| ***Total APIs Analyzed*** | ***161*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| xunit | 2.9.3 | — | 🔵 Optional | Le package NuGet est déconseillé |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

