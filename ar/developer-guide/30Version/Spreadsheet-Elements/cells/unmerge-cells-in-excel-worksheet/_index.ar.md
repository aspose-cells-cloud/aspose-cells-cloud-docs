---
title: "إلغاء دمج الخلايا في ورقة عمل Excel"
type: docs
url: /unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, إلغاء دمج الخلايا, REST API, Cloud SDK"
description: "تعرّف على كيفية استخدام Aspose.Cells Cloud REST API لإلغاء دمج الخلايا في ورقة عمل Excel، مع أمثلة على الطلبات، تنسيق الاستجابة، وأكواد عينات SDK لعدة لغات برمجة."
ArticleTitle: "إلغاء دمج الخلايا في ورقة عمل Excel"
---

يقوم هذا REST API بإلغاء دمج الخلايا في ملف Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## الأمان والمصادقة

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة قائمة على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

**مُعلمات الطلب**

| اسم المُعلمة | النوع    | الموقع | الوصف                                             |
|----------------|---------|----------|---------------------------------------------------------|
| name           | string  | path     | اسم ملف المصنف.                              |
| sheetName      | string  | path     | اسم ورقة العمل.                                  |
| startRow       | integer | query    | المؤشر الصفري-الأساسي للصف الأول المراد إلغاء دمجه.           |
| startColumn    | integer | query    | المؤشر الصفري-الأساسي للعمود الأول المراد إلغاء دمجه.        |
| totalRows      | integer | query    | عدد الصفوف التي تُشمل في عملية إلغاء الدمج.    |
| totalColumns   | integer | query    | عدد الأعمدة التي تُشمل في عملية إلغاء الدمج. |
| folder         | string  | query    | مسار المجلد الذي يُخزَّن فيه المصنف.               |
| storageName    | string  | query    | اسم خدمة التخزين.                            |

## **الاستجابة**

ترجع `CellCloudResponse`.

- **نظرة عامة على حقول الاستجابة**

| الحقل           | النوع    | الوصف                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200،400،401،500،...                                 |

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صحيح (Bad Request)                 | مُعلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصرّح له (Unauthorized)                | رمز JWT غير صالح أو ناقص. |
| 413  | حمل البيانات كبير جدًا (Payload Too Large)           | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

## كيفية استخدام PostWorksheetUnmerge API باستخدام SDKs

### مواصفات PostWorksheetUnmerge API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
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

### استخدام Aspose.Cells Cloud SDKs

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى SDK معالجة التفاصيل منخفضة المستوى وتركز أنت على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات الويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}