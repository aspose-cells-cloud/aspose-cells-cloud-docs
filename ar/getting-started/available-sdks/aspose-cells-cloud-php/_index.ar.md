---
title: "Aspose.Cells Cloud SDK لـ PHP – تحويل ودمج وتقسيم وحماية ملفات إكسل"  
second_title: "وثيقة"  
ArticleTitle: "Aspose.Cells Cloud SDK لـ PHP – تحويل ودمج وتقسيم وحماية ملفات إكسل"  
linktitle: "Aspose.Cells Cloud SDK لـ PHP"  
type: docs  
url: /ar/available-sdks/aspose-cells-cloud-php/
description: "حمّل Aspose.Cells Cloud SDK لـ PHP (الإصدار 24.3). تعلّم كيفية التثبيت عبر Composer، والمصادقة، وتحويل ملفات XLSX إلى PDF/CSV، ودمج ملفات العمل، وحماية الأوراق، وأكثر من ذلك – كل ذلك دون الحاجة لتثبيت Office."  
keywords: "Aspose.Cells، السحابة، PHP، SDK، إكسل، تحويل، دمج، تقسيم، حماية"  
weight: 30  
---  

يُعدّ SDK مفتوح المصدر ومرخّص بموجب ترخيص MIT. يمكنك الوصول إلى كود مكتبة PHP الخاصة بـ Aspose.Cells Cloud <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">هنا</a>.

# **كيفية استخدام Aspose.Cells Cloud SDK لـ PHP**

تُعتبر مكتبة Aspose.Cells Cloud SDK لـ PHP مكتبة قوية تتيح للمطورين التعامل مع ملفات مايكروسوفت إكسل ومعالجتها باستخدام **لغة البرمجة PHP**. وباستخدام هذا SDK، يمكنك إنشاء وتحرير وتحويل مستندات إكسل في السحابة، دون الحاجة لتثبيت أي برامج إضافية أو اعتماديات على جهازك المحلي.

في هذه المقالة، سنستعرض كيفية استخدام Aspose.Cells Cloud SDK لـ PHP لأداء بعض المهام الشائعة، مثل إنشاء ملف عمل إكسل جديد، وإدخال بيانات في الخلايا، وحفظ ملف العمل المعدّل في السحابة.

## البدء

قبل أن تبدأ باستخدام Aspose.Cells Cloud SDK لـ **PHP**، تحتاج إلى إعداد بيئة التطوير وتثبيت الاعتماديات المطلوبة. راجع <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">المقالة</a> على موقع Aspose للحصول على معرّف العميل (Client ID) وسرّ العميل (Client Secret).

**المتطلبات الأساسية**

- PHP الإصدار 7.4 أو أحدث  
- Composer مثبت على جهاز التطوير الخاص بك  
- معرّف عميل وسرّ عميل ساري المفعول لـ Aspose Cloud  
- وصول إلى موقع تخزين Aspose Cloud (افتراضي أو مخصص)  

## كيفية تثبيت حزمة PHP الخاصة بـ Aspose.Cells Cloud

يمكنك تثبيت Aspose.Cells Cloud SDK لـ PHP. فيما يلي الخطوات المتبعة:

- أضف Aspose.Cells Cloud كاعتمادية في ملف `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- نفّذ أمر تحديث Composer لتثبيت SDK:

   ```bash
   composer install
   ```

- أدرج مُحمّل التلقائي (Autoloader) الخاص بـ Composer في كود PHP الخاص بك:

   ```php
   require 'vendor/autoload.php';
   ```

## كيفية استخدام حزمة PHP لتحويل ملفات Xlsx إلى صيغ أخرى

- استيراد مكتبة Aspose.Cells Cloud  
  ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud SDK لـ PHP إلى مشروعك.

- تهيئة عميل API凭 التأكّد من الهوية  
  قم بمصادقة عميل API باستخدام معرّف العميل وسرّ العميل الفريد الخاص بك.

- إعداد معلمات التحويل  
  عرّف المعلمات المطلوبة لمهمة التحويل، بما في ذلك اسم الملف المصدر، وصيغة الإخراج المرغوبة، ومسار مجلد التخزين.

- تنفيذ عملية تحويل ملف العمل  
  استدعِ عملية التحويل باستخدام الدالة `PostConvertWorkbook` وتعامل مع الاستجابة.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### المرجع البرمجي لـ `PostConvertWorkbook`

| المعلمة       | الوصف                                         | النوع   | إجباري |
|---------------|------------------------------------------------|---------|---------|
| `file`        | اسم ملف إكسل المصدر (مثلًا: `sample.xlsx`).  | نص (string) | نعم |
| `format`      | صيغة الإخراج المرغوبة (`pdf`، `csv`، `png`، إلخ). | نص (string) | نعم |
| `storage`     | اسم مجلد التخزين أو مساره حيث يوجد الملف المصدر. | نص (string) | لا |
| `outPath`     | مسار اختياري لحفظ الملف المحول مباشرة في التخزين. | نص (string) | لا |

**طريقة HTTP:** POST  
**نقطة النهاية:** `/cells/convert/{format}`  

**مثال على الاستجابة (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**أكواد الحالة (Status Codes)**

- `200` – تم التحويل بنجاح.  
- `400` – طلب غير صالح (معلمات مفقودة أو غير صحيحة).  
- `401` – فشلت المصادقة.  
- `500` – خطأ في الخادم.  
---