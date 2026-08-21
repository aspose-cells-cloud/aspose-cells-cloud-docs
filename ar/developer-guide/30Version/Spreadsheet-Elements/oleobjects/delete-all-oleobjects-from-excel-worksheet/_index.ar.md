---
title: حذف جميع كائنات OLE في ورقة عمل Excel
description: تعرف على كيفية إزالة جميع كائنات OLE (الربط والتضمين) من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن عنوان النهاية (endpoint)، المعاملات، أمثلة للطلب والاستجابة، مقاطع كود SDK، المصادقة، معالجة الأخطاء، وأسئلة متكررة.
keywords: Aspose.Cells Cloud, حذف كائنات OLE, واجهة برمجة تطبيقات Excel, REST API, مسح كائنات OLE في ورقة العمل, SDK السحابية
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# حذف جميع كائنات OLE في ورقة عمل Excel

**OleObjects – Clear** تقوم بإزالة **جميع** كائنات OLE (Object Linking and Embedding - الربط والتضمين) من ورقة عمل محددة مع ترك بيانات الخلايا سليمة. هذه العملية مفيدة لتنظيف الجداول القديمة أو إعداد ملف عمل لإعادة توزيعه.

---

## المتطلبات الأساسية

- رمز وصول **Aspose Cloud JWT** صالح (OAuth 2.0).  
- يجب تخزين ملف العمل المستهدف في مساحة تخزين Aspose Cloud (أو تحديد `folder`/`storageName` حيث يقع الملف).  
- إصدار **v3.0** أو أعلى من API.  

> **ملاحظة:** العملية *متطابقة (idempotent)* – أي أن استدعائها عندما لا توجد كائنات OLE في الورقة يُعيد استجابة ناجحة `200 OK`.

---

## طلب HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### معاملات المسار (Path parameters)

| الاسم        | النوع   | المطلوب | الوصف                           |
|-------------|---------|---------|---------------------------------|
| `name`      | سلسلة نصية | ✔️       | اسم ملف ملف العمل.              |
| `sheetName` | سلسلة نصية | ✔️       | اسم ورقة العمل.                 |

### معاملات الاستعلام (Query parameters)

| الاسم          | النوع   | المطلوب | الوصف                              |
|---------------|---------|---------|------------------------------------|
| `folder`      | سلسلة نصية | اختياري  | المجلد الذي يحتوي على ملف العمل.   |
| `storageName` | سلسلة نصية | اختياري  | اسم مساحة التخزين التي يُخزن فيها ملف العمل. |

**الرؤوس (Headers)**

| الرأس                  | القيمة                            |
|------------------------|----------------------------------|
| `Authorization`        | `Bearer <jwt token>` |
| `Accept`               | `application/json` |
| `Content-Type`         | `application/json` |

---

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*استبدل `<jwt token>` برمز وصول صالح، وعَدّل `folder`/`storageName` حسب الحاجة.*

---

## الاستجابة الناجحة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                              |
|------|----------------------------|-----------------------------------------------------|
| 200  | OK                         | تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request                | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized               | رمز JWT غير صالح أو مفقود.                         |
| 413  | Payload Too Large          | حجم الملف المرفوع يتجاوز الحد المسموح به.          |
| 500  | Internal Server Error      | خطأ في الخادم غير متوقع.                           |
---

## مقاطع كود SDK

توضح مقاطع الكود التالية كيفية استدعاء **DeleteWorksheetOleObjects** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud. استبدل القيم الوهمية (`<YOUR_TOKEN>`, `<FILE_NAME>`، إلخ) ببياناتك الخاصة.

