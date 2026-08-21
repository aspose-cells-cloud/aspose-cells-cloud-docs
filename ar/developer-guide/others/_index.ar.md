---
title: "Aspise.Cells Cloud Web API – ميزات أخرى: فحص الحالة، الحصول على المفتاح العام"
linktitle: "ميزات أخرى"
ArticleTitle: "ميزات أخرى: فحص الحالة، الحصول على المفتاح العام"
second_title: "مستند"
type: docs
url: /ar/other-features/
keywords: "Aspose.Cells، واجهة ويب سحابية، فحص الحالة، المفتاح العام، رمز الوصول، إكسل، REST"
description: "استكشف ميزات Aspose.Cells Cloud الإضافية: نقطة نهاية فحص الحالة، استرجاع المفاتيح التشفيرية، وإنشاء رموز الوصول لتأمين تكاملاتك مع واجهة إكسل عبر API."
weight: 180
---

**متطلبات مسبقة** – لاستخدام الميزات المذكورة أدناه، يجب أن يكون لديك اشتراك ساري في Aspose Cloud ومفتاح **Client ID** / **Client Secret** نشط للتحقق من الهوية.

توفّر هذه "الميزات الأخرى" عمليات دعم أساسية لواجهة Aspose.Cells Cloud API، مثل التأكد من توفر الخدمة واسترجاع المفاتيح التشفيرية والحصول على رموز الوصول. وتُستدعى عادةً قبل البدء في استخدام نقاط نهاية المرتبطة بأوراق العمل.

- **[فحص حالة الخدمة السحابية لـ Aspose.Cells](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  تأكد من أن خدمة Aspose.Cells Cloud قابلة للوصول تعمل بشكل صحيح. يؤدي الطلب الناجح إلى إرجاع **HTTP 200** مع كائن JSON مثل `{ "status": "OK" }`. استخدم هذه النقطة في بداية سير عملك لتجنب الفشل غير الضروري.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">اقرأ المزيد</a>

- **[الحصول على حالة تشغيل Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  استرجاع الحالة الحالية لتشغيل الخدمة. يُظهر الاستجواب ما إذا كانت الواجهة تعمل بكامل طاقتها، أو في وضع الصيانة، أو تواجه مشاكل.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">اقرأ المزيد</a>

- **[الحصول على المفتاح العام](https://docs.aspose.cloud/cells/get-public-key/)**  
  احصل على المفتاح العام RSA (بصيغة PEM) المستخدم للتحقق من صحة رموز JWT الصادرة من Aspose.Cells Cloud. هذا المفتاح مطلوب عند التحقق من صحة الرموز من جانب الخادم الخاص بك.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">اقرأ المزيد</a>

- **[الحصول على رمز الوصول باستخدام Client ID وClient Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  أنشئ رمز الوصول OAuth 2.0 باستخدام نوع منح **client_credentials**. ضع **Client ID** و**Client Secret** في جسم الطلب؛ ويتضمّن الاستجواب الحقول `access_token` و`token_type` و`expires_in`. ويجب تضمين هذا الرمز في رأس `Authorization` لجميع الاستدعاءات اللاحقة للواجهة.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">اقرأ المزيد</a>

---