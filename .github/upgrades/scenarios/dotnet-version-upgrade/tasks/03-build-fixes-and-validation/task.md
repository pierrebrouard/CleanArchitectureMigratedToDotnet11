# 03-build-fixes-and-validation: Fix build issues and validate the solution

Run a single bounded build-and-fix pass. Known items: source-incompatible `String.Concat(ReadOnlySpan<string>)` (4 uses), binary-incompatible `ConfigurationBinder.GetValue<T>` (ServiceDefaults/Api), and Proto/IntegrationTests API notices. Behavioral notices (HttpContent, Uri, SetEnvironmentVariable, AddSimpleConsole) are advisory; address only with evidence of impact.

## Execution notes (enriched)
- Scope verified: 14 csproj modified (TFM/packages), no source changes yet. Plan: `dotnet build CleanArchitecture.sln`, fix errors/warnings in code, then `dotnet test` on Domain/Application/Infrastructure/gRPC test projects (not IntegrationTests). Decomposition: atomic (single bounded pass).

**Done when**: the whole solution builds with 0 errors (including CleanArchitecture.IntegrationTests, validated by build only since it needs containers), and all other test projects (Domain, Application, Infrastructure, gRPC tests) pass. No commits made.
