---
title: "إعادة تسمية ورقة عمل في إكسل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "الوثيقة"
ArticleTitle: "كيفية إعادة تسمية أوراق العمل في إكسل – تغيير أسماء الأوراق"
linktype: "إعادة تسمية ورقة عمل في جدول البيانات"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "إعادة تسمية ورقة عمل، Aspose.Cells Cloud، واجهة برمجة تطبيقات إكسل، جدول بيانات، SDK، واجهة برمجة تطبيقات REST"
description: "إعادة تسمية أوراق عمل إكسل بسهولة عبر واجهة برمجة تطبيقات Aspose.Cells Cloud. اعرف المعلمات المطلوبة، وشاهد أمثلة لـ cURL، واحصل على كود SDK بلغات C#، Java، Python، وغيرها."
weight: 100
---

إعادة تسمية أوراق العمل في ملفات عمل إكسل برمجيًّا باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. غيّر أسماء الأوراق، وحدّث تسميات علامات التبويب ديناميكيًّا، وأتمتة تنظيم جداول البيانات عبر استدعاءات واجهة برمجة تطبيقات REST. مفيد في توحيد الوثائق وأتمتة سير العمل.

## إعادة تسمية اسم ورقة العمل في واجهة برمجة تطبيقات جدول البيانات

### واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**مثال باستخدام cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتستلزم <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة       | النوع   | الموقع   | الوصف                                                                                                                                                                                                     |
| ------------------ | ------ | -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ملف   | FormData | **إلزامي**. ملف ملف عمل إكسل (.xlsx، .xls، إلخ) الذي يحتوي على ورقة العمل المراد إعادة تسميتها.                                                                                                               |
| **sourceName**     | نص    | استعلام    | **إلزامي**. الاسم الحالي لورقة العمل التي ترغب في إعادة تسميتها.                                                                                                                                             |
| **targetName**     | نص    | استعلام    | **إلزامي**. الاسم الجديد المراد تعيينه لورقة العمل. يجب أن يتوافق مع قواعد تسمية إكسل (بدون `:` أو `\` أو `?` أو `*` أو `[` أو `]`) وأن يكون فريدًا داخل ملف العمل.                                                      |
| **outPath**        | نص    | استعلام    | **اختياري**. مسار المجلد الوجهة في التخزين السحابي حيث سيتم حفظ ملف العمل بعد إعادة التسمية. إذا كانت القيمة `null` أو حُذفت، تحفظ الخدمة الملف في نفس المجلد الذي يحتوي على ملف العمل الأصلي (أو مسار افتراضي). |
| **outStorageName** | نص    | استعلام    | **اختياري**. المُعرّف الاسمي لخدمة التخزين السحابي المُعدّة مسبقًا (مثل `ArchiveStorage`). إذا حُذف، يُستخدم التخزين الافتراضي.                                                                   |
| **region**         | نص    | استعلام    | **اختياري**. إعداد_locale (مثل `ko-KR`) الذي قد يؤثر على ترميز الأحرف أو المعايير التسمية الإقليمية.                                                                                          |
| **password**       | نص    | استعلام    | **اختياري**. كلمة المرور اللازمة لفك تشفير ملف عمل محمي بكلمة مرور وتعديله. احذفها إذا لم يكن الملف مشفرًا.                                                                             |

**ملاحظات**: تقتصر أسماء أوراق العمل على 31 حرفًا ولا يمكن أن تحتوي على الأحرف التالية: `:` أو `\` أو `?` أو `*` أو `[` أو `]`.

### الاستجابة

يُعيد الطلب الناجح كائن JSON يحتوي على معلومات الحالة ورابط للملف المُعاد تسميته.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى               | الوصف                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | ناجح                  | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح          | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).      |
| 401  | غير مصرّح به          | رمز JWT غير صالح أو مفقود.                                     |
| 413  | حجم الحمولة كبير جدًا     | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500  | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم.                                          |

## أين يجب استخدام واجهة برمجة تطبيقات إعادة تسمية ورقة العمل في جدول البيانات؟

- **توليد التقارير وتوحيد العلامة التجارية** – عند توليد تقارير العملاء تلقائيًّا، تُعاد تسمية أسماء أوراق العمل العامة (مثل `Sheet1`) بأسماء مخصصة للعميل (مثل `AcmeCorp_Q1_Summary`) لضمان تسليم احترافي.
- **توحيد خطوط أنابيب معالجة البيانات** – في سير عمل ETL، تُعاد تسمية أوراق العمل المصدرة بأسماء غير منتظمة لتتوافق مع أسماء موحدة مثل `Raw_Data` أو `Cleaned_Data` لتلبية متطلبات التحليل اللاحق.
- **توصيل المحتوى بلغات متعددة** – بناءً على تفضيل لغة المستخدم، تُترجم أسماء أوراق العمل (مثل `数据` أو `Data`) قبل تسليم الملف، لتقديم تجربة مخصصة.

## لماذا يجب استخدام واجهة برمجة تطبيقات إعادة تسمية ورقة العمل في جدول البيانات؟

- **سهل الاستخدام للمطورين** – توفر SDKs بعدة لغات مع توثيق شامل، مما يبسّط التكامل مقارنة ببناء حل مخصص.
- **تقليل الجهد اليدوي** – تُ automátِز إعادة تسمية أوراق العمل، مما يقلل من الجهد اليدوي المطلوب.
- **نموذج الدفع حسب الاستخدام** – تحصل فقط على الرسوم مقابل استدعاءات واجهة برمجة التطبيقات، مما يلغي تكاليف الترخيص المسبق.
- **لا صيانة للخوادم** – وبكونها خدمة سحابية، تلغي الحاجة إلى استضافة وصيانة الخوادم أو تطبيق تحديثات البرمجيات.
- **دعم الأتمتة** – تسهّل توحيد الوثائق تلقائيًّا ضمن سير العمل.

## كيفية استخدام واجهة برمجة تطبيقات إعادة تسمية ورقة العمل في جدول البيانات مع SDKs

### مواصفات OpenAPI

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُفصّل واجهة برمجة تطبيقات متاحة عمومًا، مما يسمح بالتفاعل عبر REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفرة بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتسريع التطوير. يُجرّدك SDK من تفاصيل HTTP الكامنة، ويسمح بإعادة تسمية أوراق العمل برمز موجز. راجع مستودع GitHub للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}