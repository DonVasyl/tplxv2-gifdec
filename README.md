# tplxv2-gifdec
###### a Meson- & C++17-compatible fork of
## "a small C library that can be used to read GIF files"
---
> [!IMPORTANT]
> This file covers only `tplxv2-gifdec` fork-specific information. For more comprehensive
>  gifdec documentation, please refer to the original [README](README) file.

Meson project builds
---
> [!NOTE]
> The following information applies only to the `tplxv2` branch and it's descendants.

To setup project and create the build directory:
```
meson setup builddir
```

To compile the library files & the `gifplay` example:
```
meson compile -C builddir
```

To clean up the artifacts:
```
meson compile --clean -C builddir
```

To install the `gifplay` and the library files in tplxv2-gifdec directory:
```
meson install -C builddir
```
---
