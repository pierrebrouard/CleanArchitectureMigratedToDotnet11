# CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 3
- **Dependants**: 2
- **Number of Files**: 8
- **Number of Files with Incidents**: 1
- **Lines of Code**: 182
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (3)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Proto\CleanArchitecture.Proto.csproj](../projects/CleanArchitecture.Proto.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Shared\CleanArchitecture.Shared.csproj](../projects/CleanArchitecture.Shared.md)

**Depended on by (2)** — projects that reference this one:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Api\CleanArchitecture.Api.csproj](../projects/CleanArchitecture.Api.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj](../projects/CleanArchitecture.gRPC.Tests.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (2)"]
        P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
        P11["<b>📦&nbsp;CleanArchitecture.gRPC.Tests.csproj</b><br/><small>net10.0</small>"]
        click P1 "../projects/CleanArchitecture.Api.md"
        click P11 "../projects/CleanArchitecture.gRPC.Tests.md"
    end
    subgraph current["CleanArchitecture.gRPC.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.gRPC.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.gRPC.md"
    end
    subgraph downstream["Dependencies (3)"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        P10["<b>📦&nbsp;CleanArchitecture.Proto.csproj</b><br/><small>net10.0</small>"]
        P12["<b>📦&nbsp;CleanArchitecture.Shared.csproj</b><br/><small>net10.0</small>"]
        click P3 "../projects/CleanArchitecture.Domain.md"
        click P10 "../projects/CleanArchitecture.Proto.md"
        click P12 "../projects/CleanArchitecture.Shared.md"
    end
    P1 --> MAIN
    P11 --> MAIN
    MAIN --> P3
    MAIN --> P10
    MAIN --> P12

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 62 |  |
| ***Total APIs Analyzed*** | ***62*** |  |

