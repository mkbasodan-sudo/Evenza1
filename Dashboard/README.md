# Global Events Intelligence Dashboard

لوحة تحكم تجارية تعمل بالكامل محليًا دون Backend أو خادم محلي.

## التشغيل

1. فك ضغط المشروع.
2. افتح ملف `index.html` مباشرة باستخدام Chrome أو Edge أو Firefox.
3. ستظهر بيانات الملف المرفق تلقائيًا من النسخة المحلية المدمجة.
4. لتحميل قاعدة بيانات أخرى، اضغط **تحميل Excel** واختر ملف `.xlsx` أو `.xls`.

## المزايا

- مؤشرات إجمالية وديناميكية.
- فلاتر السنة، الشهر، الدولة، المدينة، النوع، الجهة المنظمة، الحالة والبحث.
- رسوم تفاعلية محسوبة من البيانات المفلترة.
- تقويم شهري مع تفاصيل الإيفنت.
- قائمة أقرب الإيفنتات القادمة.
- جدول يدعم الفرز، Pagination، إظهار وإخفاء الأعمدة، CSV، Excel والطباعة.
- Light / Dark Mode.
- العربية والإنجليزية مع RTL/LTR.
- اكتشاف تلقائي للأعمدة العربية والإنجليزية.
- اشتقاق حالة الإيفنت من تاريخ البداية والنهاية عند غياب عمود الحالة.
- معالجة القيم الفارغة والتواريخ غير الصالحة دون توقف التطبيق.

## هيكل المشروع

- `index.html`: نقطة تشغيل التطبيق.
- `css/style.css`: التصميم المتجاوب والثيمات.
- `js/app.js`: إدارة الحالة، اكتشاف الأعمدة، تحميل الملفات والترجمة.
- `js/filters.js`: الفلاتر الديناميكية.
- `js/charts.js`: الرسوم البيانية المحلية عالية الأداء.
- `js/table.js`: الجدول، الفرز، Pagination والتصدير.
- `js/calendar.js`: التقويم الشهري.
- `js/modal.js`: نافذة تفاصيل الإيفنت.
- `js/data.js`: نسخة بيانات مدمجة لضمان التشغيل المباشر عبر `file://`.
- `data/events.xlsx`: ملف Excel الأصلي.
- `libs/jszip.min.js`: مكتبة ZIP محلية.
- `libs/xlsx.full.min.js`: محرك XLSX محلي بواجهة متوافقة مع وظائف SheetJS المستخدمة.

## ملاحظات البيانات

- يختار النظام تلقائيًا ورقة العمل التي تحتوي على أكبر جدول عند رفع ملف جديد.
- لا يعتمد النظام على أسماء أعمدة ثابتة، بل يقارن الأسماء مع مرادفات عربية وإنجليزية.
- للحصول على أفضل نتائج، يجب أن يحتوي الملف على اسم إيفنت وتاريخ بداية. باقي الأعمدة اختيارية.
- عند وجود آلاف الصفوف، يتم عرض الجدول على صفحات لتقليل تكلفة الرسم في DOM.

## الخصوصية

لا يتم رفع أي ملف إلى الإنترنت. تتم القراءة والمعالجة والتصدير داخل المتصفح فقط.

## Version 2.1 updates
- Complete Arabic/English interface translation, including previously hard-coded headings, descriptions, placeholders, status text, filter counters, and page title.
- Automatic RTL/LTR layout switching with saved language preference.
- Improved mobile navigation drawer and backdrop.
- Mobile-friendly KPI cards, filters, charts, calendar, modal, and event list.
- Event table automatically changes to readable card rows on small screens.
- Optimized for screens from 320px wide and above.


## v2.2 update
- Replaced the obsolete Offline Ready label with a bilingual Live Database indicator.
- The sidebar event count is generated dynamically from the loaded dataset.
