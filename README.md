# CDNS_Services
Swift wrapper for libdns_services

## Usage

Here is an example `Package.swift`:

```Swift
import PackageDescription

#if os(macOS)
    let cdns_sd = "CDNS_Services"
#else
    let cdns_sd = "CDNS_SD"
#endif

let package = Package(
    name: "ZeroConfExample",
    dependencies: [
        .Package(url: "https://github.com/rhx/\(cdns_sd).git", majorVersion: 1),
    ],
    swiftLanguageVersions: [3, 4]
)
```

## macOS

This package is for macOS to wrap the `libdns_services.dylib` system library.

## Linux

On Linux, you need to use [CDNS_SD](https://github.com/rhx/CDNS_SD) instead.