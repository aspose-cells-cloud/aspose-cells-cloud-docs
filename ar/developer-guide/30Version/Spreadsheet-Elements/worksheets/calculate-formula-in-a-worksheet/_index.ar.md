---
title: "حساب صيغة في ورقة عمل إكسل"
second_title: "المستند"
linktype: "حساب"
type: docs
url: /worksheets/calculate-formula/
aliases: [/calculate-formula-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, حساب الصيغ, REST API, مكتبات البرمجة (SDKs), C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift"
description: "حساب الصيغ في ورقة عمل إكسل باستخدام REST API الخاص بـ Aspose.Cells Cloud. يدعم مكتبات برمجية متعددة (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go, Swift) مع أمثلة جاهزة للاستخدام."
weight: 20
ArticleTitle: "حساب صيغة في ورقة عمل إكسل – وثائق Aspose.Cells Cloud"
---

تُعيد هذه الواجهة البرمجية للخدمات السحابية (REST API) **القيمة المحسوبة للصيغة** في ورقة العمل. ويمكن استخدامها لـ **تقييم صيغة إكسل مباشرةً** من تطبيقك.

## واجهة REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/formulaResult
```

### **مُعْطَلات الطلب**

| اسم المُعطَل       | النوع   | الموقع   | الوصف                                                    |
| ------------------ | ------- | -------- | -------------------------------------------------------- |
| name               | string  | path     | اسم ملف إكسل.                                            |
| sheetName          | string  | path     | اسم ورقة العمل التي تحتوي على الصيغة.                    |
| formula            | string  | query    | الصيغة المراد تقييمها (مثل `SUM(A5:A10)`).               |
| folder             | string  | query    | المجلد الذي يُخزَّن فيه المستند.                         |
| storageName        | string  | query    | اسم خدمة التخزين (إن وُجدت).                             |

يُعرِّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetCalculateFormula) واجهة برمجة قابلة للوصول العام، ويُمكِّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

### المصادقة

يجب أن تتضمَّن جميع الطلبات رمز **Bearer JWT** صالحًا في رأس `Authorization`:

```
Authorization: Bearer <your_jwt_token>
```

يمكنك الحصول على رمز مميز (token) باتّباع سير عمل OAuth 2.0 الموصوف في دليل مصادقة Aspose.Cells Cloud.

### رموز حالات الاستجابة الممكنة

| الرمز | الوصف                                                           |
|------|------------------------------------------------------------------|
| 200  | نجح الطلب؛ وتُعاد قيمة الصيغة.                                   |
| 400  | طلب غير صحيح – مَعْطَلات مفقودة أو غير صالحة.                   |
| 401  | غير مصرّح به – رمز JWT غير صالح أو مفقود.                       |
| 404  | غير موجود – الملف أو ورقة العمل المحددة غير موجودة.             |
| 500  | خطأ داخلي في الخادم – حالة غير متوقّعة في الخادم.               |

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells Cloud بسهولة. يُظهر المثال التالي كيفية طلب نتيجة الصيغة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet2/formulaResult?formula=SUM(A5:A10)" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Value": {
    "Value": "0"
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة مكتبات البرمجة (SDK) السحابية

استخدام مكتبة برمجية (SDK) هو أسرع طريقة لدمج الواجهة البرمجية. وتتولّى المكتبة تفاصيل المستوى المنخفض تلقائيًا، مما يتيح لك التركيز على منطق تطبيقك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات برمجية متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "d1a2b3c4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a1b2c3d4e5f67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "b1c2d3e4f5g67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "c1d2e3f4g5h67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "d1e2f3g4h5i67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e1f2g3h4i5j67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f1g2h3i4j5k67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "g1h2i3j4k5l67890abcd1234ef567890" "ExampleGetWorksheetCalculateFormula.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

**انظر أيضًا:**  
- [الحصول على ورقة عمل](https://docs.aspose.cloud/cells/worksheets/get-worksheet/)  
- [تحديث ورقة عمل](https://docs.aspose.cloud/cells/worksheets/update-worksheet/)  
- [حساب جميع الصيغ](https://docs.aspose.cloud/cells/worksheets/calculate-all-formulas/)  
---