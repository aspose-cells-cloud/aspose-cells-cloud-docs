---
title: "تحويل ملف إكسل إلى تنسيق آخر أو حفظه بصيغة مختلفة."
second_title: "وثيقة"
linktype: "التحويل وحفظ باسم"
type: docs
url: /ar/conversion-and-save-as/
aliases: [  /ar/convert-excel/ , /ar/convert/ ]
keywords: "Aspose.Cells, واجهة برمجة تطبيقات تحويل إكسل, تحويل إكسل إلى PDF, إكسل إلى CSV, إكسل إلى JSON, تحويل جداول البيانات في السحابة"
description: "تعلم كيفية تحويل كتب عمل إكسل إلى تنسيقات PDF وCSV وJSON وHTML وأكثر من 15 تنسيق آخر باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تفاصيل النقاط النهائية (Endpoints)، وأوامر cURL النموذجية، وأكواد مقتطفات SDK لـ Java و.NET وPython وما إلى ذلك."
weight: 30
ArticleTitle: "تحويل ملفات إكسل إلى PDF وCSV وJSON والمزيد باستخدام Aspose.Cells Cloud"
---

إذا أنشأت ملف إكسل في البداية بصيغة معينة—مثل [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، أو [CSV](https://docs.fileformat.com/spreadsheet/csv/)— فقد تجد من المفيد تحويل ملف الإكسل إلى صيغة أخرى للاستفادة من ميزات محددة. على سبيل المثال، يُستخدم تحويل ملف إكسل إلى [PDF](https://docs.fileformat.com/pdf/) لحماية محتوياته من التعديلات غير المصرح بها، ولتسهيل قراءته ومشاركته.

**المتطلبات الأساسية**  
قبل استدعاء واجهات برمجة تطبيقات التحويل، احصل على رمز وصول OAuth 2.0 من Aspose Cloud، وتأكد من أن كتاب العمل مخزن في مساحة التخزين الخاصة بحسابك في Aspose Cloud (أو متضمن في جسم الطلب لنقطة النهاية PUT للتحويل).

عملية تحويل المستندات عملية معقدة. وتُسهم عوامل عديدة في تعقيد عملية التحويل، ويجب أخذها في الاعتبار أثناء التحويل. وتُعدّ عملية التحويل الدقيق عالي الجودة بين تنسيقات إكسل ميزة رئيسية في Aspose.Cells Cloud.

يعمل الخدمة بسلاسة لأي نوع من تنسيقات المستندات. يمكنك استيراد وتصدير المستندات بالتنسيقات التالية:

**التنسيقات المدعومة**  
- دعم الاستيراد والتصدير: [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، [CSV](https://docs.fileformat.com/spreadsheet/csv/)، [TSV](https://docs.fileformat.com/spreadsheet/tsv/)، [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)، [ODS](https://docs.fileformat.com/spreadsheet/ods/)، [TXT](https://docs.fileformat.com/word-processing/txt/)
- التصدير فقط: [PDF](https://docs.fileformat.com/pdf/)، [OTS](https://docs.fileformat.com/spreadsheet/ots/)، [XPS](https://docs.fileformat.com/page-description-language/xps/)، [DIF](https://docs.fileformat.com/spreadsheet/dif/)، [PNG](https://docs.fileformat.com/Image/png/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [BMP](https://docs.fileformat.com/image/bmp/)، [SVG](https://docs.fileformat.com/page-description-language/svg/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)، [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### واجهات برمجة تطبيقات التحويل

| API                         | الوصف                                                                                   |
| :-------------------------- | :-------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | يُعيد استرجاع كتاب عمل إكسل من التخزين السحابي ويُحوّله إلى التنسيق المطلوب.           |
| `PUT /cells/convert`        | يُحوّل كتاب عمل إكسل مُزوَّد في جسم الطلب إلى التنسيق الناتج المحدّد.                   |
| `POST /cells/{name}/saveAs` | يحفظ كتاب عمل إكسل موجود بصيغة أخرى مباشرةً في التخزين السحابي.                          |

**تفاصيل واجهة البرمجة**

- **GET /cells/{name}**  
  - **مُدخلات المسار (Path parameters):** `name` – اسم ملف كتاب العمل (إلزامي).  
  - **مُدخلات الاستعلام (Query parameters):** `format` – التنسيق المستهدف (مثل: pdf، csv، json)؛ `storage` – اسم مساحة التخزين السحابية (اختياري)؛ `folder` – مسار المجلد داخل مساحة التخزين (اختياري).  
  - **الاستجابة:** تدفق ملف لكتاب العمل المحول؛ `Content‑Type` يطابق التنسيق المستهدف.  
  - **رموز الحالة (Status codes):** 200 OK، 400 Bad Request، 401 Unauthorized، 404 Not Found، 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **جسم الطلب (Request body):** multipart/form‑data يحتوي على ملف كتاب العمل المصدر (`file`) وحقل `format` إلزامي يُحدد التنسيق المطلوب.  
  - **الاستجابة:** تدفق ثنائي للملف المحول.  
  - **رموز الحالة (Status codes):** 200 OK، 400 Bad Request، 401 Unauthorized، 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **مُدخلات المسار (Path parameters):** `name` – اسم كتاب العمل الحالي.  
  - **مُدخلات الاستعلام (Query parameters):** `format` – التنسيق المستهدف؛ `outPath` – مسار الوجهة في التخزين السحابي (اختياري)؛ `storage` – اسم مساحة التخزين (اختياري).  
  - **الاستجابة:** كائن JSON يحتوي على نتيجة العملية ومسار الملف المحفوظ. مثال على الاستجابة:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "تم حفظ الملف بنجاح.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **رموز الحالة (Status codes):** 200 OK، 400 Bad Request، 401 Unauthorized، 404 Not Found، 500 Internal Server Error.  

**مثال على أمر cURL لتحويل إلى PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**مقتطف SDK لـ Java (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**مقتطف SDK لـ .NET (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**مقتطف SDK لـ Python (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

تشرح المقالات التالية كل واجهة برمجة تطبيقات بالتفصيل، وتشمل أمثلة إضافية لأوامر cURL وSDKs:

- [تحويل ملف إكسل إلى تنسيق مختلف](/ar/cells/convert-an-excel-file-to-different-formats)
- [حفظ ملف إكسل بصيغة مختلفة](/ar/cells/save-an-excel-file-as-other-formats-files)
- [تحويل ملف إكسل إلى ملف CSV](/ar/cells/convert-excel-file-to-csv-file)
- [تحويل ملف إكسل إلى ملف DOCX](/ar/cells/convert-excel-file-to-docx-file)
- [تحويل ملف إكسل إلى ملف HTML](/ar/cells/convert-excel-file-to-html-file)
- [تحويل ملف إكسل إلى ملف JSON](/ar/cells/convert-excel-file-to-json-file)
- [تحويل ملف إكسل إلى ملف Markdown](/ar/cells/convert-excel-file-to-markdown-file)
- [تحويل ملف إكسل إلى ملف PDF](/ar/cells/convert-excel-file-to-pdf-file)
- [تحويل ملف إكسل إلى ملف PNG](/ar/cells/convert-excel-file-to-png-file)
- [تحويل ملف إكسل إلى ملف PPTX](/ar/cells/convert-excel-file-to-pptx-file)
- [تحويل ملف إكسل إلى ملف SQL](/ar/cells/convert-excel-file-to-sql-file)
- [تحويل ملف إكسل إلى ملف TIFF](/ar/cells/convert-excel-file-to-tiff-file)
---