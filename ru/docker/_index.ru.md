---
title: "Руководство по эксплуатации Aspose.Cells Cloud Docker: размещение приложения Aspose.Cells Cloud в собственной частной инфраструктуре"
second_title: "Документ"
ArticleTitle: "Руководство по эксплуатации Aspose.Cells Cloud Docker"
linktitle: "Docker"
type: docs
url: /docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: "Развертывание Aspose.Cells Cloud в виде Docker-контейнера в частной или локальной инфраструктуре, позволяющее обрабатывать электронные таблицы (Excel, PDF, CSV, JSON, Markdown) без использования общественного облака Aspose."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker-образ",
    "API для электронных таблиц",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Частное облако",
    "Развертывание",
  ]
weight: 30
---

Aspose.Cells Cloud — это облачная служба обработки электронных таблиц, поддерживающая создание, редактирование, преобразование и манипуляции с файлами в форматах, таких как Excel. Её можно быстро настроить как автономную сервисную среду с помощью развертывания через Docker, что упрощает управление зависимостями и кроссплатформенное развертывание.

В данном руководстве подробно описаны все шаги по эксплуатации — от подготовки среды до проверки работоспособности сервиса.

## Подготовка среды

Перед развертыванием контейнера Aspose.Cells Cloud Docker убедитесь, что локальная среда удовлетворяет следующим требованиям к зависимостям, чтобы избежать ошибок развертывания из-за отсутствующих компонентов.

### Основные компоненты зависимостей

- **Docker Engine:** основной движок среды выполнения контейнеров, отвечающий за создание и управление контейнерами. Минимальная требуемая версия — **18.09.0**.
- **Операционные системы:** основные операционные системы, поддерживающие Docker:

  | Тип операционной системы | Версия                     |
  | :----------------------- | :------------------------- |
  | Windows                  | Windows 10/11              |
  | Windows Server           | 2016 / 2019 / 2022         |
  | Linux                    | CentOS 7+ / Ubuntu 20.04+  |

- **Аппаратные ресурсы:** обеспечьте достаточные ресурсы для стабильной работы сервиса и избегайте сбоев из-за нехватки ресурсов:
  - CPU: 2 ядра и более.
  - Память: 4 ГБ и более.
  - Диск: не менее 10 ГБ свободного места.

### Ключевые предпосылки

- **Лицензия Aspose:** зарегистрируйтесь в учетной записи Aspose, чтобы получить действительную лицензию (можно申请ить пробную версию или приобрести коммерческую). Без лицензии функциональность сервиса может быть ограничена. Подробности см. на странице [Лицензирование](https://purchase.aspose.com/buy).
- **Подключение к сети:** убедитесь, что среда развертывания может получить доступ к Docker Hub (для загрузки образов).

## Получение образа Aspose.Cells Cloud Docker

Образ Aspose.Cells Cloud размещён на Docker Hub и может быть загружен напрямую с помощью команды `docker pull`, без необходимости самостоятельной сборки.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Запуск контейнера Aspose.Cells Cloud Docker

### Параметры запуска

| Имя                         | Описание                                                                 | Примечание                                                  |
| --------------------------- | ------------------------------------------------------------------------ | ----------------------------------------------------------- |
| LicensePublicKey            | Установка открытого ключа лицензии при использовании тарифного плана «Metered». | Действует только при использовании тарифного плана «Metered». |
| LicensePrivateKey           | Установка закрытого ключа лицензии при использовании тарифного плана «Metered». | Действует только при использовании тарифного плана «Metered». |
| storagesCredentialsFilePath | Путь к файлу конфигурации хранилища. Файл по умолчанию: `./storageResource.json`. |                                                             |
| LicenseFile                 | Указание файла лицензии при использовании тарифного плана «LicenseFile». | Действует только при использовании тарифного плана «LicenseFile». |
| AccessToken                 | Токен для доступа к API.                                                 | Если пусто, проверка токена не требуется.                   |

### Команда запуска

Запуск контейнера в пробном режиме осуществляется просто:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Для полнофункционального запуска получите [лицензию по тарифному плану «Metered»](https://purchase.aspose.com/faqs/licensing/metered/) и подключите папку хоста для хранения файлов. Пример команды запуска в этом случае:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### Ссылка на API — Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Открытые порты

| Порт | Описание                                    | Обязательный |
| ---- | ------------------------------------------- | ------------ |
| 5000 | Папка со шрифтами, используемыми для рендеринга документов | да           |

### Обязательные тома

| Путь монтирования в контейнере | Описание                                    | Обязательный | Примечание                                               |
| ----------------------------- | ------------------------------------------- | ------------ | -------------------------------------------------------- |
| C:\fonts                      | Папка со шрифтами, используемыми для рендеринга документов | нет          | Устраняет проблемы с электронными таблицами/Excel, вызванные отсутствием шрифтов. |
| C:\data                       | Папка хранения файлов                       | нет          | Увеличивает объём хранилища для удобного управления и доступа к файлам. |

## Справочная документация

- [Основные функции контейнера Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker-container-features/)
- [Настройка хранилища контейнера Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker/storage/)
- [Запуск контейнера Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)