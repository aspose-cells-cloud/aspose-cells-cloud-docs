---
title: "استرجاع كائن OLE من ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "استرجاع"
type: docs
url: /oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, كائن ole, excel, ورقة عمل, استرجاع كائن ole, rest api"
description: "استرجاع كائن OLE (صورة أو مخطط أو ملف مُضمن) من ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API. تتضمن نقطة نهاية HTTPS والمعلمات المطلوبة وعينة من كود cURL ورموز SDK بلغات برمجة متعددة."
ArticleTitle: "استرجاع كائن OLE من ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 10
---

تقوم هذه الواجهة البرمجية لواجهة الويب (REST API) باسترجاع **كائن OLE** من ورقة عمل Excel.

## الأمان والمصادقة
تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### معلمات الطلب

| اسم المعلمة | النوع   | الموقع | الوصف                                                      |
|-------------|---------|--------|-------------------------------------------------------------|
| name        | نص (string) | المسار | اسم المستند.                                                |
| sheetName   | نص (string) | المسار | اسم ورقة العمل.                                             |
| objectNumber| عدد صحيح (integer) | المسار | رقم الكائن داخل ورقة العمل.                               |
| format      | نص (string) | استعلام | تنسيق التصدير المرغوب للكائن (مثل: `png`, `jpeg`). |
| folder      | نص (string) | استعلام | المجلد الذي يحتوي على المستند.                            |
| storageName | نص (string) | استعلام | اسم وحدة التخزين المراد استخدامها.                         |

### خيارات وحدة التخزين

- **folder** – يُحدد المجلد الفرعي داخل وحدة التخزين الافتراضية حيث يكمن ملف العمل.
- **storageName** – يُتجاوز اسم وحدة التخزين الافتراضية إذا كان ملف العمل محفوظًا في مكان آخر.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) واجهة برمجة قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمة الويب Aspose.Cells. يوضح المثال التالي كيفية طلب كائن OLE كصورة PNG.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### استجابة الصورة الثنائية

عند تعيين `format` إلى نوع صورة (مثل `png`)، تُعيد الواجهة بيانات الصورة الثنائية مع الرأس:

```
Content-Type: image/png
```

_(يُرسل ملف الصورة مباشرة إلى العميل.)_

### استجابة البيانات الوصفية بصيغة JSON

إذا حُذفت المعلمة `format` أو وُضعت على `json`، تُعيد الواجهة حمولة JSON تصف كائن OLE:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## استجابات الأخطاء

| حالة HTTP | رمز الخطأ     | الوصف                                              |
|-----------|----------------|-----------------------------------------------------|
| 400       | BadRequest     | معلمات مفقودة أو غير صالحة.                         |
| 401       | Unauthorized   | رمز JWT غير صالح أو مفقود.                          |
| 404       | NotFound       | لم يتم العثور على ملف العمل أو ورقة العمل أو كائن OLE. |
| 500       | ServerError    | خطأ غير متوقع في الخادم.                            |

**مثال على استجابة الخطأ 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "لم يتم العثور على كائن OLE المطلوب برقم 0 في ورقة العمل 'Sheet1'."
}
```

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لدمج الواجهة البرمجية. تُدار التفاصيل من المستوى المنخفض بواسطة SDKs، ما يتيح لك التركيز على منطق عملك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}