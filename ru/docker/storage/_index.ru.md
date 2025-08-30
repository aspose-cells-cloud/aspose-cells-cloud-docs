---
title: Сторэг
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/docker/storage/
description: Как настроить позицию хранилища Aspose.Cells Cloud for Docker
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Хранилище
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

##  Позиция по умолчанию ##


- **окна**

```powershell

c:\app\storageResource.json

```

- **линукс**

```linux

/app/storageResource.json


```

##  Пользовательская конфигурация хранилища ##

Необходимо повторно указать профиль хранения для файла образа облака Aspose.Cells, когда клиенту необходимо указать папку хранения.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Справочный документ** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)
