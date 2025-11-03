# Lab 4 — Data Cleaning & Probability (DSARM 1)

This repository is ready for **GitHub Codespaces.**  A dev container is included to ensure a reproducible Python environment with useful VS Code extensions and automatic dependency installation.

## Contents

- **Lab4.ipynb** — lab notebook for module 4 covering data cleaning and probability tasks.
- **L4L5dataset.csv** — dataset used for Labs 4 and 5.
- **figures/** — directory to save generated plots. Git is configured to ignore its contents; a `.gitkeep` placeholder is provided.
- **.devcontainer/** — dev container definition used by GitHub Codespaces to preinstall dependencies and useful VS Code extensions.
- **requirements.txt** — Python requirements for a lightweight scientific stack.
- **.gitattributes** — configures `nbstripout` to clean notebook diffs.
- **.gitignore** — ignores temporary files, OS clutter, and the `figures/` folder.
- **LICENSE** — CC0‑1.0 license notice.

## Quick start (GitHub Codespaces)

1. Click the **“Open in GitHub Codespaces”** button or go to **Code → Create codespace on `main`**.  The Codespace will build using the provided dev container; dependencies install automatically via `requirements.txt`, and `nbstripout` is installed to keep notebook diffs clean.
2. Once your Codespace is ready, open `Lab4.ipynb` and run cells from top to bottom (`Kernel → Restart & Run All`) to avoid hidden state.
3. Save any plots to the `figures/` folder, e.g.:

   ```python
   plt.savefig("figures/box_demo.png", dpi=150, bbox_inches="tight")
   ```

4. Use VS Code’s **Data Wrangler** (`Command Palette → "Launch Data Wrangler"`) for interactive inspection/cleaning if helpful.

### Saving your work

Codespaces auto‑saves changes in the workspace, but they are **not** synced to GitHub until you commit and push.  To persist your work:

- Use the **Source Control** view to commit changes with a message.
- Click **Sync** or run `git push` to push the commit to GitHub.
- Consider exporting key figures or PDFs as an extra backup.

Inactive Codespaces may be deleted after 30 days.  Commit and push regularly to avoid losing work.

## Reproducibility & good practices

- Always run notebook cells in order.  After restarting the kernel, run all cells again.
- Save plots to the `figures/` folder.  The folder is ignored by Git to keep history slim.  The `.gitkeep` file ensures the folder exists.
- To enforce clean diffs locally outside Codespaces, install `nbstripout` and run `nbstripout --install` in the repo (the dev container does this automatically).
- Use `pip install -r requirements.txt` in other environments to install dependencies.

## Troubleshooting

- **`ModuleNotFoundError`**:  Run `pip install -r requirements.txt` in the active environment.
- **`FileNotFoundError: figures/...`**:  Ensure the `figures/` directory exists, e.g. `os.makedirs("figures", exist_ok=True)`.
- **Changes not persisting**:  Commit and push; Codespaces can be temporary.

## License

This work is released under the CC0 1.0 Universal public domain dedication.  See `LICENSE` for details.
