---
title: "حذف الخلفية من ورقة عمل Excel"
second_title: "مستند"
linktitle: "حذف"
type: docs
url: /ar/worksheets/background/delete/
aliases: [  /ar/delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud، حذف خلفية ورقة العمل، Excel، REST API، SDK، C#، Java، PHP، Ruby، Node.js، Python، Perl، Go"
description: "استخدم Aspose.Cells Cloud REST API لحذف صورة الخلفية من ورقة عمل Excel. تتوفر SDKs لـ C#، Java، PHP، Ruby، Node.js، Python، Perl، و Go."
weight: 210
ArticleTitle: "حذف الخلفية من ورقة عمل Excel باستخدام Aspose.Cells Cloud API"
---

يقوم هذا الـ REST API بحذف صورة الخلفية من ورقة عمل.

**المتطلبات المسبقة:** يجب أن يكون الملف المصنف مخزنًا في مساحة تخزين Aspose Cloud، وأن تمتلك رمز وصول JWT صالحًا للمصادقة.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **معلمة الطلب**

| اسم المعلمة | النوع | الموقع | الوصف |
| ------------ | ------ | -------- | ------------------------------------------------------ |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي سيتم حذف خلفيتها. |
| folder | string | query | المجلد في مساحة التخزين حيث يقع الملف. |
| storageName | string | query | اسم مساحة التخزين (إذا لم تكن مساحة التخزين الافتراضية). |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة cURL سطر الأوامر للوصول إلى خدمات Aspose.Cells بسهولة. تتطلب جميع الطلبات رمز JWT صالحًا. احصل على الرمز عبر نقطة نهاية رمز OAuth2 كما هو موصوف في دليل المصادقة.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
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

**كودات حالة HTTP**

| الكود | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error | خطأ داخلي غير متوقع في الخادم. |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل الـ SDK مع التفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}