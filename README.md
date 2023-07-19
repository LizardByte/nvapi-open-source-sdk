## Summary

This repository contains a mirror of the NVIDIA NVAPI SDK. The SDK is mirrored here to allow for easy integration
into other projects via git submodules.

NVAPI is NVIDIA Corporation's core software development kit that allows access to NVIDIA GPUs and drivers on all
Windows platforms. NVAPI provides support for categories of operations that range beyond the scope of those found in
familiar graphics APIs such as DirectX and OpenGL.

LizardByte is not affiliated with NVIDIA Corporation.

The sdk files can be found in the `sdk` branch of this repository. Each release of the SDK is tagged with an
equivalent tag in this repository, e.g. Release R535 is tagged as `R535`.

## Updates

### SDK updates

There is a workflow that runs once daily to check for new updates to the SDK. If an update is found, it is downloaded
and committed to the `sdk` branch and tagged with the new release number.

### Keeping your project up to date

It is recommended that you use git submodules to integrate the NVAPI SDK into your project. This will allow you to
use @dependabot to keep your project up to date with the latest version of the SDK automatically.

```yml
---
# .github/dependabot.yml

version: 2
updates:
  - package-ecosystem: "gitsubmodule"
    directory: "/"
    schedule:
      interval: "daily"
```
