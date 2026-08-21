---
title: "حذف التنسيق الشرطي – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells، التنسيق الشرطي، حذف، واجهة برمجة تطبيقات، Excel، سحابة"
description: "حذف قاعدة تنسيق شرطي من ورقة عمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يتضمن المُعلمات، المصادقة، أمثلة على الطلبات والاستجابات، ومقتطفات من SDK."
weight: 60
---

# حذف التنسيق الشرطي

## الخلفية
يتيح لك التنسيق الشرطي تطبيق أنماط بصرية على الخلايا التي تتوافق مع معايير محددة (مثل: تمييز القيم الأكبر من حدٍ معين). قد تحتاج في سيناريوهات الأتمتة إلى إزالة قاعدة موجودة. تُستخدم هذه النقطة النهائية لحذف قاعدة تنسيق شرطي من ورقة عمل في ملف Excel مخزن في مساحة التخزين السحابية لـ Aspose Cloud.

## المتطلبات الأساسية
- حساب **Aspose Cloud** مع تمكين منتج **Cells**.  
- **رمز وصول JWT** تم إنشاؤه عبر تدفق مُصادقة OAuth 2.0 لبيانات اعتماد العميل.  
- يجب أن يكون ملف المصنف (`{name}`) موجودًا مسبقًا في **المجلد** المحدد و**مساحة التخزين** (إن وُجدت).  
- تُستخدم إصدار واجهة برمجة التطبيقات **v3.0** (الافتراضي) في الروابط الموضحة أدناه.

## المصادقة
تتطلب جميع نقاط نهاية Aspose.Cells Cloud **مصادقة تعتمد على رمز JWT**.

```http
Authorization: Bearer <access_token>
```

### الحصول على رمز وصول (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**الاستجابة**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

استخدم `access_token` الذي تم إعادته في رأس `Authorization` لكل طلب.

## طلب HTTP

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### مُعلمات المسار (Path Parameters)

| الاسم        | النوع    | مطلوب | الوصف |
|-------------|----------|--------|--------|
| `name`      | نص (string) | نعم | اسم ملف المصنف (مثل: `Book1.xlsx`). |
| `sheetName` | نص (string) | نعم | اسم ورقة العمل التي تحتوي على التنسيق الشرطي. |
| `index`     | عدد صحيح (integer) | نعم | المؤشر الصفري (zero-based) لقاعدة التنسيق الشرطي المراد حذفها. |

### مُعلمات الاستعلام (Query Parameters)

| الاسم           | النوع    | مطلوب | الوصف |
|----------------|----------|--------|--------|
| `folder`       | نص (string) | لا    | مجلد السحابة حيث يقع المصنف. |
| `storageName`  | نص (string) | لا    | اسم خدمة تخزين Aspose Cloud. |

## مثال على الطلب (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### استجابة ناجحة

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**رموز حالة HTTP**

| الرمز | المعنى               | الوصف |
|-------|----------------------|--------|
| 200   | ناجح (OK)            | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | مُعلمات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم). |
| 401   | غير مُصادق (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## استجابات الأخطاء

| رمز HTTP | السبب | جسم المثال |
|-----------|--------|-------------|
| **400**   | طلب غير صالح (Bad Request) – مُعلمات مفقودة أو غير صحيحة. | `{ "Code":"400", "Message":"قيمة المُعلمة غير صحيحة." }` |
| **401**   | غير مُصادق (Unauthorized) – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"رمز الوصول مفقود أو غير صالح." }` |
| **404**   | غير موجود (Not Found) – المصنف أو ورقة العمل غير موجودة. | `{ "Code":"404", "Message":"الملف غير موجود." }` |
| **500**   | خطأ داخلي في الخادم (Internal Server Error) – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"حدث خطأ غير متوقع." }` |

## أمثلة SDK
تُظهر المقتطفات التالية كيفية تنفيذ عملية **حذف التنسيق الشرطي** باستخدام SDKs الرسمية لـ Aspose.Cells Cloud.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// تكوين عميل API
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// حذف التنسيق الشرطي
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('تم حذف التنسيق الشرطي.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("تمت إزالة التنسيق الشرطي.")
```

*(تتوفر مقتطفات SDK إضافية لـ Ruby و Go و Perl و Swift في [مستودع GitHub](https://github.com/aspose-cells-cloud).)*

## انظر أيضًا
- **دليل المصادقة** – [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **مواصفات OpenAPI** – مخطط مفصّل لنقطة النهاية هذه (يفتح في نافذة جديدة)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a>`  
- **نظرة عامة على التنسيق الشرطي** – تعلّم كيفية إنشاء وتحديث وعرض قواعد التنسيق.  
- **SDKs لـ Aspose.Cells Cloud** – القائمة الكاملة للغات البرمجة المدعومة في [مستودع GitHub](https://github.com/aspose-cells-cloud).  

---  

*تتبع هذه الصفحة القالب القياسي لتوثيق واجهة برمجة تطبيقات Aspose.Cells Cloud، وتشمل قسم المتطلبات الأساسية، وتوافق أفضل ممارسات إمكانية الوصول وتحسين محركات البحث (SEO).*