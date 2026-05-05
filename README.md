# Personal academic webpage — deployment guide

This folder contains a complete static website for **Dr. Srebrenka Letina**, ready to be hosted on **GitHub Pages** for free at the URL `https://srebrenka.github.io`.

---

## Folder structure

```
site/
├── index.html              ← the main page (edit text here)
├── style.css               ← all styling
├── .nojekyll               ← tells GitHub Pages "do not run Jekyll"
├── README.md               ← this file
└── assets/
    ├── images/             ← put your profile photo + travel photos here
    └── files/              ← put CV.pdf and PhD theses here
```

---

## Step 1 — Add your assets

Before pushing to GitHub, drop these files into the folders above. Filenames **must match exactly** (case-sensitive on GitHub):

### `assets/images/`

| Filename         | What it is                       |
|------------------|----------------------------------|
| `profile.jpg`    | Your headshot (the portrait you sent) |
| `zadar.jpg`      | Zadar, Croatia                    |
| `zagreb.jpg`     | Zagreb, Croatia                   |
| `melbourne.jpg`  | Melbourne, Australia              |
| `budapest.jpg`   | Budapest, Hungary                 |
| `norrkoping.jpg` | Norrköping, Sweden                |
| `glasgow.jpg`    | Glasgow, UK                       |
| `amsterdam.jpg`  | Amsterdam, Netherlands            |
| `limerick.jpg`   | Limerick, Ireland                 |

The page is robust to missing images — empty boxes will show but the layout won't break.

### `assets/files/`

| Filename                     | What it is                          |
|------------------------------|-------------------------------------|
| `CV_Srebrenka_Letina.pdf`    | Your CV exported as PDF             |
| `PhD_Psychology_Zagreb.pdf`  | PhD thesis — Psychology (Zagreb)    |
| `PhD_NetworkScience_CEU.pdf` | PhD thesis — Network Science (CEU)  |

---

## Step 2 — Preview locally (optional but recommended)

Just **double-click `index.html`** — it will open in your browser and show the full site exactly as it will appear online. Nothing else to install.

---

## Step 3 — Create the GitHub repository

GitHub Pages gives you one free site at `https://<username>.github.io` if you create a repo with that exact name. Your username is `Srebrenka`, so:

1. Sign into GitHub.
2. Click **+** (top right) → **New repository**.
3. **Repository name**: `Srebrenka.github.io`  *(must match this pattern exactly)*
4. **Public**.
5. Leave "Add a README" unchecked (you already have one).
6. Click **Create repository**.

---

## Step 4 — Push the files

The easiest path is **GitHub Desktop** (graphical, no terminal needed):

1. Install [GitHub Desktop](https://desktop.github.com/) if you don't have it.
2. **File → Clone repository →** pick `Srebrenka/Srebrenka.github.io`.
3. Choose a folder on your computer to clone into.
4. Copy **everything inside this `site/` folder** (the `index.html`, `style.css`, `.nojekyll`, `README.md`, and the whole `assets/` folder) into the cloned folder.
5. Back in GitHub Desktop you'll see all the files listed as changes.
6. Type a commit summary like *"initial site"* → click **Commit to main** → click **Push origin**.

Alternatively, with git on the command line:

```bash
cd /path/to/where/you/want/the/repo
git clone https://github.com/Srebrenka/Srebrenka.github.io.git
cd Srebrenka.github.io
# copy contents of this site/ folder into here, then:
git add .
git commit -m "initial site"
git push origin main
```

---

## Step 5 — Turn on GitHub Pages

1. Go to your repository on github.com.
2. Click **Settings** (top tab).
3. In the left sidebar, click **Pages**.
4. Under **Build and deployment → Source**, select **Deploy from a branch**.
5. Under **Branch**, select `main` and folder `/ (root)`. Click **Save**.
6. Wait 30–60 seconds. Your site will be live at:

   **`https://srebrenka.github.io`**

GitHub will show a green check on the Pages settings page when it's deployed.

---

## How to update the site later

- **Edit text** → open `index.html` in any text editor (VS Code is recommended), find the section you want to change, edit, save, commit, push.
- **Add a new publication** → in `index.html` find the `<ol class="pubs">` list inside the Publications section and add a new `<li>...</li>` item at the top.
- **Replace a photo** → just overwrite the file in `assets/images/` with the same filename.
- **Add a new section** → copy any existing `<section>` block and adapt it. Don't forget to add a corresponding link to the top nav.

---

## Tips

- **Keep filenames lowercase** and avoid spaces — GitHub Pages is case-sensitive on Linux servers, even if Windows/Mac aren't.
- **Compress photos** before uploading (try [tinypng.com](https://tinypng.com)) — keeps the site fast.
- **Test changes locally first** by double-clicking `index.html` before pushing.
- **The `.nojekyll` file** is important — without it, GitHub Pages tries to run Jekyll on your site and may break paths.

If you ever want to migrate to a more powerful Jekyll-based template (e.g., academicpages) later, all the publication and bio content you have in `index.html` will transfer over easily.

---

*Site built May 2026.*
