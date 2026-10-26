# Scoop DevTools bucket

Scoop manifests maintained separately from their application code and release archives.

- **MSVC source and release:** https://github.com/0xFais/msvc
- **MSVC package:** `scoop install devtools/msvc`
- **Pinned compiler versions:** `scoop install devtools/msvc-14.44` (also 14.51, 14.40, 14.38 and 14.29)
- **DevTools Studio package:** `scoop install devtools/devtools-studio`

Add this bucket with:

```powershell
scoop bucket add devtools https://github.com/0xFais/scoop-devtools
```

The MSVC manifests download the matching release ZIP from the `0xFais/msvc` repository and verify its SHA256. Microsoft compiler and SDK payloads are downloaded by MSVC directly from Microsoft. Review Microsoft's license terms before installing: https://visualstudio.microsoft.com/license-terms/.

The DevTools Studio manifest downloads its versioned Windows ZIP from the DevTools-Project repository and verifies its SHA256. DevTools Studio requires the .NET 10 Desktop Runtime (x64) and requests administrator access at startup.
