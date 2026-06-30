# zoo-rules

Curated `.md` rule files for Roo Code agents. Each file drops directly into `.roo/rules/`.

## Quick Install

Paths below are workspace-relative. For global install, replace `.roo/` with `~/.roo/`.

### Option A: Copy individual files

```bash
cp conda.md .roo/rules/
```

### Option B: Clone + symlinks (workspace is NOT a git repo)

```bash
git clone https://github.com/sihangchen97/zoo-rules.git .roo/zoo-rules
mkdir -p .roo/rules
cd .roo/rules
ln -s ../zoo-rules/conda.md .
```

### Option C: Submodule + symlinks (workspace IS a git repo)

```bash
git submodule add https://github.com/sihangchen97/zoo-rules.git .roo/zoo-rules
mkdir -p .roo/rules
cd .roo/rules
ln -s ../zoo-rules/conda.md .
```

## Available Rules

| File | Description |
|------|-------------|
| [`conda.md`](conda.md) | Activate conda env (`$ZOO_CONDA_ENV`) before running python/pip |
| [`ponytail.md`](ponytail.md) | Lazy senior dev mode — YAGNI, reuse, minimum code |
| [`python-file-header.md`](python-file-header.md) | Python file header instruction |

## Third-Party Sources

Rules under [`third-party/`](third-party/) contain the upstream repos. The top-level `.md` files are the curated, ready-to-use copies.
