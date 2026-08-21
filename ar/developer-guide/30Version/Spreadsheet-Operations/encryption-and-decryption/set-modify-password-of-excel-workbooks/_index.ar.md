---
title: "تعديل حماية كلمة المرور لملف مصنف Excel"
second_title: "مستند"
linktitle: "تعديل كلمة مرور ملف Excel"
type: docs
url: /workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "كلمة مرور Excel، Aspose.Cells Cloud، الحماية ضد الكتابة، واجهة REST API، تعديل كلمة مرور المصنف"
description: "تغيير كلمة مرور الحماية ضد الكتابة لملف مصنف Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن أمثلة باستخدام cURL وSDKs."
weight: 100
ArticleTitle: "تعديل حماية كلمة المرور لملف مصنف Excel – Aspose.Cells Cloud"
---

تقوم هذه الواجهة **بتغيير كلمة مرور الحماية ضد الكتابة** لمصنف Excel موجود مسبقًا.

يتيح تحديث كلمة مرور الحماية ضد الكتابة برمجيًا تدوير كلمات المرور أو استبدالها دون تنزيل الملف. وهي مفيدة جدًا عند إدارة المصنفات المؤمنة المخزنة في مساحة التخزين الخاصة بـ Aspose.Cells Cloud.


## واجهة REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### الأمان والمصادقة

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### معاملات الطلب

| اسم المعامل      | النوع   | الموقع     | الوصف                                            |
| ---------------- | ------- | ---------- | ------------------------------------------------ |
| **name**         | نص (string) | المسار (path) | اسم ملف مصنف Excel (مطلوب).                       |
| **password**     | نص (string) | الجسم (body) بصيغة JSON | كلمة مرور الحماية ضد الكتابة الجديدة المراد تعيينها (مطلوب). |
| **folder**       | نص (string) | الاستعلام (query) | المجلد اختياري حيث يُخزَّن المصنف.                |
| **storageName**  | نص (string) | الاستعلام (query) | اسم خدمة التخزين اختياري.                        |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                            |
|-------|-------------------------------|--------------------------------------------------|
| 200   | ناجح (OK)                     | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request)   | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مصرّح (Unauthorized)      | رمز JWT غير صالح أو مفقود. |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PutDocumentProtectFromChanges باستخدام SDKs

### مواصفات واجهة PutDocumentProtectFromChanges

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) الواجهة البرمجية العامة المُتاحة التي تسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح أمر cURL أدناه كيفية استدعاء واجهة Cloud API.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. تُتعامل SDKs مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على المنطق التجاري. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}