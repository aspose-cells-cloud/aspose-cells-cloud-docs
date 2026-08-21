---
title: "إخفاء صفوف في ورقة عمل Excel"
second_title: "مستند"
linktitle: "إخفاء"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "إخفاء الصفوف، Aspose.Cells Cloud، Excel API، REST، SDK"
description: "تعرّف على كيفية إخفاء صف واحد أو عدة صفوف في ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API. يتضمن مثال cURL، مقاطع كود للـ SDK، المعاملات، المصادقة، تفاصيل الاستجابة، ومعالجة الأخطاء."
weight: 40
ArticleTitle: "إخفاء الصفوف في ورقة عمل Excel باستخدام Aspose.Cells Cloud API"
---

يقوم هذا الـ REST API بإخفاء الصفوف في ورقة عمل Excel.

**المتطلبات الأساسية:** رمز JWT Bearer ساري المفعول تم الحصول عليه من نقطة نهاية OAuth الخاصة بـ Aspose Cloud، وملف المصنف المخزن في مستودع Aspose Cloud، واسم ورقة العمل التي تحتوي على الصفوف المراد إخفاؤها. يعمل الـ API مع ملفات Excel بصيغ XLS وXLSX وغيرها من الصيغ المدعومة.

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| المعامل         | النوع     | الموقع   | الوصف                                                              |
|------------------|-----------|----------|---------------------------------------------------------------------|
| **name**         | سلسلة نصية | المسار   | اسم ملف المصنف.                                                     |
| **sheetName**    | سلسلة نصية | المسار   | اسم ورقة العمل التي تحتوي على الصفوف المراد إخفاؤها.               |
| **startrow**     | عدد صحيح  | الاستعلام | المؤشر الصفر-based للصف الأول المراد إخفاؤه.                      |
| **totalRows**    | عدد صحيح  | الاستعلام | عدد الصفوف المتتالية المراد إخفاؤها، ابتداءً من **startrow**.      |
| **folder**       | سلسلة نصية | الاستعلام | المجلد في المستودع حيث يوجد المصنف.                                |
| **storageName**  | سلسلة نصية | الاستعلام | اسم خدمة التخزين.                                                   |

يُوفّر [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows) واجهة برمجة تطبيقات مفتوحة ومتاحة للعامة تسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات ويب Aspose.Cells. يتطلب الـ API رمز JWT Bearer تم الحصول عليه من نقطة نهاية OAuth الخاصة بـ Aspose Cloud؛ ويجب تضمينه في الرأس `Authorization`. يوضح المثال التالي كيفية إخفاء صف باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
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

**رموز حالة الاستجابة**

| الرمز | الوصف                              |
|-------|-------------------------------------|
| 200   | نجاح – تم إخفاء الصفوف              |
| 400   | طلب غير صالح – معاملات غير صحيحة   |
| 401   | غير مصرّح به – رمز JWT مفقود أو غير صالح |
| 404   | غير موجود – المصنف أو ورقة العمل غير موجودة |
| 500   | خطأ في الخادم – فشل في المعالجة الداخلية |

تُعيد الاستدعاءات الناجحة كائن JSON يحتوي على الحقلين `Code` و`Status`. وفي حال حدوث خطأ، تتضمن الاستجابة حقول إضافية مثل `Message` ورموز الحالة HTTP المناسبة (مثل 400، 401، 404، 500).

**ملاحظات:** تأكد من أن قيمة `startrow` تقع ضمن نطاق الصفوف في ورقة العمل؛ وإلا فسيُعيد الـ API خطأ 400. وتكون مؤشرات الصفوف صفرية البداية، لذا فإن `startrow=0` يشير إلى الصف الأول.

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لدمج هذه الوظيفة في تطبيقك. وتتولى SDKs إدارة التفاصيل من المستوى المنخفض، بحيث يمكنك التركيز على المنطق التجاري. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

 تعرض مقاطع الكود التالية كيفية إخفاء الصفوف باستخدام مكتبات SDK مختلفة. (تشير أسماء الملفات في الأمثلة إلى "Unhide" بسبب تسمية قديمة؛ بينما يقوم الكود داخل كل مقتطف بتنفيذ عملية **Hide**.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}