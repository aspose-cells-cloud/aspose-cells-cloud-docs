---
title: "إضافة كائن قائمة (جدول) إلى ورقة عمل Excel"
second_title: "الوثيقة"
linktitle: "إضافة"
type: docs
url: /list-objects/add/
aliases: [/add-a-list-object-or-table-inside-the-worksheet/, /tables/add/]
keywords: "Aspose.Cells Cloud، واجهة برمجة تطبيقات Excel، كائن القائمة، جدول، واجهة برمجة تطبيقات REST، ورقة العمل"
description: "تعرّف على كيفية إضافة كائن قائمة (جدول Excel) إلى ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل الـ endpoint، المَعلمات، خطوات المصادقة، مثال cURL، وأمثلة على أكواد SDK."
weight: 10
ArticleTitle: "إضافة كائن قائمة (جدول) إلى ورقة عمل Excel – وثائق Aspose.Cells Cloud"
---

تضيف واجهة برمجة التطبيقات هذه **كائن قائمة (جدول)** إلى ورقة عمل Excel.

قبل استخدام هذه الـ endpoint، تأكّد من امتلاك رمز JWT صالح، واحتفاظ الملف المصنف بتخزين سحابي مدعوم، ووجود ورقة العمل.

## واجهة برمجة التطبيقات REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### مَعلمات الطلب

| اسم المعلمة    | النوع    | الموقع | الوصف                                                              |
| --------------- | ------- | ------ | ------------------------------------------------------------------ |
| **name**        | string  | path   | اسم ملف المصنف.                                                    |
| **sheetName**   | string  | path   | اسم ورقة العمل.                                                     |
| **startRow**    | integer | query  | المؤشر المُعدّ من الصفر لصف أول نطاق الجدول.                        |
| **startColumn** | integer | query  | المؤشر المُعدّ من الصفر لعمود أول نطاق الجدول.                     |
| **endRow**      | integer | query  | المؤشر المُعدّ من الصفر لصف آخر نطاق الجدول.                        |
| **endColumn**   | integer | query  | المؤشر المُعدّ من الصفر لعمود آخر نطاق الجدول.                     |
| **hasHeaders**  | boolean | query  | `true` إذا كان الصف الأول يحتوي على رؤوس أعمدة؛ وإلا `false`.      |
| **listObject**  | object  | body   | تعريف كائن القائمة (انظر **مخطط جسم الطلب**).                      |
| **folder**      | string  | query  | المجلد الذي يحتوي على المصنف.                                      |
| **storageName** | string  | query  | اسم التخزين.                                                       |

### مخطط جسم الطلب

يصف كائن **listObject** الجدول الذي سيتم إنشاؤه. تُعرض فقط الخصائص الأكثر شيوعًا؛ وللحصول على القائمة الكاملة، راجع مواصفات OpenAPI.

```json
{
  "displayName": "MyTable",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MyTable",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### مثال على الاستجابة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### رموز الأخطاء

| الحالة HTTP | السبب                 | الوصف                                            |
| ----------- | --------------------- | ------------------------------------------------ |
| **400**     | Bad Request (طلب غير صالح) | مَعلمات النطاق غير صالحة أو جسم JSON غير مُنسّق بشكل صحيح. |
| **401**     | Unauthorized (غير مُصادَق) | رمز JWT مفقود أو منتهٍ.                          |
| **404**     | Not Found (غير موجود)     | المصنف أو ورقة العمل المحدّدة غير موجودين.      |
| **500**     | Internal Server Error (خطأ داخلي في الخادم) | فشل غير متوقّع من جانب الخادم.         |

**مثال على استجابة 400**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**مثال على استجابة 401**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

توفر [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) العقد الكاملة لهذه العملية.

## مجموعة أدوات Cloud SDK

يُعد استخدام SDK الطريقة الأفضل لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى وتركز أنت على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---