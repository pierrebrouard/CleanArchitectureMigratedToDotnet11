# CleanArchitecture.Domain\CleanArchitecture.Domain.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 1
- **Dependants**: 7
- **Number of Files**: 59
- **Number of Files with Incidents**: 1
- **Lines of Code**: 2206
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depends on (1)** — projects this one references:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Shared\CleanArchitecture.Shared.csproj](../projects/CleanArchitecture.Shared.md)

**Depended on by (7)** — projects that reference this one:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Api\CleanArchitecture.Api.csproj](../projects/CleanArchitecture.Api.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Application.Tests\CleanArchitecture.Application.Tests.csproj](../projects/CleanArchitecture.Application.Tests.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Application\CleanArchitecture.Application.csproj](../projects/CleanArchitecture.Application.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain.Tests\CleanArchitecture.Domain.Tests.csproj](../projects/CleanArchitecture.Domain.Tests.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC.Tests\CleanArchitecture.gRPC.Tests.csproj](../projects/CleanArchitecture.gRPC.Tests.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj](../projects/CleanArchitecture.gRPC.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj](../projects/CleanArchitecture.Infrastructure.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (7)"]
        P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
        P2["<b>📦&nbsp;CleanArchitecture.Application.csproj</b><br/><small>net10.0</small>"]
        P4["<b>📦&nbsp;CleanArchitecture.Infrastructure.csproj</b><br/><small>net10.0</small>"]
        P5["<b>📦&nbsp;CleanArchitecture.Application.Tests.csproj</b><br/><small>net10.0</small>"]
        P6["<b>📦&nbsp;CleanArchitecture.Domain.Tests.csproj</b><br/><small>net10.0</small>"]
        P9["<b>📦&nbsp;CleanArchitecture.gRPC.csproj</b><br/><small>net10.0</small>"]
        P11["<b>📦&nbsp;CleanArchitecture.gRPC.Tests.csproj</b><br/><small>net10.0</small>"]
        click P1 "../projects/CleanArchitecture.Api.md"
        click P2 "../projects/CleanArchitecture.Application.md"
        click P4 "../projects/CleanArchitecture.Infrastructure.md"
        click P5 "../projects/CleanArchitecture.Application.Tests.md"
        click P6 "../projects/CleanArchitecture.Domain.Tests.md"
        click P9 "../projects/CleanArchitecture.gRPC.md"
        click P11 "../projects/CleanArchitecture.gRPC.Tests.md"
    end
    subgraph current["CleanArchitecture.Domain.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Domain.md"
    end
    subgraph downstream["Dependencies (1)"]
        P12["<b>📦&nbsp;CleanArchitecture.Shared.csproj</b><br/><small>net10.0</small>"]
        click P12 "../projects/CleanArchitecture.Shared.md"
    end
    P1 --> MAIN
    P2 --> MAIN
    P4 --> MAIN
    P5 --> MAIN
    P6 --> MAIN
    P9 --> MAIN
    P11 --> MAIN
    MAIN --> P12

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 1371 |  |
| ***Total APIs Analyzed*** | ***1371*** |  |

