# libvudroid.so

[![GitHub Repo](https://img.shields.io/badge/GitHub-Repo-blue?logo=github)](https://github.com/Petr-Kovalev/libvudroid)

This repository provides the source code and pre-compiled binaries for `libvudroid.so`, a shared library commonly used for PDF preview functionality in Android applications. It is based on a fork of the original [Vudroid project](https://code.google.com/archive/p/vudroid/) and has been updated to compile successfully with modern Android NDK versions.

## Overview

`libvudroid.so` is often integrated into Android projects for rendering and previewing PDF files. For example, it powers libraries like [android-pdfview](https://github.com/JoanZapata/android-pdfview).

This fork focuses solely on the JNI components required to build `libvudroid.so`. The full Vudroid project is not included—only the `jni` folder with minor fixes applied to resolve compilation errors when using the latest NDK.

## What's Included

- **Source Code**: The `jni` folder containing the necessary C/C++ sources for building `libvudroid.so`.
- **Pre-compiled Binaries**: Ready-to-use `.so` files in the `libs` folder, compiled for supported CPU architectures (arm64-v8a, x86_64, armeabi-v7a, x86).
- **Build Compatibility**: Compiled using Android NDK version 28.2.13676358.

## Build Instructions

To build `libvudroid.so` from source:

1. Ensure you have the Android NDK installed.
2. Navigate to the repository root.
3. Run the following command (adjust the NDK path as needed):

   ```
   /Users/{username}/Library/Android/sdk/ndk/28.2.13676358/ndk-build --directory=jni
   ```

4. The resulting binaries will be generated in the `libs` folder, organized by CPU architecture.

## Usage

Integrate the compiled `libvudroid.so` into your Android project by placing the appropriate architecture-specific files in your app's libs directory. Refer to projects like [android-pdfview](https://github.com/JoanZapata/android-pdfview) for implementation examples.
