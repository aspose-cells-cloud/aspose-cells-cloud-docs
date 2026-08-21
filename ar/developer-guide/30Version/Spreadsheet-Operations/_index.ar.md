---
title: "عمليات جداول البيانات"
second title: "المستند"
type: docs
url: /spreadsheet-operations/
keywords: "Aspose Cells Cloud، واجهة برمجة تطبيقات Excel، عمليات جداول البيانات، الضبط التلقائي، المعالجة الدفعية، حماية الملفات، التحويل، الاستيراد والتصدير، معالجة النصوص"
description: "تعرّف على كيفية تنفيذ عمليات جداول البيانات مثل الضبط التلقائي، والتحويل الدفعي، والحماية، والدمج، واستبدال النصوص باستخدام واجهة Aspose.Cells Cloud REST API. يشمل دليلاً موجزًا للاستخدام وإرشادات أمثلة برمجية."
weight: 100
ArticleTitle: "عمليات جداول البيانات – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقدم **عمليات جداول البيانات** دليلاً موجزًا لأكثر الإجراءات شيوعًا التي يمكنك تنفيذها على أوراق عمل Excel باستخدام **Aspose.Cells Cloud** (الإصدار 3.0). سواء كنت بحاجة إلى ضبط عرض الأعمدة تلقائيًا، أو معالجة الملفات دفعيًا، أو حماية الأوراق، أو معالجة النصوص، فإن واجهة برمجة تطبيقات REST توفر نقاط نهاية مخصصة تعمل عبر لغات برمجة متعددة مثل Python و C# و Java. يحتوي القائمة أدناه على روابط مباشرة إلى التوثيق التفصيلي لكل عملية، مع ملاحظات استخدام موجزة لمساعدتك في البدء بسرعة.

**المتطلبات المسبقة**: لاستدعاء نقاط النهاية هذه، يجب أن تمتلك مفتاح API صالح لـ Aspose.Cells Cloud، وتضمين رأس `Authorization` (بالصيغة `Bearer <access-token>`). وتفترض الأمثلة استخدام إصدار API v3.0.

- **[خيارات الضبط التلقائي](/cells/auto-fitter-options/)** – ضبط عرض الأعمدة وارتفاع الصفوف تلقائيًا. `POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[المعالجة الدفعية لملفات Excel: التحويل، القفل، الحماية، التجزئة، وفك القفل](/cells/batch/)** – تنفيذ إجراءات جماعية (التحويل، القفل، الحماية، التجزئة، فك القفل) على ما يصل إلى 100 ملف في كل طلب. `POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[ضغط وإصلاح ملفات Excel](/cells/compress-and-repair-excel-files/)** – تقليل حجم الملف وإصلاح المشكلات الهيكلية. `POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[تحويل ملف Excel إلى تنسيق آخر أو حفظه بصيغة مختلفة](/cells/conversion-and-save-as/)** – تحويل ملف Excel إلى PDF أو CSV أو HTML، أو تغيير تنسيق الإخراج. `GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[خيارات تحويل أوراق العمل](/cells/convert-workbook-options/)** – ضبط إعدادات التحويل بدقة، مثل حجم الصفحة، خيارات العرض، وحماية كلمة المرور. `POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[إنشاء ملفات Excel أو بناء تقارير Excel](/cells/creating-files-and-reports/)** – إنشاء أوراق عمل جديدة من الصفر أو من قوالب جاهزة. `PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[استيراد البيانات إلى ملفات Excel وتصدير البيانات منها](/cells/data-import-and-export/)** – تحميل البيانات من ملفات CSV أو JSON أو قواعد البيانات، وتصدير بيانات الأوراق. `POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[تشفير وفك تشفير وتوقيع ملفات Excel رقميًا](/cells/protect/)** – تطبيق حماية بكلمة مرور، تشفير، أو توقيع رقمي. `POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[معلومات الملف](/cells/file-info/)** – استرجاع البيانات الوصفية مثل الحجم، التنسيق، وتاريخ الإنشاء. `GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[دمج وتقسيم ملفات Excel](/cells/merge-and-split/)** – دمج أوراق عمل متعددة في ملف واحد أو تقسيم ورقة عمل إلى ملفات منفصلة. `POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[البحث واستبدال محتوى النصوص داخل ملفات Excel](/cells/search-and-replace/)** – البحث واستبدال السلاسل النصية عبر الأوراق. `POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[معالجة النصوص في Excel: إضافة نصوص، إزالة أحرف، تقليص النصوص، تحديث حالة الكلمات، والمزيد](/cells/text-processing/)** – تنفيذ عمليات متقدمة على قيم الخلايا. `POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[إضافة علامات مائية أو تعيين خلفيات في ملفات Excel](/cells/watermark-and-background/)** – إضافة علامات مائية نصية أو صورية، وتعيين خلفيات للأوراق. `POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[العمل مع ملفات Excel: حساب الصيغ، الضبط التلقائي، مسح الكائنات، والمزيد](/cells/workbook/)** – تنفيذ مهام شائعة مثل حساب الصيغ، مسح الكائنات، والضبط التلقائي. `POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```