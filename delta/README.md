# Delta Squad

موقع لوحة المتصدرين / الأعضاء / المهام لفريق Delta Squad.

## البنية

```
delta/
├── index.html          # الصفحة الرئيسية (كل شي فيها: لوحة المتصدرين، الأعضاء، المهام)
└── assets/
    ├── logo.png         # شعار الفريق
    └── members/
        └── kyubi.jpg    # صورة العضو (ضيف صور باقي الأعضاء هنا)
```

## تضيف صورة عضو جديد

1. حط صورته داخل `assets/members/` (مثلاً `assets/members/falcon.jpg`).
2. افتح `index.html`، ودوّر على `MEMBER_PHOTOS` بالسكربت، وضيف سطر:
   ```js
   const MEMBER_PHOTOS = {
     "Kyubi": "assets/members/kyubi.jpg",
     "Falcon Ops": "assets/members/falcon.jpg"
   };
   ```
   الاسم لازم يطابق حرفياً الاسم الموجود بمصفوفة `membersData`.

## رفعه على GitHub Pages

1. سوّي repository جديد وارفع محتويات مجلد `delta/` كامل (مو مضغوط) لجذر الـ repo.
2. من إعدادات الـ repo: **Settings → Pages → Source** اختر الفرع (`main`) والمجلد (`/root`).
3. بعد دقيقة أو دقيقتين، الموقع يصير متاح على:
   `https://<username>.github.io/<repo-name>/`

## ملاحظة

كل التعديلات (تغيير الاسم، الرتبة...) اللي تصير من المتصفح تُحفظ محلياً بمتصفح الزائر فقط (localStorage)، ومو منعكسة على الملف نفسه أو لباقي الزوار.
