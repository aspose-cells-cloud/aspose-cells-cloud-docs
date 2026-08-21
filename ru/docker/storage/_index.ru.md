---
---
title: "Как настроить положение хранилища для контейнера Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Настройка хранилища контейнера Aspose.Cells Cloud"
linktitle: "Хранилище контейнера"
type: docs
url: /docker/storage/ru/
description: "Настройка расположения хранилища для контейнеров Aspose.Cells Cloud с использованием JSON, PowerShell или Bash."
weight: 30
keywords: "Aspose.Cells, Docker, хранилище контейнера, конфигурация JSON, PowerShell, Bash"
---

**Краткое описание**: В данном руководстве показано, как настроить расположение хранилища для контейнеров Aspose.Cells Cloud на Windows и Linux с использованием файлов конфигурации JSON и команд Docker run.

## Конфигурация хранилища по умолчанию ##

**Необходимые условия**: Убедитесь, что установлен Docker Engine версии 20.10 или выше, у вас есть действующие ключи лицензии Aspose.Cells Cloud (`LicensePublicKey` и `LicensePrivateKey`), а также целевая папка хоста, которую вы планируете использовать в качестве хранилища (например, `c:/data` в Windows или `/data` в Linux), существует и имеет соответствующие права доступа.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
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

```json
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

## Расположение по умолчанию ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Настраиваемая конфигурация хранилища ##

Укажите пользовательский профиль хранилища, если необходимо использовать другую папку для данных Aspose.Cells Cloud.

```bash
docker run -d \
  -v c:/data:c:/data \   # монтирование папки хоста в качестве хранилища контейнера
  -p 47900:5000 \        # проброс порта API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Пример для Linux*:

```bash
docker run -d \
  -v /data:/data \   # монтирование папки хоста в качестве хранилища контейнера
  -p 47900:5000 \    # проброс порта API
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Справочный документ**:

- [Как запустить контейнер Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Функции контейнера Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [Загрузка образа Docker Aspose.Cells Cloud](https://docs.aspose.cloud/cells/docker/download-image/)
- [Управление тегами контейнера](https://docs.aspose.cloud/cells/docker/manage-tags/)