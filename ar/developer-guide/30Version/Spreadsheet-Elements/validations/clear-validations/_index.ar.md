---
title: "حذف جميع قواعد التحقق من البيانات في ورقة العمل – واجهة Aspose.Cells Cloud API"
second_title: "التوثيق"
linktitle: "حذف"
type: docs
url: /ar/validations/clear/
keywords: "Aspose.Cells Cloud, حذف قواعد التحقق من البيانات في ورقة العمل, Excel, REST API, التحقق من صحة جدول البيانات, API"
description: "إزالة جميع قواعد التحقق من البيانات من ورقة عمل في ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن خطوات المصادقة، تفاصيل الطلب، مثال باستخدام cURL، مخطط الاستجابة، معالجة الأخطاء، ومقتطفات SDK."
weight: 10
---

**المتطلبات المسبقة**

- حساب صالح على منصة Aspose Cloud.
- رمز وصول JWT تم الحصول عليه عبر واجهة مصادقة Aspose Cloud (`/connect/token`).
- يجب أن يكون المصنف مخزنًا في مساحة التخزين الخاصة بك على Aspose Cloud (أو يجب توفير معامِلات الاستعلام المناسبة `folder`/`storageName`).

تقوم هذه الواجهة البرمجية REST بحذف جميع قواعد التحقق من البيانات في ورقة عمل Excel.

## واجهة REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **معامِلات الطلب**

| اسم المعامل | النوع   | الموقع | الوصف                                                |
| ----------- | ------ | ------ | ----------------------------------------------------- |
| name        | string | path   | اسم مستند Excel.                                     |
| sheetName   | string | path   | اسم ورقة العمل التي تحتوي على قواعد التحقق.          |
| folder      | string | query  | المجلد الذي يتم تخزين المستند فيه.                  |
| storageName | string | query  | اسم خدمة التخزين.                                    |

يُعرِّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء الواجهة البرمجية باستخدام cURL بعد الحصول على رمز JWT.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
  -X DELETE \
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

### معالجة الأخطاء

| حالة HTTP | المعنى              | الوصف                                               |
| --------- | ------------------- | ---------------------------------------------------- |
| 400       | طلب غير صالح        | الطلب غير مكوّن بشكل صحيح أو تفتقد معامِلات مطلوبة. |
| 401       | غير مصرّح به        | رمز JWT مفقود أو غير صالح أو منتهٍ.                 |
| 404       | غير موجود           | المصنف أو ورقة العمل المحددة غير موجودة.           |
| 500       | خطأ داخلي في الخادم | حدث خطأ غير متوقع من جانب الخادم.                   |

يتّبع حمل الخطأ نفس البنية JSON مع حقلَي `Code` و `Message`، كما في المثال التالي:

```json
{
  "Code": 401,
  "Message": "رمز غير صالح أو منتهٍ."
}
```

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. فSDK يُجرّدك من التفاصيل التقنية منخفضة المستوى، ليُمكّنك من التركيز على منطق الأعمال. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}