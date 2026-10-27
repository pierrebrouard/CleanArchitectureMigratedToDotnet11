# Task 02 progress
- Changed: all 14 csproj TFM net10.0->net11.0; Microsoft.AspNetCore.{Authentication.JwtBearer,OpenApi,Mvc.Testing}, Microsoft.EntityFrameworkCore.*, Extensions.Caching.StackExchangeRedis, Extensions.Diagnostics.HealthChecks.EntityFrameworkCore -> 11.0.0-rc.1.26425.128.
- Deviation: Microsoft.Extensions.Http.Resilience and ServiceDiscovery have no 11.0.0-rc.1.26425.128 on nuget.org (NU1102, latest 10.11.0); kept at 10.10.0 (net11 compatible). MockQueryable.NSubstitute 10.0.12 third-party, unchanged.
- Command: dotnet restore CleanArchitecture.sln (repo root) -> exit 0. Warnings NU1902/NU1903 System.Security.Cryptography.Pkcs 9.0.13 (transitive, pre-existing; not addressed).
- global.json untouched; nothing committed.
