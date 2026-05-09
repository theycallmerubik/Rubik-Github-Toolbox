# ⬇️ URL Downloader

Download any file from a direct URL and automatically store it in your GitHub repository.

### How to Use

1. Go to **Actions** tab in your repository
2. Select **⬇️ Download from url** workflow
3. Click **Run workflow**
4. Fill in the inputs:

   - **urls**: Space-separated list of download links  
     Example: `https://example.com/file.zip https://example.com/video.mp4`
   - **mode**:
     - `normal` → saves files as-is (recommended for small files)
     - `zip` → always creates 7z archive
   - **password** (optional): Password for 7z encryption

5. Click **Run workflow**

### Features
- Automatic file splitting for files > 90 MB (GitHub limit)
- 7z compression with optional password
- Automatic sanitization of filenames
- Creates a nice README with download info in each folder

**Repository Maintenance**: Use the Maintenance workflow regularly to delete old files.
