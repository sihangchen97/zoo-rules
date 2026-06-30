# Conda

Before running any `python` or `pip` command, activate the conda environment first. The conda environment name is stored in `$ZOO_CONDA_ENV`.

Run `conda activate "$ZOO_CONDA_ENV"` (or `%ZOO_CONDA_ENV%` on cmd / `$env:ZOO_CONDA_ENV` on PowerShell).

## When `$ZOO_CONDA_ENV` is Not Set

1. List available environments: `conda env list`
2. Ask the user which environment to use, or pick the most obvious one.
3. Set it in the workspace VSCode settings (`.vscode/settings.json`) — use the correct OS key:
4. Reopen the terminal so the new environment variable takes effect, then re-run the command.

```json
{
  "terminal.integrated.env.<linux/osx/windows>": {
    "ZOO_CONDA_ENV": "your-env-name"
  }
}
```
