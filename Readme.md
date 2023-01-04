# WPILibInstaller-Avalonia

Welcome to the WPILibInstaller repository, which hosts the source code used to install the various components, libraries, and applications of the wpilibsuite.

## Generating Installers

### Required Dependencies

- DotNetCore 7.0 or higher.
- Java 11

### Building

An installer can be generated by running the following command:

```
gradlew generateInstallers -PXmx3072m -PlinuxBuild -PjenkinsBuild
```

``-PlinuxBuild`` can be replaced with the OS of your choice to build.

- ``-PlinuxBuild``
- ``-PmacBuild``
- ``-PmacBuildArm``
- ``-PwindowsBuild``

If no OS argument is given, it will default to building Windows 64. Additionally, the other gradle options ensure that the build has enough RAM to build properly. It's not recommended to build the installer if your system has less than 4GB of RAM.

## Organization of repository

This is the organization of the repository directories

- WPILibInstaller-Avalonia (Contains the C# application files for the installer UI, as well as the main installer program)
- WPILibShortcutCreator (Contains various scripts to handle creating shortcuts on different OSes)
- apps (Integrates with Gradle into downloading the various WPILib tools and applications needed)
- files (Miscellaneous script files that are used for VSCode integration, and path handling)
- scripts (Core gradle scripts that download required dependencies)

## License

This repository is licensed under BSD 3. Copyright FIRST All rights reserved.
