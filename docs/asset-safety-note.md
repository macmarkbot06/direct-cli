# Asset Safety Note

## Why this matters
Generated assets can create noisy diffs, obscure meaningful changes, and accidentally bloat the repository when they are committed directly.

## Recommended practices
- Keep generated files out of version control by adding them to `.gitignore` when they are not meant to be committed.
- Review the diff for any generated output before staging it, especially when the file is large or changes frequently.
- Prefer storing build artifacts and exports outside the source tree unless they are explicitly required for release or documentation.
- Double-check that regenerated assets are reproducible so reviewers can understand what changed and why.

Large binary files should be reviewed before commit.