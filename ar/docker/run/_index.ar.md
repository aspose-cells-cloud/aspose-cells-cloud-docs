﻿---
title: رو
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/docker/run/
description: كيفية تشغيل Aspose.Cells Cloud for Docker
weight: 30
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، Run
---
## فضح المنفذ

ميناء | الوصف | مطلوب
---|:--:|---:
5000 | مجلد يحتوي على الخطوط، والذي سيتم استخدامه لعرض المستندات | حقيقي


##  الكميات المطلوبة ##
مسار التحميل في الحاوية | الوصف | مطلوب
---|:--:|---:
ج:\الخطوط | مجلد يحتوي على الخطوط، والذي سيتم استخدامه لعرض المستندات | خطأ شنيع
ج:\البيانات | مجلد تخزين الملفات | خطأ شنيع

##  تشغيل المعلمات ##

الاسم | الوصف | مطلوب
---|:--:|---:
مفتاح الترخيص العام | المفتاح العام للرخصة | حقيقي
مفتاح الترخيص الخاص | المفتاح الخاص للرخصة | حقيقي
تخزين بيانات الاعتماد FilePath | مسار ملف تكوين التخزين. الملف الافتراضي هو ./storageResource.json | حقيقي

##  الأمر Run ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}


**وثيقة مرجعية** : 
  - [تشغيل عامل الميناء]( https://docs.docker.com/engine/reference/commandline/run/)
