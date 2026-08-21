---
title: "واجهة برمجة تطبيقات تنزيل الملف في Aspose.Cells Cloud – واجهة لتنزيل الملفات بسرعة في السحابة"
second_title: "وثيقة"
ArticleTitle: "واجهة برمجة تطبيقات تنزيل الملف في Aspose.Cells Cloud – واجهة لتنزيل الملفات بسرعة في السحابة"
linktitle: "واجهة برمجة تطبيقات تنزيل الملف"
type: docs
url: /download-file/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات تنزيل الملف، تخزين Excel السحابي، واجهة برمجة تطبيقات REST، تنزيل الملف، PDF، CSV، SDK"
description: "قم بتنزيل ملفات Excel وPDF وCSV وملفات أخرى من تخزين Aspose.Cells Cloud باستخدام واجهة برمجة تطبيقات تنزيل الملف (الإصدار 4.0). تتضمن النقطة النهائية (endpoint)، والمعلمات، وتفاصيل المصادقة، وأمثلة على الأكواد."
weight: 100
---

تتيح لك واجهة برمجة التطبيقات **DownloadFile** استرجاع الملفات المخزنة في تخزين Aspose.Cells Cloud. تُعد واجهة برمجة تطبيقات تنزيل الملف ضرورية للوصول مباشرةً إلى جداول Excel وملفات PDF وCSV وتنسيقات أخرى مدعومة من السحابة.

## **واجهة برمجة تطبيقات Excel: تنزيل الملف**

### واجهة برمجة التطبيقات عبر الويب

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معلمات الطلب لواجهة برمجة التطبيقات **DownloadFile**

| اسم المعلمة | النوع | الموقع (مسار / استعلام) | الوصف |
|------------|-------|------------------------|-------|
| path | سلسلة نصية | المسار | المسار الظاهري للملف الذي ترغب في تنزيله. |
| storageName | سلسلة نصية | استعلام | اسم التخزين الذي سيتم استرجاع الملف منه. |
| versionId | سلسلة نصية | استعلام | معرّف الإصدار للملف المراد تنزيله، إن وُجد. |

### **الاستجابة**

تعيد واجهة برمجة التطبيقات **تدفق ملف ثنائي**. يتوافق رأس `Content-Type` مع تنسيق الملف (مثلاً، `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` لملفات XLSX). ولا يتم إرجاع أي حمولة (payload) بصيغة JSON.

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|--------|-------|
| 200 | ناجح (OK) | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُauthorized (Unauthorized) | رمز JWT غير صالح أو ناقص. |
| 413 | حملة كبيرة جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) واجهة برمجة تطبيقات قابلة للوصول العام، وتسمح لك بإجراء تفاعلات REST مباشرةً من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs لـ Aspose.Cells Cloud

يُعد استخدام SDKs أفضل طريقة لتسريع عملية التطوير. فتتولى SDKs إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}