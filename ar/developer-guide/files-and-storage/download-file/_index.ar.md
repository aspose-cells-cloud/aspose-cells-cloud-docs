---
title: تنزيل الملف من Aspose.Cells AP
second_title: Developer Guide for Aspose.Cells AP
linktitle: تنزيل ملف AP
type: docs
url: /ar/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: تعرف على كيفية استخدام Aspose.Cells API لتنزيل الملفات بما في ذلك Excel وPDF وCSV والمزيد بكفاءة
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، تنزيل ملف Excel، استرجاع ملف فارغ Cells
---
## **Excel API: تنزيل الملف**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **وصف الوظيفة**

 ال**تنزيل الملف** يتيح لك API استرجاع الملفات المخزنة في مساحة التخزين السحابية Aspose. تُعد هذه الوظيفة أساسية لإدارة تنسيقات الملفات المختلفة والوصول إليها، بما في ذلك جداول البيانات Excel وملفات PDF وCSV.

###  معلمات الطلب**تنزيل الملف** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| المسار إلى الملف الذي تريد تنزيله.|
| اسم التخزين| خيط| استفسار| اسم وحدة التخزين التي سيتم استرجاع الملف منها.|
| معرف الإصدار| خيط| استفسار| معرف إصدار الملف الذي سيتم تنزيله، إذا كان ذلك ممكنًا.|

### **وصف الاستجابة**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعالج التفاصيل البسيطة وتُمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
