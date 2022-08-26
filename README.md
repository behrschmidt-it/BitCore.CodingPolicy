# BitCore.CodingPolicy

## Description

The BitCore.Coding policy is a collection of naming and coding rules for the C# programming language. The rules are based on the [C# Coding Conventions]("https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions") and the [C# identifier naming rules and conventions]("https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names").

The rules only respect `.cs` files. Code analyzer for other files than .cs code aren't supported right now.

## Analyzer

Following analyzers are configured in the `BitCore.ruleset` file:
| Analyzer | CodeId-Prefix |
|---|---|
| SonarAnalyzer.CSharp | S |
| StyleCop.Analyzers | SA, SX |
| Microsoft.CodeQuality.Analyzers | CA |
| Microsoft.NetCore.Analyzers | CA |
| Microsoft.NetCore.CSharp.Analyzers | CA |
| Microsoft.CodeQuality.CSharp.Analyzers | CA |
| IDisposableAnalyzers | IDISP |

## Files

* BitCore.ruleset: Configuration for Analyzers
* stylecop.json: Further Stylecop.Analyzer rules

## Notes

The `.csproj` is required for `dotnet` to be able to create a nuget package

```console
> dotnet pack --no-build BitCore.CodingPolicy.csproj
```

## Links

* [StyleCop Configuration](https://github.com/DotNetAnalyzers/StyleCopAnalyzers/blob/master/documentation/Configuration.md)
* [Sonar Rules]("https://rules.sonarsource.com/csharp")
