---
title: "تحويل كائن القائمة إلى نطاق – واجهة Aspose.Cells Cloud API"
ArticleTitle: "تحويل كائن القائمة إلى نطاق باستخدام واجهة Aspose.Cells Cloud API"
second_title: "وثيقة"
linktitle: "التحويل"
type: docs
url: /ar/list-objects/to-range/
aliases:
  - /convert-list-object-or-table-to-range/
  - /tables/to-range/
keywords: "واجهة Aspose Cells API، تحويل كائن القائمة إلى نطاق، واجهة Excel REST API"
description: "تعلم كيفية تحويل كائن القائمة (جدول) في ملف Excel إلى نطاق باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن بناء الجملة الخاصة بالطلب، والمَعلمات، ونموذج cURL، ومخطط الاستجابة، وتفاصيل المصادقة، وأكواد الأخطاء، وأمثلة لواجهات برمجة التطبيقات (SDK)."
weight: 30
---

تقوم هذه الواجهة REST بتحويل **كائن القائمة (جدول)** إلى **نطاق** داخل ورقة عمل Excel.

**المتطلبات المسبقة:**  
قبل استدعاء نقطة النهاية (endpoint)، تأكد من أن ملف المصنف مُحمّل في مساحة التخزين الخاصة بـ Aspose Cloud، وتحتوي ورقة العمل على كائن القائمة المستهدف، وأنك تستخدم تنسيق ملف مدعوم (مثل .xlsx أو .xlsm).

## واجهة REST API

**المصادقة**  
لاستدعاء هذه العملية، يجب أن تتضمن رأس `Authorization` رمزًا صحيحًا من نوع JWT. احصل على الرمز بإرسال طلب POST إلى نقطة نهاية رموز OAuth 2.0 باستخدام مُعرّف العميل (client ID) والسر السري لمُعرّف العميل (client secret). يجب أن يشمل الرمز النطاق `Cells.ReadWrite`، ويظل صالحًا لمدة الوقت المُعيّن من خدمة الرموز.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/ConvertToRange
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مَعلمات الطلب

| الاسم               | النوع    | الموقع  | مطلوب | القيمة الافتراضية | الوصف                                                    |
| ------------------- | ------- | ------- | ------ | ----------------- | ---------------------------------------------------------- |
| **name**            | سلسلة نصية | مسار    | نعم    | –                 | اسم ملف Excel.                                            |
| **sheetName**       | سلسلة نصية | مسار    | نعم    | –                 | اسم ورقة العمل التي تحتوي على كائن القائمة.              |
| **listObjectIndex** | عدد صحيح | مسار    | نعم    | –                 | المؤشر المُعد من الصفر لكائن القائمة (الجدول) المراد تحويله. |
| **folder**          | سلسلة نصية | استعلام | لا     | –                 | مسار المجلد الذي يُخزَّن فيه الملف.                      |
| **storageName**     | سلسلة نصية | استعلام | لا     | –                 | اسم خدمة التخزين.                                         |

> **ملاحظة:** تعمل هذه العملية فقط مع تنسيقات Excel الحديثة مثل **.xlsx** و **.xlsm**. لا يجب أن يكون كائن القائمة محميًا. لمزيد من المعلومات حول كائنات القوائم، راجع [نظرة عامة على كائنات القوائم](/list-objects/). وللحصول على تفاصيل حول العمل مع النطاقات، راجع [وثيقة النطاقات](/ranges/).

### مثال على cURL (الطلب)

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0/ConvertToRange" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

#### مخطط الاستجابة

تُعيد الواجهة استجابة **200 OK** مع تفاصيل النطاق الجديد الذي تم إنشاؤه.

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

| الحقل           | النوع    | الوصف                                              |
| --------------- | ------- | ---------------------------------------------------- |
| **Code**        | عدد صحيح | رمز حالة مشابه لبروتوكول HTTP (200 يشير إلى نجاح العملية). |
| **Status**      | سلسلة نصية | رسالة الحالة النصية.                               |
| **RangeName**   | سلسلة نصية | الاسم المُسنَد إلى النطاق الذي تم إنشاؤه.          |
| **Address**     | سلسلة نصية | العنوان الكامل للنطاق، بما في ذلك اسم ورقة العمل.   |
| **FirstRow**    | عدد صحيح | المؤشر المُعد من الصفر لصف أول عنصر في النطاق.      |
| **FirstColumn** | عدد صحيح | المؤشر المُعد من الصفر لعمود أول عنصر في النطاق.    |
| **RowCount**    | عدد صحيح | عدد الصفوف في النطاق.                               |
| **ColumnCount** | عدد صحيح | عدد الأعمدة في النطاق.                              |

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                |
|------|-----------------------------|------------------------------------------------------|
| 200  | OK                          | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request                 | مَعلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized                | رمز JWT غير صالح أو مفقود.                           |
| 413  | Payload Too Large           | حجم الملف المرفّع يتجاوز الحد المسموح.               |
| 500  | Internal Server Error       | خطأ غير متوقع في الخادم.                             |

**مخطط استجابة الخطأ (مثال):**

```json
{
  "Code": 400,
  "Message": "Invalid listObjectIndex. Index must be between 0 and 5."
}
```

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "RangeName": "A1:C10",
  "Address": "Sheet1!A1:C10",
  "FirstRow": 0,
  "FirstColumn": 0,
  "RowCount": 10,
  "ColumnCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK التعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectConvertToRange.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectConvertToRange.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectConvertToRange.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectConvertToRange.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectConvertToRange.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectConvertToRange.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectConvertToRange.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectConvertToRange.go" >}}

{{< /tab >}}

{{< /tabs >}}