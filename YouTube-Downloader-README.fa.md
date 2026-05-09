# 🎬 دانلودکننده پیشرفته یوتیوب

دانلود ویدیوهای یوتیوب (حتی ویدیوهای محدود شده و age-restricted) با موفقیت بالا.

### نحوه استفاده

1. به **Actions** → **🎬 Enhanced YouTube Downloader** بروید.
2. **Run workflow** را بزنید.
3. فیلدها را پر کنید:
   - **youtube_url**: لینک کامل ویدیو
   - **quality**: `480`، `720`، `1080`، `1440`، `best`، `audio` و غیره
   - **password** (اختیاری): 7z رمز
   - **use_cookies**: `yes` (به شدت توصیه می‌شود)

### راه‌اندازی کوکی یوتیوب (بسیار مهم)

**چرا کوکی لازم است؟** بسیاری از ویدیوها بدون لاگین دانلود نمی‌شوند.

#### مراحل استخراج کوکی:

1. [افزونه](https://chromewebstore.google.com/detail/get-cookiestxt-locally/cclelndahbckbenkjhflpdbgdldlbecc) **Get cookies.txt LOCALLY** را نصب کنید.
2. وارد حساب یوتیوب خود شوید.
3. روی افزونه کلیک کنید و **Export cookies** را بزنید → فایل را با نام `cookies.txt` ذخیره کنید.
4. محتوای فایل را **Base64** کنید:

   ```bash
   # لینوکس / macOS
   base64 -w 0 cookies.txt
   ```

   ```powershell
   # PowerShell (ویندوز)
   [Convert]::ToBase64String([IO.File]::ReadAllBytes("cookies.txt"))
   ```

5. به ریپازیتوری خود بروید → **Settings** → **Secrets and variables** → **Actions**
6. یک Secret جدید با نام `YOUTUBE_COOKIES` بسازید و مقدار Base64 را paste کنید.

حالا دانلودکننده به صورت خودکار از کوکی‌های شما استفاده می‌کند.

**نکته**: استفاده از کوکی موفقیت دانلود را بسیار افزایش می‌دهد.
