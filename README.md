# Belp.SDK.Common
The base of all Belp SDKs: contains common features shared by Belp SDKs.

## Installation
It is not recommended to install Belp.SDK.Common directly.

### Requirements
- A project written in SDK-style. This includes any project for .NET Core(or newer) or .NET 5(or newer).

### Install using an Editor
1. Locate the project file(for example, `Project.csproj`, `Project.fsproj`).
1. Open the project file in an editor.
1. Add a new `Sdk` element under the root `Project` element with the `Name` attribute set to `Belp.SDK.Common` and the `Version` attribute set to `1.0.0`. For example, `<Sdk Name="Belp.SDK.Common" Version="1.0.0" />`.

## Usage

### Import SDK
`Belp.SDK.Common` is additive and functions in conjunction with another SDK, such as `Microsoft.NET.Sdk`. It is recommended to import `Belp.SDK.Common`'s `Sdk.props` before any others, and import its `Sdk.targets` after all others.

### Test NuGet package locally
- Run `dotnet pack` with the `-p:DevelopmentNuGet=true` argument.
- Export or set the environment variable `DevelopmentNuGet` to true.

The NuGet package will be pushed to a source named `tmp`. If the source doesn't exist, create a new local NuGet source with `dotnet nuget add source <SOURCE_PATH> --name tmp`.

## Development

### Prerequisites
- Install the .NET 7.0 SDK version 7.0.100 or newer.

### Building with Visual Studio
1. Open `Belp.SDK.Common.sln`.
1. Open the Solution Explorer.
1. Right click on the project `Belp.SDK.Common` in the Solution Explorer.
1. Click on `Pack`.

### Building with .NET CLI
1. Open a terminal in the repository root.
1. Run `dotnet pack`

### Output
By default, the output is located in `src/Belp.SDK.Common/Belp.SDK.Common/bin/Release/`.
