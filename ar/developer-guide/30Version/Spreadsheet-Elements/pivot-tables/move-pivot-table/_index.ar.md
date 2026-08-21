---
title: "نقل جدول محوري في ملف Excel"
second_title: "مستند"
linktype: نقل
type: docs
url: /ar/pivot-tables/move/
aliases: [  /ar/move-pivot-table/ ]
keywords: "Aspose.Cells Cloud، نقل جدول محوري، Excel، REST API، SDK، C#، Go، Java، Node.js، Perl، PHP، Python، Ruby، Swift"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لنقل جدول محوري داخل ملف Excel. توفر SDKs لـ Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift."
weight: 120
---

تقوم هذه الواجهة REST بنقل جدول محوري داخل ملف Excel.

**المتطلبات المسبقة:** قبل استدعاء هذه العملية، يجب أن يكون لديك رمز وصول JWT صالح، ويجب أن يكون الملف مخزنًا في مساحة تخزين Aspose Cloud. حدد المعاملات `folder` و`storageName` حسب الحاجة.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Move
```

### **معاملات الطلب**

| اسم المعامل        | النوع    | الموقع   | الوصف                                                     |
| ------------------ | -------- | -------- | --------------------------------------------------------- |
| name               | string   | path     | اسم ملف Excel.                                            |
| sheetName          | string   | path     | اسم ورقة العمل التي تحتوي على الجدول المحوري.              |
| pivotTableIndex    | integer  | path     | الفهرس الصفرِي للجدول المحوري المراد نقله.                |
| fieldIndex         | integer  | query    | فهرس الحقل المحوري المراد نقله.                          |
| from               | string   | query    | المنطقة المصدر للحقل (مثل `Row` أو `Column`).             |
| to                 | string   | query    | المنطقة الوجهة للحقل (مثل `Row` أو `Column`).             |
| folder             | string   | query    | المجلد داخل مساحة التخزين حيث يقع الملف.                  |
| storageName        | string   | query    | اسم خدمة التخزين.                                         |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldMoveTo) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Move?fieldIndex=0&from=C1&to=C10" \
  -X POST \
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

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل من المستوى المنخفض، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// استخدم نقاط نهاية HTTPS في الإنتاج.
public void Run_PivotTable_Move()
{
    url = @"https://api.aspose.com/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = @"https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{\"rowIndex\":0,\"columnIndex\":0,\"type\":\"String\",\"value\":\"Sport\",\"style\":null}, ... ],\"DestinationWorksheet\":\"Sheet2\",\"IsInsert\":false}";
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/Move?row=10&column=10&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    url = "https://api.aspose.com/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Move?fieldIndex=1&from=Row&to=Column&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "60360c7d035abd1b2c9e36c68c9f00fb" >}}

{{< /tab >}}

{{< /tabs >}}