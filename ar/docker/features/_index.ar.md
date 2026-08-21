---
title: "الوظائف الأساسية لحاوية Aspose.Cells Cloud Docker: تحويل الجداول الحسابية، دمجها، تقسيمها، حمايتها، معالجة البيانات، والمزيد."
second_title: "وثيقة"
ArticleTitle: "الوظائف الأساسية لحاوية Aspose.Cells Cloud Docker"
linktitle: "الميزات"
type: docs
url: /ar/docker-container-features/
description: "تشغيل واجهة Aspose.Cells Cloud API محليًا باستخدام حاوية Aspose.Cells Cloud Docker — وهي خدمة مُحتَصرة مبنية على Docker وتوفّر معالجة كاملة للجداول الحسابية مع ضمان الخصوصية والقدرة على العمل دون اتصال بالإنترنت دون الاعتماد على السحابة العامة لـ Aspose."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - تحويل الجداول الحسابية
  - معالجة Excel
  - تصدير PDF
  - التعامل مع CSV
  - واجهة REST API
  - خدمة مُحتَصرة
  - سحابة خاصة
  - معالجة دون اتصال بالإنترنت
---

## ما هي حاوية Aspose.Cells Cloud Docker؟

حاوية Aspose.Cells Cloud Docker هي خدمة مُحتَصرة تُقدّمها Aspose وتستند إلى تقنية Docker، وتتيح لك نشر وظائف واجهة Aspose.Cells Cloud API في بيئات محلية أو سحابية خاصة دون الاعتماد على خدمات السحابة العامة لـ Aspose.

## لماذا يجب استخدام حاوية Aspose.Cells Cloud Docker؟

حاوية Aspose.Cells Cloud Docker هي خدمة مُحتَصرة قوية لمعالجة الجداول الحسابية وتُدعم بها ما يلي:

### الميزات الأساسية

- قراءة وكتابة ملفات Excel (XLS و XLSX و CSV و ODS وما إلى ذلك)
- حساب الصيغ، الرسوم البيانية، التنسيق الشرطي، الجداول المحورية، إلخ.
- تحويل التنسيقات (مثل Excel إلى PDF و HTML والصور وما إلى ذلك)
- عمليات الخلايا، إعدادات التنسيق، إدارة أوراق العمل، إلخ.

تحتوي حاوية Aspose.Cells Cloud Docker على هذه الميزات كواجهة RESTful API وتُغلفها في صورة Docker، ما يسمح لك بتشغيلها على البنية التحتية الخاصة بك.

### المزايا الرئيسية

| المزايا                             | الوصف                                                                 |
| ----------------------------------- | --------------------------------------------------------------------- |
| خصوصية البيانات والأمان            | تتم جميع عمليات الملفات داخل شبكتك الخاصة؛ ولا يلزم رفعها إلى سحابة طرف ثالث. |
| التوفّر دون اتصال بالإنترنت        | لا تعتمد على السحابة العامة لـ Aspose، مما يجعلها مناسبة للشبكات الداخلية أو البيئات المعزولة. |
| القابلية للتوسّع                  | قابلة للتوسّع بسهولة عبر Docker/Kubernetes.                         |
| واجهة برمجة تطبيقات موحدة         | متوافقة بالكامل مع واجهة Aspose.Cells Cloud API العامة؛ ولا يلزم إجراء أي تعديلات على الكود. |
| التحكم في الترخيص                  | تدعم نوعين من التفويض؛ واختر ما يناسب وضعك.                          |

## كيفية استخدام حاوية Aspose.Cells Cloud Docker

راجع دليل المستخدم — [كيفية استخدام حاوية Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**المتطلبات المسبقة**

- تثبيت محرك Docker الإصدار 20.10 أو أحدث على الجهاز المضيف.  
- تخصيص 2 جيجابايت كحد أدنى من الذاكرة العشوائية (RAM) ونواتَيْ معالجة (CPU) للحاوية لتشغيل أعباء العمل النموذجية.  
- وجود ملف ترخيص Aspose.Cells Cloud صالح (أو رمز وصول) مُخزّن في دليل سيتم تحميله داخل الحاوية.

**بدء سريع**

1. اسحب صورة Docker: `docker pull aspose/cells-cloud`.  
2. شغّل الحاوية مع تحميل أدلة الترخيص والبيانات، على النحو التالي:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. اتصل بواجهة REST API عبر `http://localhost:8080/v3.0/`. للاطّلاع على استخدام مفصّل لواجهة API، راجع [مرجع واجهة Aspose.Cells Cloud API](https://docs.aspose.cloud/cells/api-reference/).

## الوثائق المرجعية

- [كيفية تكوين تخزين حاوية Aspose.Cells Cloud Docker.](https://docs.aspose.cloud/cells/docker/storage/)
---