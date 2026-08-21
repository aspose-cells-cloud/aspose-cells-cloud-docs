---
title: "Aspose.Cells Cloud – دمج وتقسيم واستيراد بيانات جداول البيانات"
second_title: "وثيقة"
ArticleTitle: "معالجة بيانات جداول البيانات – الدمج والتقسيم والاستيراد"
linktype: "معالجة البيانات"
type: docs
url: /data-processing/
keywords: "Aspose.Cells Cloud، معالجة بيانات جداول البيانات، دمج Excel، تقسيم Excel، استيراد CSV، استيراد JSON، واجهة برمجة تطبيقات"
description: "دليل تفصيلي لاستيراد بيانات CSV/JSON، ودمج كتب عمل Excel عن بُعد، وتقسيم جداول البيانات الكبيرة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST، بما في ذلك أمثلة على الطلبات والاستجابات."
weight: 30
---

**Aspose.Cells Cloud** – خدمة قائمة على REST تتيح التعامل البرمجي مع ملفات Excel في السحابة. وهي تدعم استيراد البيانات من تنسيقات متعددة، ودمج كتب العمل، وتقسيم جداول البيانات الكبيرة.

يتيح لك قسم **معالجة البيانات** في واجهة برمجة تطبيقات Aspose.Cells Cloud استيراد بيانات جداول البيانات ودمجها وتقسيمها برمجيًا. استخدم النقاط النهائية (Endpoints) التالية للتعامل مع استيرادات CSV/JSON، ودمج كتب العمل، أو تقسيم الملفات الكبيرة إلى قطع أصغر سهلاً.

## استيراد البيانات وإدارتها

- **[استيراد بيانات CSV وJSON وXML إلى ملفات Excel](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

تتلقى عملية الاستيراد محتوى بصيغة CSV أو JSON أو XML، ثم تُنشئ ورقة عمل جديدة (أو تحدّث ورقة موجودة مسبقًا) داخل كتاب العمل المستهدف.

**تفاصيل نقطة النهاية (Endpoint)**

| طريقة HTTP | نقطة النهاية | جسم الطلب | استجابة ناجحة |
|-------------|----------|--------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` أو `text/csv` (حسب التنسيق) | `200 OK` مع ملف JSON يحتوي على بيانات تعريف كتاب العمل المُحدَّث |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *لا شيء* | يُعيد ملف كتاب العمل الذي تمت معالجته |

**طلب cURL نموذجي (استيراد CSV)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**استجابة JSON نموذجية**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MyWorkbook.xlsx",
    "Worksheets": 3
  }
}
```

> **المتطلبات المسبقة**: يلزم وجود رمز وصول OAuth2. يجب أن يكون الملف المصدر موجودًا في مساحة تخزين Aspose Cloud أو يُزوَّد عبر تحميل متعدد الأجزاء (multipart upload).

## عملية دمج الملفات

- **[دمج ملفات Excel عن بُعد داخل كتاب عمل محدد](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[دمج ملفات Excel متعددة داخل كتاب عمل واحد](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[دمج ملفات Excel المطابقة داخل مجلد عن بُعد](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

تقوم عملية الدمج بدمج كتابي عمل أو أكثر في كتاب عمل واحد مستهدف. وتُدعم في واجهة برمجة التطبيقات قوائم الملفات الصريحة، بالإضافة إلى عمليات الدمج المبنية على الأنماط داخل مجلد التخزين.

**تفاصيل نقطة النهاية (Endpoint)**

| طريقة HTTP | نقطة النهاية | المُعطيات (Parameters) | استجابة ناجحة |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (مصفوفة لأسماء الملفات)، `target` (اسم كتاب العمل المستهدف اختياريًا) | `200 OK` مع ملف JSON يصف كتاب العمل المدمج |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`، `pattern`، `target` | `200 OK` مع بيانات تعريف كتاب العمل المدمج |

**طلب cURL نموذجي (دمج قائمة صريحة)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**استجابة JSON نموذجية**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **المتطلبات المسبقة**: يجب أن تكون جميع كتب العمل المصدر مخزنة في نفس موقع مساحة التخزين السحابية، وأن يمتلك المستخدم المُنفِّذ صلاحيات قراءة/كتابة.

## عملية تقسيم الملفات

- **[تقسيم ملف Excel إلى ملفات متعددة بناءً على أوراق العمل](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[تقسيم ملف Excel وفق قواعد مخصصة](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

تستخرج عملية التقسيم أوراق عمل فردية أو مجموعات من الصفوف/الأعمدة إلى ملفات كتب عمل منفصلة.

**تفاصيل نقطة النهاية (Endpoint)**

| طريقة HTTP | نقطة النهاية | المُعطيات (Parameters) | استجابة ناجحة |
|-------------|----------|------------|------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (مثلًا: `worksheet`)، `outputFolder` | `200 OK` مع قائمة روابط الملفات المُولَّدة |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON للقاعدة المخصصة (حجم الصفحة، نطاق الصفوف، إلخ) | `200 OK` مع تفاصيل الملفات المُقسَّمة |

**طلب cURL نموذجي (تقسيم حسب ورقة العمل)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/BigReport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**استجابة JSON نموذجية**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "BigReport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "BigReport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **المتطلبات المسبقة**: يجب أن يكون كتاب العمل المصدر متاحًا في مساحة تخزين Aspose Cloud، وأن يمتلك المستخدم المُنفِّذ صلاحية الكتابة في المجلد الوجهة.