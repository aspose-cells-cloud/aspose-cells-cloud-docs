---
title: كيفية تعيين موضع التخزين لتخزين حاوية Cloud Docker Aspose.Cells
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: تخزين الحاويات
type: docs
url: /ar/docker/storage/
description: كيفية تعيين موضع التخزين لتخزين حاوية Cloud Docker Aspose.Cells
weight: 30
kwords: Excel حاوية Docker السحابية، حاوية Docker ذاتية السحابة، حاوية REST Docker، جدول بيانات، PDF، CSV، JSON، Markdown، صورة Docker، تشغيل حاوية Docker
---
## تكوين التخزين الافتراضي ##

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

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**وثيقة مرجعية** :

- [كيفية تشغيل حاوية Aspose.Cells Cloud Docker.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
