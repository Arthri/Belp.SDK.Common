# Belp.SDK.Common
The base of all Belp SDKs: contains common features shared by Belp SDKs.

## Installation
It is not recommended to install Belp.SDK.Common directly.

### Requirements
- A project written in SDK-style. This includes any project for .NET Core(or newer) or .NET 5(or newer).

### Install in Project Manually
1. Locate the project file(for example, `Project.csproj`, `Project.fsproj`).
1. Open the project file in an editor.
1. Add the [`<Sdk Name="Belp.SDK.Common" Version="<VERSION>" />`](https://learn.microsoft.com/en-us/visualstudio/msbuild/sdk-element-msbuild) element under the root `<Project>` element.

## Usage

### Test NuGet package locally
- Run `dotnet pack` with the `-p:DevelopmentNuGet=true` argument.
- Export or set the environment variable `DevelopmentNuGet` to true.

The NuGet package will be pushed to a source named `tmp`. If the source doesn't exist, create a new local NuGet source with `dotnet nuget add source <SOURCE_PATH> --name tmp`.

### Output Packed Package Path to GitHub Actions
Run `dotnet build`, `dotnet pack`, `dotnet msbuild`, or other msbuild aliases with the `-p:BELP_EXPOSE_CI_VARIABLES=true` argument.

## Development

### Prerequisites
- Install .NET 7.0 SDK version 7.0.100 or newer.

### Building (with Visual Studio)
1. Open `Belp.SDK.Common.sln`.
1. Open the Solution Explorer.
1. Right click on the project `Belp.SDK.Common` in the Solution Explorer.
1. Click on `Pack`.

### Building (with .NET CLI)
1. Open a terminal in the repository root.
1. Run `dotnet pack`

### Output
The output is located in `src/Belp.SDK.Common/Belp.SDK.Common/bin/<CONFIGURATION>`.
