# Picture Checklist — GitHub Pages

A simple, responsive visual checklist containing 356 WebP pictures.

## Features
- Five columns on desktop; responsive on tablets and phones.
- Click a picture to mark it complete (greyed out); click again to undo.
- Progress counter and progress bar.
- Reset button.
- Completion state is saved in the browser's local storage.

## Publish with GitHub Pages
1. Create a new **public** repository on GitHub, for example `picture-checklist`.
2. Extract this ZIP on your computer.
3. Open the extracted `picture-checklist` folder. You should see `index.html`, `images.json`, and the `images` folder.
4. In the new GitHub repository, choose **Add file → Upload files**.
5. Drag the three items (`index.html`, `images.json`, and the `images` folder) into the upload area. Do not upload the outer ZIP.
6. Commit the files to the `main` branch.
7. Open **Settings → Pages**.
8. Under **Build and deployment**, choose **Deploy from a branch**.
9. Select branch **main** and folder **/(root)**, then click **Save**.
10. Wait for GitHub Pages to publish. Your site address will look like:
    `https://YOUR-USERNAME.github.io/picture-checklist/`

## Notes
- All image files are already WebP; no conversion was needed.
- Progress is saved separately in each browser/device. It does not sync between devices.
- Keep `index.html`, `images.json`, and the `images` folder together at the repository root.
