---
title: "تشفير مصنف Excel باستخدام واجهة Aspose.Cells Cloud API – أمثلة سريعة لـ cURL و SDK"
second_title: "وثيقة"
linktitle: "تشفير ملف Excel"
type: docs
url: /ar/excel-file-encrypt/
aliases: [  /ar/encrypt-excel-workbooks/ , /ar/workbook/encrypt/ ]
keywords: "تشفير مصنف Aspose Cells، واجهة تشفير Excel، واجهة REST API، cURL، .NET، Java، Python، PHP، Ruby، Node.js، Go، Perl"
description: "تعلم كيفية تشفير مصنف Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يشمل مثالًا لأمر cURL، وأكواد مرجعية لـ SDK (C#، Java، Python، إلخ)، والمعلمات المطلوبة، وإدارة الأخطاء."
weight: 20
ArticleTitle: "تشفير مصنف Excel باستخدام واجهة Aspose.Cells Cloud API – أمثلة لـ cURL و SDK"
---

تقوم هذه الواجهة (REST API) بتشفير **مصنف** Excel.

**المتطلبات المسبقة:** يجب أن تمتلك رمز JWT صالحًا، وأن يكون المصنف مُرفَعًا في موقع تخزين قبل استدعاء هذه النقطة النهائية (endpoint).

## واجهة PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الاستعلام (Query Parameters)**

| اسم المعلمة | النوع   | مطلوبة | الوصف                                   |
| ------------ | ------ | -------- | ---------------------------------------- |
| folder       | string | ✗        | مسار المجلد الذي يحتوي على المصنف الأصلي. |
| storageName  | string | ✗        | اسم وحدة التخزين المراد استخدامها.        |

### **معلمة جسم الطلب (Request Body Parameter)**

| اسم المعلمة | النوع                      | مطلوبة | الوصف                              |
| ------------ | -------------------------- | -------- | ----------------------------------- |
| encryption   | WorkbookEncryptionRequest  | ✓        | إعدادات التشفير الخاصة بالمصنف.     |

#### **WorkbookEncryptionRequest**

| اسم المعلمة     | النوع   | مطلوبة | الوصف                                                                                   |
| --------------- | ------- | -------- | ---------------------------------------------------------------------------------------- |
| EncryptionType  | string  | ✓        | خوارزمية التشفير. انظر الجدول أدناه للاطلاع على القيم المدعومة ومقاصدها.                |
| KeyLength       | integer | ✗        | طول مفتاح التشفير بالبتات (يُهمل لقيمتَي `XOR` و `Compatible`).                         |
| Password        | string  | ✓        | كلمة المرور المستخدمة في التشفير.                                                       |

#### **قيم EncryptionType**

| القيمة                             | الوصف                                                      |
| ---------------------------------- | ----------------------------------------------------------- |
| `XOR`                              | خوارزمية XOR البسيطة (قديمة، أمان منخفض).                   |
| `Compatible`                       | تشفير متوافق مع Excel 97‑2003 (بمفتاح 40‑بت).               |
| `EnhancedCryptographicProviderV1` | AES‑128 مع تجزئة SHA‑1.                                     |
| `StrongCryptographicProvider`     | AES‑256 مع تجزئة SHA‑512 (أقوى خوارزمية مدعومة).            |

### الاستجابة (Response)

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الكود | المعنى                     | الوصف                                                                 |
|------|----------------------------|----------------------------------------------------------------------|
| 200  | ناجح (OK)                  | تم تطبيق التشفير بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.         |
| 400  | طلب غير صالح (Bad Request)| معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                 |
| 401  | غير مصادق عليه (Unauthorized)| رمز JWT غير صالح أو مفقود.                                           |
| 413  | حجم الحمولة كبيرة جدًا (Payload Too Large)| تجاوز حجم الملف المرفوع الحد المسموح به.                         |
| 500  | خطأ داخلي في الخادم (Internal Server Error)| حدث خطأ غير متوقع في الخادم.                                      |

## كيفية استخدام واجهة PostEncryptDocument باستخدام SDKs

### مواصفات واجهة PostEncryptDocument

تُعرِّف <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# تشفير المصنف "test.xlsx" باستخدام خوارزمية XOR (مفتاح 128‑بت) وكلمة المرور "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**استجابات الأخطاء المحتملة**

| حالة HTTP | الرمز                | الرسالة                                         |
| --------- | -------------------- | ----------------------------------------------- |
| 400       | BadRequest           | معلمات مفقودة أو غير صالحة.                    |
| 401       | Unauthorized         | رمز المصادقة مفقود أو غير صالح.                |
| 403       | Forbidden            | صلاحيات غير كافية للوصول إلى وحدة التخزين.      |
| 500       | InternalServerError  | خطأ غير متوقع في الخادم.                        |

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. وتتولى SDK إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهة الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}