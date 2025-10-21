Pre-commit setup

This project includes a `.pre-commit-config.yaml` which will run a local hook to ensure UI HTML files include the theme styles before committing.

Install:

1. Install pre-commit (recommended):

```powershell
pip install pre-commit
```

2. Install the git hook in your repo:

```powershell
pre-commit install
```

3. Test the hook manually:

```powershell
pre-commit run --all-files
```

Notes:
- The hook runs `python prototype/ui/apply_theme_to_all_html.py` and will modify HTML files in-place if it finds missing includes. Commit the changes after the hook runs.
- If you prefer the hook to only check (not modify), ask me and I'll switch it to a check-only mode that fails the commit instead of fixing files.
