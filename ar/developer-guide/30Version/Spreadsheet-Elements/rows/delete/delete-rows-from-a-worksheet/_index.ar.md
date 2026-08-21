---
title: "حذف صفوف متعددة من ورقة عمل Excel"
second_title: "وثيقة"
linktitle: "الصفوف"
type: docs
url: /rows/delete/rows/
keywords: "Aspose.Cells Cloud, حذف الصفوف, حذف صفوف متعددة, ورقة عمل Excel, واجهة REST API, SDK"
description: "تعرّف على كيفية حذف صف واحد أو أكثر من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمّن تفاصيل نقطة النهاية، والمُعاملات، ومثالًا باستخدام cURL، وأمثلة للكود باستخدام SDKs بلغات برمجة متنوعة."
weight: 80
ArticleTitle: "حذف صفوف متعددة من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة البرمجية لـ REST بحذف صفوف متعددة **من** ورقة عمل Excel.

**المتطلبات المسبقة:** لاستدعاء هذه نقطة النهاية، يجب أن يكون لديك رمز وصول JWT صالح تم الحصول عليه من عملية مصادقة Aspose Cloud، وامتلاك صلاحيات تخزين مناسبة للملف المُستند.

## API DeleteWorksheetRows

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا عاليًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل  | النوع    | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                                                 |
|-------------|---------|-----------------------------------|------------------------------------------------------------------------|
| name        | string  | path                              | اسم الملف المُستند (workbook).                                         |
| sheetName   | string  | path                              | اسم ورقة العمل (worksheet).                                           |
| startrow    | integer | query                             | المؤشر الصفر-based للصف الأول المراد حذفه (مثال: `0` = الصف الأول). |
| totalRows   | integer | query                             | عدد الصفوف المراد حذفها.                                              |
| updateReference | boolean | query                         | ما إذا كان سيتم تحديث الإشارات المرجعية بعد الحذف (`true`/`false`). |
| folder      | string  | query                             | مجلد المستند.                                                         |
| storageName | string  | query                             | اسم وحدة التخزين.                                                     |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL. **تتطلب جميع نقاط النهاية استخدام بروتوكول HTTPS؛ وتم إيقاف دعم بروتوكول HTTP.**

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

**رموز الاستجابة المحتملة**

| حالة HTTP | الوصف |
|-----------|--------|
| 200 | تم حذف الصفوف بنجاح. |
| 400 | طلب غير صالح – معاملات غير صحيحة. |
| 401 | غير مُصادق – رمز JWT مفقود أو غير صالح. |
| 404 | غير موجود – الملف أو ورقة العمل غير موجودين. |
| 500 | خطأ داخلي في الخادم – حدثت حالة غير متوقعة. |

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK إدارة التفاصيل من المستوى المنخفض، وتُمكّنك من التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}