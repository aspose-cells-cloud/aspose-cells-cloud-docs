---
title: رو
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/docker/run/
description: كيفية تشغيل Aspose.Cells Cloud for Docker
weight: 30
---
## كشف الميناء

المنفذ | الوصف | مطلوب
---|:--:|---:
5000 | مجلد مع الخطوط ، والذي سيتم استخدامه لتقديم المستندات | حقيقي


##  الأحجام المطلوبة ##
مسار التركيب في الحاوية | الوصف | مطلوب
---|:--:|---:
ج: \ الخطوط | مجلد مع الخطوط ، والذي سيتم استخدامه لتقديم المستندات | خطأ شنيع
ج: \ بيانات | مجلد تخزين الملفات | خطأ شنيع

##  تشغيل المعلمات ##

الاسم | الوصف | مطلوب
---|:--:|---:
LicensePublicKey | المفتاح العام للترخيص | حقيقي
مفتاح الترخيص الخاص | المفتاح الخاص للترخيص | حقيقي
storagesCredentialsFilePath | تخزين تكوين مسار الملف. الملف الافتراضي هو ./storageResource.json | حقيقي

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
  - [تشغيل عامل ميناء]( https://docs.docker.com/engine/reference/commandline/run/)