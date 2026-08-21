---
title: "العمل مع صور Excel"
second_title: "مستند"
linktype: "صور"
type: docs
url: /ar/pictures/
aliases: [/ar/working-with-pictures/]
keywords: "Excel، صورة، Aspose.Cells Cloud، REST API، معالجة الصور، صور Excel"
description: "تعلم كيفية استرجاع وإضافة وتحديث وحذف الصور في أوراق عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل أمثلة كود لغات C#، Java، Python، وأخرى."
weight: 100
ArticleTitle: "العمل مع صور Excel – وثائق Aspose.Cells Cloud"
---

## العمل مع الصور في ملف Excel

يشرح هذا الدليل كيفية التعامل مع **الصور** (والتي تُعرف أيضًا بالصور الرقمية) في أوراق عمل Excel من خلال واجهة Aspose.Cells Cloud REST API. ويتناول العمليات الأساسية المتعلقة بالصور—استرجاعها، وإضافتها، وتحديثها، وحذفها—ويوجهك إلى أمثلة مفصّلة لكل مهمة.

**المتطلبات المسبقة**: حساب Aspose.Cells Cloud ومفتاح API صالح وحزمة تطوير البرمجيات (SDK) المناسبة المُثبَّتة للغة البرمجة التي تختارها.

- [كيفية استرجاع صورة بتنسيق معيّن من ورقة عمل Excel.](/ar/cells/pictures/get/) – استرجاع صورة واحدة بتنسيق مطلوب (PNG، JPEG، إلخ) من ورقة العمل.  
- [كيفية استرجاع معلومات جميع الصور من ورقة عمل Excel.](/ar/cells/pictures/get-all/) – سرد البيانات التعريفية لكل صورة موجودة في ورقة العمل.  
- [كيفية إضافة صورة إلى ورقة عمل Excel.](/ar/cells/pictures/add/) – إدخال صورة جديدة إلى ورقة العمل، مع تحديد موقعها وحجمها.  
- [كيفية تحديث صورة معيّنة من ورقة عمل Excel.](/ar/cells/pictures/update/) – تعديل خصائص الصورة (مثل الأبعاد والموقع) لصورة موجودة مسبقًا.  
- [كيفية حذف جميع الصور من ورقة عمل Excel.](/ar/cells/pictures/clear/) – إزالة كائنات الصور جميعها من ورقة العمل في استدعاء واحد.  
- [كيفية حذف صورة معيّنة من ورقة عمل Excel.](/ar/cells/pictures/delete/) – حذف صورة واحدة محددة حسب فهرسها.  

**مرجع واجهة برمجة التطبيقات**

**استرجاع صورة بتنسيق معيّن**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | طلب مثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|----------|---------------|-------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (مسار)، `sheetName` (مسار)، `pictureIndex` (مسار)، `format` (استعلام) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | بيانات الصورة الثنائية (PNG، JPEG، إلخ) | 200 OK، 400 طلب غير صالح، 401 غير مُصرّح، 404 غير موجود، 500 خطأ في الخادم |

**استرجاع معلومات جميع الصور**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | طلب مثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|----------|---------------|-------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (مسار)، `sheetName` (مسار) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | مصفوفة JSON تحتوي على بيانات تعريفية للصور (الفهرس، الاسم، الموقع، الحجم) | 200 OK، 400، 401، 404، 500 |

**إضافة صورة**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | جسم الطلب المثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|------------------|---------------|-------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (مسار)، `sheetName` (مسار) | `{ "image": "<base64‑encoded‑image>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 تم الإنشاء، 400، 401، 404، 500 |

**تحديث صورة**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | جسم الطلب المثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|------------------|---------------|-------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (مسار)، `sheetName` (مسار)، `pictureIndex` (مسار) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK، 400، 401، 404، 500 |

**حذف جميع الصور**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | طلب مثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|----------|---------------|-------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (مسار)، `sheetName` (مسار) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK، 400، 401، 404، 500 |

**حذف صورة معيّنة**

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة | طلب مثال | استجابة مثال | رموز الحالة |
|-----------|-------------|------------------|----------|---------------|-------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (مسار)، `sheetName` (مسار)، `pictureIndex` (مسار) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK، 400، 401، 404، 500 |

**مواضيع ذات صلة**

استكشف عمليات أخرى مرتبطة بالصور في Aspose.Cells Cloud:  
- [العمل مع الأشكال](/ar/cells/shapes/) – إضافة وتعديل وحذف أشكال الرسم.  
- [العمل مع المخططات البيانية](/ar/cells/charts/) – إنشاء كائنات المخططات البيانية والتعامل معها.  
- [العمل مع الصور في أوراق العمل](/ar/cells/images/) – تضمين وإدارة ملفات الصور الأولية.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "العمل مع صور Excel – وثائق Aspose.Cells Cloud",
  "description": "دليل لاسترجاع وإضافة وتحديث وحذف صور Excel عبر واجهة Aspose.Cells Cloud REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "صور Excel، Aspose.Cells Cloud، REST API، معالجة الصور",
  "url": "https://docs.aspose.cloud/ar/cells/pictures/"
}
</script>