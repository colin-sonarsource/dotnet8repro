# dotnet8repro
```
colin@MAC-L0034 dotnet8repro % dotnet sonarscanner begin \
  /o:colinmuellerbbc4-1 \
  /k:colinmuellerbbc4-1_dontet \
  /d:sonar.host.url=https://sonarcloud.io
SonarScanner for MSBuild 5.13.1
Using the .NET Core version of the Scanner for MSBuild
Pre-processing started.
Preparing working directories...
10:21:11.483  Updating build integration targets...
10:21:11.998  Fetching analysis configuration settings...
10:21:12.555  Provisioning analyzer assemblies for cs...
10:21:12.555  Installing required Roslyn analyzers...
10:21:12.555  Processing plugin: csharp version 9.12.0.78982
10:21:12.836  Processing plugin: vbnet version 9.12.0.78982
10:21:12.989  Processing plugin: securitycsharpfrontend version 10.3.0-M1.25227
10:21:13.318  Provisioning analyzer assemblies for vbnet...
10:21:13.318  Installing required Roslyn analyzers...
10:21:13.318  Processing plugin: csharp version 9.12.0.78982
10:21:13.323  Processing plugin: vbnet version 9.12.0.78982
10:21:13.331  Incremental PR analysis: Base branch parameter was not provided.
10:21:13.331  Cache data is empty. A full analysis will be performed.
10:21:13.344  Pre-processing succeeded.
colin@MAC-L0034 dotnet8repro % dotnet build
MSBuild version 17.8.0+6cdef4241 for .NET
  Determining projects to restore...
  All projects are up-to-date for restore.
/usr/local/share/dotnet/sdk/8.0.100-rc.2.23502.2/Sdks/Microsoft.NET.Sdk/targets/Microsoft.NET.RuntimeIdentifierInference.targets(311,5): message NETSDK1057: You are using a preview version of .NET. See: https://aka.ms/dotnet-support-policy [/Users/colin/Source/dotnet8repro/dotnet8repro.csproj]
  dotnet8repro -> /Users/colin/Source/dotnet8repro/bin/Debug/net8.0/dotnet8repro.dll

Build succeeded.
    0 Warning(s)
    0 Error(s)

Time Elapsed 00:00:01.78
colin@MAC-L0034 dotnet8repro % dotnet sonarscanner end
SonarScanner for MSBuild 5.13.1
Using the .NET Core version of the Scanner for MSBuild
Post-processing started.
10:21:25.613  The SonarScanner for MSBuild integration failed: SonarCloud was unable to collect the required information about your projects.
Possible causes:
  1. The project has not been built - the project must be built in between the begin and end steps
  2. An unsupported version of MSBuild has been used to build the project. Currently MSBuild 14.0.25420.1 and higher are supported.
  3. The begin, build and end steps have not all been launched from the same folder
  4. None of the analyzed projects have a valid ProjectGuid and you have not used a solution (.sln)
10:21:25.613  Generation of the sonar-properties file failed. Unable to complete the analysis.
10:21:25.615  Post-processing failed. Exit code: 1
```
