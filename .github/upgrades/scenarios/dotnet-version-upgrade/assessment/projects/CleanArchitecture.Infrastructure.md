# CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 2
- **Dependants**: 3
- **Number of Files**: 40
- **Number of Files with Incidents**: 1
- **Lines of Code**: 2358
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (2)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Shared\CleanArchitecture.Shared.csproj](../projects/CleanArchitecture.Shared.md)

**Depended on by (3)** — projects that reference this one:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Api\CleanArchitecture.Api.csproj](../projects/CleanArchitecture.Api.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Infrastructure.Tests\CleanArchitecture.Infrastructure.Tests.csproj](../projects/CleanArchitecture.Infrastructure.Tests.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.IntegrationTests\CleanArchitecture.IntegrationTests.csproj](../projects/CleanArchitecture.IntegrationTests.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (3)"]
        P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
        P7["<b>📦&nbsp;CleanArchitecture.Infrastructure.Tests.csproj</b><br/><small>net10.0</small>"]
        P8["<b>📦&nbsp;CleanArchitecture.IntegrationTests.csproj</b><br/><small>net10.0</small>"]
        click P1 "../projects/CleanArchitecture.Api.md"
        click P7 "../projects/CleanArchitecture.Infrastructure.Tests.md"
        click P8 "../projects/CleanArchitecture.IntegrationTests.md"
    end
    subgraph current["CleanArchitecture.Infrastructure.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Infrastructure.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Infrastructure.md"
    end
    subgraph downstream["Dependencies (2)"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        P12["<b>📦&nbsp;CleanArchitecture.Shared.csproj</b><br/><small>net10.0</small>"]
        click P3 "../projects/CleanArchitecture.Domain.md"
        click P12 "../projects/CleanArchitecture.Shared.md"
    end
    P1 --> MAIN
    P7 --> MAIN
    P8 --> MAIN
    MAIN --> P3
    MAIN --> P12

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 301 |  |
| ***Total APIs Analyzed*** | ***301*** |  |

## NuGet Package Issues

| Package | Current Version | Suggested Version | Severity | Issue |
| :--- | :---: | :---: | :---: | :--- |
| Microsoft.EntityFrameworkCore | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |
| Microsoft.EntityFrameworkCore.Design | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |
| Microsoft.EntityFrameworkCore.Relational | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |
| Microsoft.EntityFrameworkCore.SqlServer | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |
| Microsoft.EntityFrameworkCore.Tools | 11.0.0-rc.1.26425.128 | 11.0.0-rc.3.26522.148 | 🟡 Potential | La mise à niveau du package NuGet est recommandée |

Every project affected by these packages, and the versions the repository settles on: [aggregate NuGet packages](../nuget/aggregate-packages.md).

