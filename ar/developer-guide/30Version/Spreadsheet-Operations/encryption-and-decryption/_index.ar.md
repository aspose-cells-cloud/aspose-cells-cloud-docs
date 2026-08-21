---
title: "تشفير وفك تشفير وتوقيع ملفات Excel رقميًا"
second_title: "المستند"
linktype: "حماية ملف Excel"
type: docs
url: /ar/protect/
aliases: [  /ar/workbook/password/ ]
keywords: "Excel, حماية, تشفير, فك التشفير, التوقيع الرقمي, Aspose.Cells Cloud, REST API, كلمة مرور, أمان"
description: "تعرّف على كيفية حماية وتشفير وفك تشفير والتوقيع الرقمي لملفات Excel باستخدام واجهة Aspose.Cells Cloud REST API – أمثلة على الكود بلغات Android وC# وJava وPython وغيرها."
ArticleTitle: "تشفير وفك تشفير والتوقيع الرقمي وحماية ملفات Excel باستخدام واجهة Aspose.Cells Cloud API"
weight: 36
---

## **حماية ملفات Excel وإزالة الحماية عنها**

**ما معنى "الحماية" في Aspose.Cells Cloud؟**  
تُطبّق عملية **الحماية** أماناً لملف Excel عن طريق تطبيق كلمة مرور تمنع فتح الملف أو تعديله أو تعديل هيكله. كما تدعم واجهة برمجة التطبيقات تشفير الملف وإزالة التشفير عنه وإضافة توقيع رقمي لضمان سلامة المحتوى ضد أي تلاعب.

**مرجع واجهة برمجة التطبيقات**  

| طريقة HTTP | نقطة النهاية | المعاملات المطلوبة (استعلام/جسم الطلب) | مثال على جسم الطلب | الاستجابات الشائعة |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (مسار)، `password` (استعلام) | `{ "password": "MySecret123" }` | `200 OK` – تم تطبيق الحماية، `400 Bad Request`، `401 Unauthorized`، `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (مسار)، `password` (استعلام) | N/A | `200 OK` – تم إزالة الحماية، أكواد الأخطاء كما هو مذكور أعلاه |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (مسار)، `password` (استعلام) | N/A | `200 OK` – تم تشفير الملف |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (مسار)، `password` (استعلام) | N/A | `200 OK` – تم فك تشفير الملف |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (مسار) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – تم إضافة التوقيع الرقمي |

**مثال على الكود (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// تهيئة عميل واجهة برمجة التطبيقات
var config = new Configuration
{
    AppSid = "YOUR_APP_SID",
    AppKey = "YOUR_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// حماية المصنف
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**المتطلبات الأساسية**  
- اشتراك نشط في Aspose.Cells Cloud.  
- `AppSid` و`AppKey` للمصادقة.  

**المصادقة**  
يجب أن تتضمّن جميع الطلبات رأس `Authorization` يحتوي على رمز JWT ساري المفعول تم الحصول عليه من نقطة نهاية مصادقة Aspose Cloud.

**معالجة الأخطاء**  
تحقق من رمز حالة HTTP ومن كائن `Error` الذي تُرجعه استجابة الجسم. تشمل الأخطاء الشائعة: كلمة مرور غير صحيحة (`400`)، الملف مفقود (`404`)، وفشل المصادقة (`401`).

**ملاحظات**  
- يمكن استخدام نفس نقطة النهاية لـ **تشفير** أو **فك التشفير** عن طريق تغيير جزء الإجراء (`/encrypt`، `/decrypt`).  
- يتطلّب التوقيع الرقمي ملف شهادة ساري المفعول يكون متوفرًا لواجهة برمجة التطبيقات.

- [تشفير ملف Excel باستخدام واجهة Aspose.Cells Cloud API](/cells/excel-file-encrypt/)
- [حماية ملف Excel باستخدام واجهة Aspose.Cells Cloud API](/cells/protect-excel-file/)
- [إضافة توقيع رقمي لملف Excel](/cells/excel-digital-signature/)
- [حماية ملفات Excel – دليل مفصّل](/cells/protect-excel-files/)
- [تعيين كلمة مرور لملف Excel](/cells/workbook/password/modify/)
- [فك تشفير ملف Excel](/cells/excel-file-decrypt/)
- [إزالة الحماية عن ملف Excel](/cells/excel-file-unprotect/)
- [إلغاء قفل ملفات Excel](/cells/unlock-excel-files/)
- [مسح كلمة مرور ملف Excel](/cells/clear-excel-files-password/)
---