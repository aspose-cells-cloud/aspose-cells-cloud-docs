---
title: "حذف جدول محوري في ورقة عمل Excel"
second_title: "Document"
linktitle: Delete
type: docs
url: /ar/pivot-tables/delete/
aliases: [  /ar/delete-worksheet-pivot-table-by-index/ ]
keywords: "Aspose.Cells, جدول محوري, حذف, Excel, REST API"
description: "حذف جدول محوري من ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن تنسيق الطلب، مثال على cURL، رموز الأخطاء، وأجزاء كود SDK بلغات C#، Java، Python، وNode.js."
weight: 70
ArticleTitle: "كيف تحذف جدولًا محوريًا في ورقة عمل Excel باستخدام Aspose.Cells Cloud"
---

يقوم هذا الـ REST API بحذف جدول محوري من ورقة عمل باستخدام فهرسه.

**المتطلبات المسبقة** – يجب أن يكون لديك رمز وصول JWT صالح لـ Aspose.Cells Cloud، وأن يكون ملف Excel المستهدف مخزنًا في موقع مدعوم للتخزين. تأكد من تحديد اسم الملف، واسم الورقة، وتفاصيل التخزين بشكل صحيح قبل استدعاء الـ API.

تعتبر الجداول المحورية وسيلة قوية لتلخيص البيانات في **ورقة عمل Excel**. باستخدام Aspose.Cells Cloud، يمكنك حذف جدول محوري غير مرغوب فيه برمجيًا باستخدام طلب HTTP DELETE واحد. وتُعد هذه العملية مثالية عند الحاجة إلى تنظيف ورقات العمل، أو أتمتة توليد التقارير، أو دمج تعديل ملفات Excel في تطبيقاتك.

## API DeleteWorksheetPivotTable

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعلمات الطلب**

| اسم المُعلمة       | النوع    | الموقع   | الوصف                                              |
| ------------------ | -------- | -------- | --------------------------------------------------- |
| name               | string   | path     | اسم مستند Excel.                                   |
| sheetName          | string   | path     | اسم ورقة العمل التي تحتوي على الجدول المحوري.      |
| pivotTableIndex    | integer  | path     | الفهرس الصفري (zero-based) للجدول المحوري المراد حذفه. |
| folder             | string   | query    | المسار إلى المجلد الذي يحتوي على المستند.         |
| storageName        | string   | query    | اسم خدمة التخزين.                                  |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) واجهة برمجة تطبيقات متاحة عمومًا، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى الـ API السحابي باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**مثال على الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

تتبع الاستجابة مخطط JSON بسيط:

```json
{
  "Code": integer,   // رمز الحالة المشابه لـ HTTP لعملية الحذف
  "Status": string   // وصف نصي، مثل "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### معالجة الأخطاء

تُدرج أدناه رموز حالة الاستجابة الشائعة:

| حالة HTTP | الوصف                                                        |
|----------|-------------------------------------------------------------|
| 400      | طلب غير صالح – مُعلمات مفقودة أو غير صالحة.                 |
| 401      | غير مصرح به – رمز JWT غير صالح أو مفقود.                    |
| 404      | غير موجود – الملف أو الورقة أو الجدول المحوري غير موجود.     |
| 500      | خطأ داخلي في الخادم – حدثت حالة غير متوقعة على الخادم.      |

## عائلة SDK السحابية

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---