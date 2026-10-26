# موقع المحامي الدكتور عادل بهبهاني

موقع ثابت (HTML / CSS / JS) لمكتب الدكتور عادل بهبهاني المحامي – للمحاماة والاستشارات القانونية.

## الهيكل

```
index.html            الصفحة الرئيسية
assets/css/style.css  التنسيقات
assets/js/main.js     القائمة على الموبايل وتأثيرات الظهور
assets/img/           الصور
.github/workflows/    النشر التلقائي على Hostinger
```

## النشر على Hostinger

كل `push` على فرع `main` يرفع الملفات تلقائياً على Hostinger عن طريق FTP.

أضف في الريبو من **Settings ← Secrets and variables ← Actions**:

| النوع | الاسم | القيمة |
|---|---|---|
| Secret | `FTP_SERVER` | عنوان FTP من hPanel (مثال: `ftp.example.com` أو IP) |
| Secret | `FTP_USERNAME` | اسم مستخدم FTP |
| Secret | `FTP_PASSWORD` | كلمة سر FTP |
| Variable (اختياري) | `FTP_SERVER_DIR` | مجلد الرفع، الافتراضي `public_html/` |

بيانات FTP موجودة في hPanel ← **Files ← FTP Accounts**.

> لو اسم المستخدم مربوط بمجلد `public_html` مباشرة، خلي `FTP_SERVER_DIR` = `./`

لتشغيل النشر يدوياً: **Actions ← Deploy to Hostinger ← Run workflow**.

## التشغيل محلياً

افتح `index.html` في المتصفح، أو:

```bash
python3 -m http.server 8000
```
