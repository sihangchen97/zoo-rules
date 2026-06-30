# zoo-rules

Curated `.md` rule files for Roo Code agents. Each file drops directly into `.roo/rules/`.

## Quick Install

### Option A: Copy individual files

```bash
cp ponytail.md ~/.roo/rules/
```

### Option B: Submodule + symlinks (recommended for updates)

```bash
# Add as submodule inside .roo/
git -C ~/.roo/ submodule add <repo-url> zoo-rules

# Link the rules you want
mkdir -p ~/.roo/rules
ln -s ~/.roo/zoo-rules/ponytail.md ~/.roo/rules/
```

## Available Rules

| File | Description |
|------|-------------|
| [`conda.md`](conda.md) | Activate conda env (`$ZOO_CONDA_ENV`) before running python/pip |
| [`ponytail.md`](ponytail.md) | Lazy senior dev mode — YAGNI, reuse, minimum code |
| [`python-file-header.md`](python-file-header.md) | Python file header instruction |

## Third-Party Sources

Rules under [`third-party/`](third-party/) contain the upstream repos. The top-level `.md` files are the curated, ready-to-use copies.
