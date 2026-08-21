---
title: "تقييم Aspose.Cells Cloud"
second_title: "وثيقة"
ArticleTitle: "تقييم Aspose.Cells Cloud"
LinkTitle: "تقييم"
type: docs
url: /ar/evaluate-aspose-cells/
description: "استكشف Aspose.Cells Cloud، وهي واجهة REST API لإنشاء ملفات Excel وتحويلها ودمجها وتقسيمها وحمايتها وتعديلها، بالإضافة إلى تنسيقات الجداول المحسوبة الأخرى."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - تعديل الجداول المحسوبة
  - نسخة تجريبية مجانية
  - تقييم
---

يمكنك تقييم **واجهات Aspose.Cells Cloud REST API** من خلال إنشاء حساب تجريبي مجاني على لوحة تحكم Aspose Cloud. بعد التسجيل، ستتلقى **معرف عميل (Client Id)** و**سر عميل (Client Secret)** تسمح لك بـ 150 استدعاء لواجهة برمجة التطبيقات شهريًا.

**المتطلبات الأساسية**  
قبل البدء، تأكد من امتلاكك اتصال نشط بالإنترنت وبيئة تطوير مدعومة. يمكن استدعاء واجهة برمجة التطبيقات مباشرة عبر بروتوكول HTTP، أو يمكنك استخدام أحد SDKs الخاصة بـ Aspose.Cells (مثل .NET أو Java أو Python أو PHP) لتسهيل التكامل.

**خطوات البدء السريع**

1. **إنشاء حساب تجريبي مجاني** – قم بزيارة [لوحة تحكم Aspose Cloud](https://dashboard.aspose.cloud)، وسجّل حسابك، وتأكيد عنوان بريدك الإلكتروني.  
2. **الحصول على بيانات الاعتماد** – ابحث عن *معرف العميل (Client Id)* و*سر العميل (Client Secret)* في قسم **المصادقة (Authentication)** داخل لوحة التحكم.  
3. **توليد رمز وصول (Access Token)** – أرسل طلب `POST` إلى العنوان `https://api.aspose.cloud/connect/token` مع بيانات اعتمادك (انظر مرجع واجهة برمجة التطبيقات لتفاصيل الضبط الدقيق للطلب).  
4. **إجراء أول استدعاء لواجهة برمجة التطبيقات** – تضمين رمز الوصول في رأس الطلب `Authorization: Bearer <token>` واستدعاء نقطة نهاية بسيطة، مثل `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

توفر النسخة التجريبية لك فرصة عملية لتجربة قدرات الخدمة، مما يسمح لك بالبدء في التطوير والاختبار مبكرًا دون أي تكلفة.

**ملخص مرجع واجهة برمجة التطبيقات**

| العملية | الطريقة | العنوان URL | المعلمات المطلوبة | استجابة مثال |
|---------|--------|-------------|-------------------|--------------|
| الحصول على رمز وصول | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`، `client_id`، `client_secret` (بالصيغة `application/x-www-form-urlencoded`) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| سرد أوراق العمل | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | المسار: `{file}` – اسم ملف المصنف المرفوع؛ الرأس: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

للحصول على تفاصيل حول الأسعار والقيود الاستخدامية وخيارات الخطط الإضافية، راجع صفحة [الخطة التجريبية](https://purchase.aspose.cloud/trial).