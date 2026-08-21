---
title: "واجهة Aspose.Cells Cloud Web API – تعيين / تعديل كلمة مرور فتح لملفات Excel"
second_title: "دليل المطور الشامل"
ArticleTitle: "حماية جداول البيانات – تعيين كلمة مرور الفتح وكلمة مرور التعديل"
linktitle: "الحماية"
type: docs
url: /protection/
keywords: "Aspose.Cells, Cloud, API, Spreadsheet, Protection, Open Password, Read‑Write Password, Excel"
description: "تعرّف على كيفية حماية ملف Excel باستخدام كلمة مرور فتح أو كلمة مرور قراءة/كتابة باستخدام واجهة Aspose.Cells Cloud REST API. يشمل بناء الجملة للطلب، وأمثلة على الأكواد، وإدارة الأخطاء."
weight: 60
---

في هذا الدليل، ستتعلم كيفية تعيين وتعديل وإزالة **كلمة مرور الفتح** و**كلمة مرور القراءة/الكتابة** لجداول البيانات باستخدام واجهة Aspose.Cells Cloud Web API. تُساعدك هذه الميزات في حماية البيانات الحساسة الموجودة في ملفات عمل Excel الخاصة بك.

**المتطلبات المسبقة**  
- حساب نشط على Aspose.Cells Cloud مع مفتاح API وSID ساري المفعول.  
- يجب أن يكون ملف العمل الذي ترغب في حمايته مُحمّلًا على مساحة التخزين في Aspose Cloud أو متاحًا عبر رابط عام.  

**مرجع الواجهة البرمجية (API)**  

| **طريقة HTTP** | **النهاية (Endpoint)** | **المُعلمات (Query / Path)** | **الوصف** |
|----------------|------------------------|------------------------------|------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (مسار) – اسم ملف العمل<br>`openPassword` (استعلام، اختياري) – كلمة المرور المطلوبة لفتح الملف<br>`readWritePassword` (استعلام، اختياري) – كلمة المرور المطلوبة لتعديل الملف | تعيين أو تحديث كلمات مرور الفتح و/أو قراءة/كتابة لملف العمل المحدد. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (مسار) – اسم ملف العمل | إزالة أي كلمات مرور تحمي ملف العمل. |

**مثال على جسم الطلب (JSON)**  

```json
{
  "OpenPassword": "MyOpenPwd123",
  "ReadWritePassword": "MyEditPwd456"
}
```

**مثال على الاستجابة (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "تم تحديث حماية ملف العمل بنجاح."
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|-------|----------------------------|---------------------------------------------|
| 200   | ناجح (OK)                  | تطبيق الحماية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مصرّح (Unauthorized)   | رمز JWT غير صالح أو مفقود. |
| 413   | حجم البيانات كبيرة جدًا (Payload Too Large) | حجم الملف المرفّع يتجاوز الحد المسموح به. |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

**أمثلة على الأكواد**

*C# (SDK لـ Aspose.Cells Cloud)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "MyOpenPwd123",
    readWritePassword: "MyEditPwd456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (SDK لـ Aspose.Cells Cloud)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="MyOpenPwd123",
    read_write_password="MyEditPwd456"
)
api.set_workbook_protection(request)
```

**إدارة الأخطاء**  
عند حدوث خطأ، تُعيد الواجهة البرمجية جسم JSON يحتوي على `Code` و`Message`، وربما `Description`. تحقق من رمز الحالة وتعامل معه وفقًا لمنطق تطبيقك.

**مواضيع ذات صلة**  

- **[كيفية حماية جدول بيانات بكلمة مرور باستخدام Aspose.Cells Cloud](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[كيفية إلغاء حماية جدول بيانات بكلمة مرور باستخدام Aspose.Cells Cloud](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---