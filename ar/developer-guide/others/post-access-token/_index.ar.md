---
title: "واجهة برمجة تطبيقات Aspose.Cells السحابية - نشر رمز الوصول"
second_title: "مستند"
ArticleTitle: "الحصول على رمز الوصول باستخدام مُعرّف العميل والسر"
linktype: "نشر رمز الوصول"
type: docs
url: /ar/post-access-token/
keywords: "Aspose.Cells, السحابة, رمز الوصول, OAuth2, واجهة برمجة التطبيقات, المصادقة, REST, إكسل, السحابة المكتبية"
description: "الحصول على رمز وصول OAuth2 لـ Aspose.Cells Cloud من خلال استدعاء نقطة نهاية POST /cells/connect/token باستخدام مُعرّف العميل والسر الخاص بك."
weight: 100
---

الحصول على رمز وصول باستخدام واجهة برمجة تطبيقات Cells Cloud Get Token مع مُعرّف العميل والسر.

## واجهة برمجة تطبيقات نشر رمز الوصول

قبل استدعاء نقطة النهاية، تأكّد من امتلاك ما يلي:

* حساب مسجّل في Aspose Cloud.  
* **مُعرّف العميل (Client ID)** و**السر (Client Secret)** اللذين تم إنشاؤهما في بوابة Aspose Cloud.  

### واجهة برمجة التطبيقات عبر الويب

```
POST https://api.aspose.cloud/v4.0/cells/connect/token
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| ----------- | ----- | ------ | ----- |
| grant_type | نص (string) | الجسم (مُرمّز كـ form-url-encoded) | القيمة الثابتة `client_credentials` المطلوبة لـ OAuth. |
| client_id | نص (string) | الجسم (مُرمّز كـ form-url-encoded) | المُعرّف الذي تم إصداره لك. |
| client_secret | نص (string) | الجسم (مُرمّز كـ form-url-encoded) | السر المرتبط بمُعرّف العميل. |

**مثال على الطلب (باستخدام cURL)**  

```bash
curl -X POST "https://api.aspose.cloud/v4.0/cells/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET"
```

### الاستجابة

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ------ | ------- | ------ |
| 200 | ناجح (OK) | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب خاطئ (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم البيانات كبير جدًا (Payload Too Large) | ملف مرفوع يتجاوز الحد الأقصى للحجم. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

**مثال على معالجة الأخطاء**

```json
{
  "error": "invalid_client",
  "error_description": "فشل مصادقة العميل."
}
```

## كيفية استخدام واجهة برمجة تطبيقات Get public key باستخدام مكتبات SDK

### مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) واجهة برمجة تطبيقات قابلة للوصول العام، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

يُعد استخدام مكتبة SDK أسرع طريقة للبدء. تُجرّدك المكتبة من تفاصيل HTTP الأساسية، وتتيح لك الحصول على رمز وصول لـ Cells باستخدام كود minimal.

يرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud. وتتولّى مكتبة SDK إدارة التفاصيل منخفضة المستوى، لتتمكن أنت من التركيز على مهام مشروعك.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة: