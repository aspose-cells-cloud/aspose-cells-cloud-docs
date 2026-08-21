---
title: "تحويل نطاق إكسل إلى صورة – واجهة برمجة تطبيقات Aspose.Cells Cloud"
description: "تحويل نطاق محدد من ملف إكسل محلي إلى تنسيق PNG أو JPEG أو SVG أو TIFF أو BMP عبر واجهة برمجة تطبيقات Aspose.Cells Cloud REST API – لا يتطلب تحميل الملف الكامل للورقة الحسابية."
keywords: "Aspose.Cells Cloud، تحويل النطاق إلى صورة، واجهة برمجة تطبيقات إكسل، تنسيقات الصور، PNG، JPEG، SVG، TIFF، BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

يقوم هذا الاستدعاء بقراءة ملف جدول بيانات محلي، وتحويل النطاق المحدّد، ثم إعادة الصورة كدفق ثنائي.

## طريقة تحويل النطاق إلى صورة

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## مُعاملات الطلب

| الاسم                 | الموقع                            | النوع   | الإجبارية | الوصف                                                                          |
| --------------------- | --------------------------------- | ------- | --------- | ------------------------------------------------------------------------------ |
| **Spreadsheet**       | Form‑Data (`multipart/form-data`) | ملف    | **نعم**   | ملف إكسل الذي سيتم معالجته.                                                    |
| **worksheet**         | Query                             | سلسلة نصية | **نعم**   | اسم ورقة العمل التي تحتوي على النطاق (مثال: `Sheet1`).                          |
| **range**             | Query                             | سلسلة نصية | **نعم**   | منطقة الخلايا المراد تحويلها، مثال: `A1:C10`.                                   |
| **format**            | Query                             | سلسلة نصية | **نعم**   | تنسيق الصورة الناتجة (`png`، `jpeg`، `svg`، `tiff`، `bmp`).                      |
| **printHeadings**     | Query                             | منطقي   | لا        | `true` لتضمين عناوين الصفوف والأعمدة في الصورة.                                 |
| **outPath**           | Query                             | سلسلة نصية | لا        | مسار المجلد لحفظ الملف المُولّد إذا أردت تخزينه في مساحة التخزين السحابية.     |
| **outStorageName**    | Query                             | سلسلة نصية | لا        | اسم خدمة التخزين (مثال: `MyStorage`).                                          |
| **fontsLocation**     | Query                             | سلسلة نصية | لا        | عنوان URL أو مسار خطوط مخصّصة تُستخدم أثناء التحويل.                            |
| **region**            | Query                             | سلسلة نصية | لا        | معرّف المنطقة (مثال: `en-US`، `fr-FR`)؛ يؤثّر على تنسيق الأرقام والتاريخ.       |
| **password**          | Query                             | سلسلة نصية | لا        | كلمة المرور لملفات العمل المشفرة.                                              |
| **AutoRowsFit**       | Query                             | منطقي   | لا        | ضبط ارتفاع الصفوف تلقائيًا قبل العرض.                                          |
| **AutoColumnsFit**    | Query                             | منطقي   | لا        | ضبط عرض الأعمدة تلقائيًا قبل العرض.                                           |

## الاستجابة

تُعيد واجهة برمجة التطبيقات ملف HTML مُحوّل كـ **دفق ثنائي** (`application/octet-stream`).

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

### مثال على استجابة ناجحة (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

احفظ محتوى جسم الاستجابة في ملف (مثل `report.png`) لعرض الصورة المُولّدة في المتصفح.

---

**أكواد حالة HTTP**

| الكود | المعنى                | الوصف                                                           |
| ----- | --------------------- | --------------------------------------------------------------- |
| 200   | ناجح                 | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.     |
| 400   | طلب غير صالح         | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).          |
| 401   | غير مُصادَق           | رمز JWT غير صالح أو مفقود.                                     |
| 413   | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح.                          |
| 500   | خطأ داخلي في الخادم   | خطأ غير متوقع في الخادم.                                       |

## كيف تستخدم واجهة برمجة تطبيقات تحويل النطاق إلى صورة باستخدام مكتبات SDK؟

### مواصفات OpenAPI

تُحدّد [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) واجهة برمجة تطبيقات متاحة عمومًا، مما يتيح التفاعل عبر REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إرسال طلبات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة لتطوير التطبيقات، لأنها تجنبك التفاصيل منخفضة المستوى، مما يتيح لك تحويل نطاق من البيانات إلى ملف صورة بأقل قدر ممكن من الكود.  
استكشف القائمة الكاملة لمكتبات SDK الخاصة بـ Aspose.Cells Cloud في [مستودع GitHub](https://github.com/aspose-cells-cloud).

توضح الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة. إذا كان تحميل الأمثلة من Gist ممنوعًا، يمكنك تحميل الأمثلة مباشرةً من المستودع.

---