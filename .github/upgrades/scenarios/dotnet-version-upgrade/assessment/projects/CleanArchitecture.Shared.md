# CleanArchitecture.Shared\CleanArchitecture.Shared.csproj

[← Back to the assessment index](../../assessment.md)

## Project Info

- **Current Target Framework:** net10.0
- **Proposed Target Framework:** net11.0
- **SDK-style**: True
- **Project Kind:** ClassLibrary
- **Dependencies**: 0
- **Dependants**: 3
- **Number of Files**: 12
- **Number of Files with Incidents**: 1
- **Lines of Code**: 164
- **Estimated LOC to modify**: 0+ (at least 0,0% of the project)

## Related Projects

**Depended on by (3)** — projects that reference this one:

- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Domain\CleanArchitecture.Domain.csproj](../projects/CleanArchitecture.Domain.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.gRPC\CleanArchitecture.gRPC.csproj](../projects/CleanArchitecture.gRPC.md)
- [C:\Users\pierr\projets\CleanArchitecture-upgrade-agent\CleanArchitecture.Infrastructure\CleanArchitecture.Infrastructure.csproj](../projects/CleanArchitecture.Infrastructure.md)

## Dependency Graph

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart TB
    subgraph upstream["Dependants (3)"]
        P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
        P4["<b>📦&nbsp;CleanArchitecture.Infrastructure.csproj</b><br/><small>net10.0</small>"]
        P9["<b>📦&nbsp;CleanArchitecture.gRPC.csproj</b><br/><small>net10.0</small>"]
        click P3 "../projects/CleanArchitecture.Domain.md"
        click P4 "../projects/CleanArchitecture.Infrastructure.md"
        click P9 "../projects/CleanArchitecture.gRPC.md"
    end
    subgraph current["CleanArchitecture.Shared.csproj"]
        MAIN["<b>📦&nbsp;CleanArchitecture.Shared.csproj</b><br/><small>net10.0</small>"]
        click MAIN "../projects/CleanArchitecture.Shared.md"
    end
    P3 --> MAIN
    P4 --> MAIN
    P9 --> MAIN

```

## API Compatibility

| Category | Count | Impact |
| :--- | :---: | :--- |
| 🔴 Binary Incompatible | 0 | High - Require code changes |
| 🟡 Source Incompatible | 0 | Medium - Needs re-compilation and potential conflicting API error fixing |
| 🔵 Behavioral change | 0 | Low - Behavioral changes that may require testing at runtime |
| ✅ Compatible | 258 |  |
| ***Total APIs Analyzed*** | ***258*** |  |

