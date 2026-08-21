---
title: "حذف كائن OLE في ورقة عمل Excel"
second_title: "المستند"
linktitle: "حذف"
type: docs
url: /ar/oleobjects/delete/
aliases: [  /ar/delete-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "Aspose.Cells, Cloud, حذف, OLE, كائن, Excel, ورقة عمل, REST, API, SDK"
description: "تعرّف على كيفية حذف كائن OLE من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 4.0). يتضمن عنوان HTTPS، وخطوات المصادقة، ومثال باستخدام أداة cURL، وأكواد مقتطفات SDK، وإرشادات معالجة الأخطاء، وروابط خطوات ما بعد ذلك."
weight: 50
ArticleTitle: "حذف كائن OLE من ورقة عمل Excel باستخدام Aspose.Cells Cloud API"
---

تشرح هذه الصفحة كيفية حذف كائن OLE محدّد من ورقة عمل في ملف Excel باستخدام **Aspose.Cells Cloud**. يمكن أن يكون كائن OLE صورة مُرتبطة، أو مخططًا، أو أي كائن مُضمن آخر تخزنه Excel ككيان منفصل.

## الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### معاملات الطلب

| اسم المعامل | النوع    | الموقع | الوصف                                                |
|------------|---------|--------|-------------------------------------------------------|
| name       | string  | path   | اسم ملف العمل (workbook).                            |
| sheetName  | string  | path   | اسم ورقة العمل.                                      |
| oleObjectIndex | integer | path | فهرس كائن OLE المراد حذفه.                           |
| folder     | string  | query  | المجلد الذي يحتوي على ملف العمل. (اختياري)         |
| storageName| string  | query  | اسم خدمة التخزين. (اختياري)                         |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء الطلب باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### تفاصيل الاستجابة

| الحالة HTTP          | الوصف                                                                 | مثال JSON                                                          |
|----------------------|-----------------------------------------------------------------------|--------------------------------------------------------------------|
| **200 OK**           | تم حذف كائن OLE بنجاح.                                                | `{ "Code": 200, "Status": "OK" }`                                  |
| **401 Unauthorized** | رمز JWT مفقود أو غير صالح.                                           | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | ملف العمل أو ورقة العمل أو فهرس كائن OLE المحدّد غير موجود.         | `{ "Code": 404, "Message": "OLE object index out of range." }`     |
| **400 Bad Request**  | معاملات مطلوبة مفقودة أو بصيغة غير صحيحة.                           | `{ "Code": 400, "Message": "Invalid request parameters." }`       |

تعامل مع هذه الاستجابات في تطبيقك من خلال التحقق من رمز الحالة (status code) وعرض الرسالة المرافقة.

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تُعنى SDK بمعالجة التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}