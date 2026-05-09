# 🌐 Web Browser & Archiver

Browse any website and save it as an archive inside the repository.

### How to Use

1. Go to **Actions** → **🌐 Browser**
2. Click **Run workflow**
3. Enter:
   - **url**: Website address (with or without `https://`)
   - **mode**:
     - `full` → Screenshot + HTML + media files (recommended)
     - `text-only` → Only HTML source
   - **zip_password** (optional): Encrypt the archive

4. Click **Run workflow**

### Result
- A new folder is created in `pages/`
- Contains: `index.md`, screenshot (full mode), `page.html`, media files
- Everything is zipped for easy download

**Great for**:
- Archiving important pages
- Saving paywalled or dynamic content
- Research preservation
