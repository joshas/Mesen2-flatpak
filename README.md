# Mesen2 flatpak

My atempt to run Mesen2 in a flatpak. Using currently latest* version from GitHub, but it might get old very soon.

## Install build dependencies
```
$ flatpak install flathub org.freedesktop.Platform//22.08 org.freedesktop.Sdk//22.08
$ flatpak install org.freedesktop.Sdk.Extension.dotnet6//22.08
$ flatpak install org.freedesktop.Sdk.Extension.llvm15//22.08
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
