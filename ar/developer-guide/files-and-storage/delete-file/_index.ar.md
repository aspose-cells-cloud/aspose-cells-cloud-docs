---
title: "Aspose.Cells Cloud – واجهة برمجة تطبيقات حذف الملف"
second_title: "وثيقة"
ArticleTitle: "Aspose.Cells Cloud – واجهة برمجة تطبيقات حذف الملف"
linktitle: "حذف الملف"
type: docs
url: /ar/delete-file/
keywords: "Aspose Cells, واجهة برمجة تطبيقات حذف الملف, تخزين Excel السحابي, واجهة برمجة تطبيقات REST, إدارة الملفات"
description: "احذف ملف Excel من تخزين Aspose.Cells Cloud باستخدام واجهة برمجة تطبيقات حذف الملف التي تعمل عبر REST. يتضمن المسار النهائي (Endpoint)، المعاملات، المصادقة، ونماذج من الكود."
weight: 100
---

تقوم واجهة برمجة التطبيقات **deleteFile** بإزالة الملف المحدد من التخزين السحابي، مما يساعدك على إدارة الموارد والبيانات بكفاءة.

## **واجهة برمجة تطبيقات Excel: حذف الملف**

### واجهة برمجة التطبيقات عبر الويب

```http
DELETE https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                                                                           |
| :---------- | :------ | :----- | :---------------------------------------------------------------------------------------------- |
| `path`      | نص (string) | المسار (Path) | المسار المشفر في عنوان URL للملف الذي يجب حذفه.                                                |
| `storageName` | نص (string) | الاستعلام (Query) | اسم التخزين الذي يوجد فيه الملف. اتركه فارغًا إذا تم استخدام التخزين الافتراضي.                |
| `versionId` | نص (string) | الاستعلام (Query) | مُعرّف إصدار محدد من الملف لحذفه. إذا تم تجاهله، سيتم حذف الإصدار الأحدث.                      |

### وصف الاستجابة

يعيد الطلب الناجح رمز الحالة **HTTP 200** مع جسم استجابة فارغ. لا يتم إرجاع أي حمولة (payload) بصيغة JSON.

```json
{}
```

**رموز حالة HTTP**

| الرمز | المعنى                  | الوصف                                                           |
| ----- | ----------------------- | --------------------------------------------------------------- |
| 200   | ناجح (OK)               | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.    |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).           |
| 401   | غير مصرّح (Unauthorized) | رمز JWT غير صالح أو مفقود.                                      |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                       |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                       |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) واجهة برمجة تطبيقات متاحة للعامة، وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى حزم التطوير إدارة التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة.