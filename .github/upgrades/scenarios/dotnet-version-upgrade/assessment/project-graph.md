# Projects Relationship Graph

[← Back to the assessment index](../assessment.md)

Legend:
📦 SDK-style project
⚙️ Classic project

```mermaid
flowchart LR
    P1["<b>📦&nbsp;CleanArchitecture.Api.csproj</b><br/><small>net10.0</small>"]
    P2["<b>📦&nbsp;CleanArchitecture.Application.csproj</b><br/><small>net10.0</small>"]
    P3["<b>📦&nbsp;CleanArchitecture.Domain.csproj</b><br/><small>net10.0</small>"]
    P4["<b>📦&nbsp;CleanArchitecture.Infrastructure.csproj</b><br/><small>net10.0</small>"]
    P5["<b>📦&nbsp;CleanArchitecture.Application.Tests.csproj</b><br/><small>net10.0</small>"]
    P6["<b>📦&nbsp;CleanArchitecture.Domain.Tests.csproj</b><br/><small>net10.0</small>"]
    P7["<b>📦&nbsp;CleanArchitecture.Infrastructure.Tests.csproj</b><br/><small>net10.0</small>"]
    P8["<b>📦&nbsp;CleanArchitecture.IntegrationTests.csproj</b><br/><small>net10.0</small>"]
    P9["<b>📦&nbsp;CleanArchitecture.gRPC.csproj</b><br/><small>net10.0</small>"]
    P10["<b>📦&nbsp;CleanArchitecture.Proto.csproj</b><br/><small>net10.0</small>"]
    P11["<b>📦&nbsp;CleanArchitecture.gRPC.Tests.csproj</b><br/><small>net10.0</small>"]
    P12["<b>📦&nbsp;CleanArchitecture.Shared.csproj</b><br/><small>net10.0</small>"]
    P13["<b>📦&nbsp;CleanArchitecture.AppHost.csproj</b><br/><small>net10.0</small>"]
    P14["<b>📦&nbsp;CleanArchitecture.ServiceDefaults.csproj</b><br/><small>net10.0</small>"]
    P1 --> P2
    P1 --> P3
    P1 --> P9
    P1 --> P4
    P1 --> P14
    P2 --> P3
    P2 --> P10
    P3 --> P12
    P4 --> P3
    P4 --> P12
    P5 --> P2
    P5 --> P3
    P6 --> P3
    P7 --> P4
    P8 --> P1
    P8 --> P4
    P9 --> P3
    P9 --> P10
    P9 --> P12
    P11 --> P2
    P11 --> P3
    P11 --> P9
    click P1 "projects/CleanArchitecture.Api.md"
    click P2 "projects/CleanArchitecture.Application.md"
    click P3 "projects/CleanArchitecture.Domain.md"
    click P4 "projects/CleanArchitecture.Infrastructure.md"
    click P5 "projects/CleanArchitecture.Application.Tests.md"
    click P6 "projects/CleanArchitecture.Domain.Tests.md"
    click P7 "projects/CleanArchitecture.Infrastructure.Tests.md"
    click P8 "projects/CleanArchitecture.IntegrationTests.md"
    click P9 "projects/CleanArchitecture.gRPC.md"
    click P10 "projects/CleanArchitecture.Proto.md"
    click P11 "projects/CleanArchitecture.gRPC.Tests.md"
    click P12 "projects/CleanArchitecture.Shared.md"
    click P13 "projects/CleanArchitecture.AppHost.md"
    click P14 "projects/CleanArchitecture.ServiceDefaults.md"

```

