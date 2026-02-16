# ⚠️ TROUBLESHOOTING - "I only see README"

## Problem: GitHub shows README instead of the app

### ✅ Solution - Check Your Repo Structure

Your repo should look like this:

```
catalog-maker-v5/           ← repo root
├── index.html              ← MUST be in root!
├── manifest.json
├── service-worker.js
├── icon-192.png
├── icon-512.png
├── README.md
├── DEPLOY.md
└── .gitignore
```

## 🔧 Fix Steps

### 1. Verify Files Are in Root
Go to: `https://github.com/prince63x/catalog-maker-v5`

You should see ALL files listed directly (not in a subfolder).

**❌ WRONG:**
```
catalog-maker-v5/
└── catalog-maker/    ← nested folder (BAD!)
    ├── index.html
    └── ...
```

**✅ CORRECT:**
```
catalog-maker-v5/
├── index.html        ← directly in root (GOOD!)
├── manifest.json
└── ...
```

### 2. Check GitHub Pages Settings

1. Go to: `https://github.com/prince63x/catalog-maker-v5/settings/pages`
2. Verify:
   - Source: **Deploy from a branch**
   - Branch: **main** (or master)
   - Folder: **/ (root)**
3. Click Save

### 3. Force Refresh

After fixing structure:
1. Wait 2-3 minutes
2. Hard refresh: **Ctrl + Shift + R** (Windows) or **Cmd + Shift + R** (Mac)
3. Or try incognito/private window

### 4. Test Direct Access

Try accessing directly:
```
https://prince63x.github.io/catalog-maker-v5/index.html
```

If this works but the base URL doesn't, there's a GitHub Pages config issue.

## 🚨 Common Mistakes

### Mistake #1: Files in Subfolder
**Solution:** Move all files to repository root

### Mistake #2: Wrong Branch
**Solution:** Make sure files are on `main` branch (or whatever branch is set in Pages settings)

### Mistake #3: Case Sensitivity
**Solution:** Use lowercase: `index.html` not `Index.html`

### Mistake #4: Old Cache
**Solution:** Clear browser cache or try incognito

## ✅ Quick Test

1. Go to: `https://github.com/prince63x/catalog-maker-v5`
2. Can you see `index.html` listed?
   - **YES** → Files are in correct location
   - **NO** → Upload files again to root

3. Click on `index.html` in GitHub
4. Click "Raw" button
5. Does it show the HTML code?
   - **YES** → File is uploaded correctly
   - **NO** → Re-upload the file

## 🔄 How to Fix Wrong Structure

If files are in a subfolder:

### Option A: Re-upload (Easiest)
1. Delete the subfolder
2. Upload all 8 files directly to root
3. Commit changes

### Option B: Move Files
1. In GitHub, click each file
2. Click edit (pencil icon)
3. In filename, remove the folder path
4. Commit changes

## 📝 Still Not Working?

Share a screenshot of:
1. Your repo file list: `https://github.com/prince63x/catalog-maker-v5`
2. GitHub Pages settings
3. Browser console errors (F12)

---

**Expected Result:**
`https://prince63x.github.io/catalog-maker-v5/` should show the Catalog Maker app, NOT the README.
