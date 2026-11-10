# Image Checklist Gallery — GitHub Pages

A responsive image checklist containing **348 images** from the supplied archive.

## Features

- Tap/click an image to mark it completed; completed images become greyed out with a checkmark.
- Tap again to undo completion.
- Live completion count, percentage, and progress bar.
- Filter by All, Remaining, or Completed.
- Search image filenames.
- Reset progress and export a JSON backup.
- Automatically saves progress in browser `localStorage`.
- Responsive layout for desktop, tablet, and mobile.

## Publish on GitHub Pages

1. Create a GitHub repository (for example, `image-checklist`).
2. Extract this ZIP on your computer.
3. Upload **the contents** of the extracted folder to the repository root:
   - `index.html`
   - `images.json`
   - the complete `images/` folder
4. Commit the files to the `main` branch.
5. In the repository, open **Settings → Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select branch **main** and folder **/(root)**, then click **Save**.
8. Wait for deployment. Your gallery will be available at:
   `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`

## How progress is saved

Progress is saved automatically in the browser's local storage for the published website. It remains after refreshes and browser restarts on that same browser/device.

**Important:** GitHub Pages only serves static files. It cannot write visitor progress back into the GitHub repository, and browser local storage does not sync across devices or browsers. Use **Export progress** to download a backup. Shared or cross-device progress requires connecting a backend/database (such as Supabase or Firebase) and configuring it with your own project credentials.

## Project structure

```text
.
├── index.html
├── images.json
└── images/
    └── ... 348 image files
```

The image manifest was rebuilt from the actual files in the archive so the gallery does not reference missing image paths.
