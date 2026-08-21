---
title: "إضافة عمود فارغ إلى ورقة عمل إكسل - واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "إضافة"
type: docs
url: /columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "إضافة، عمود، إكسل، API، Aspose.Cells، سحابة، REST، إدراج"
description: "تعلم كيفية إدراج عمود جديد في ملف إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بناء الجملة الخاص بالطلب، مثال باستخدام cURL، وأمثلة لشيفرات SDK."
weight: 20
ArticleTitle: "إضافة عمود فارغ إلى ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بإدراج عمود واحد أو أكثر داخل ورقة عمل.

**المتطلبات الأساسية**  
قبل استدعاء هذه النقطة النهائية، تأكد من إتمام الخطوات التالية:

- احصل على رمز وصول OAuth 2.0 صالح وشَمْلَه في الرأس `Authorization`.  
- اخزن ملف العمل المستهدف في التخزين المحدّد (الافتراضي = "Default") أو حدّد معامَلات `folder` و`storageName` المناسبة.  
- تحقق من أن اسم ورقة العمل المُعطى في `sheetName` موجود في ملف العمل.

## واجهة PutInsertWorksheetColumns

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة باستخدام رمز JWT</a>.

### معامَلات الطلب

| اسم المعامل         | النوع   | الموقع | الوصف                                                                |
| ------------------- | ------- | ------ | -------------------------------------------------------------------- |
| **name**            | نصّ    | المسار | اسم ملف ملف العمل.                                                  |
| **sheetName**       | نصّ    | المسار | اسم ورقة العمل.                                                     |
| **columnIndex**     | عدد صحيح | المسار | المؤشّر بصفر (0) للعمود الذي يبدأ منه الإدراج.                     |
| **totalColumns**    | عدد صحيح | الاستعلام | عدد الأعمدة المراد إدراجها.                                         |
| **updateReference** | منطقي  | الاستعلام | عند القيمة **true**، تُحدّث المرجعيات الخلوية لتعكس الإدراج.      |
| **folder**          | نصّ    | الاستعلام | مسار المجلّد الذي يحتوي على ملف العمل.                             |
| **storageName**     | نصّ    | الاستعلام | اسم خدمة التخزين.                                                   |

**ملاحظات**

- يجب أن يكون `columnIndex` بين 0 وعدد الأعمدة الحالي في ورقة العمل. وعند الإدراج خارج النطاق الحالي، يتوسّع الملف تلقائيًا.  
- يؤدي إدراج أعمدة متعددة (`totalColumns` > 1) إلى تحريك الأعمدة الموجودة نحو اليمين.  
- يفترض الإعداد الافتراضي لعلامَة `updateReference` القيمة `false`؛ لذا، اضبطها على `true` لتحديث الصيغ والمجالات المسماة.

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells. يُظهر المثال التالي طلبًا كاملاً يتضمّن المصادقة ومعاملات المسار الصحيحة.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**كود الاستجابة**

| الكود | الوصف                                       |
|------|---------------------------------------------|
| 200  | تمّ إدراج العمود/الأعمدة بنجاح.             |
| 400  | طلب خاطئ – معامَلات مفقودة أو غير صالحة.   |
| 401  | غير مصرّح به – رمز وصول غير صالح أو مفقود.  |
| 404  | ملف العمل أو ورقة العمل غير موجود.          |
| 500  | خطأ داخلي في الخادم.                        |

**أمثلة على استجابات الأخطاء**

```json
// 400 Bad Request – معامَلات مفقودة أو غير صالحة
{
  "Code": 400,
  "Message": "معامل غير صالح: يجب أن يكون totalColumns عددًا صحيحًا موجبًا."
}

// 401 Unauthorized – رمز وصول غير صالح أو مفقود
{
  "Code": 401,
  "Message": "فشلت المصادقة. رمز الوصول مفقود أو غير صالح."
}

// 404 Not Found – ملف العمل أو ورقة العمل غير موجود
{
  "Code": 404,
  "Message": "لم يتم العثور على ملف العمل 'test.xlsx'."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "حدث خطأ غير متوقع في الخادم."
}
```

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير البرمجيات. فتتولّى SDK تفاصيل المستوى المنخفض، ما يتيح لك التركيز على منطق مشروعك. راجع <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الشيفرة التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}