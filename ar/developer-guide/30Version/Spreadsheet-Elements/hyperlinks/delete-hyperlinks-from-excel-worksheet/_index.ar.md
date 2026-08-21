---
title: "مسح الروابط التشعبية"
type: docs
url: /ar/hyperlinks/clear/
aliases: [  /ar/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, مسح الروابط التشعبية, حذف الروابط التشعبية, REST API, ورقة عمل, SDK"
description: "تعرّف على كيفية إزالة جميع الروابط التشعبية من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API أو أي SDK مدعوم (C#، Java، Python، Node.js، Go، PHP، Ruby، Perl، إلخ)."
weight: 40
ArticleTitle: "مسح الروابط التشعبية – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لـ REST بحذف **جميع الروابط التشعبية** الموجودة في ورقة عمل Excel.

## الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|--------|--------|--------|
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل. |
| folder | string | query | المجلد الذي يحتوي على المستند. |
| storageName | string | query | اسم خدمة التخزين. |

### استجابات الأخطاء

| كود HTTP | السبب | مثال على جسم الاستجابة |
|----------|--------|------------------------|
| **400** | طلب غير صالح – معاملات مفقودة أو غير صالحة. | `{ "Code":"400", "Message":"قيمة معامل غير صالحة." }` |
| **401** | غير مُصرّح – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"رمز الوصول مفقود أو غير صالح." }` |
| **404** | غير موجود – المصنف أو ورقة العمل غير موجودين. | `{ "Code":"404", "Message":"الملف غير موجود." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"حدث خطأ غير متوقع." }` |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) واجهة برمجة تطبيقات متاحة للعامة، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية حذف جميع الروابط التشعبية من ورقة عمل.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للحوسبة السحابية

استخدام SDK يُسرّع التطوير من خلال معالجة التفاصيل منخفضة المستوى نيابةً عنك. للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud، تفضل بزيارة [مستودع GitHub](https://github.com/aspose-cells-cloud).

توضّح أمثلة الكود التالية كيفية حذف الروابط التشعبية من ورقة العمل باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}