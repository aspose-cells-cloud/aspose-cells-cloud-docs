---
title: "تجميع الصفوف في ورقة عمل Excel"
second_title: "مستند"
linktitle: "تجميع"
type: docs
url: /ar/rows/group/
aliases: [  /ar/group-rows-in-excel-worksheet/ ]
keywords: "تجميع الصفوف، Excel، Aspose.Cells Cloud، REST API، SDK، ورقة عمل، Excel API"
description: "تجميع الصفوف في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. تدعم العديد من SDKs (C#، Java، PHP، Ruby، Node.js، Python، Perl، Go) لسهولة التكامل."
weight: 60
ArticleTitle: "تجميع الصفوف في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بتجميع الصفوف في ورقة عمل Excel.

**المتطلبات المسبقة:**  
- يجب تزويدها برمز وصول OAuth 2.0 صالح (Bearer JWT) في الرأس `Authorization`.  
- يجب أن تكون المصنف موجودًا مسبقًا في المسار `folder` المُحدَّد ضمن `storageName` المختار (أو وحدة التخزين الافتراضية) قبل إرسال الطلب.

## واجهة PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **الأمان والمصادقة**

تعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معطيات الطلب**

| اسم المعطى | النوع | الموقع | الوصف |
| -------------- | ------- | -------- | ------------------------------------------------------------------------ |
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل. |
| firstIndex | integer | query | المؤشر (بدءًا من الصفر) للصف الأول المطلوب تجميعه. |
| lastIndex | integer | query | المؤشر (بدءًا من الصفر) للصف الأخير المطلوب تجميعه. |
| hide | boolean | query | يُشير إلى ما إذا كان يجب إخفاء الصفوف المُجمّعة (`true` أو `false`). |
| folder | string | query | المسار إلى المجلد الذي يحتوي على المصنف. |
| storageName | string | query | اسم وحدة التخزين التي يوجد فيها المصنف. |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) واجهة برمجة تطبيقات متاحة علنًا، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
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

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | ناجح (OK) | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معطيات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حملة البيانات كبيرة جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

استجابات الخطأ الشائعة:

- **400 Bad Request** – تحقق من أن `firstIndex` و `lastIndex` أرقام صحيحة صالحة، وأن `firstIndex` ≤ `lastIndex`.  
- **401 Unauthorized** – تحقق من أن رأس `Authorization` يحتوي على رمز JWT ساري المفعول.  
- **404 Not Found** – تأكد من وجود المصنف (`name`) وورقة العمل (`sheetName`) في المسار `folder` / `storageName` المحددين.

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:** [فك تجميع الصفوف في ورقة عمل Excel](../rows/ungroup/ "فك تجميع الصفوف في ورقة عمل Excel")، [إخفاء الصفوف في ورقة عمل Excel](../rows/hide/ "إخفاء الصفوف في ورقة عمل Excel")، [إظهار الصفوف المُخفية في ورقة عمل Excel](../rows/unhide/ "إظهار الصفوف المُخفية في ورقة عمل Excel").

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، بحيث يمكنك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}