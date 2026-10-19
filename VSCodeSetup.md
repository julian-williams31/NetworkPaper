# VS Code Setup for NetworkPaper

This guide documents the VS Code configuration and tooling used for this project so a co-author can set up their environment in the same way.

## 1) Install the base tools

Install the following:

- VS Code
- Git
- Python 3.11+
- GitHub account sign-in inside VS Code

## 2) Install these VS Code extensions

Recommended extensions:

- GitHub Copilot
- GitHub Copilot Chat
- Python
- Pylance
- Jupyter
- Markdown All in One
- Markdown Preview Enhanced
- LaTeX Workshop (if writing manuscript content in LaTeX)
- Prettier - Code formatter
- GitLens — Git supercharged
- Material Icon Theme

Optional but useful:

- Live Share
- Todo Tree
- YAML
- Excel Viewer (if working with spreadsheets)

## 3) Recommended workspace settings

Create a `.vscode/settings.json` file in the project root with the following:

```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "editor.rulers": [80, 100],
  "files.trimTrailingWhitespace": true,
  "files.insertFinalNewline": true,
  "files.encoding": "utf8",
  "workbench.editor.enablePreview": false,
  "workbench.colorTheme": "Default Dark Modern",
  "workbench.iconTheme": "Material Icon Theme",
  "markdown.preview.fontSize": 16,
  "markdown.preview.lineHeight": 1.6,
  "python.defaultInterpreterPath": "${workspaceFolder}/.venv/bin/python",
  "python.analysis.typeCheckingMode": "basic",
  "python.analysis.autoImportCompletions": true,
  "python.testing.pytestEnabled": true,
  "python.testing.unittestEnabled": false,
  "python.testing.pytestArgs": [
    "Numerics",
    "Data"
  ]
}
```

If the project uses a different interpreter or environment, update `python.defaultInterpreterPath` accordingly.

## 4) Recommended Python environment

For the Numerics/Data work, create a project virtual environment:

```bash
cd /path/to/NetworkPaper
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install jupyter pandas numpy matplotlib scipy seaborn
```

If you are using a requirements file later, install with:

```bash
pip install -r requirements.txt
```

## 5) Suggested Git workflow in VS Code

- Open the repo root as the workspace folder.
- Use the Source Control view for staging, committing, and pull requests.
- Keep branch names short and descriptive.
- Use the integrated Terminal for Python, Git, and any manuscript/data scripts.

## 6) Recommended extension settings

Some settings are worth enabling in the UI:

- Enable GitHub Copilot suggestions for Markdown and Python.
- Use the built-in terminal for local project commands.
- Turn on auto-save if preferred.
- Use the Problems panel to catch Python and Markdown issues quickly.

## 7) Suggested project layout

This repo is organized as:

- `Manuscript/` — manuscript drafts, notes, and writing files
- `Numerics/` — modeling, simulation, analysis scripts
- `Data/` — raw or processed datasets
- `Thesis/` — thesis-related materials
- `NetworkPaperLog.md` — project log

## 8) Quick setup checklist

1. Install VS Code and Git.
2. Install the recommended extensions.
3. Create `.vscode/settings.json` using the config above.
4. Create a Python virtual environment in the project root.
5. Install the Python packages needed for analysis.
6. Open the project folder as the workspace root.

## 9) Optional theme and UI setup

These are not required, but they help keep the environment consistent:

- Theme: Default Dark Modern or one of the VS Code dark themes
- Font: JetBrains Mono or Fira Code
- Enable minimap if helpful for large manuscript and code files

## 10) Final note

This setup is designed for a writing + analysis workflow: Markdown/LaTeX manuscript work, Python-based numerical experiments, and collaboration through GitHub.

If you want, I can also create a matching `.vscode/settings.json` file in the repo so it can be copied directly.
