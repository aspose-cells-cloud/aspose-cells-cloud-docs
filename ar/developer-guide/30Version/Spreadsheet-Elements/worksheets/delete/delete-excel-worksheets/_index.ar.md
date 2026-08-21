---
title: "حذف أوراق عمل متعددة في Excel"
second_title: "Document"
linktitle: "أوراق عمل متعددة"
type: docs
url: /worksheets/delete-multiple/
aliases: [/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, حذف أوراق عمل متعددة, Excel API, REST API, v3.0, حذف أوراق عمل"
description: "تعلم كيفية حذف عدة أوراق عمل من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن نقطة نهاية آمنة عبر HTTPS، والمعاملات المطلوبة، ومثالًا مُصححًا لاستخدام cURL، ومقتطفات كود من SDKs للغات برمجة متعددة."
weight: 20
ArticleTitle: "حذف أوراق عمل متعددة في Excel باستخدام واجهة Aspose.Cells Cloud REST API"
---

تقوم هذه الواجهة REST بحذف أوراق عمل متعددة من ملف عمل.

## الأمان والمصادقة
واجهات Aspose.Cells Cloud آمنة وتطالب بالمصادقة باستخدام [رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **معاملات الطلب**

| اسم المعامل      | النوع   | الموقع  | الوصف                                                                     |
| ---------------- | ------- | ------- | -------------------------------------------------------------------------- |
| name             | string  | path    | اسم ملف Excel.                                                            |
| matchCondition   | object  | body    | كائن `MatchConditionRequest` يحدد أوراق العمل التي سيتم حذفها.            |
| folder           | string  | query   | مسار المجلد في التخزين حيث يقع الملف.                                      |
| storageName      | string  | query   | اسم خدمة التخزين.                                                         |

**خصائص MatchConditionRequest**

| الاسم               | النوع     | الوصف                                      | الملاحظات |
| ------------------- | --------- | ------------------------------------------ | --------- |
| RegexPattern        | string    | تعبير نمطي لمطابقة أسماء أوراق العمل.      | اختياري   |
| FullMatchConditions | string[]  | أسماء أوراق العمل الدقيقة المراد حذفها.    | اختياري   |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL. **يلزم وجود رمز JWT صالح في رأس `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

يمكن أن يُعدّ الطلب أيضًا بإجابات أخطاء شائعة، مثل:

| حالة HTTP | المعنى                                      | محتوى الاستجابة النموذجي                                  |
| --------- | -------------------------------------------- | -------------------------------------------------------- |
| 400       | طلب غير صالح – JSON أو معاملات غير صحيحة   | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401       | غير مُصادَق – رمز JWT مفقود أو غير صالح    | `{"Code":401,"Message":"Authentication failed."}`        |
| 403       | ممنوع – صلاحيات غير كافية                   | `{"Code":403,"Message":"Access denied."}`                |
| 404       | غير موجود – الملف أو ورقة العمل غير موجودة | `{"Code":404,"Message":"Resource not found."}`           |
| 500       | خطأ داخلي في الخادم                          | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK إدارة التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:**  
- [حذف ورقة عمل واحدة](https://docs.aspose.cloud/cells/worksheets/delete/)  
- [نسخ ورقة عمل](https://docs.aspose.cloud/cells/worksheets/copy/)  
- [نقل ورقة عمل](https://docs.aspose.cloud/cells/worksheets/move/)  
---