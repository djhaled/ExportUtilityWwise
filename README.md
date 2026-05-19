# Export Utility Wwise

Console tool that **exports Wwise audio events** from Unreal-based games (Valorant, Sea of Thieves, and others) to **WAV** files—automating repetitive sound extraction.

## What it does

- Reads game archives via CUE4Parse
- Decodes audio with external **vgmstream**
- Writes exports to `MediaExports/` from `AudioExportConfig.json`

## Why it exists

Pulling Wwise events one-by-one was not scalable for personal pipeline work. This utility batches export from a single config file.

## Quick start

1. Build or download a release build of `ExportUtilityWwise.exe`.
2. Install [vgmstream](https://github.com/vgmstream/vgmstream) and ensure it is on your PATH or configured per README in repo.
3. Edit `AudioExportConfig.json` (game directory, AES key, object path, game override).
4. Run:

```bash
dotnet run --project ExportUtilityWwise
```

Outputs land in `MediaExports/`.

Initialize submodules if building from source:

```bash
git submodule update --init --recursive
```

## Requirements

- .NET 6 SDK
- CUE4Parse submodule
- vgmstream
- Local game install and keys as required by your target title

## Project status

See commit history.

## License

See repository license file (README references MIT).
