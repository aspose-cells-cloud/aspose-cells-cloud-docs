---
title: "تصدير ورقة عمل باستخدام واجهة Aspose.Cells Cloud API – التنسيقات وأمثلة cURL وSDK"
second_title: "مستند"
linktype: "docs"
url: "/worksheets/get-worksheet/"
keywords: "Aspose.Cells Cloud Get Worksheet، تصدير ورقة عمل، Excel API، REST، CSV، PDF، PNG، JPEG، GIF، BMP، TIFF، EMF، XPS، OTS، XLS، XLSX، XLSB، XLSM، ODS، FODS، Numbers، cloud API"
description: "تعلّم كيفية تصدير ورقة عمل واحدة من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن_endpoint_ والمُعلمات ومثال cURL مُصحّح وتفاصيل المصادقة ومعالجة الأخطاء وأجزاء من كود SDK لـ C# وJava وPython وغيرهما."
weight: 10
ArticleTitle: "تصدير ورقة عمل باستخدام واجهة Aspose.Cells Cloud API – التنسيقات وأمثلة cURL وSDK"
---

تتيح لك واجهة REST هذه **تصدير ورقة عمل** من ملف Excel إلى العديد من تنسيقات الملفات المختلفة.

**الملخص** – استخدم نقطة النهاية **Get Worksheet** لتنزيل ورقة عمل واحدة من مصنف Excel بالتنسيق الذي تختاره.

يمكنك التصدير إلى التنسيقات التالية:

| التنسيق | الامتداد | نوع MIME                                                         |
| ------- | -------- | ---------------------------------------------------------------- |
| XLS     | .xls     | application/vnd.ms-excel                                          |
| XLSX    | .xlsx    | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb    | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv     | text/csv                                                          |
| TSV     | .tsv     | text/tab-separated-values                                         |
| XLSM    | .xlsm    | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods     | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt     | text/plain                                                        |
| PDF     | .pdf     | application/pdf                                                   |
| OTS     | .ots     | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps     | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif     | application/x-dif                                                 |
| PNG     | .png     | image/png                                                         |
| JPEG    | .jpeg    | image/jpeg                                                        |
| GIF     | .gif     | image/gif                                                         |
| BMP     | .bmp     | image/bmp                                                         |
| WMF     | .wmf     | image/wmf                                                         |
| TIFF    | .tiff    | image/tiff                                                        |
| EMF     | .emf     | image/emf                                                         |
| NUMBERS | .numbers | application/vnd.apple.numbers                                     |
| FODS    | .fods    | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## الأمان والمصادقة
تعمل واجهات برمجة تطبيقات Aspose.Cells Cloud بشكل آمن وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **مُعلمات الطلب**

| اسم المُعلمة            | النوع    | الموقع | الوصف                                                              |
| ------------------------ | ------- | ------ | ------------------------------------------------------------------ |
| **name**                 | string  | path   | **مطلوبة.** اسم ملف Excel.                                         |
| **sheetName**            | string  | path   | **مطلوبة.** اسم ورقة العمل المراد تصديرها.                         |
| **format**               | string  | query  | تنسيق ملف الوجهة لورقة العمل المُصدَّرة (مثل: `pdf`، `png`).       |
| **verticalResolution**   | integer | query  | دقة الصورة بالـ DPI للتنسيقات التي تدعم الدقة (مثل: PNG، JPEG).    |
| **horizontalResolution** | integer | query  | دقة الصورة بالـ DPI للتنسيقات التي تدعم الدقة.                      |
| **area**                 | string  | query  | نطاق الخلايا المراد تصديره (مثل: `A1:D10`).                       |
| **pageIndex**            | integer | query  | مؤشر الصفحة المراد تصديرها عندما تكون ورقة العمل مقسّمة إلى صفحات. |
| **folder**               | string  | query  | مسار المجلد في التخزين حيث يوجد الملف المصدر.                      |
| **storageName**          | string  | query  | اسم تخزين Aspose Cloud.                                            |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تعرّف واجهة برمجة تطبيقات متاحة علنًا وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<بيانات ثنائية>
```

{{< /tab >}}

{{< /tabs >}}

## معالجة الأخطاء

تردّ الواجهة على تنسيق رموز الحالة (HTTP status codes) القياسية. تشمل الردود الشائعة ما يلي:

| رمز الحالة | المعنى                                                     | مثال جسم JSON                              |
| ---------- | ----------------------------------------------------------- | ------------------------------------------ |
| **200**    | نجاح – يتم إرجاع تدفق ورقة العمل.                           | `{ "stream": "..." }`                      |
| **400**    | طلب غير صحيح – مُعلمات مفقودة أو غير صالحة.                | `{ "error": "Invalid format parameter." }` |
| **401**    | غير مصادق عليه – رمز JWT غير صالح أو مفقود.                | `{ "error": "Authentication failed." }`    |
| **404**    | غير موجود – الملف أو ورقة العمل المحددة غير موجودة.       | `{ "error": "Worksheet not found." }`      |
| **500**    | خطأ داخلي في الخادم – حالة غير متوقعة على الخادم.         | `{ "error": "Unexpected error." }`         |

قم بمعالجة هذه الردود في كود العميل لتقديم ملاحظات مناسبة للمستخدمين.

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}