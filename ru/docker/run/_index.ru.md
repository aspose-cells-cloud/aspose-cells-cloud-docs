﻿---
title: RU
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/docker/run/
description: Как запустить Aspose.Cells Cloud для Docker
weight: 30
kwords: Excel, Office Облако, REST API, электронная таблица, PDF, CSV, Json, Markdwon, запуск
---
## Открыть порт

Порт | Описание | Необходимый
---|:--:|---:
5000 | Папка со шрифтами, которые будут использоваться для рендеринга документов | истинный


##  Требуемые объемы ##
Путь монтирования в контейнере | Описание | Необходимый
---|:--:|---:
C:\шрифты | Папка со шрифтами, которые будут использоваться для рендеринга документов | ЛОЖЬ
C:\данные | Папка для хранения файлов | ЛОЖЬ

##  Параметры запуска ##

Имя | Описание | Необходимый
---|:--:|---:
ЛицензияPublicKey | Открытый ключ лицензии | истинный
ЛицензияPrivateKey | Закрытый ключ лицензии | истинный
хранилищаCredentialsFilePath | Путь к файлу конфигурации хранилища. Файл по умолчанию: ./storageResource.json | истинный

##  Команда Run ##

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


**Справочный документ** : 
  - [Докер Запуск]( https://docs.docker.com/engine/reference/commandline/run/)
