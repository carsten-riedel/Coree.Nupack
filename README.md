[![Language: C#](https://img.shields.io/badge/language-C%23-blue.svg)](https://github.com/carsten-riedel/Coree.Nupack)
# Coree.Nupack
Coree.Nupack is a C# NuGet package for easy creation of NuGet packages during the build process of consuming projects.

## Project Description
1. **Introduction**<br>
    "Coree.Nupack" is a build dependency NuGet package that simplifies the process of creating and distributing NuGet packages. With "Coree.Nupack", you can create customized NuGet packages quickly and easily, without having to manually adjust your project settings.

2. **Key Features**<br>
    Simplifies the process of creating and distributing NuGet packages
    Automatically generates prerelease and release packages based on your build configuration<br>
    Provides a centralized location for editing package variables, making it easy to customize package metadata across different projects<br>
    Offers default files that can be easily overwritten with customized versions<br>
    Helps save time and reduce costs by streamlining the package creation and distribution process<br>
    Increases efficiency and reduces the risk of errors<br>
    Enables you to create and distribute customized NuGet packages quickly and easily, with consistent metadata and reduced risk of errors, ultimately leading to a more efficient and cost-effective development process.


2. **Dependencies and System Requirements**<br>
Visual Studio 2017 version 15.7 or later (for building NuGet packages using the "dotnet pack" command)<br>
Windows operating system (not tested on Linux or macOS)

1. **Building from Source**<br>
    If you want to build "Coree.Nupack" from source, here are some key steps you'll need to follow:<br>
    To get started, you'll need to clone or fork the "Coree.Nupack" repository on GitHub. This will create a copy of the repository that you can modify and customize to fit your specific needs.<br>
    Rename everything: Since you'll be the release owner of your customized package, you can't use the "Coree.Nupack" name in the NuGet gallery. To avoid conflicts, you'll need to rename everything in the repository to match your own package name.<br>
    Edit the "This" folder: After renaming everything, you'll need to edit the items in the "This" folder to match your own package information.<br>
    Edit the ".csproj" file: Next, you'll need to edit the ".csproj" file to include your own package information and settings.<br>
    Add your Nuget.key file: Finally, you'll need to add a valid "Nuget.key" file to the root of your project. This file should contain your raw NuGet API key, which allows you to push your package to the NuGet gallery.
    You need to remove the line  &lt;NugetKey&gt;&lt;/NugetKey&gt; in .csproj to get it published to nuget gallery.

## Installation
1.  **Requirements and Dependencies** <br>
    Windows 7 SP1 (for vs2017 15.7) <br>
    Visual Studio 2017 version 15.7 and later (nuget pack needed)
2.  **Installation via NuGet Package Manager or Package Manager Console** <br>
    To install "Coree.Nupack", you can use the NuGet Package Manager ->
 [![NuGet](https://img.shields.io/nuget/v/Coree.NuPack.svg)](https://www.nuget.org/packages/Coree.NuPack/)
1. **Manual Installation Instructions (Visual Studio)** <br>
Open the NuGet Package Manager Settings and select "Package Sources".
Add a new package source with the file path or URL to the local package directory. Save the new package source. Browse to the list of availible packages.


## Usage
1. **Configuring "Coree.Nupack" in your project** <br>
   The "Coree.Nupack" package is designed to simplify the process of building and distributing NuGet packages.<br>
   "Coree.Nupack" includes a feature that automatically generates prerelease packages when building in debug mode and release packages when building in release mode. As well as automatic generation of VersionBuild and VersionRevision based on a date logic. This helps ensure that your packages are correctly labeled and versioned.
   You can use the Visual Studio->Build->Pack feature to create and distribute your NuGet packages. Simply as you normally would, and the package will be automatically generated and pushed to the NuGet gallery if the NuGet key in the "NuPack.Secrets.props" file is configured."Coree.Nupack" provides several points of override and customization in the "Coree.NuPack.props" folder. These points allow you to easily edit and replace key elements of your NuGet package. Some of the most common points of override include:<br><br>
"NuPack.Edit.props": This is a major metadata edit point where you can modify your package information to better suit your needs.<br>
"NuPack.Secrets.props": If you've set your API key, the "pack" command will automatically push your package to the NuGet gallery, making it easier to distribute your package to others.<br>
"ICON.png": This file can be easily overridden with your own icon, allowing you to customize the visual appearance of your package.<br>
"LICENSE.txt": If you have your own license, simply replace the default "LICENSE.txt" file with your own to ensure that your package is properly licensed.<br>
"ReleaseNotes.txt": Similarly, if you have specific release notes for your package, replace the default "ReleaseNotes.txt" file with your own notes.<br>
"NuPack.Constants.props": If you want to change the default behavior of the package in some way, you can modify the constants in this file to better suit your needs.<br>

1. **Common Use Cases and Scenarios** <br>
    The "Coree.Nupack" package offers several benefits that can save time and simplify the process of building and distributing NuGet packages. Some common use cases and scenarios include:<br>
    Faster package creation: By providing a pre-configured set of files and variables, "Coree.Nupack" can help reduce the time and effort required to create and customize a NuGet package. This can be particularly useful for developers who need to create multiple packages with similar configurations.
    Simplified editing: "Coree.Nupack" offers a centralized location for editing package variables, which makes it easier to manage and maintain the package. This can help reduce the risk of errors and ensure consistency across different packages.<br>
    Easy customization: "Coree.Nupack" includes default files that can be easily overwritten with customized versions. This allows developers to quickly customize the package to meet their specific requirements, without having to start from scratch.

## License
"Coree.Nupack" is licensed under the MIT License. This means that you are free to use, modify, and distribute the software as long as you include the original copyright notice and disclaimer.
- License: MIT License
- License Text: See [LICENSE](https://github.com/carsten-riedel/Coree.Nupack/blob/main/LICENSE) 

- Disclaimer of Liability: The software is provided "AS IS" without warranty of any kind, either express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose and non-infringement. In no event shall the authors or copyright holders be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the software or the use or other dealings in the software.



