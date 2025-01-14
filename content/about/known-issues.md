---
title: "Known issues - Mach engine"
draft: false
layout: "docs"
docs_type: "about"
rss_ignore: true
---

# Known issues

If you're trying to run the Mach examples or similar, you may be running into one of these known issues.

## nixOS

If you are using nixOS, we have tips on how to use Mach with it [here](../nixos-usage).

## Windows

## File not found

If you encounter an error like this:

![image](/img/windows-symlinks.png)

Windows does not have symlinks enabled, or Git is not configured to use them. This is very annoying and [has been reported to Microsoft](https://twitter.com/slimsag/status/1508114938933362688).

**Two solutions exist:**

1. Enable symlinks in Windows:
   * [Turn on Development Mode](https://docs.microsoft.com/en-us/windows/apps/get-started/enable-your-device-for-development)
   * [Ensure symlinks are installed in Git](https://stackoverflow.com/a/59761201) `git config --global core.symlinks true`
   * Re-clone the repository and try again.
2. Build and run native Windows binaries from inside WSL:
   * `cd mach-examples`
   * `zig build -Dtarget=x86_64-windows textured-cube`
   * Run the native Windows exe in `./zig-out/bin/foo.exe`

### "SSL certificate problem: unable to get local issuer certificate"

This is a curl SSL CA issue, you may want to Google for proper solutions on your system. That said, you can `set CURL_INSECURE=true` and retry to disable SSL verification if you want to workaround the issue.

## Linux

### "Error: vkCreateInstance failed with VK_ERROR_INCOMPATIBLE_DRIVER"

Some distros require packages to be installed to support the Vulkan graphics API.

For instance, Arch Linux has [specific packages](https://wiki.archlinux.org/title/Vulkan#Installation) for Nvidia, Intel and AMD GPUs.

You may also try using OpenGL using the env var `MACH_GPU_BACKEND=opengl`.

### "Error: Couldn't load Vulkan. Searched /tmp/mach/gpu/zig-out/bin/libvulkan.so.1"

We're aware of a bug failing to find `libvulkan.so` on some Linux distros such as [Guix](https://guix.gnu.org/).

```
Error: Couldn't load Vulkan. Searched /tmp/mach/gpu/zig-out/bin/libvulkan.so.1, /tmp/mach/gpu/zig-out/bin/libvulkan.so.1, libvulkan.so.1.
    at operator() (/home/runner/work/mach-gpu-dawn/mach-gpu-dawn/libs/dawn/src/dawn/native/vulkan/BackendVk.cpp:198)
    at Initialize (/home/runner/work/mach-gpu-dawn/mach-gpu-dawn/libs/dawn/src/dawn/native/vulkan/BackendVk.cpp:203)
    at Create (/home/runner/work/mach-gpu-dawn/mach-gpu-dawn/libs/dawn/src/dawn/native/vulkan/BackendVk.cpp:165)
    at operator() (/home/runner/work/mach-gpu-dawn/mach-gpu-dawn/libs/dawn/src/dawn/native/vulkan/BackendVk.cpp:420)

found Null backend on CPU adapter: Null backend,
```

This is [a bug in Dawn](https://github.com/NixOS/nixpkgs/issues/150398), you can workaround it for now by specifying the path to `libvulkan.so` on your system `LD_PRELOAD` like e.g.:

```
LD_PRELOAD=/run/current-system/profile/lib/libvulkan.so zig-out/bin/gpu-hello-triangle
```

## Other

### Choosing a different GitHub download mirror (Chinese users)

**Background**: `zig build` on the first time around will download a 20-30MB file of Dawn (Google's WebGPU implementation) from https://github.com/hexops/mach-gpu-dawn/releases - the build system uses `curl` to do this automatically. You can of course build Dawn from source using the `-Ddawn-from-source=true` flag, but this will require a clone of the Dawn sources which are a larger download and takes a few minutes to build as it is a large C++ codebase.

Users in Chinese mainland may find that download speeds to github.com are too slow (hours to download a 30 MB file), and apparently it is common to use GitHub mirror sites like https://fastgit.org to download files from GitHub.

You can have Mach use such websites by setting an environment variable e.g.:

```sh
MACH_GITHUB_BASE_URL=https://download.fastgit.org
```