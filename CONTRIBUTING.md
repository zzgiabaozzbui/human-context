# Contributing

Thanks for helping improve human-context. This project is intentionally small:
there is no package manager, build step, server, or framework required.

## Getting Started

1. Fork and clone the repository.
2. Open `human-context/md-folder-viewer.html` directly in Chrome or Edge.
3. Click `Open Folder` and choose a folder that contains Markdown files.
4. Make your change and refresh the browser to test it.

Firefox is supported through the `webkitdirectory` file input fallback. The
primary development path is still Chrome or Edge because they support the File
System Access API and folder memory.

## Project Structure

- `human-context/md-folder-viewer.html` - the main single-file folder viewer.
- `human-context/md-reader.html` - a simpler single-file Markdown reader.
- `README.md` - project overview, usage notes, and roadmap.

There are no dependencies to install and no generated files to commit.

## Coding Style

- Use vanilla JavaScript, HTML, and CSS only.
- Do not add frameworks, bundlers, TypeScript, or new runtime dependencies.
- Keep colors in CSS custom properties under the `:root` theme blocks.
- Prefer descriptive `verbNoun` function names, such as `buildTree`,
  `loadFile`, and `renderMarkdown`.
- Use the existing section comments, such as `Tree icon mapper`,
  `Heading icon mapper`, and `Wrap H2 sections into cards`, to find the right
  area before editing.
- Keep changes focused and avoid unrelated formatting churn.

## Manual Test Checklist

Before opening a pull request, check:

- [ ] The viewer opens in Chrome or Edge from the local HTML file.
- [ ] The Firefox file picker fallback still works for folder selection.
- [ ] Dark mode still toggles and persists correctly.
- [ ] File navigation, search, and table of contents still work.
- [ ] Browser devtools show no new console errors.
- [ ] No new external dependencies were added.

## Pull Request Checklist

- Link the issue your PR fixes, if one exists.
- Describe what changed and why.
- Include the browsers you manually tested.
- Keep the PR limited to one feature, fix, or documentation update.
