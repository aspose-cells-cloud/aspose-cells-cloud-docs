---
title: دوكي
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells سحابة
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، Docker
---
## Aspose.Cells دوكر السحابي

تتوفر صورة السحابة Aspose.Cells لنظام Linux، وMicrosoft Windows 11 Pro، وMicrosoft Windows Server 2016، وMicrosoft Windows Server 2019، وMicrosoft Windows Server 2022.

## API مرجع - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## منفذ العرض

المنفذ | الوصف | مطلوب
---|:--:|---:
5000 | مجلد يحتوي على الخطوط التي سيتم استخدامها لعرض المستندات | صحيح

##  الأحجام المطلوبة ##

مسار التثبيت في الحاوية | الوصف | مطلوب
---|:--:|---:
C:\fonts | مجلد يحتوي على الخطوط التي سيتم استخدامها لعرض المستندات | خطأ
C:\data | مجلد تخزين الملفات | خطأ

##  معلمات التشغيل ##

الاسم | الوصف | مطلوب
---|:--:|---:
LicensePublicKey | المفتاح العام للترخيص | صحيح
LicensePrivateKey | المفتاح الخاص للترخيص | صحيح
مسار ملف بيانات اعتماد التخزين | مسار ملف تهيئة التخزين. الملف الافتراضي هو ./storageResource.json | صحيح

##  أمر التشغيل ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}

**وثيقة مرجعية** :

- [تشغيل Docker]( https://docs.docker.com/engine/reference/commandline/run/)
-

يرى:

- [معلومات التنزيل](/cells/ar/docker/downloads/)
- [معلومات إصدار التشغيل](/cells/ar//docker/tag-list/)
- [معلومات التخزين](/cells/ar/docker/storage/)
