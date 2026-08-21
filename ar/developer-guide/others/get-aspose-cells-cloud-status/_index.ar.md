---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب - الحصول على حالة خدمة Aspose Cells Cloud"
second_title: "مستند"
ArticleTitle: "الحصول على حالة خدمة Aspose.Cells Cloud"
linktitle: "الحصول على حالة خدمة Aspose.Cells Cloud"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات السحابة، فحص الصحة، Excel، REST"
description: "مراقبة حالة صحة خدمة Aspose.Cells Cloud في الوقت الفعلي."
weight: 100
---

احصل على حالة صحة خدمة Aspose.Cells Cloud في الوقت الفعلي.

**المتطلبات المسبقة:** لاستدعاء هذه الواجهة البرمجية، يجب عليك الحصول على رمز وصول من نوع Bearer باستخدام بيانات اعتماد عميل Aspose Cloud الخاص بك. وأضف هذا الرمز في رأس الطلب `Authorization` على النحو التالي: `Bearer {access_token}`.

## **الحصول على حالة خدمة Aspose.Cells Cloud**

### **واجهة برمجة التطبيقات عبر الويب**

تستخدم هذه النقطة النهائية طريقة HTTP **GET** ولا تتطلب وجود محتوى في جسم الطلب.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|------------|-------|-------------------------------------|--------|
| Authorization | نص | الرأس | رمز Bearer للمصادقة (مطلوبة). |
| format | نص | سلسلة الاستعلام | تنسيق الاستجابة المطلوب، مثل `json`. |

### **الاستجابة**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**مخطط الاستجابة**

| الحقل | النوع | الوصف |
|-------|--------|--------|
| status | نص | حالة صحة الخدمة (`OK`، `Degraded`، إلخ). |
| service | نص | اسم الخدمة. |
| timestamp | نص (ISO‑8601) | وقت إجراء فحص الحالة. |

تعيد الواجهة البرمجية حمولة JSON قياسية تتضمن **حالة** صحة خدمة Aspose.Cells Cloud الحالية.

**رموز حالة HTTP**

- **200 OK** – الخدمة سليمة وتتضمن الاستجابة معلومات الحالة.
- **401 Unauthorized** – نقص رمز المصادقة أو عدم صحته.
- **503 Service Unavailable** – الخدمة متوقفة حاليًا للصيانة أو تواجه مشكلات.

## كيفية استخدام واجهة برمجة تطبيقات الحصول على حالة خدمة Aspose.Cells Cloud باستخدام مكتبات SDK

### **مواصفات OpenAPI**

تعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) واجهة برمجة تطبيقات قابلة للوصول من خارج النظام، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

### **استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud**

استخدام مكتبة SDK يبسّط عملية الدمج ويقلل من كمية الشيفرة النمطية (Boilerplate code). فالمكتبة تتعامل مع التفاصيل الأساسية تلقائيًا، مما يسمح لك باسترجاع حالة تشغيل خدمة Aspose.Cells Cloud بجهد محدود. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.