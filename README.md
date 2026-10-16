# CinnaGen EC Equipment

سایت جستجوی تجهیزات (معادل تب Search اکسل) – سازگار با موبایل.

## راه‌اندازی (فقط یک بار، حدود ۱۰ دقیقه)
1. در GitHub یک Repository بسازید (مثلاً `ec-equipment`) و **همه‌ی محتوای این پوشه** را در آن آپلود کنید
   (پوشه‌ی `.github` هم باید باشد؛ اگر در ویندوز مخفی است، Show hidden files را بزنید).
2. در Repository: **Settings → Pages → Build and deployment → Source = GitHub Actions**.
3. تب **Actions** را باز کنید؛ بعد از ۱–۲ دقیقه آدرس سایت ظاهر می‌شود:
   `https://USERNAME.github.io/ec-equipment/`
4. آدرس را در موبایل باز کنید → Share → Add to Home Screen تا مثل اپ شود.

## آپدیت کردن دیتابیس (هر بار)
فایل اکسل جدید را در پوشه‌ی `data/` آپلود کنید (Add file → Upload files → Commit).
به‌صورت خودکار تبدیل و منتشر می‌شود (~۱ دقیقه). **جدیدترین فایل داخل `data/` استفاده می‌شود**؛
فایل قبلی را می‌توانید پاک کنید یا بگذارید بماند (اسم فایل‌ها مهم نیست).

## نکات
- شیت‌های لازم: `EQ` (داده‌ها) و `Personel` (اسم کامل کاربران). ستون‌ها بر اساس **اسم هدر** خوانده می‌شوند.
- ستون جدید در شیت EQ اضافه کنید → خودکار در داده می‌آید (برای نمایش در کارت، `web/index.html` را ویرایش کنید).
- **حریم خصوصی:** در GitHub Pages رایگان، آدرس سایت عمومی است. اگر داده‌ها محرمانه‌اند،
  به‌جای آن Cloudflare Pages + Cloudflare Access (رایگان تا ۵۰ کاربر) را استفاده کنید؛ همین پوشه بدون تغییر کار می‌کند
  (Build command: `pip install openpyxl && python scripts/build.py` ، Output: `dist`).
- تست روی کامپیوتر: `pip install openpyxl && python scripts/build.py` سپس `dist/index.html` را باز کنید.
