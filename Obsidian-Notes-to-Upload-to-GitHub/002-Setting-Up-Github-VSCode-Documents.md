Love this for you: “I suffered so others don’t have to” is peak Lantern energy. 🕯️🧬

Let’s do both:

1. A **beginner-friendly guide** you can basically paste into a README to save other humans from the Git Hydra.
    
2. A **step-by-step HTML workflow**: write in VSCode → save as `.html` → push to GitHub → (optionally) have GitHub render it as a pretty web page.
    

---

## 1️⃣ Beginner’s Guide: Mac Documents + VS Code + GitHub (Without Pain)

You can copy-paste this section into a README and lightly edit.

---

### 🔧 Goal

Set things up so:

- You have **ONE folder** on your Mac for the project
    
- That folder **is the Git repo**
    
- VS Code always opens **that** folder
    
- GitHub syncs with **that** folder
    

No duplicates, no nested repos, no “where did my file go??”

---

### Step 0 – Pick a “Projects” home on your Mac

In Finder, make a parent folder where all your code projects will live, e.g.:

```text
/Users/<yourname>/Documents/Projects
```

or in your case:

```text
/Users/jennikeller/Documents/ChironsLantern
```

This is just an organizer. Git doesn’t care about this yet.

---

### Step 1 – Create the repo on GitHub (in the browser)

1. Go to GitHub → **New repository**
    
2. Name it (e.g.):  
    `nursing-to-bioinformatics-learning-journey`
    
3. Choose:
    
    - Public or private
        
    - Add a README if you want (nice for humans)
        
4. Click **Create repository**
    

This creates the **remote home** for your project.

---

### Step 2 – Clone the repo _into_ your Projects folder

Now bring that repo down to your Mac.

#### Option A: Using VS Code (nice for beginners)

1. Open VS Code
    
2. `Cmd + Shift + P` → **Git: Clone**
    
3. Paste the repo URL, e.g.:
    
    ```text
    https://github.com/ChironsLantern/nursing-to-bioinformatics-learning-journey.git
    ```
    
4. When it asks for a folder:
    
    - Choose: `/Users/<you>/Documents/ChironsLantern`
        
5. VS Code will create:
    
    ```text
    /Users/<you>/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey
    ```
    

This folder **is now your local repo**.

#### Option B: Using Terminal

```bash
cd ~/Documents/ChironsLantern
git clone https://github.com/ChironsLantern/nursing-to-bioinformatics-learning-journey.git
```

Same result.

---

### Step 3 – Open _that folder_ in VS Code (and ONLY that folder)

In VS Code:

- **File → Open Folder…**
    
- Choose:
    
    ```text
    /Users/<you>/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey
    ```
    

You’ll know it’s right when:

- The Explorer shows that folder name at the top
    
- Bottom-left shows a branch like `main` (Git integration)
    
- Source Control (the branch icon) shows your repo
    

**Rule of thumb:**  
If VS Code isn’t showing the repo name at the top → you’re in the wrong place.

---

### Step 4 – Golden Rule: If it’s not in this folder, GitHub will never see it

Everything you want under version control (HTML, Python, notes) must live **inside**:

```text
/Users/<you>/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey
```

If you save a file somewhere else (e.g. random “HTML-files-for-GitHub” folder), Git does not care. It’s invisible.

So:

- Create subfolders **inside** the repo, like:
    
    ```text
    Biology-Refresher/
    rosalind/
    notes/
    ```
    
- Save your work in there.
    

---

### Step 5 – The basic Git cycle (for humans)

From inside the repo folder:

```bash
cd ~/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey
```

Your loop is:

```bash
# 1. See what changed
git status

# 2. Stage changes (example: everything in Biology-Refresher)
git add Biology-Refresher

# 3. Commit with a short message
git commit -m "Add amino acid notes"

# 4. Keep in sync with GitHub
git pull --rebase origin main

# 5. Push your changes up
git push origin main
```

That’s it. That’s the spell.

**Key sanity mantras:**

- **One repo = one folder.**
    
- **Always work inside the cloned folder.**
    
- **If `git status` doesn’t show your changes, your file is probably not in the repo folder.**
    

---

## 2️⃣ Step-by-Step: Write HTML in VS Code → Save → Push → View

Now, how to go from “brain” → “pretty HTML file in GitHub repo.”

---

### Step 1 – Make (or open) the repo in VS Code

We already have:

```text
~/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey
```

In VS Code:

- File → Open Folder… → that folder.
    

You should see your repo files in the Explorer.

---

### Step 2 – Create a folder for your HTML notes

Inside the repo (in VS Code Explorer):

1. Right-click → **New Folder**
    
2. Name it something like:
    
    ```text
    Biology-Refresher
    ```
    

Inside that folder is where all your HTML biology notes will live.

---

### Step 3 – Create a new HTML file in VS Code

1. Right-click on `Biology-Refresher` → **New File**
    
2. Name it:
    
    ```text
    biology-refresher-001-amino-acids.html
    ```
    

**Make sure it ends with `.html`** (not `.html.txt`).

---

### Step 4 – Add HTML content (with a basic template)

