---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – دمج نطاق خلايا"
second_title: "مستند"
linktitle: "دمج"
type: docs
url: /ar/ranges/merge/
aliases: [  /ar/combines-a-range-of-cells-into-a-single-cell/ ]
keywords: "Aspose.Cells، دمج الخلايا، واجهة برمجة تطبيقات إكسل، REST، حزمة تطوير البرامج السحابية"
description: "دمج نطاق من الخلايا في خلية واحدة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تعلّم تنسيق الطلب، المعلمات، وأمثلة حزم تطوير البرامج (SDK) بلغات C#، Java، Python، وغير ذلك."
weight: 20
---

تقوم هذه الواجهة البرمجية لـ REST بدمج نطاق من الخلايا في خلية واحدة داخل ورقة عمل إكسل.

**نظرة عامة** – يؤدي دمج النطاق إلى دمج الخلايا المحددة في خلية واحدة، مع الاحتفاظ بقيمة الخلية العلوية اليسرى وتُهمل القيم المتبقية. استخدم هذه العملية عندما تحتاج إلى إنشاء رأس يمتد عبر أعمدة أو صفوف متعددة، أو عندما ترغب في تبسيط تخطيط ورقة العمل.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **معلمات الطلب**

| اسم المعلمة    | النوع   | الموقع | الوصف                                               |
| --------------- | ------ | ------ | --------------------------------------------------- |
| **name**        | نص     | المسار | اسم ملف المصنف.                                     |
| **sheetName**   | نص     | المسار | اسم ورقة العمل.                                     |
| **range**       | كائن   | الجسم | كائن النطاق الذي يحدد الخلايا المراد دمجها.         |
| **folder**      | نص     | الاستعلام | المجلد الذي يُخزَّن فيه المصنف.                    |
| **storageName** | نص     | الاستعلام | اسم وحدة التخزين.                                  |

#### مخطط جسم الطلب

يجب أن يحتوي كائن **النطاق** على الحقول التالية (جميع الحقول الأخرى اختيارية):

| الخاصية         | النوع    | الإلزام | الوصف                                                |
| --------------- | -------- | ------ | ---------------------------------------------------- |
| **FirstRow**    | عدد صحيح | نعم     | مؤشر الصف الأول في النطاق (مبني على الصفر).         |
| **FirstColumn** | عدد صحيح | نعم     | مؤشر العمود الأول في النطاق (مبني على الصفر).       |
| **RowCount**    | عدد صحيح | نعم     | عدد الصفوف المُضمنة في النطاق.                      |
| **ColumnCount** | عدد صحيح | نعم     | عدد الأعمدة المُضمنة في النطاق.                     |
| **Name**        | نص      | لا      | اسم اختياري للنطاق.                                 |
| **RefersTo**    | نص      | لا      | صيغة يشير إليها النطاق.                             |
| **Worksheet**   | نص      | لا      | اسم ورقة العمل (إذا اختلف عن معلمة المسار).          |
| **RowHeight**   | رقم     | لا      | ارتفاع الصفوف في النطاق (بالبكسل).                   |
| **ColumnWidth** | رقم     | لا      | عرض الأعمدة في النطاق (بالبكسل).                     |

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### تفاصيل الاستجابة

| حالة HTTP                     | الوصف                                                  | JSON مثال                                              |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | تم دمج النطاق بنجاح.                                    | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | معلمات النطاق غير صالحة (مثل: مؤشرات خارج النطاق).      | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | رمز JWT مفقود أو غير صالح.                             | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | المصنف أو ورقة العمل غير موجودين.                      | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | خطأ في الخادم الداخلي غير متوقع.                      | `{ "Code": 500, "Message": "Internal server error." }` |

## عائلة حزم تطوير البرامج السحابية

استخدام حزمة تطوير البرامج (SDK) هو أفضل طريقة لتسريع عملية التطوير. وتتولى حزم التطوير تفاصيل المستوى المنخفض تلقائيًا، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}