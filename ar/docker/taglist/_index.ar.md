---
title: "وسوم صور Docker الخاصة بـ Aspose.Cells Cloud"
second_title: "مستند"
ArticleTitle: "وسوم صور Docker الخاصة بـ Aspose.Cells Cloud"
linktitle: "وسوم الصور"
type: docs
url: /docker/tag-list/
description: "اعثر على أحدث وسوم صور Docker الخاصة بـ Aspose.Cells Cloud لخوادم Windows Server (2016-2022) وLinux. احصل على أوامر sPull وتفاصيل البنية المعمارية وملاحظات الترقية في مكان واحد."
weight: 30
keywords:
  - "وسوم صور Docker الخاصة بـ Aspose.Cells Cloud"
  - "أوامر docker pull"
  - "وسوم Docker لخوادم Windows Server"
  - "وسوم Docker لـ Linux"
  - "Aspose.Cells Cloud"
---

تقدم Aspose.Cells Cloud صور Docker جاهزة للتشغيل لخوادم Windows Server (2016 و2019 و2022) وLinux.  
كل صورة تحمل **وسمًا (tag)** يُعرّف إصدار المنتج ونظام التشغيل المستهدف.  
استخدم الوسوم أدناه لسحب الصورة المطلوبة بالضبط، وراجع الأمثلة المرافقة لسحب الصورة وتشغيلها للبدء السريع.

*آخر تحديث: 2026-07-01*

**المتطلبات المسبقة:** تأكد من تثبيت محرك Docker الإصدار 20.10 أو أحدث، وامتلاك مفتاح ترخيص صالح لـ Aspose.Cells Cloud. تم بناء الصور لتعمل على إصدارات Windows Server المحددة أو على Linux x64.

## صور خوادم Windows Server 2016 ##

الوسوم | البنية المعمارية | ملف Dockerfile | ملاحظات
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | ملف Dockerfile غير منشور – راجع [ملاحظات الإصدار](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) للحصول على تفاصيل البناء. | لن يُصدر وسم جديد لاحقًا لخادم Windows Server 2016؛ هذه هي النسخة النهائية المُطلَقة.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

موارد إضافية: [تنزيل Docker](/cells/docker/downloads/)، [ملاحظات الإصدار](/cells/release-notes/)، [المتطلبات المسبقة](/cells/docker/prerequisites/).  
راجع [نظرة عامة على Docker](/cells/docker/) لمزيد من التفاصيل.

## صور خوادم Windows Server 2019 ##

الوسوم | البنية المعمارية | ملف Dockerfile | ملاحظات
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | ملف Dockerfile غير منشور – راجع [ملاحظات الإصدار](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) للحصول على تفاصيل البناء. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

موارد إضافية: [تنزيل Docker](/cells/docker/downloads/)، [ملاحظات الإصدار](/cells/release-notes/)، [المتطلبات المسبقة](/cells/docker/prerequisites/).  
راجع [نظرة عامة على Docker](/cells/docker/) لمزيد من التفاصيل.

## صور خوادم Windows Server 2022 ##

الوسوم | البنية المعمارية | ملف Dockerfile | ملاحظات
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | ملف Dockerfile غير منشور – راجع [ملاحظات الإصدار](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) للحصول على تفاصيل البناء. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

موارد إضافية: [تنزيل Docker](/cells/docker/downloads/)، [ملاحظات الإصدار](/cells/release-notes/)، [المتطلبات المسبقة](/cells/docker/prerequisites/).  
راجع [نظرة عامة على Docker](/cells/docker/) لمزيد من التفاصيل.

## صور Linux ##

الوسوم | البنية المعمارية | ملف Dockerfile | ملاحظات
---|---|---|---
✅ `linux.25.10.0` | x64 | ملف Dockerfile غير منشور – راجع [ملاحظات الإصدار](https://github.com/aspose-cells/dockerfiles/tree/main/linux) للحصول على تفاصيل البناء. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

موارد إضافية: [تنزيل Docker](/cells/docker/downloads/)، [ملاحظات الإصدار](/cells/release-notes/)، [المتطلبات المسبقة](/cells/docker/prerequisites/).  
راجع [نظرة عامة على Docker](/cells/docker/) لمزيد من التفاصيل.

**سجل تغييرات الإصدارات**

الوسم | التغييرات
---|---
`ltsc2016.23.5.0` | الإصدار النهائي لخادم Windows Server 2016؛ يشمل تصحيحات الأمان وتحسينات الأداء.
`ltsc2019.25.10.0` | تم التحديث إلى Aspose.Cells 25.10.0؛ يضيف دعمًا جديدًا للصيغ وإصلاحات للأخطاء.
`ltsc2022.25.10.0` | مطابق للوسم الخاص بـ 2019، مع تحسينات لبيئة تشغيل خادم Windows Server 2022.
`linux.25.10.0` | صورة Linux الأساسية مع Aspose.Cells 25.10.0؛ يشمل تبعيات مُحدّثة وتحسينات خاصة بـ Linux.