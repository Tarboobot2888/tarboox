
# TARBOO DEOBFUSCATE — دمج webcrack

كل خوارزميات فك الشيفرة (deobfuscate/unminify/unpack) وأكواد الواجهة من مشروع webcrack-master الآن داخل مشروعك الحالي، في مجلد lib/webcrack.

---

## محتوى المجلد

- **deobfuscate/** — خوارزميات فك التشفير (array-rotator, control-flow, string-array, وغيرها)
- **unminify/** — تحويل الكود المصغر (minified) إلى كود قابل للقراءة
- **unpack/** — فك الباندلز (Webpack/Browserify)
- **apps/playground/** — واجهة المستخدم التجريبية لتجربة الخوارزميات بشكل بصري
- **index.ts** — نقطة دخول رئيسية
- باقي الملفات: أدوات مساعدة، إعدادات، توثيق...

---

## مثال: استدعاء خوارزمية من المسار الجديد

```js
// استدعاء من Node.js أو Next.js أو مشروعك
const { deobfuscateStringArray } = require('./lib/webcrack/deobfuscate/string-array');
const result = deobfuscateStringArray(sourceCode);
```

أو مع TypeScript:

```ts
import { deobfuscateStringArray } from './lib/webcrack/deobfuscate/string-array';
const result = deobfuscateStringArray(sourceCode);
```

نفس الطريقة لأي ملف آخر في المجلد.

---

## تشغيل واجهة التجربة (playground)

```bash
cd lib/webcrack/apps/playground
npm install
npm run dev
```
ثم افتح الرابط الذي يظهر لك.

---

## نصائح:
- يمكنك نقل أو تحديث أي ملف بسهولة مستقبلًا.
- جميع الأكواد أصلية لم يتم تغيير أي منطق فيها سوى المسار.
- استخدم الأكواد الجديدة مع أي محرر أو صفحة لديك.

---

*صديقك البرمجي: دمج الخوارزميات هو سحر التقنية وعبقرية الجيل الجديد!*

---

## تحديث جديد: إضافة ملفات ومجلدات من packages.zip

تم دمج جميع الأكواد والمكتبات والمكونات البرمجية من ملف packages.zip بالكامل في نفس المسار:
lib/webcrack/
بدون أي تعارض في الأسماء أو فقدان لأي كود.

يمكنك استخدام واستدعاء أي ملف أو مكون من مجلد lib/webcrack، سواء من webcrack-master أو من packages.

جميع التعليمات السابقة صالحة، فقط ابحث عن ملفك أو خوارزميتك داخل نفس المجلد.

---
