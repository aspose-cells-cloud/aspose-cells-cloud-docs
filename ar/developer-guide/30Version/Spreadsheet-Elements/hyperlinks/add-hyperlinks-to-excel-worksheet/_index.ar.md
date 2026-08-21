---
title: "إضافة رابط تشعبي إلى ورقة عمل"
type: docs
url: /ar/hyperlinks/add/
aliases: [  /ar/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells, إضافة رابط تشعبي, Excel REST API, SDK سحابي"
description: "تعرّف على كيفية إضافة رابط تشعبي إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API الإصدار 3.0. تتضمن الرابط، دليلاً كاملاً للمعاملات، مثالًا باستخدام cURL، وأكواد مقتطفة للغات C# وJava وPython وغير ذلك."
weight: 20
---

تقوم هذه الواجهة البرمجية للواجهة (REST API) بإضافة رابط تشعبي إلى ورقة عمل Excel.

## واجهة برمجة التطبيقات REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### معاملات الطلب

| اسم المعامل | النوع  | الموقع | الوصف                                                                                     |
|-------------|--------|--------|-------------------------------------------------------------------------------------------|
| name        | string | path   | اسم المستند.                                                                              |
| sheetName   | string | path   | اسم ورقة العمل.                                                                           |
| firstRow    | integer | query | المؤشر المبدئي (من الصفر) للصف الأول في النطاق الذي سيُطبّق عليه الرابط التشعبي.        |
| firstColumn | integer | query | المؤشر المبدئي (من الصفر) للعمود الأول في النطاق الذي سيُطبّق عليه الرابط التشعبي.      |
| totalRows   | integer | query | عدد الصفوف التي يغطيها نطاق الرابط التشعبي.                                              |
| totalColumns| integer | query | عدد الأعمدة التي يغطيها نطاق الرابط التشعبي.                                             |
| address     | string | query | عنوان URL الهدف الذي يشير إليه الرابط التشعبي (مُشفّر بتنسيق URL).                       |
| folder      | string | query | مجلد المستند.                                                                             |
| storageName | string | query | اسم وحدة التخزين.                                                                         |

يمكن أن يتضمّن الطلب أيضًا جسمًا JSON يحتوي على نفس الحقول (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). يُفضّل تزويد الجسم عند تفضيل استخدام حمولة البيانات (payload) على معاملات سلسلة الاستعلام.

### استجابات الأخطاء

| الكود HTTP | السبب                                                  | مثال على الجسم                                                           |
|------------|--------------------------------------------------------|---------------------------------------------------------------------------|
| **400**    | طلب غير صالح – معاملات مفقودة أو غير صالحة.          | `{ "Code":"400", "Message":"Invalid parameter value." }`                 |
| **401**    | غير مُصادَق – رمز JWT مفقود أو غير صالح.             | `{ "Code":"401", "Message":"Access token is missing or invalid." }`      |
| **404**    | غير موجود – المستند أو ورقة العمل غير موجودة.         | `{ "Code":"404", "Message":"File not found." }`                          |
| **500**    | خطأ داخلي في الخادم – فشل غير متوقع في الخادم.       | `{ "Code":"500", "Message":"An unexpected error occurred." }`            |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يُظهر المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
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

في حال فشل الطلب، تُعيد الواجهة أكواد HTTP الأخطائية القياسية (مثل 400 Bad Request، 401 Unauthorized، 404 Not Found، 500 Internal Server Error)، مُرفقةً بحمولة JSON تحتوي على رسالة ورمز الخطأ.

## عائلة SDK السحابية

يُعد استخدام SDK أسرع طريقة لتطوير التطبيقات. فتتولى SDK التعامل مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}