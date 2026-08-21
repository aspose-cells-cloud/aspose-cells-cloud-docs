---
title: "Aspose.Cells Cloud – التحقق من صحة الخدمة (واجهة برمجة تطبيقات)"
second_title: "وثيقة"
ArticleTitle: "فحص صحة خدمة Aspose.Cells Cloud"
linktype: "docs"
url: /check-cloud-service-health/
keywords: "Aspose.Cells Cloud، فحص صحة واجهة برمجة التطبيقات، حالة REST، مراقبة الخدمة السحابية"
description: "راقب صحة خدمة Aspose.Cells Cloud في الزمن الفعلي. تعرّف على نقطة النهاية GET /v4.0/cells/status/check، والمعاملات، وتنسيق الاستجابة، وأمثلة SDK."
weight: 100
---

تحقق من حالة صحة خدمات Aspose.Cells Cloud.

**المتطلبات الأساسية**  
لاستدعاء نقطة النهاية هذه، يجب أن يكون لديك رمز وصول صالح لـ Aspose Cloud. احصل على الرمز من خلال تسجيل تطبيق في لوحة تحكم Aspose Cloud، ثم استخدام client-id وclient-secret لطلب رمز Bearer عبر نقطة نهاية رموز OAuth2. تضمين الرمز في رأس `Authorization` كما هو موضح أدناه.

## **فحص صحة الخدمة السحابية**

### **واجهة برمجة التطبيقات عبر الويب**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب**

| المعامل         | النوع   | الإجباري | الوصف                                                                 |
| --------------- | ------- | -------- | --------------------------------------------------------------------- |
| Authorization   | رأس    | نعم      | رمز Bearer للمصادقة (`Authorization: Bearer <token>`).               |
| detail          | استعلام | لا       | ضبطها على `true` لتضمين معلومات مفصّلة عن المكونات.                   |
| Accept          | رأس    | لا       | تنسيق الاستجابة المطلوب، الافتراضي هو `application/json`.            |

### **الاستجابة**

تُعيد الخدمة حمولة JSON عند نجاح الطلب.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Operational",
    "storage": "Operational",
    "database": "Operational"
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                 | الوصف                                                         |
| ----- | ---------------------- | ------------------------------------------------------------- |
| 200   | OK (نجاح)             | الخدمة صحّية؛ راجع مثال JSON أعلاه.                            |
| 401   | غير مصادَق             | رمز مصادقة غير صالح أو مفقود.                                |
| 503   | الخدمة غير متاحة       | الخدمة غير صحّية حاليًا أو خاضعة للصيانة.                     |
| 4xx   | خطأ من العميل          | معاملات طلب غير صحيحة أو طلب معطّل الصيغة.                    |
| 5xx   | خطأ من الخادم          | فشل غير متوقع في الخادم؛ أعد المحاولة لاحقًا.                 |

## كيفية استخدام واجهة برمجة تطبيقات حالة Aspose.Cells Cloud باستخدام مكتبات SDK

### مواصفات OpenAPI

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات متاحة علنًا وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع التطوير. فالمكتبة SDK تتعامل مع التفاصيل الأساسية، مما يتيح لك تنفيذ فحص صحة خدمة Cells باستخدام كود محدود جدًا.  
يرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

وفيما يلي مقاطع نموذجية توضّح كيفية استدعاء نقطة النهاية الخاصة بفحص الصحة باستخدام أكثر مكتبات SDK شيوعًا.

---