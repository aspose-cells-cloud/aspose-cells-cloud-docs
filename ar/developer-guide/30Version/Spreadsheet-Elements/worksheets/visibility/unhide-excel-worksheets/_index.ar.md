---
title: "إظهار ورقة عمل في إكسل"
second_title: "مستند"
linktype: "إظهار"
type: docs
url: /worksheets/unhide/
aliases: [/unhide-excel-worksheets/]
keywords: "Aspose.Cells، إظهار ورقة عمل، واجهة برمجة تطبيقات إكسل، جدول بيانات سحابي، REST، رؤية ورقة العمل، ملف عمل إكسل"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لإظهار ورقة عمل في ملف عمل إكسل. يتضمن تفاصيل الطلب، وأمثلة باستخدام cURL، وأكواد مقتطفات SDK بلغات برمجة متعددة."
weight: 60
---

توفر هذه الواجهة البرمجية لواجهة REST نقطة نهاية **إظهار ورقة عمل** في ملف عمل إكسل.

**المتطلبات الأساسية**  
قبل استدعاء هذه العملية، يجب أن تتوفر لديك ما يلي:

* رمز وصول Aspose Cloud صالح (JWT) مُدرج في رأس `Authorization`.  
* ملف العمل مخزن في موقع تخزين مدعوم تحدده باستخدام معلمتَي الاستعلام `folder` و`storageName`.  
* يجب أن يكون ملف العمل بصيغة مدعومة من قِبل Aspose.Cells (مثل `.xls`، `.xlsx`، `.xlsm`).  

## واجهة برمجة تطبيقات REST

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **مُعلمات الطلب**

| اسم المعلمة | النوع   | الموقع | الوصف                                    |
|-------------|---------|--------|--------------------------------------------|
| name        | string  | path   | اسم المستند.                               |
| sheetName   | string  | path   | اسم ورقة العمل.                            |
| isVisible   | boolean | query  | القيمة الجديدة لرؤية ورقة العمل (`true`). |
| folder      | string  | query  | مجلد المستند.                              |
| storageName | string  | query  | اسم التخزين.                               |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet) واجهة برمجة تطبيقات متاحة عمومًا تتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء الطلب باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=true" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"   # استبدل <jwt token> برمز الوصول الخاص بك
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز الاستجابة المحتملة**

| رمز HTTP | المعنى                                   | نموذج جسم الاستجابة (عند التطابق)                           |
|----------|-------------------------------------------|--------------------------------------------------------------|
| 200      | تم تحديث رؤية ورقة العمل بنجاح           | `{ "Code": 200, "Status": "OK" }`                           |
| 400      | طلب غير صالح – معلمات مفقودة أو غير صحيحة | `{ "Code": 400, "Message": "Invalid request parameters." }` |
| 401      | غير مُصادَق – رمز JWT مفقود أو غير صالح  | `{ "Code": 401, "Message": "Authentication failed." }`      |
| 404      | غير موجود – ملف العمل أو ورقة العمل غير موجود | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| 500      | خطأ داخلي في الخادم                       | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

{{< /tab >}}

{{< /tabs >}}

## مجموعة أدوات SDK السحابية

استخدام SDK هو أسرع طريقة للتطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Perl" tabName8="Android" tabName9="Objective C" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-UnhideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UnhideExcelWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UnhideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UnhideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UnhideWorksheet-unhide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e30ac521e9cdb174baa702a743be16ae" >}}

{{< /tab >}}

{{< /tabs >}}