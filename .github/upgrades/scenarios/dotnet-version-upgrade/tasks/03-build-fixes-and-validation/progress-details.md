# Progress details: 03-build-fixes-and-validation

## Commands (cwd = repo root)
- `dotnet build CleanArchitecture.sln -nologo -v q` -> exit 0, 0 errors (IntegrationTests built only).
- `dotnet test CleanArchitecture.<P> -nologo --no-restore` for Domain.Tests (84 pass), Application.Tests (9), Infrastructure.Tests (11), gRPC.Tests (4); 0 failures; all net11.0.

## Files modified
None (no source changes were needed). Known notices (String.Concat span, GetValue<T>) produced no compile errors/warnings.

## Remaining warnings (recorded, not suppressed)
- NU1902/NU1903: System.Security.Cryptography.Pkcs 9.0.13 (Infrastructure, Infrastructure.Tests, IntegrationTests) and 10.0.12 + MessagePack 2.5.302 (AppHost) - transitive third-party/SDK packages; not changed to avoid unnecessary package changes.
- ASPIRE010 (AppHost, AspireUseCliBundle=false) - Aspire SDK 13.6.0 notice, not upgrade-related.
- CS0618 in IntegrationTests: NUnit `OrderAttribute` obsolete and Testcontainers parameterless builders obsolete. Come from unchanged third-party packages (pre-existing, unrelated to TFM move); fixing needs test redesign/container image choices, left as-is.

## Deviations / blockers
None. global.json untouched; nothing committed or installed.

## Review
Skipped: no content diff outside workflow artifacts (per step 9). Verdict: N/A.
