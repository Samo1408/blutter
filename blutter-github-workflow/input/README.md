# Blutter input files

Place the two ARM64 Android Flutter libraries in this folder:

- `libapp.so`
- `libflutter.so`

Do not rename the files. Keep proprietary or sensitive binaries private by using a private repository.

Then run the **Blutter Analyze** workflow from the Actions tab, or push a change under `input/`.
The workflow uploads `blutter-output.zip` as an Actions artifact after successful analysis.
