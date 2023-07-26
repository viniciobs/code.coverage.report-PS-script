# Code Coverage Report Generator

This is a PowerShell script for generating code coverage report with [dotnet-reportgenerator](https://www.nuget.org/packages/dotnet-reportgenerator-globaltool).

## How to run
1. Open a PowerShell
2. Type `./report-generator.ps1`

It accepts two optional args:
1. **outputdir**: Defines the output directory where the results will be placed at. The default is `./testresults`
2. **excludeassemblies**: Defines assemblies which will be excluded from code coverage. To specify more than one assembly, separate them by semicolon

### Example
For [this project](https://github.com/viniciobs/Aspnet-Core6.Identiy-with-MongoDB) there some projects that does not need to be tested (in the project owner opinion), they are _Infra_ and _Ioc_. In this case the script should look like
> ./report-generator.ps1 -excludeassemblies:"Infra;Ioc"
