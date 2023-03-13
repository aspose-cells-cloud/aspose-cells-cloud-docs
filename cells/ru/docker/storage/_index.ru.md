---
title: Склад
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/docker/storage/
description: Как установить место хранения около Aspose.Cells Облако для Docker
weight: 30
---
##  Конфигурация хранилища по умолчанию ##

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

##  Положение по умолчанию ##


- **окна**

```powershell

c:\app\storageResource.json

```

- **линукс**

```linux

/app/storageResource.json


```

##  Пользовательская конфигурация хранилища ##

Необходимо повторно указать профиль хранилища для файла облачного образа Aspose.Cells, когда клиенту необходимо указать папку для хранения.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Справочный документ** : 
  - [Докер Бег]( https://docs.docker.com/engine/reference/commandline/run/)