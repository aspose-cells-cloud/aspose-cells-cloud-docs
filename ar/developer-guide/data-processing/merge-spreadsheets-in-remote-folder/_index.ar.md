---
---
title: "دمج جداول البيانات المتطابقة في مجلد بعيد"
description: "دمج ملفات جداول البيانات المخزنة في مساحة تخزين Aspose Cloud في ملف واحد. يدعم أكثر من 30 تنسيقًا للإخراج مثل PDF وCSV وJSON وXLSX وODS وXPS وغيرها."
keywords: "Aspose.Cells، دمج جداول البيانات، مجلد بعيد، واجهة برمجة تطبيقات، PDF، CSV، JSON، XLSX، ODS، XPS"
weight: 100
type: docs
url: /merge-spreadsheets-in-remote-folder/
---

دمج ملفات جداول البيانات المتعددة الموجودة في مجلد بعيد في مساحة تخزين Aspose Cloud إلى ملف إخراج واحد. تتم العملية بالكامل في السحابة، مما يلغي الحاجة إلى تنزيل الملفات المصدر محليًا. ويُدعم أكثر من 30 تنسيقًا للإخراج (PDF وCSV وJSON وXLSX وODS وXPS…).

## واجهة برمجة التطبيقات MergeSpreadsheetsInRemoteFolder

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب <a id="request-parameters"></a>

| الاسم                      | النوع    | الموقع   | مطلوب | الوصف                                                                                               |
| ------------------------- | -------- | -------- | ----- | ---------------------------------------------------------------------------------------------------- |
| **folder**                | string   | query    | نعم   | مجلد مساحة التخزين السحابية الذي يحتوي على جداول البيانات المصدر.                                   |
| **fileMatchExpression**   | string   | query    | نعم   | النمط المستخدم لاختيار الملفات (مثل `*report*.xlsx`). يدعم الرموز البديلة `*` و`?`.                 |
| **outFormat**             | string   | query    | نعم   | تنسيق الإخراج المطلوب (`PDF` أو `CSV` أو `JSON` أو `XLSX` أو `ODS` أو `XPS`…).                        |
| **mergeInOneSheet**       | boolean  | query    | نعم   | `true` – دمج كل البيانات في ورقة عمل واحدة. `false` – يحصل كل ملف مصدر على ورقة عمل خاصة به.         |
| **storageName**           | string   | query    | لا     | اسم مساحة التخزين المخصصة؛ ويُستخدم التخزين الأساسي افتراضيًا إذا تُرك فارغًا.                      |
| **outPath**               | string   | query    | لا     | مجلد الوجهة لحفظ ملف الدمج. وإذا تُرك فارغًا، يُحفظ الملف في مجلد المصدر.                           |
| **outStorageName**        | string   | query    | لا     | اسم مساحة التخزين التي ستُكتب فيها ملفات الدمج.                                                     |
| **fontsLocation**         | string   | query    | لا     | مسار مجلد يحتوي على الخطوط المخصصة (يُحتاج هذا الخيار عند تصدير PDF أو صور).                       |
| **region**                | string   | query    | لا     | الإعدادات الإقليمية لتنسيق الأرقام والتاريخ والعملات (مثل `en-US` أو `de-DE`).                     |
| **password**              | string   | query    | لا     | كلمة المرور لفتح أي جدول بيانات مصدر مُحمي.                                                         |

## مثال على الطلب (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **الاستجابة**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

يمكن تنزيل الملف مباشرةً من عنوان `FileUrl` أو حفظه في الموقع المحدد عبر `outPath`.

**تفاصيل استجابة ناجحة**

| رمز الحالة | نوع المحتوى              | الوصف                                               |
| ---------- | ------------------------ | --------------------------------------------------- |
| 200 OK     | `application/octet-stream` | تدفق ثنائي لملف المصنف المدمج.                     |
| 202 Accepted | `application/json`       | JSON يحتوي على `FileUrl` و`FileName` وغيرها.       |

**رموز حالات HTTP**

| الرمز | المعنى                  | الوصف                                                       |
| ----- | ----------------------- | ------------------------------------------------------------ |
| 200   | OK                      | تمت عملية التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request             | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).         |
| 401   | Unauthorized            | رمز JWT غير صالح أو مفقود.                                   |
| 413   | Payload Too Large       | حجم الملف المرفق يتجاوز الحد المسموح.                         |
| 500   | Internal Server Error   | خطأ غير متوقع في الخادم.                                     |

## كيفية استخدام واجهة برمجة تطبيقات دمج جداول البيانات مع مكتبات SDK

### مواصفات OpenAPI

توفر <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">مواصفات OpenAPI</a> وصفًا قابلًا للقراءة آليًا لواجهة برمجة التطبيقات، مما يتيح التفاعل المباشر مع REST.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، لأنها تخفي التفاصيل منخفضة المستوى، مما يسمح لك باستيراد البيانات إلى ورقة عمل جدول بيانات باستخدام كود قصير. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

---