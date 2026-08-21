---
title: "نقل نطاق مسمّى باستخدام ورقة عمل Excel"
second_title: "وثيقة"
linktitle: "نقل"
type: docs
url: /ranges/move/
aliases: [/move-a-named-range-with-an-excel-worksheet/]
keywords: "Aspose.Cells Cloud, نقل نطاق مسمّى, ورقة عمل Excel, REST API, نقل النطاق, أمثلة SDK"
description: "تعرّف على كيفية نقل نطاق مسمّى ضمن ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API الإصدار 3.0، مع تفاصيل نقطة النهاية، المصادقة، أمثلة وأكواد SDK."
weight: 20
ArticleTitle: "نقل نطاق مسمّى باستخدام ورقة عمل Excel عبر واجهة Aspose.Cells Cloud API"
---

يُعد نقل النطاق المسمّى مهمة شائعة عندما تحتاج إلى إعادة تنظيم البيانات برمجيًا. يشرح هذا القسم كيفية نقل نطاق مُعرّف إلى موقع جديد على نفس ورقة العمل باستخدام واجهة Aspose.Cells Cloud REST API.

تقوم هذه الواجهة البرمجية بنقل النطاق المحدّد إلى نطاق وجهة في ورقة عمل Excel.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### المصادقة
تتطلب الواجهة رمز <strong>Bearer JWT</strong> يُحصل عليه عبر تدفق OAuth الخاص بـ Aspose Cloud. يجب تضمين الرمز في رأس `Authorization`:

```
Authorization: Bearer <jwt token>
```

ويجب أن يحتوي الرمز على النطاق **Cells**.

### المتطلبات الأساسية
- يجب أن يكون المصنف مخزنًا في مساحة التخزين الخاصة بـ Aspose Cloud.  
- قدم اسم التخزين (`storageName`) ومسار المجلد (`folder`) إن لم يكن الملف في الدليل الجذر.  
- استخدم أحدث إصدار من SDK الخاص بـ Aspose.Cells Cloud الذي يدعم إصدار الواجهة **v3.0**.

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| الاسم           | النوع   | الموقع | الوصف |
|----------------|--------|----------|-------------|
| **name**       | سلسلة نصية | المسار     | اسم ملف المصنف |
| **sheetName**  | سلسلة نصية | المسار     | اسم ورقة العمل |
| **destRow**    | عدد صحيح| الاستعلام    | مؤشر الصف الابتدائي لنطاق الوجهة (يبدأ من 0) |
| **destColumn**| عدد صحيح| الاستعلام    | مؤشر العمود الابتدائي لنطاق الوجهة (يبدأ من 0) |
| **range**      | كائن | الجسم     | تعريف النطاق المصدر المراد نقله |
| **folder**     | سلسلة نصية | الاستعلام    | مسار المجلد حيث يُخزّن المصنف |
| **storageName**| سلسلة نصية | الاستعلام    | اسم مساحة تخزين Aspose Cloud |

### جسم الطلب

| الحقل          | النوع   | الإلزام | الوصف |
|----------------|--------|----------|-------------|
| **ColumnCount**| عدد صحيح| لا | عدد الأعمدة في النطاق المصدر |
| **ColumnWidth**| عدد صحيح| لا | عرض كل عمود (بالنقاط) |
| **FirstColumn**| عدد صحيح| لا | المؤشر المُعدَّ من الصفر لأول عمود في النطاق المصدر |
| **FirstRow**   | عدد صحيح| لا | المؤشر المُعدَّ من الصفر لأول صف في النطاق المصدر |
| **Name**       | سلسلة نصية | لا | اسم النطاق (إن كان نطاقًا مسمّى) |
| **RefersTo**   | سلسلة نصية | لا | مرجع بنمط A1 يُعرّف النطاق |
| **RowCount**   | عدد صحيح| لا | عدد الصفوف في النطاق المصدر |
| **RowHeight**  | عدد صحيح| لا | ارتفاع كل صف (بالنقاط) |
| **Worksheet**  | سلسلة نصية | لا | ورقة العمل التي تحتوي على النطاق المصدر |

### سير العمل

1. **ارفع** المصنف إلى مساحة تخزين Aspose Cloud (إن لم يكن موجودًا مسبقًا).  
2. **ولّد** رمز JWT باستخدام نقطة نهاية OAuth.  
3. **ابنِ** حمولة JSON التي تصف النطاق المصدر.  
4. **استدعِ** نقطة النهاية `moveto` باستخدام المعاملات المطلوبة (المسار، معاملات الاستعلام وجسم JSON).  
5. **تحقق** من الاستجابة؛ فاستدعاء ناجح يُعيد حالة `200 OK`.

### مثال على طلب/استجابة

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
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

عند حدوث خطأ، تتضمن الاستجابة حقلًا اختياريًا `ErrorMessage` يوفّر تفاصيل إضافية حول السبب.

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح به (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | يتجاوز حجم الملف المرفوع الحد المسموح. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

**مخطّط الاستجابة**

| الحقل | النوع   | الوصف |
|-------|--------|-------------|
| **Code** | عدد صحيح | رمز حالة مشابه لـ HTTP تعيده الواجهة (مثل 200) |
| **Status** | سلسلة نصية | وصف نصي للنتيجة (مثل "OK") |
| **ErrorMessage** | سلسلة نصية (اختياري) | تفاصيل الخطأ المقروءة من قِبل الإنسان عند فشل الاستدعاء |

## عائلة SDK للسحابة

يُعد استخدام SDK الطريقة الأفضل لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى لتمكينك من التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}