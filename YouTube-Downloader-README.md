# 🎬 Enhanced YouTube Downloader

Download YouTube videos (including age-restricted) with high reliability.

### How to Use

1. Go to **Actions** → **🎬 Enhanced YouTube Downloader**
2. Click **Run workflow**
3. Fill in:
   - **youtube_url**: Full YouTube link
   - **quality**: `480`, `720`, `1080`, `1440`, `best`, `audio`, etc.
   - **password** (optional): For 7z encryption
   - **use_cookies**: `yes` (strongly recommended)

### Important: Setting Up YouTube Cookies (Recommended)

**Why cookies?** Many videos are age-restricted or blocked without login.

#### Step-by-step Cookie Extraction:

1. Install "**Get cookies.txt LOCALLY**" [extension](https://chromewebstore.google.com/detail/get-cookiestxt-locally/cclelndahbckbenkjhflpdbgdldlbecc) (Chrome/Firefox)
2. Log in to [youtube.com](https://youtube.com)
3. Go to any YouTube page
4. Click the cookie extension → **Export cookies** → Save as `cookies.txt`
5. Open GitHub repository → **Settings** → **Secrets and variables** → **Actions**
6. Create new repository secret:
   - **Name**: `YOUTUBE_COOKIES`
   - **Value**: **Base64 encode** `cookies.txt` first:

     ```bash
     # Linux / macOS
     base64 -w 0 cookies.txt
     ```

     ```powershell
     # PowerShell (Windows)
     [Convert]::ToBase64String([IO.File]::ReadAllBytes("cookies.txt"))
     ```

7. Paste the Base64 string as the secret value.

Now the downloader will use your cookies automatically.

### Features
- Multiple download methods + fallback
- Cloudflare WARP proxy
- Automatic splitting + 7z compression
- High success rate on restricted videos
