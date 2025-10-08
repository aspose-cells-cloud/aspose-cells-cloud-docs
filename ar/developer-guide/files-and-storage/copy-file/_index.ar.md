---
title: نسخ الملف - Excel AP
second_title: Documen
linktitle: نسخ الملف
type: docs
url: /ar/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: تعرف على كيفية استخدام CopyFile API لـ Excel لمضاعفة جداول البيانات بكفاءة والتعامل مع تنسيقات الملفات المختلفة
weight: 100
kwords: Excel API، Office السحابة، REST API، نسخ جدول بيانات، PDF التحويل، تصدير CSV، معالجة JSON، دعم Markdown، نسخ Excel الملف، مطابقة الخلية الفارغة
---
## **Excel API: نسخ الملف**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **وصف الوظيفة**

 ال**نسخ الملف** يتيح API للمستخدمين تكرار ملف Excel من مسار مصدر محدد إلى مسار وجهة، مع دعم خيارات تخزين مختلفة.

###  معلمات الطلب**نسخ الملف** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|-------------- ||--------------------- |-------------------------------------- |
| مسار src| خيط| طريق| المسار المصدر للملف الذي سيتم نسخه.|
| مسار الوجهة| خيط| استفسار| المسار الوجهة الذي سيتم حفظ الملف فيه.|
| اسم تخزين src| خيط| استفسار| اسم مصدر التخزين.|
| اسم التخزين| خيط| استفسار| اسم التخزين الوجهة.|
| معرف الإصدار| خيط| استفسار| معرف الإصدار الاختياري للملف الذي سيتم نسخه.|

### **وصف الاستجابة**

```json
{
Void
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/CopyFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. تُدير هذه الحزمة التفاصيل البسيطة، مما يُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
