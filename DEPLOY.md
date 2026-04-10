# CAB Brief Form — Deployment Guide
## Goes live at: https://[your-org].github.io/cab-brief

---

## What's in this folder

| File/Folder | What it is |
|---|---|
| `src/App.jsx` | The entire form (React component) |
| `src/main.jsx` | Wires the form into the page (don't touch) |
| `index.html` | The page shell (don't touch) |
| `package.json` | Project dependencies (don't touch) |
| `vite.config.js` | Build config (don't touch) |
| `.github/workflows/deploy.yml` | Auto-deploys when you push to GitHub |

---

## One-time setup (~30 minutes total)

### Step 1 — Create a GitHub account (skip if you have one)
Go to https://github.com and sign up. Free.

### Step 2 — Create a new repository
1. Click the **+** in the top right → **New repository**
2. Name it: `cab-brief`
3. Set it to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 3 — Upload the files
1. On the new repo page, click **uploading an existing file**
2. Drag the entire contents of this zip into the upload area
   - Make sure the folder structure is preserved:
     - `src/App.jsx`
     - `src/main.jsx`
     - `index.html`
     - `package.json`
     - `vite.config.js`
     - `.github/workflows/deploy.yml`
3. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to the repo → **Settings** tab
2. In the left sidebar click **Pages**
3. Under **Source** select **GitHub Actions**
4. Click **Save**

### Step 5 — Watch it deploy
1. Click the **Actions** tab in the repo
2. You'll see a workflow called "Deploy to GitHub Pages" running
3. When it shows a green ✓, your site is live

### Step 6 — Get your URL
It will be:
```
https://[your-github-username].github.io/cab-brief
```

Or if you're using the Amplitude org on GitHub:
```
https://amplitude.github.io/cab-brief
```

**Paste this link into #advisory-boards-2026 and you're done.**

---

## Making updates later

If you need to update the form (new attendee, fix a name, etc.):
1. Go to the repo on GitHub
2. Click `src/App.jsx`
3. Click the pencil ✏️ icon to edit
4. Make your change
5. Click **Commit changes**

The site automatically rebuilds and updates in ~2 minutes.

---

## Custom domain (optional)

If you want `brief.amplitude.com` instead of `amplitude.github.io/cab-brief`:
1. Go to repo Settings → Pages
2. Under **Custom domain** enter `brief.amplitude.com`
3. Ask your IT/DNS team to add a CNAME record:
   - Name: `brief`
   - Value: `amplitude.github.io`

---

## Questions?
Contact claire.butler@amplitude.com
