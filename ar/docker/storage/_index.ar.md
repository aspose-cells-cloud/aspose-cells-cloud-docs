---
title: تخزين
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/docker/storage/
description: كيفية تعيين موضع التخزين حول Aspose.Cells Cloud لـ Docker
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، التخزين
---
##  تكوين التخزين الافتراضي ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}

```

{{< /tab >}}

{{< /tabs >}}

##  الموضع الافتراضي ##


- **النوافذ**

```powershell

c:\app\storageResource.json

```

- **لينكس**

```linux

/app/storageResource.json


```

##  تكوين التخزين المخصص ##

هناك حاجة إلى إعادة تحديد ملف تعريف التخزين لملف صورة السحابة Aspose.Cells عندما يحتاج العميل إلى تحديد مجلد التخزين.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**وثيقة مرجعية** : 
  - [تشغيل Docker]( https://docs.docker.com/engine/reference/commandline/run/)
