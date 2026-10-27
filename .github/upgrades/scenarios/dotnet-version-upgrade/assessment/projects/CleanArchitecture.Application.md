# CleanArchitecture.Application\CleanArchitecture.Application.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 2
- **Dependants**: 3
- **Number of Files**: 32
- **Number of Files with Incidents**: 1
- **Lines of Code**: 1208
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (2)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Proto\CleanArchitecture.Proto.csproj](../projects/CleanArchitecture.Proto.md)

**Depended on by (3)** — projects that reference this one:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Api\CleanArchitecture.Api.csproj](../projects/CleanArchitecture.Api.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Application.Tests\CleanArchitecture.Application.Tests.csproj](../projects/CleanArchitecture.Application.Tests.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj](../projects/CleanArchitecture.gRPC.Tests.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (3)"]
        P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
        P5["<b>📦&nbsp;CleanArchitecture.Application.Tests.csproj</b><br/><small>net10.0</small>"]
        P11["<b>📦&nbsp;CleanArchitecture.gRPC.Tests.csproj</b><br/><small>net10.0</small>"]
        click P1 "../projects/CleanArchitecture.Api.md"
        click P5 "../projects/CleanArchitecture.Application.Tests.md"
        click P11 "../projects/CleanArchitecture.gRPC.Tests.md"
    end
    subgraph current["CleanArchitecture.Application.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Application.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Application.md"
    end
    subgraph downstream["Dependencies (2)"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        P10["<b>📦&nbsp;CleanArchitecture.Proto.csproj</b><br/><small>net10.0</small>"]
        click P3 "../projects/CleanArchitecture.Domain.md"
        click P10 "../projects/CleanArchitecture.Proto.md"
    end
    P1 --> MAIN
    P5 --> MAIN
    P11 --> MAIN
    MAIN --> P3
    MAIN --> P10

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 828 |  |
| ***Total APIs Analyzed*** | ***828*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| Microsoft.EntityFrameworkCore | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

