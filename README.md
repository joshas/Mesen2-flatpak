# Mesen2 flatpak

My atempt to run Mesen2 in a flatpak. Using currently latest* version from GitHub, but it might get old very soon.

## Install build dependencies
```
$ flatpak install flathub org.freedesktop.Platform//24.08 org.freedesktop.Sdk//24.08 org.freedesktop.Sdk.Extension.dotnet8//24.08 org.freedesktop.Sdk.Extension.llvm19//24.08
```

## Build and install flatpak
```
$ flatpak-builder --user --install build-dir ca.mesen.Mesen2.yaml
```

## Run flatpak
Flatpak will be available in your desktop environent menu, but you can run it from command line too:
```
$ flatpak run ca.mesen.Mesen2
```

## Update nuget dependencies
Use [Flatpak .NET Generator](https://github.com/flatpak/flatpak-builder-tools/tree/master/dotnet) script to build updated `sources-app.json`. 
```
$ python flatpak-dotnet-generator.py sources-app.json Mesen2-master/UI/UI.csproj
```
