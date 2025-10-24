# rodent_to_gbif — example repository

## borgefjell branch

In this branch lays the most recent progress on the convertion from COAT format to a Camtrap Data Package.

## General purpose of the repo

This repository holds code and example data for converting camera-trap outputs into Darwin Core / GBIF-ready formats.

Note about local backups
- A local folder `gbif_backups/` exists at the repository root. It contains untracked backup copies of the original large data files (file names ending in `.bak`). These backups are intentionally kept outside version control and are listed in `.gitignore`.
- The repository itself contains a trimmed example (branch `example-trimmed`) with sampled rows to keep the repo small and shareable.

Original full datasets
- The full original datasets are not stored in this repository. If you need to reference or restore the full raw files, retrieve them from the institutional storage location used by your group (e.g. NIRD/Sigma2 storage, S3, or Zenodo). Replace the text below with the exact URL or storage path used by your project:

  ORIGINALS_LOCATION: <update-with-path-or-URL>

Git LFS
- Large files in `raw/` and `processed/` are tracked with Git LFS so the repository can hold example data while managing large binaries efficiently.

If you want me to update the README with an exact storage location or add a short retrieval script, tell me the storage path and I will add it.
# nina-template-r

Modify this `README.md` file, to explain what your software does.

# Additional resources

In addition to this template, here is a list of useful resources you could start from:
- https://github.com/NINAnor/NinaR

# Good practices

## .gitignore

Add paths and files that you do not want to be committed by adding them to .gitignore.

## pre-commit

`pre-commit` can run tools to check your changes and refactor code (using `styler`), to keep your repository clean and avoid common mistakes. The list of actions that are executed are defined in `.pre-commit-config.yaml`.

### Installation

1. Install Python if not available. It can be downloaded from [python.org/downloads](https://www.python.org/downloads/). Be sure to add Python to your PATH.
2. Install `pipx`, as it is the suggested way to install Python tools:
   - Windows users: `py -3 -m pip install pipx`
   - Linux users: `python3 -m pip install pipx`
3. Install `pre-commit`: `pipx install pre-commit`
4. Configure PATH: `pipx ensurepath`
5. Close and open your shell again
6. Enter into your git repository and install the hooks: `pre-commit install` (optional, but recommended)

### How to use it

In case you executed `pre-commit install`, `pre-commit` hooks will be executed each time you will try to commit (`git commit`). If any of the checks fail or if any files that is going to be committed is changed (because a tool refactored or cleaned it), the commit will fail.

The suggested method to use `pre-commit` is to run it before trying to commit your changes, using `pre-commit run -a`. You can run this command multiple times, to check if the changes are ready to be committed.
After all the tests succeeded, the changes can be staged (`git add`) and committed.
