---
title: "تحديث كائن قائمة في ورقة عمل Excel"
ArticleTitle: "تحديث كائن قائمة في ورقة عمل Excel – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "تحديث"
type: docs
url: /ar/list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells، ListObject، تحديث الجدول، واجهة برمجة تطبيقات Excel، REST، حزمة تطوير البرامج السحابية، تحديث كائن القائمة، ورقة عمل Excel، جدول"
description: "تعرّف على كيفية تحديث جدول Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0). تتضمن النقطة الطرفية، المعلمات، مثال cURL، أكواد الأخطاء وأمثلة SDK."
weight: 20
---

تقوم واجهات برمجة تطبيقات Aspose.Cells Cloud بتحديث خصائص **كائن القائمة** (الجدول) في ورقة عمل Excel.

## الأمان والمصادقة

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## مخطط جسم الطلب

يحتوي كائن البيانات `listObject` (DTO) على الحقول التالية. الحقول المطلوبة في جسم الطلب هي فقط تلك التي تحتاج إلى تغييرها.

| الحقل                                           | النوع               | الإلزام | الوصف                                                                |
| ----------------------------------------------- | ------------------ | -------- | -------------------------------------------------------------------------- |
| **DisplayName**                                 | string             | اختياري | الاسم المعروض للجدول.                                          |
| **StartRow** / **StartColumn**                  | integer            | اختياري | الفهرس الصفر-based للصف/العمود الأول في الجدول.                     |
| **EndRow** / **EndColumn**                      | integer            | اختياري | الفهرس الصفر-based للصف/العمود الأخير في الجدول.                      |
| **Range**                                       | string             | اختياري | عنوان بنمط A-1 يُعرّف نطاق الجدول (مثل `A1:D10`).           |
| **ShowHeaderRow**                               | boolean            | اختياري | `true` لعرض صف العنوان.                                          |
| **ShowTotals**                                  | boolean            | اختياري | `true` لعرض صف المجموعات.                                          |
| **TableStyleName**                              | string             | اختياري | اسم نمط الجدول الجاهز المراد تطبيقه.                                 |
| **TableStyleType**                              | string             | اختياري | نوع النمط (`TableStyleLight`، `TableStyleMedium`، إلخ).                  |
| **ListColumns**                                 | array of objects   | اختياري | مجموعة تعريفات الأعمدة (`Name`، `TotalsCalculation`).            |
| **Sorter**، **AutoFilter**، **ShowTableStyle…** | object             | اختياري | خيارات متقدمة للتنسيق والتصفية (انظر مُعرّف البيانات الكامل في مواصفات OpenAPI). |

### مثال الحد الأدنى من حمولة الطلب

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **معلمات الطلب**

| اسم المعلمة      | النوع    | الموقع | الوصف                         |
| ------------------- | ------- | -------- | ----------------------------------- |
| **name**            | string  | path     | اسم المستند.                      |
| **sheetName**       | string  | path     | اسم ورقة العمل.                     |
| **listObjectIndex** | integer | path     | فهرس كائن القائمة المراد تحديثه. |
| **listObject**      | object  | body     | كائن البيانات `ListObject` في جسم الطلب. |
| **folder**          | string  | query    | المجلد الذي يحتوي على المستند.  |
| **storageName**     | string  | query    | اسم وحدة التخزين.                |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك تنفيذ تفاعلات REST مباشرة من متصفح ويب.

### الطلب

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### الاستجابة

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

تشمل الاستجابة الناجحة الحقول التالية:

| الحقل   | النوع   | الوصف                              |
| ------- | ------ | ---------------------------------------- |
| Code    | integer| رمز حالة HTTP (200 للنجاح).      |
| Status  | string | وصف نصي للحالة.       |
| UpdatedObject *(اختياري)* | object | تمثيل `ListObject` المُحدّث، ويحتوي على الخصائص التي تم تعديلها. |

{{< /tab >}}

{{< /tabs >}}

## استجابات الأخطاء

| رمز HTTP | الوصف                                                                   | مثال حمولة الطلب                                         |
| --------- | ----------------------------------------------------------------------------- | ------------------------------------------------------ |
| **400**   | طلب غير صالح – حقول مفقودة أو JSON غير صحيح.                      | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**   | غير مُصادق عليه – رمز JWT مفقود أو غير صالح.                               | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**   | غير موجود – المستند أو ورقة العمل أو كائن القائمة المحدد غير موجود. | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**   | خطأ داخلي في الخادم – شرط غير متوقع من جانب الخادم.              | `{ "Code": 500, "Message": "Server error." }`          |

## الأسئلة الشائعة

<details>  
<summary>كيف أُحدّث كائن قائمة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud؟</summary>

استخدم النقطة الطرفية `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. تضمن جسم JSON يحتوي على الخصائص التي ترغب في تعديلها (مثل `DisplayName`، `ShowHeaderRow`). قم بالمصادقة باستخدام رمز JWT في رأس `Authorization`.

</details>

<details>  
<summary>ما هي الاستجابة التي أتلقاها بعد التحديث الناجح؟</summary>

يُعاد كائن JSON يحتوي على `Code: 200` و `Status: "OK"`. في حالة حدوث خطأ، تحتوي الاستجابة على رمز حالة HTTP المناسب وكائن `Error` يصف المشكلة.

</details>

<details>  
<summary>هل يمكنني تحديث مجموعة فرعية فقط من خصائص كائن القائمة؟</summary>

نعم. قم بتضمين الحقول التي ترغب في تعديلها فقط في جسم الطلب؛ ستظل جميع الحقول المُهمَلة دون تغيير.

</details>

## الوثائق ذات الصلة

- [إضافة كائن قائمة](https://docs.aspose.cloud/cells/ar/list-objects/add/)
- [الحصول على كائن قائمة](https://docs.aspose.cloud/cells/ar/list-objects/get/)
- [حذف كائن قائمة](https://docs.aspose.cloud/cells/ar/list-objects/delete/)

## عائلة حزم SDK السحابية

استخدام حزمة SDK هي أفضل طريقة لتسريع عملية التطوير. فحزمة SDK تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بحزم SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}