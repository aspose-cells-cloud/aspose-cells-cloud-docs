---
title: "كيفية تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud"
second_title: "مستند"
ArticleTitle: "كيفية تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud"
linktitle: "تشغيل الحاوية"
type: docs
url: /run-aspose-cells-cloud-docker-container/
description: "تعرّف على كيفية تشغيل Aspose.Cells Cloud داخل حاوية Docker على Windows Server 2022. أوامر خطوة بخطوة لتوضيح طريقة التشغيل في وضع التجربة، أو وضع الفوترة المُقاسة، أو وضع الفوترة بالترخيص، وضبط وحدة التخزين، وفحص الحالة."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, وضع التجربة, الفوترة المُقاسة, الفوترة بالترخيص, إعداد التخزين"
---

تقدم Aspose.Cells Cloud Docker صورة جاهزة للحاوية يمكن تشغيلها محليًا أو في سحابة خاصة لاستضافة واجهة برمجة تطبيقات Aspose.Cells Cloud. يوضح هذا الدليل كيفية تشغيل الحاوية في ثلاثة أوضاع ترخيص شائعة — **التجربة**، **الفوترة المُقاسة**، و**الفوترة بالترخيص** — كما يتضمن إصدارًا يعتمد على رمز وصول (AccessToken). جميع الأوامر مكتوبة لبيئة PowerShell على Windows Server 2022؛ قم بتعديل مسارات وحدات التخزين (volume paths) إذا كنت تستخدم نظام Linux.

**المتطلبات الأساسية**

- Docker Engine إصدار 20.10 أو أحدث مثبت ومُشغَّل.  
- PowerShell 5.1 أو PowerShell 7+.  
- فتح منفذ 5000 داخل الحاوية (ويُربط بالمنفذ 47900 على المضيف) وتأكد من السماح بحركة المرور الواردة على المنفذ 47900 في جدار الحماية الخاص بالمضيف.  
- لوضع الفوترة المُقاسة أو الفوترة بالترخيص، تأكد من توفر `LicensePublicKey` و`LicensePrivateKey` أو ملف الترخيص، أو `AccessToken` إذا كنت تستخدم وضع الرمز.  
- مجلد محلي (مثل `C:\data`) لاستخدامه كوحدة تخزين للحاوية.

**بدء سريع (وضع التجربة)**  

شغّل الأمر التالي لبدء تشغيل الحاوية في وضع التجربة:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud في وضع التجربة

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

تعمل الحاوية في الوضع الأمامي (foreground)، وتستمع على منفذ المضيف **47900**، الذي يُحوّل إلى المنفذ الداخلي **5000** في الحاوية.

## تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud في وضع الفوترة المُقاسة

```powershell
# Windows Server 2022
# وضع الفوترة المُقاسة: ضبط متغيري البيئة LicensePublicKey وLicensePrivateKey.
# ربط مجلد تخزين (من المضيف إلى الحاوية)
#   -v c:/data:c:/data
# ربط مجلد خطوط نظام Windows لتمكين واجهة برمجة التطبيقات من الوصول إلى الخطوط المثبتة على النظام
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

تعمل الحاوية في الوضع المنفصل (`-d`). بعد بدء التشغيل، يمكنك التحقق من جاهزية الخدمة عبر الأمر التالي:

```powershell
curl http://localhost:47900/v3.0/health
```

**مثال على ملف `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud في وضع الفوترة بالترخيص

```powershell
# Windows Server 2022
# وضع الفوترة بالترخيص: تزويد ملف الترخيص عبر متغير البيئة LicenseFile.
# ربط مجلد تخزين (من المضيف إلى الحاوية)
#   -v c:/data:c:/data
# ربط مجلد خطوط نظام Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud باستخدام رمز وصول (AccessToken)

```powershell
# Windows Server 2022
# وضع رمز الوصول: ضبط AccessToken مع مفاتيح الفوترة المُقاسة اختياريًا.
# ربط مجلد تخزين
#   -v c:/data:c:/data
# ربط مجلد خطوط نظام Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=yourLicensePublicKey `
  -e LicensePrivateKey=yourLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

بعد بدء تشغيل الحاوية، تحقق من جاهزية الخدمة باستخدام الأمر نفسه المستخدم لفحص الحالة مسبقًا.

## المستند المرجعي

- [كيفية تكوين وحدة التخزين لحاوية Docker الخاصة بـ Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)

---

### استكشاف الأخطاء وإصلاحها

- **فشل فحص الحالة** – تأكد من أن المنفذ 47900 غير مُحذور بواسطة جدار الحماية، وأن الحاوية قيد التشغيل (`docker ps`).  
- **أخطاء في الترخيص** – تحقق من صحة قيم `LicensePublicKey` و`LicensePrivateKey` أو `LicenseFile`، وتأكد من أن متغيرات البيئة تم تمريرها دون مسافات زائدة.  
- **وحدة التخزين غير قابلة للوصول** – تأكد من وجود المجلد المحلي (`c:/data`)، ومن أن Docker يملك الصلاحيات للقراءة والكتابة فيه.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "كيفية تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud",
  "description": "دليل خطوة بخطوة لتشغيل Aspose.Cells Cloud داخل حاوية Docker على Windows Server 2022، يشمل أوضاع: التجربة، الفوترة المُقاسة، الفوترة بالترخيص، ووضع رمز الوصول.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, وضع التجربة, الفوترة المُقاسة, الفوترة بالترخيص, إعداد التخزين"
}
</script>