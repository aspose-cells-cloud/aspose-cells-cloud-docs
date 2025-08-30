---
title: Докке
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Облако
weight: 30
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Облачный докер

Облачный образ Aspose.Cells доступен для Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022.

## API Ссылка - Aspose.Cells Облачный докер

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Выставить порт

Порт | Описание | Обязательно
---|:--:|---:
5000 | Папка со шрифтами, которые будут использоваться для рендеринга документов | true

##  Требуемые объемы ##

Путь монтирования в контейнере | Описание | Обязательно
---|:--:|---:
C:\fonts | Папка со шрифтами, которые будут использоваться для рендеринга документов | false
C:\data | Папка хранения файлов | false

##  Параметры запуска ##

Имя | Описание | Обязательно
---|:--:|---:
LicensePublicKey | Открытый ключ лицензии | true
LicensePrivateKey | Закрытый ключ лицензии | true
storagesCredentialsFilePath | Путь к файлу конфигурации хранилища. Файл по умолчанию: ./storageResource.json | true

##  Выполнить команду ##

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

**Справочный документ** :

- [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)
-

видеть:

- [Информация о загрузке](/cells/ru/docker/downloads/)
- [Информация о версии запуска](/cells/ru//docker/tag-list/)
- [Информация о хранении](/cells/ru/docker/storage/)
