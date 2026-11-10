# Shared Image Checklist Gallery

Updated from your latest `collection.zip`. This version contains **344 images**.

## Features

- New image collection and rebuilt `images.json` manifest.
- Click an uncompleted image to mark it complete (greyed out and locked).
- Clicking a completed image asks for confirmation before unchecking it.
- Live completion count and progress bar.
- Search and All / Remaining / Completed filters.
- `progress.json` is the shared source of truth stored in this repository.
- GitHub API sync reads and writes `progress.json`.
- Export a JSON backup at any time.

## Publish / update on GitHub Pages

Upload or replace the repository-root files and `images/` folder with the contents of this ZIP. Keep the files at the repository root:

```text
.
├── index.html
├── images.json
├── progress.json
└── images/
```

Then let GitHub Pages deploy the new commit.

## Enable shared repository saving

GitHub Pages is static hosting: a webpage cannot commit to its repository anonymously. To let the gallery update `progress.json`:

1. On GitHub, open **Settings → Developer settings → Personal access tokens → Fine-grained tokens**.
2. Create a token limited to this one repository.
3. Grant **Contents: Read and write** (Metadata read-only is normally added automatically).
4. Open the published gallery and click **GitHub sync settings**.
5. Enter the GitHub owner, repository name, branch (usually `main`), and token.
6. Click **Save settings & sync**.

The token is stored in the browser's local storage, not in the repository files. Configure it on every device/browser that needs to make changes. Devices without a token can still read the public repository's shared `progress.json`, but cannot update it.

**Security note:** A token in a browser is suitable only for a trusted personal/private workflow. Anyone with access to that browser profile could potentially use the token. Do not expose the token in source code, commit it, or use this design for an untrusted public multi-user application. For public multi-user writes, use a backend (for example, Supabase or a small authenticated server) instead.

## Initial progress

`progress.json` has been seeded from `gallery-progress-backup.json` in the uploaded archive, retaining only completed paths that still exist in the updated image collection. It is the shared progress file used by the gallery.
