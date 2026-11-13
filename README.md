# GUNSHOT - VST3 distortion for FL Studio

8 firearm presets x 3 modes (HARD / NORMAL / BIT), JUCE 7, VST3, stereo, 2x oversampled.

## Build on Windows (needs Visual Studio 2022 "Desktop C++" + CMake)
    cmake -B build -G "Visual Studio 17 2022" -A x64
    cmake --build build --config Release

Output: `build\Gunshot_artefacts\Release\VST3\GUNSHOT.vst3`
Copy that folder to `C:\Program Files\Common Files\VST3\`.

## No compiler? Use GitHub
Push this folder to a GitHub repo -> Actions tab -> "Build VST3" -> download the `GUNSHOT-vst3` artifact.

## FL Studio
Options > Manage plugins > Find installed plugins (verify). GUNSHOT appears under Distortion / Fx.

## Notes
- Reported latency (~a few samples) is compensated for the dry signal, so MIX stays phase-aligned.
- BIT mode: SENSITIVITY = how much level/transients drive the effect, DEPTH = how far drive swings, SPEED = how fast it follows.
