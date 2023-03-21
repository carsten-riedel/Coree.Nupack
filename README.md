# Coree.Nupack
Coree.Nupack is a C# NuGet package for easy creation of NuGet packages during the build process of consuming projects.

## Project Description
- Introduction
- Key Features
- How It Works
- Dependencies and System Requirements
- Building from Source

## Installation
- Requirements and Dependencies
- Installation via NuGet Package Manager or Package Manager Console
- Manual Installation Instructions (if applicable)
- Troubleshooting Installation Issues

## Usage
- Configuring "Coree.Nupack" as a "DevelopmentDependency"
- Creating a Custom Build Task
- Examples
- Common Use Cases and Scenarios

## Contributing
- Guidelines for Contributing
- Code of Conduct and Expectations for Contributors
- Contribution Guidelines
- List of Open Issues and Suggested Contributions

## License
- License Information
- Additional Terms and Conditions
- Legal Notices or Disclaimers


## History

I wanted to create some nuget package lately, while using mainly Visual Studio for development it ended up changing the csproj/targets/props to use the "pack" "dotnet pack" functionality. Then I wanted to split the original project into sub-projects. It ended up in the usual copy and paste orgy because of the static values between projects like icon-author-url etc and the dynamic ones like description-release notes etc. (Lots of file editing) My csproj looked quite ugly, and there was not real workflow. 

## Task

Make it easy make if fast, template it somehow. Import a nuget package that speeds things up somehow. 

## Description

Coree.Nupack is a nuget package to create nuget packages, it it marked as "DevelopmentDependency" so your created packages won't have propergate the reference to Coree.Nupack.
Coree.Nupack injects a folder into your project with a predefined set of file for the creation of your own nuget package. Coree.Nupack is mainly a msbuild target file that is processed before or after the standard msbuild targets. (BeforeBuild,GenerateNuspec,Pack)
It has three main configuration files "NuPack.Constants.props" for thinks that do not change in your regulary, "NuPack.Edit.props" things you should adjust in every project and NuPack.Secrets.props for thinks you don't want to have recoreded in a version history.
In an ideal setup you just add the "Coree.Nupack" package to your project and copy files over from an other project to the new one. (e.g. licence authors, company etc. are the same.)

### Basic workflow should always look like this
- Add the package
```
dotnet add package Coree.NuPack
```

- Edit files or copy over from other project in 
```
$ProjectPath\Coree.NuPack
```

- Use Visual Studio->Build->Pack or dotnet pack to create a nuget package
