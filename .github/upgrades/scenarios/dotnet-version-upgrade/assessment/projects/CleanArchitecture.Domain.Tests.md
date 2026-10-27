# CleanArchitecture.Domain.Tests\CleanArchitecture.Domain.Tests.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** DotNetCoreApp
- **Dependencies**: 1
- **Dependants**: 0
- **Number of Files**: 28
- **Number of Files with Incidents**: 1
- **Lines of Code**: 2068
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (1)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph current["CleanArchitecture.Domain.Tests.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Domain.Tests.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Domain.Tests.md"
    end
    subgraph downstream["Dependencies (1)"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        click P3 "../projects/CleanArchitecture.Domain.md"
    end
    MAIN --> P3

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 727 |  |
| ***Total APIs Analyzed*** | ***727*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| xunit | 2.9.3 | — | 🔵 Optional | Le package NuGet est déconseillé |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

