---
title: "حماية ملفات Excel"
second_title: "الوثيقة"
linktype: "تشفير ملفات Excel"
type: docs
url: /protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells، واجهة برمجة تطبيقات حماية Excel، تشفير مصنف Excel، أمان جداول البيانات في السحابة، واجهة برمجة تطبيقات REST"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud REST لحماية ملفات Excel. يوضح هذا الدليل كيفية تشفير مصنفات عبر HTTP POST وcURL وSDKs بلغات برمجة متعددة، وذلك اعتبارًا من عام 2026."
weight: 40
---

تقوم هذه واجهة برمجة تطبيقات REST بحماية ملفات Excel.

## واجهة برمجة تطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### الأمان والمصادقة

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| ----------- | ----- | ------ | ------ |
| file | ملف | formData (body) | الملف المرفوع |
| password | نص | سلسلة الاستعلام (`password`) | كلمة المرور المستخدمة لحماية المصنف |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "اسم الملف المحمي: smaple1.xlsx",
      "FileSize": الحجم,
      "FileContent": "-----سلسلة Base64 لملف sample1-----"
    },
    {
      "Filename": "اسم الملف المحمي: sample2.xlsx",
      "FileSize": الحجم,
      "FileContent": "-----سلسلة Base64 لملف sample2-----"
    }
  ]
}
```

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
| ----- | ------ | ------ |
| 200 | نجاح | تم تطبيق الحماية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا | تجاوز حجم الملف المرفوق الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostProtect API مع SDKs

### مواصفات واجهة PostProtect API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----سلسلة Base64 لملف sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----سلسلة Base64 لملف sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **معالجة الأخطاء**

– يمكن أن تُعيد واجهة برمجة التطبيقات رموز الحالة التالية:

| رمز HTTP | المعنى | محتوى خطأ JSON مثال |
| --------- | ------ | ------------------- |
| 400 | طلب غير صالح (مثل ملف مفقود) | `{"Code":400,"Message":"الملف مطلوب."}` |
| 401 | غير مصرّح به (رمز غير صالح أو مفقود) | `{"Code":401,"Message":"رمز الوصول غير صالح."}` |
| 403 | ممنوع (صلاحيات غير كافية) | `{"Code":403,"Message":"تم رفض الوصول."}` |
| 500 | خطأ داخلي في الخادم | `{"Code":500,"Message":"خطأ غير متوقع في الخادم."}` |

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة لتطوير التطبيقات. فتتولى SDKs إدارة التفاصيل من المستوى المنخفض، ما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}