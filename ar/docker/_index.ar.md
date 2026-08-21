---
title: "دليل تشغيل Aspose.Cells Cloud عبر Docker: استضافة تطبيق Aspose.Cells Cloud على بنية تحتية خاصة بك."
second_title: "وثيقة"
ArticleTitle: "دليل تشغيل Aspose.Cells Cloud عبر Docker"
linktitle: "Docker"
type: docs
url: /ar/docker-developer-guide/
aliases: [  /ar/docker/ , /ar/docker/run/ ]
description: "نشر Aspose.Cells Cloud كحاوية Docker على بنية تحتية خاصة أو داخلية، مما يمكّن من معالجة جداول البيانات (Excel وPDF وCSV وJSON وMarkdown) دون استخدام السحابة العامة الخاصة بـ Aspose."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "صورة Docker",
    "واجهة برمجة تطبيقات جداول البيانات",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "سحابة خاصة",
    "النشر",
  ]
weight: 30
---

Aspose.Cells Cloud هي خدمة معالجة جداول بيانات مبنية على السحابة، وتدعم إنشاء وتعديل وتحويل وتشغيل ملفات بصيغ مثل Excel. ويمكن إعدادها بسرعة كبيئة خدمة مستقلة عبر نشر Docker، مما يبسّط إدارة التبعيات وعمليات النشر عبر أنظمة التشغيل المختلفة.

يوفر هذا الدليل مقدمة مفصلة لخطوات التشغيل الكاملة — بدءًا من تحضير البيئة وصولًا إلى التحقق من الخدمة.

## تحضير البيئة

قبل نشر حاوية Aspose.Cells Cloud عبر Docker، تأكّد من استيفاء متطلبات التبعيات التالية لتجنب فشل النشر بسبب مكونات ناقصة.

### مكونات التبعيات الأساسية

- **Docker Engine:** المحرك الأساسي لوقت تشغيل الحاويات، ومسؤول عن إنشاء وإدارة الحاويات. الحد الأدنى المطلوب لإصداره هو **18.09.0**.
- **أنظمة التشغيل:** أنظمة التشغيل الشائعة التي تدعم Docker:

  | نوع نظام التشغيل | الإصدار                     |
  | :---------------- | :-------------------------- |
  | Windows           | Windows 10/11               |
  | Windows Server    | 2016 / 2019 / 2022          |
  | Linux             | CentOS 7+ / Ubuntu 20.04+   |

- **المصادر المادية:** تأكّد من توفر موارد كافية لتشغيل الخدمة بسلاسة لتجنّب الأعطال الناتجة عن نقص الموارد:
  - المعالج (CPU): 2 نواتج أو أكثر.
  - الذاكرة العشوائية (RAM): 4 جيجابايت أو أكثر.
  - مساحة التخزين: 10 جيجابايت فارغة على الأقل.

### الشروط الأساسية الجوهرية

- **رخصة Aspose:** سجّل حسابًا رسميًا لدى Aspose للحصول على رخصة صالحة (يمكنك طلب نسخة تجريبية أو شراء نسخة تجارية). وبدون رخصة، قد تُقيَّد وظائف الخدمة. يُرجى الرجوع إلى صفحة [الرخص](https://purchase.aspose.com/buy) لمزيد من التفاصيل.
- **اتصال بالشبكة:** تأكّد من قدرة بيئة النشر على الوصول إلى Docker Hub (لجلب الصور).

## الحصول على صورة Aspose.Cells Cloud عبر Docker

تُخزَّن صورة Aspose.Cells Cloud على Docker Hub، ويمكن جلبها مباشرة باستخدام الأمر `docker pull`، دون الحاجة إلى بنائها يدويًا.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## تشغيل حاوية Aspose.Cells Cloud عبر Docker

### معاملات التشغيل

| الاسم                         | الوصف                                                                 | الملاحظات                                                   |
| ----------------------------- | --------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey             | تعيين المفتاح العام للرخصة عند استخدام نمط الفوترة حسب الاستخدام (Metered). | يعمل فقط عند تفعيل نمط الفوترة حسب الاستخدام (Metered).     |
| LicensePrivateKey            | تعيين المفتاح الخاص للرخصة عند استخدام نمط الفوترة حسب الاستخدام (Metered). | يعمل فقط عند تفعيل نمط الفوترة حسب الاستخدام (Metered).     |
| storagesCredentialsFilePath  | مسار ملف إعدادات التخزين. الملف الافتراضي هو `./storageResource.json`. |                                                             |
| LicenseFile                  | تعيين ملف الرخصة عند استخدام نمط الفوترة عبر ملف الرخصة (LicenseFile). | يعمل فقط عند تفعيل نمط الفوترة عبر ملف الرخصة (LicenseFile). |
| AccessToken                  | الرمز المميّز للوصول إلى واجهة برمجة التطبيقات (API).               | إن كان فارغًا، فلا تُطلَب مصادقة بالرمز المميّز.             |

### أمر التشغيل

يمكن تشغيل الحاوية في الوضع التجريبي بهذه البساطة:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

ولتشغيل مزوّد بميزات كاملة، احصل على [رخصة Metered](https://purchase.aspose.com/faqs/licensing/metered/)، وركّب مجلدًا من المضيف لتخزين الملفات. سيبدو أمر التشغيل كالتالي في هذه الحالة:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### مرجع واجهة برمجة التطبيقات – Aspose.Cells Cloud عبر Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### منفذ العرض

| المنفذ | الوصف                                        | مطلوب |
| ------ | --------------------------------------------- | ------ |
| 5000   | المجلد الذي يحتوي على الخطوط المستخدمة لعرض المستندات | نعم    |

### الأحجام المطلوبة

| مسار التحميل داخل الحاوية | الوصف                                        | مطلوب | الملاحظة                                                      |
| -------------------------- | --------------------------------------------- | ------ | -------------------------------------------------------------- |
| C:\fonts                   | المجلد الذي يحتوي على الخطوط المستخدمة لعرض المستندات | لا      | يحل مشاكل جداول البيانات/Excel الناتجة عن نقص الخطوط.          |
| C:\data                    | مجلد تخزين الملفات                           | لا      | يزيد مساحة التخزين لتسهيل إدارة الملفات والوصول إليها.        |

## الوثائق المرجعية

- [الميزات الأساسية لحاوية Aspose.Cells Cloud عبر Docker](https://docs.aspose.cloud/cells/docker-container-features/)
- [كيفية تكوين تخزين حاوية Aspose.Cells Cloud عبر Docker](https://docs.aspose.cloud/cells/docker/storage/)
- [كيفية تشغيل حاوية Aspose.Cells Cloud عبر Docker](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)