Here’s a minimal template you can paste into the new file and edit:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Amino Acids & Proteins — Biology Refresher</title>
  <style>
    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      max-width: 800px;
      margin: 2rem auto;
      padding: 1.5rem;
      line-height: 1.6;
      background: #050513;
      color: #f4f4ff;
    }
    h1, h2, h3 {
      color: #e2d9ff;
    }
    h1 {
      text-align: center;
      margin-bottom: 0.5rem;
    }
    hr {
      border: none;
      border-top: 1px solid #4b3b88;
      margin: 1.5rem 0;
    }
    code, pre {
      background: #111322;
      padding: 0.25rem 0.4rem;
      border-radius: 4px;
      font-family: "SF Mono", Menlo, Monaco, Consolas, "Liberation Mono", monospace;
    }
    pre {
      padding: 0.75rem;
      overflow-x: auto;
    }
    .tag {
      display: inline-block;
      padding: 0.1rem 0.5rem;
      border-radius: 999px;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      background: #2f234d;
      color: #fcefff;
      margin-right: 0.3rem;
    }
    .pill-el5 { background: #3b3b8a; }
    .pill-med { background: #2f6b5f; }
    .pill-bis { background: #60419a; }
  </style>
</head>
<body>

  <h1>🧬 <strong>Amino Acids & Proteins — EL5 → Med → Bioinformatics</strong></h1>
  <p>A unified field guide for your future bioinformatics empire.</p>
  <hr />

  <span class="tag pill-el5">EL5</span>
  <span class="tag pill-med">Med</span>
  <span class="tag pill-bis">BIS</span>

  <h2>1️⃣ Amino Acids</h2>

  <h3>EL5 + Med: What They Are</h3>
  <p>
    Amino acids are <strong>20 little LEGO people with different hats</strong>.<br />
    You snap them into chains; their hats dictate their behavior:
  </p>

  <ul>
    <li>shy vs loud → hydrophobic vs hydrophilic</li>
    <li>sticky vs slippery → charged vs neutral</li>
    <li>bendy vs stiff → glycine vs proline</li>
    <li>good at passing protons, forming bonds, or taking molecular “tags”</li>
  </ul>

  <!-- keep going with your content here -->

</body>
</html>
```

You can paste the rest of your notes into the `<body>` where indicated.

---

### Step 5 – Save the file as real `.html`

In VS Code:

- `Cmd + S`
    
- Confirm the filename in the tab (and Explorer) ends with `.html`
    

If macOS ever sneakily appends `.txt`, fix it in VS Code or Finder.

---

### Step 6 – Preview the HTML (locally)

Two easy options:

#### Option A: Open in browser directly

1. In VS Code Explorer, right-click the HTML file → **Reveal in Finder**
    
2. Double-click the file in Finder → it opens in your default browser
    
3. Admire your shiny page
    

#### Option B: Use a VS Code extension (e.g. “Live Server”)

- Install “Live Server” from the Extensions tab
    
- Right-click HTML file → **Open with Live Server**
    
- It opens in browser with auto-refresh on save
    

Either way, this preview does **not** involve GitHub yet. This is just “does my page look how I want?”

---

### Step 7 – Commit & push the HTML to GitHub

From the repo root:

```bash
cd ~/Documents/ChironsLantern/nursing-to-bioinformatics-learning-journey

git status                # you should see Biology-Refresher as changed
git add Biology-Refresher
git commit -m "Add amino acids HTML refresher"
git push origin main
```

Your HTML is now safely on GitHub.

---

### Step 8 – Viewing it “pretty” via GitHub

Important distinction:

- **In the GitHub repo UI** (the file browser):  
    GitHub will show your HTML as **source code**, not rendered. That’s normal.
    
- **To see it rendered as a web page from GitHub**, you have two options:
    

#### Option 1: Download or open locally

Click the file → **Download raw** → open with browser.  
Simple, but manual.

#### Option 2 (better): Turn the repo (or a subfolder) into a GitHub Pages site

1. Go to your repo on GitHub
    
2. Click **Settings → Pages**
    
3. Under “Build and deployment”:
    
    - Source: `Deploy from a branch`
        
    - Branch: `main`
        
    - Folder: `/ (root)` or `/docs` (we can reorganize later)
        
4. Save
    

GitHub will give you a URL like:

```text
https://ChironsLantern.github.io/nursing-to-bioinformatics-learning-journey/
```

If your HTML is at:

```text
Biology-Refresher/biology-refresher-001-amino-acids.html
```

you’ll be able to visit:

```text
https://ChironsLantern.github.io/nursing-to-bioinformatics-learning-journey/Biology-Refresher/biology-refresher-001-amino-acids.html
```

And **that** will be the fully rendered, styled page.

That’s your “pretty GitHub page” version.

---

### Tiny summary for humans you’re saving

> **Workflow:**
> 
> - Clone the repo into Documents
>     
> - Always work inside that folder
>     
> - Make HTML files in VS Code
>     
> - Save as `.html`
>     
> - `git add` → `git commit` → `git push`
>     
> - Turn on GitHub Pages if you want web-style rendering
>     

That’s it. You went from “nested repo ouroboros” to “actually teaching others how not to suffer.”

Very on-brand for a Lantern-bearer.