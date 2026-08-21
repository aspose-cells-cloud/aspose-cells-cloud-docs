---
title: "فك تشفير ملف Excel"
second_title: "مستند"
linktitle: "فك تشفير ملف Excel"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, فك تشفير Excel, REST API, SDK للحوسبة السحابية"
description: "تعرّف على كيفية فك تشفير ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل المعلمات المطلوبة، مثال cURL، أمثلة للكود باستخدام SDK، وتفاصيل التعامل مع الأخطاء."
ArticleTitle: "كيفية فك تشفير ملف Excel باستخدام واجهة Aspose.Cells Cloud API"
weight: 50
---

**المتطلبات الأساسية**

- رمز وصول JWT صالح.
- يجب أن يكون الملف المحمي ببيانات سرية قد تم رفعه إلى مساحة تخزين Aspose Cloud مع تحديد مساره في معامل الاستعلام `folder`.

## واجهة DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الاستعلام

| اسم المعامل | النوع   | الوصف                                               |
|-------------|--------|-----------------------------------------------------|
| folder      | string | مسار المجلد الذي يوجد فيه ملف Excel الأصلي.          |
| storageName | string | اسم مساحة التخزين التي يوجد فيها ملف Excel.         |

### معامل جسم الطلب

| اسم المعامل | النوع                      | الوصف                                           |
|-------------|----------------------------|-------------------------------------------------|
| encryption  | WorkbookEncryptionRequest | إعدادات التشفير المطلوبة لفك التشفير.            |

### WorkbookEncryptionRequest

| اسم المعامل    | النوع    | الوصف                                                                                             |
|----------------|----------|---------------------------------------------------------------------------------------------------|
| EncryptionType | string   | خوارزمية التشفير (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer  | طول مفتاح التشفير بالبتات.                                                                         |
| Password       | string   | كلمة المرور المستخدمة لفك التشفير.                                                                |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

** أمثلة على استجابات الأخطاء**

```json
{
  "Code": "400",
  "Message": "معاملات طلب غير صالحة."
}
```

```json
{
  "Code": "401",
  "Message": "فشل المصادقة. رمز JWT غير صالح أو مفقود."
}
```

```json
{
  "Code": "413",
  "Message": "حجم البيانات كبير جدًا. تجاوز الملف المرفوع الحد المسموح به."
}
```

```json
{
  "Code": "500",
  "Message": "خطأ داخلي في الخادم. يُرجى المحاولة مرة أخرى لاحقًا."
}
```

**رموز حالة HTTP**

| الكود | المعنى                        | الوصف                                               |
|-------|-------------------------------|-----------------------------------------------------|
| 200   | ناجح (OK)                     | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request)    | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401   | غير مخوّل (Unauthorized)       | رمز JWT غير صالح أو مفقود.                          |
| 413   | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز الملف المرفوع الحد المسموح به.               |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                            |
## كيفية استخدام واجهة DeleteDecryptWorkbook API باستخدام حزم التطوير (SDKs)

### مواصفات واجهة DeleteDecryptWorkbook API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### استخدام حزم تطوير Aspose.Cells Cloud (SDKs)

استخدام حزم التطوير (SDKs) هو أفضل طريقة لتسريع عملية التطوير. فتتولى حزم التطوير إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم تطوير مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}