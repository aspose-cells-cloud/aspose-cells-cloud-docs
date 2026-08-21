---
title: "إعادة تسمية ورقة عمل إكسل"
second_title: "مستند"
linktitle: "إعادة التسمية"
type: docs
url: /worksheets/rename/
aliases: [/rename-excel-worksheet/]
keywords: "Aspose.Cells Cloud، إعادة تسمية ورقة عمل إكسل، واجهة برمجة تطبيقات REST، مكتبة أدوات جداول البيانات، إعادة تسمية ورقة العمل، التخزين السحابي"
description: "إعادة تسمية ورقة عمل في ملف إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تتوفر مكتبات أدوات (SDKs) لمنصات Android و C# و Go و Java و Node.js و Perl و PHP و Python و Ruby و Swift."
weight: 20
---

تقوم هذه الواجهة البرمجية REST بإعادة تسمية ورقة عمل في ملف إكسل.

## واجهة برمجة التطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rename
```

### **مُعاملات الطلب**

| اسم المُعامل | النوع | الموقع | الوصف |
|-------------|--------|--------|--------|
| name | string | path | اسم ملف إكسل. |
| sheetName | string | path | الاسم الحالي لورقة العمل المراد إعادة تسميتها. |
| newname | string | query | الاسم الجديد لورقة العمل. |
| folder | string | query | مسار المجلد في التخزين (اختياري). |
| storageName | string | query | اسم التخزين (اختياري). |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostRenameWorksheet) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/rename?newname=newSheet" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة مكتبات الأدوات السحابية

استخدام مكتبة أدوات (SDK) هو أفضل طريقة لتسريع عملية التطوير. فالمكتبة تتعامل مع التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات أدوات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات Aspose.Cells عبر واجهات برمجة التطبيقات باستخدام مكتبات أدوات متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostRenameWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostRenameWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-rename_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "RenameExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-RenameWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-RenameWorksheet-rename-excel-worksheeet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-RenameWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "accf2723cfaa2a328d3dea355156e4d9" >}}

{{< /tab >}}

{{< /tabs >}}