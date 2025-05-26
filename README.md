#### **Introduction:**
This is a personal website built with [Hugo](https://gohugo.io/) using the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme, and deployed automatically to GitHub Pages using GitHub Actions.

---

### 1. **Editing Each Page**
- All content lives in the `content/` directory.
- Each section (About, Projects, Blog, etc.) has its own folder or `_index.md` file.
- To edit a page, open the corresponding `.md` file in `content/` and edit using Markdown.

#### **Sections:**
- **About:** `content/about/_index.md`
- **Projects:** `content/projects/_index.md`
- **Blog:** `content/posts/` (each post is a separate `.md` file)
- **5-9:** `content/5-9/_index.md` (or similar)
- **Reading:** `content/reading/_index.md`

### 2. **Adding a Blog Post with Abstract and Substack Card**
- Create a new file in `content/posts/`, e.g. `my-new-post.md`.
- Use this frontmatter template:
  ```markdown
  ---
  title: "My Blog Post Title"
  date: 2024-05-22
  abstract: "A short summary or abstract for this post."
  substack_url: "https://your-substack-url.com/p/your-post"
  draft: false
  ---
  
  Your post content here in Markdown.
  
  <!-- Optionally, embed your Substack card below: -->
  {{< substack url="https://your-substack-url.com/p/your-post" >}}
  ```
- The `abstract` will be shown in blog lists (if you update the theme to display it).
- The `substack_url` can be used to link or embed a Substack card.

### 3. **Editing Other Sections**
- Just edit the corresponding Markdown file in `content/`.
- Use standard Markdown for formatting.
- You can add images by placing them in `static/img/` and referencing them as `/img/yourimage.jpg`.

---

## ⚙️ How GitHub Actions Deploys Your Site
- The workflow file is at `.github/workflows/hugo.yaml`.
- On every push to `main`, GitHub Actions:
  1. Installs Hugo (latest version).
  2. Checks out your code and theme submodules.
  3. Builds the site with Hugo (converts Markdown to static HTML).
  4. Uploads the built site to GitHub Pages.
- You can see build logs in the **Actions** tab on GitHub.

---

## 🛠️ Configuration Files
- **`config.yml` and `hugo.toml`:**
  - Set your site title, baseURL, menu, theme, and other options.
  - `baseURL` must match your deployed site URL (e.g. `https://shrey1306.github.io/`).
  - `profileMode` controls the homepage profile section.
  - `customCSS` lets you add your own styles.
- **`.github/workflows/hugo.yaml`:**
  - Controls the GitHub Actions build and deploy process.
  - Make sure the Hugo version is up to date for PaperMod.

---

## 📝 Adding Information to Each Section
- **About:** Edit `content/about/_index.md`.
- **Projects:** Edit `content/projects/_index.md`.
- **Blog:** Add/edit files in `content/posts/`. Use frontmatter for title, date, abstract, substack_url.
- **5-9:** Edit `content/5-9/_index.md` (or similar).
- **Reading:** Edit `content/reading/_index.md`.

---

## 💡 Tips
- Use [Markdown Guide](https://www.markdownguide.org/basic-syntax/) for formatting.
- For math, use `$...$` or `$$...$$` (KaTeX is enabled).
- For images, put them in `static/img/` and use `/img/yourimage.jpg` in Markdown.
- To preview locally: `hugo server -D` and visit [http://localhost:1313/](http://localhost:1313/)

---

## 📦 Deploying
- Just push to `main`—GitHub Actions will build and deploy automatically.
- Your site will be live at: `https://shrey.github.io/` 
