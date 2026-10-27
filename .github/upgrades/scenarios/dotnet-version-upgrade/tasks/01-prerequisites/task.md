# 01-prerequisites: Verify SDK and toolchain

Confirm the .NET 11 SDK (11.0.100-rc.1) is resolved through the existing `global.json` and that restore works against the required feeds. `global.json` is a local setup file and must not be modified or committed; nothing is installed globally. If the SDK is missing, report it rather than altering the environment.

**Research**: global.json pins 11.0.100-rc.1.26425.128 (rollForward latestFeature, allowPrerelease, paths: dotnet_11_benchmark/.dotnet, $host$). Verification-only task; no source edits. Decomposition: atomic.

**Done when**: `dotnet --version` resolves to the 11.0.100-rc.1 SDK using the unchanged `global.json`, and `global.json` has no diff.
