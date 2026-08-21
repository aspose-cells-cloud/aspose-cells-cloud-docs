---
title: "إخفاء عنصر حقل محوري في جدول محوري"
second_title: "Document"
linktitle: إخفاء
type: docs
url: /ar/pivot-tables/hide-pivot-field-item/
aliases: [  /ar/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, إخفاء عنصر حقل محوري, واجهة برمجة تطبيقات الجداول المحورية, واجهة برمجة تطبيقات REST, حزمة تطوير البرمجيات السحابية"
description: "تعرّف على كيفية إخفاء عنصر حقل محوري في جدول محوري باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمّن تفاصيل الطلب، مثالًا باستخدام cURL، وأجزاء كود حزمة تطوير البرمجيات (SDK) بلغات برمجة متعددة."
weight: 110
ArticleTitle: "إخفاء عنصر حقل محوري في جدول محوري – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

قبل استدعاء الواجهة، تأكّد من توافر ما يلي:

* رمز وصول **JWT** صالح (يمكن الحصول عليه عبر عملية مصادقة Aspose Cloud).  
* ملف المصنف المستهدف مُحمّل بالفعل في مساحة التخزين الخاصة بك في Aspose Cloud.  
* وجود ورقة العمل والجدول المحوري مُنشئَين مسبقًا.

تُساعدك هذه الشروط المسبقة في تجنّب أخطاء المصادقة واستجابات "المورد غير موجود". وتوضّح الخطوات التالية الإعدادات المطلوبة قبل استدعاء الواجهة.

تُستخدم هذه الواجهة البرمجية لإخفاء عنصر حقل محوري في جدول محوري.

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **الأمان والمصادقة**

تتطلّب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة قائمَة على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>، وهي آمنة.

### **مُعاملات الطلب**

| اسم المُعامل      | النوع     | الموقع   | الوصف                                                                                           |
| ----------------- | --------- | -------- | ----------------------------------------------------------------------------------------------- |
| name              | string    | path     | اسم ملف Excel.                                                                                 |
| sheetName         | string    | path     | ورقة العمل التي تحتوي على الجدول المحوري.                                                       |
| pivotTableIndex   | integer   | path     | مؤشر الجدول المحوري داخل ورقة العمل.                                                          |
| pivotFieldType    | string    | query    | نوع الحقل المحوري (Row، Column، Page، Data، إلخ).                                             |
| fieldIndex        | integer   | query    | المؤشر المُعدّ من الصفر للحقل المحوري المُراد تعديله.                                         |
| itemIndex         | integer   | query    | مؤشر العنصر المُحدّد داخل الحقل المُراد إخفاؤه.                                               |
| isHide            | boolean   | query    | ضعها على **true** لإخفاء العنصر، و**false** لإظهاره.                                          |
| needReCalculate   | boolean   | query    | يُشير إلى ما إذا كان يجب إعادة حساب الجدول المحوري بعد التعديل. القيمة الافتراضية هي **false**. |
| folder            | string    | query    | مسار المجلد حيث يُخزّن ملف المصنف.                                                             |
| storageName       | string    | query    | اسم خدمة التخزين.                                                                              |

**مرجع سريع للمُعاملات المطلوبة في الاستعلام**

- **pivotFieldType** – نوع الحقل (مثل `Row`).  
- **fieldIndex** – المؤشر المُعدّ من الصفر للحقل المُراد تعديله.  
- **itemIndex** – المؤشر المُعدّ من الصفر للعنصر المُراد إخفاؤه/إظهاره.  
- **isHide** – `true` لإخفاء، `false` لإظهار.  
- **needReCalculate** – اختياري، وقيمته الافتراضية `false`.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) واجهة برمجة تطبيقات قابلة للوصول من قِبل المطورين، ويتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells Web. ويوضّح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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

**تفاصيل الاستجابة**

| كود الحالة | الوصف                                                            |
| ---------- | ---------------------------------------------------------------- |
| 200        | تمت عملية الإخفاء بنجاح.                                        |
| 400        | طلب غير صالح – مُعطَلات ناقصة أو غير صالحة.                    |
| 401        | غير مُصادَق – رمز JWT غير صالح أو ناقص.                        |
| 500        | خطأ في الخادم – تعذّر إكمال العملية.                            |

**ملاحظة:** إذا كان المؤشر `fieldIndex` أو `itemIndex` خارج النطاق المسموح، تُعيد الواجهة استجابة **400 Bad Request**.

## مجموعة أدوات Cloud SDK

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لتطوير التطبيقات ضد هذه الواجهة. وتتولّى SDKs معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق عملك. يمكنك الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات لـ Aspose.Cells Cloud.

يُظهر الأمثلة التالية كيفية إخفاء عنصر حقل محوري باستخدام SDKs مختلفة.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // إعداد المصنف وورقة العمل
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // رفع المصنف
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // إنشاء ورقة العمل التي ستحتوي على الجدول المحوري
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // إنشاء ورقة عمل ثانية تحتوي على بيانات تجريبية
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // استيراد بيانات تجريبية في Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // مقتطعة للاختصار
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // إضافة جدول محوري إلى PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // إخفاء عنصر حقل صف معيّن
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**ملاحظة:** تفترض أمثلة SDK أنك قد قمت مسبقًا بإعداد المصادقة (رمز JWT) وأن ملف المصنف موجود في مجلد التخزين المحدّد. قم بتعديل المُعاملات `folder` و `storageName` وفقًا لاحتياجات بيئة العمل الخاصة بك.