---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – الحصول على قائمة الملفات (محتويات المجلد)"
description: "استرجاع قائمة الملفات والمجلدات الفرعية من مجلد معيّن في تخزين Aspose.Cells Cloud."
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

تُعيد عملية **الحصول على قائمة الملفات** مجموعة الملفات والمجلدات الفرعية المخزَّنة في مجلد معيّن ضمن تخزين Aspose.Cells Cloud.  
وهي نقطة الدخول الرئيسية لتصفح كتب عمل Excel المخزَّنة في السحابة، والملفات المؤرشفة، وأنواع الملفات الأخرى المدعومة.

## واجهة برمجة تطبيقات Aspose.Cells Cloud – الحصول على قائمة الملفات (محتويات المجلد)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **الأمان والمصادقة**

تتميّز واجهات برمجة تطبيقات Aspose.Cells Cloud بالأمان وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| الاسم              | الموقع   | النوع      | الإلزام | الوصف                                                                      |
| ------------------ | -------- | ---------- | ------ | --------------------------------------------------------------------------- |
| **path**           | المسار   | سلسلة نصية | نعم    | مسار المجلد في التخزين السحابي.                                             |
| **storageName**    | الاستعلام | سلسلة نصية | لا      | اسم التخزين المراد استخدامه. إذا تُرك فارغًا، يُستخدم التخزين الافتراضي.     |
| **pageSize**       | الاستعلام | عدد صحيح   | لا      | الحد الأقصى لعدد العناصر المراد إعادتها لكل صفحة (الافتراضي: 100).          |
| **pageNumber**     | الاستعلام | عدد صحيح   | لا      | رقم الصفحة المراد استرجاعها (يبدأ من 1، الافتراضي: 1).                      |

- **Value** – مصفوفة من كائنات `StorageFile`. يحتوي كل كائن على:
  - `Name` – اسم الملف أو المجلد.
  - `IsFolder` – `true` إذا كان العنصر مجلدًا.
  - `Size` – الحجم بالبايت (تُبلّغ المجلدات بالقيمة `0`).
  - `ModifiedDate` – طابع الوقت الأخير للتعديل (بصيغة ISO 8601).

### **الاستجابة**

**رموز حالة HTTP**

| رمز HTTP | حالة HTTP            | الوصف                                                                   |
|---------|----------------------|--------------------------------------------------------------------------|
| 200     | ناجح (OK)            | تم استدعاء واجهة برمجة التطبيقات بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400     | طلب خاطئ (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                     |
| 401     | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود.                                              |
| 413     | حجم الحمولة كبير جدًا (Payload Too Large) | ملف مُحمّل يتجاوز الحد الأقصى للحجم.                                     |
| 500     | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                                 |
|         |                      |                                                                          |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDKs أفضل طريقة لتسريع عملية التطوير. فالـ SDK يُدير التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات ويب Aspose.Cells باستخدام SDKs متنوعة: