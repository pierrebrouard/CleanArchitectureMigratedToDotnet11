# .NET Version Upgrade

## Preferences
- **Flow Mode**: Automatic
- **Target Framework**: net11.0

## Source Control
- **Source Branch**: upgrade/dotnet-11-agent
- **Working Branch**: upgrade/dotnet-11-agent (stay on current branch)
- **Commit Strategy**: Manual (user: commit nothing)
- **Branch Sync**: Disabled

## User Preferences

### Technical Preferences
- Use exact package versions 11.0.0-rc.1.26425.128 wherever a .NET 11 version is required (SDK 11.0.100-rc.1 via global.json).
- Keep third-party packages unchanged unless they block the build.
- Do NOT modify or commit global.json (local setup file). Install nothing globally.
- CleanArchitecture.IntegrationTests needs containers: validate with full solution build plus the other test projects.

## Upgrade Options

### Strategy
| Option | Selected | Why |
|--------|----------|-----|
| Upgrade Strategy | All-at-Once | 14 SDK-style projects all on net10.0, shallow graph, low difficulty everywhere |

### Reliability
| Option | Selected | Why |
|--------|----------|-----|
| Test Coverage | Skip | Default; non-interactive run |

## Strategy
**Selected**: All-at-Once
**Rationale**: 14 modern SDK-style projects (net10.0), all low difficulty, ≤3 tiers deep.

### Execution Constraints
- Single atomic upgrade: all TFMs + packages updated together, then one bounded build-and-fix pass.
- Use exact 11.0.0-rc.1.26425.128 for every .NET 11 package; do not touch global.json; no commits.
- Third-party packages unchanged unless they block the build.
- Validate with full solution build; run all test projects except CleanArchitecture.IntegrationTests (build only, needs containers).

## Decisions
- Non-interactive run: all questions answered with recommended/default options; user cannot answer questions.
- Assumed: stay on current branch, no commits, no branch sync.
