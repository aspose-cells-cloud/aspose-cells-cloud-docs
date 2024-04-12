---
title: Склад
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/docker/storage/
description: Как установить место хранения Aspose.Cells Cloud для Docker
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

- **Linux**

```linux

/app/storageResource.json


```

##  Пользовательская конфигурация хранилища ##

Необходимо повторно указать профиль хранения для файла образа облака Aspose.Cells, если клиент указывает папку хранения.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Справочный документ** : 
  - [Докер Запуск]( https://docs.docker.com/engine/reference/commandline/run/)