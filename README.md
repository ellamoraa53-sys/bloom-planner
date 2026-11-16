# Bloom 🌷

A gentle personal planning app for daily intentions, goals, vision boards, and rewards you choose. Built with plain HTML, CSS, and JavaScript. No installation, API keys, or build step required.

## Features

- Create tasks with planned dates, life areas, reminder times, and custom petal values.
- Complete tasks to collect petals; reopening a task reverses its points.
- Track numeric goals over monthly, quarterly, or yearly horizons.
- Create monthly, quarterly, and yearly vision boards with images, symbols, and notes.
- Set your own rewards and petal prices, then redeem earned petals.
- Export and import JSON backups.
- Responsive layout for mobile and desktop.

## Run locally

Open `index.html` in a browser, or serve the folder with Python:

```sh
python3 -m http.server 8000
```

Visit `http://localhost:8000`.

## Add to GitHub

1. Create an empty GitHub repository named `bloom-planner`.
2. Extract this ZIP on your computer.
3. Upload the files **inside** the `bloom-planner` folder to the repository root. `index.html`, `styles.css`, and `app.js` should be at the top level.
4. Commit the uploaded files.

Alternatively, from the extracted project folder:

```sh
git init
git add .
git commit -m "Add Bloom planner"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/bloom-planner.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your GitHub username.

## Host with GitHub Pages

In your repository, open **Settings → Pages**. Choose **Deploy from a branch**, then select **main** and **/ (root)** and save. GitHub displays the site address after deployment. Pages availability depends on your repository visibility and GitHub plan.

This export is a standalone static site. The ChatGPT sign-in gate on the original private preview is not included. Anyone who can access the deployed static site can open the app, but their plans are stored separately in their own browser.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | Page structure and dialog shell |
| `styles.css` | Colors, typography, components, responsive layout |
| `app.js` | Local storage, tasks, goals, boards, rewards, reminders, backups |
| `.nojekyll` | Serve as a plain static site on GitHub Pages |

## Customize

- Change the colors in the `:root` variables in `styles.css`.
- Change the app name, tagline, and initial avatar in `index.html`.
- Change example tasks, goals, dreams, and rewards in the initial `state` object in `app.js`.
- Fonts load from Google Fonts; system fonts act as fallbacks.

## Current limits

- Data is stored in `localStorage` on the current browser and origin, with no account, backend, or cross-device sync. Moving to another URL does not migrate your plans: export a backup and import it on the new site.
- Clearing browser data removes saved plans. Export backups regularly.
- Timed reminders require the app to stay open and the browser to run it. Browser notifications also need permission and a supported secure context. There are no background push, email, or SMS reminders.
- Boards are grouped by Monthly, Quarterly, or Yearly; they do not yet have individual calendar month, quarter, or year selectors.
- Uploaded pictures are stored in browser storage and limited to 2 MB each; total capacity varies by browser.
- Goals have manual progress controls; petals are earned through task completion.
- Existing entries can be removed and recreated; an edit screen is not yet included.

## Verification

The original app was checked in a browser for task creation, completion, petal updates, persistence after refresh, and vision-board navigation. This export retains that app logic in separate files. Background reminders and cross-device sync are not implemented.