| اللغة | المثال |
|-------|--------|
| **C#** | <details><summary>إظهار مثال C#</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = "<YOUR_TOKEN>", BasePath = "https://api.aspose.cloud" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: "Sample.xlsx", sheetName: "Sheet1", folder: "Samples", storageName: null);\n```</details> |
| **Java** | <details><summary>إظهار مثال Java</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken("<YOUR_TOKEN>");\nconfig.setBasePath("https://api.aspose.cloud");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects("Sample.xlsx", "Sheet1", "Samples", null);\n```</details> |
| **Python** | <details><summary>إظهار مثال Python</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>إظهار مثال Node.js</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>إظهار مثال Go</summary>```go\npackage main\nimport (\n    "context"\n    "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = "<YOUR_TOKEN>"\n    cfg.Host = "https://api.aspose.cloud"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), "Sample.xlsx", "Sheet1", map[string]interface{}{ "folder": "Samples" })\n    if err != nil { panic(err) }\n    println("All OLE objects deleted")\n}\n```</details> |

*يمكنك الاطلاع على ملفات المصدر الكاملة لكل اللغات المدعومة في [مستودع Aspose.Cells Cloud على GitHub](https://github.com/aspose-cells-cloud).*

---

## الأخطاء ومعالجتها

- **التطابق (Idempotency)** – حذف كائنات OLE من ورقة عمل لا تحتوي على أي كائنات لا يزال يُعيد `200 OK`.  
- **انتهاء صلاحية الرمز** – إذا تلقيت `401 Unauthorized`، فاحصل على رمز JWT جديد وحاول مرة أخرى.  
- **اسم ورقة العمل غير صحيح** – تأكد من أن اسم ورقة العمل يطابق الحالة (أحرف كبيرة/صغيرة) المستخدمة في ملف العمل؛ وإلا سيُعاد `400 Bad Request`.  

طبّق منطق إعادة المحاولة مع تأخير أسي (exponential back-off) لأخطاء `500` المؤقتة.

---

## الأسئلة المتكررة (FAQ)

**س1: هل أحتاج إلى تحديد معاملات `folder` و `storageName`؟**  
**ج:** لا. إذا تُركتا دون تحديد، يفترض Aspose Cloud استخدام مساحة التخزين الافتراضية والمجلد الجذر.

**س2: هل يمكنني حذف كائنات OLE من خلية محددة فقط؟**  
**ج:** تُزيل هذه النهاية **جميع** كائنات OLE في ورقة العمل. لحذف كائن واحد فقط، استخدم عملية *حذف كائن OLE محدد*.

**س3: ماذا يحدث إذا كان ملف العمل مقفلًا للتحرير؟**  
**ج:** سيعيد API `400 Bad Request` مع رسالة تشير إلى أن الملف مقفل. تأكد من أن الملف غير مفتوح في مكان آخر قبل استدعاء النهاية.

**س4: هل هناك حد لحجم ملف العمل؟**  
**ج:** تلتزم الخدمة بحدود حجم ملفات Aspose Cloud العامة (حتى 2 جيجابايت لكل ملف حاليًا). قد تحتاج الملفات الأكبر إلى التقسيم أو المعالجة على دفعات.

---

## أفضل الممارسات

- **الأداء** – استخدم سمات `async` أو `defer` عند تحميل نصوص الجهة الثالثة في موقع التوثيق الخاص بك لتقليل وقت تحميل الصفحة الأولي.  
- **الأمان** – أضف `rel="noopener noreferrer"` إلى أي روابط خارجية تفتح في علامة تبويب جديدة.  
- **إتاحة الوصول** – يجب أن تحتوي الأيقونات الت装ية (مثل الأسهم المُسفلة في الشريط الجانبي) على `alt=""` و `role="presentation"` للاستيفاء بمعايير WCAG AA.  
- **الاتساق** – احتفظ بتنسيق التواريخ بصيغة ISO‑8601 (`YYYY‑MM‑DD`) لتجنب ظهور تشوهات في الترميز.

---

## العمليات ذات الصلة

- **إضافة كائن OLE** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **حذف كائن OLE محدد** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

استخدم الروابط التنقلية في أسفل الصفحة للتنقل بين إجراءات API ذات الصلة.

---