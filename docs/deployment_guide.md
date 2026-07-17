# 🚀 Deployment & Local Hosting Guide

This guide details instructions on how to run, serve, and deploy the **News Reader Website** locally or to cloud hosting providers.

---

## 💻 Local Hosting Options

As a static project consisting of HTML5, CSS3, and local images, you have multiple ways to run it:

### 1. Direct Browser Opening
- Locate the file [mainpage.html](file:///d:/news-reader-website/web/mainpage.html) inside the `web` folder.
- Double-click the file to open it directly in Chrome, Edge, Firefox, or Safari.
- *Note:* Relative paths between files will resolve natively.

### 2. Live Server (VS Code Extension)
- Open the project directory in VS Code.
- Install the **Live Server** extension by Ritwick Dey.
- Right-click [mainpage.html](file:///d:/news-reader-website/web/mainpage.html) and select **Open with Live Server**.
- The site will launch on `http://127.0.0.1:5500/web/mainpage.html`.

### 3. CLI Static Server (Python / Node.js)
If you have a terminal open, you can spin up a lightweight local server:

#### Python 3.x
Run the following command from the root project directory:
```bash
python -m http.server 8000
```
Then visit `http://localhost:8000/web/mainpage.html` in your browser.

#### Node.js / npm
Install and run the `http-server` package:
```bash
npx http-server ./
```
Then visit `http://localhost:8080/web/mainpage.html`.

---

## 🌐 Production Deployment

Since the site is static, it can be deployed for free on various platforms:

### 1. GitHub Pages (Recommended)
1. Push the project repository to your GitHub account.
2. In the GitHub repository settings, navigate to the **Pages** tab.
3. Under **Build and deployment**, select **Deploy from a branch** and pick your target branch (e.g. `main`).
4. Select `/ (root)` or `/docs` (if you wish to deploy docs) and click **Save**.
5. Once built, the page will be live at `https://<username>.github.io/news-reader-website/web/mainpage.html`.

### 2. Vercel / Netlify
1. Install the Vercel or Netlify CLI:
   ```bash
   npm install -g vercel
   # OR
   npm install -g netlify-cli
   ```
2. Run the command to initialize and deploy:
   ```bash
   vercel
   # OR
   netlify deploy
   ```
3. Follow the CLI prompt steps to set up and deploy.
