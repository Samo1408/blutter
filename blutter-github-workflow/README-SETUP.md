# Blutter GitHub Actions setup

This bundle adds a GitHub Actions workflow to the root of the `worawit/blutter` repository (or your fork).

## Install
1. Copy `.github/workflows/blutter.yml` into the same path in your repository.
2. Add `input/libapp.so` and `input/libflutter.so` to the repository.
3. Open **Actions → Blutter Analyze → Run workflow**.
4. When the job succeeds, open its run summary and download the `blutter-output` artifact ZIP.

The workflow also runs when files under `input/` change.

## Notes
- The runner uses Ubuntu 24.04 and GCC/G++ 13.
- Blutter may compile a Dart runtime for the target version, so first runs can take a long time.
- The workflow has a six-hour job timeout; GitHub runner limits and upstream downloads/build failures may still affect a run.
- The output artifact is retained for 14 days.
- Keep the repository private if the binaries or analysis output are sensitive.
