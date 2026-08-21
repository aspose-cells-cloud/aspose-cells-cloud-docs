---
title: "Как запустить Docker-контейнер Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Как запустить Docker-контейнер Aspose.Cells Cloud"
linktype: "Container Run"
type: docs
url: /ru/run-aspose-cells-cloud-docker-container/
description: "Узнайте, как запустить Aspose.Cells Cloud в Docker-контейнере на Windows Server 2022. Пошаговые команды для пробной версии, оплаты по тарифу «измерение потребления», оплаты по лицензии, настройки хранилища и проверки состояния."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, пробный режим, оплата по измерению потребления, оплата по лицензии, настройка хранилища"
---

Docker-контейнер Aspose.Cells Cloud предоставляет готовый к запуску образ, размещающий API Aspose.Cells Cloud локально или в частном облаке. В данном руководстве описано, как запустить контейнер в трёх распространённых лицензионных режимах — **Пробный**, **Оплата по измерению потребления** и **Оплата по лицензии** — а также приведён пример запуска с использованием токена доступа. Все команды написаны для PowerShell на Windows Server 2022; при использовании Linux адаптируйте пути к томам.

**Предварительные требования**

- Docker Engine 20.10 или более поздней версии установлен и запущен.  
- PowerShell 5.1 или PowerShell 7+.  
- Открыт порт 5000 внутри контейнера (сопоставленный с хост-портом 47900), а также разрешён входящий трафик на порт 47900 в брандмауэре хоста.  
- Для режимов оплаты по измерению потребления или по лицензии подготовьте `LicensePublicKey`, `LicensePrivateKey` или файл лицензии, либо `AccessToken` при использовании режима с токеном.  
- Создайте локальную папку (например, `C:\data`), которая будет использоваться контейнером в качестве хранилища.

**Быстрый старт (пробный режим)**  

Выполните следующую команду, чтобы запустить контейнер в пробном режиме:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Запуск Docker-контейнера Aspose.Cells Cloud в пробном режиме

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Контейнер запускается в интерактивном режиме и прослушивает хост-порт **47900**, который перенаправляется на внутренний порт контейнера **5000**.

## Запуск Docker-контейнера Aspose.Cells Cloud в режиме оплаты по измерению потребления

```powershell
# Windows Server 2022
# Режим оплаты по измерению потребления: задайте LicensePublicKey и LicensePrivateKey как переменные среды.
# Подключите папку хранилища (хост → контейнер)
#   -v c:/data:c:/data
# Подключите папку шрифтов Windows, чтобы API мог получить доступ к системным шрифтам
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=вашLicensePublicKey `
  -e LicensePrivateKey=вашLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Контейнер запускается в отсоединённом режиме (`-d`). После запуска вы можете проверить доступность сервиса:

```powershell
curl http://localhost:47900/v3.0/health
```

**Пример `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Запуск Docker-контейнера Aspose.Cells Cloud в режиме оплаты по лицензии

```powershell
# Windows Server 2022
# Режим оплаты по лицензии: укажите файл лицензии через переменную среды LicenseFile.
# Подключите папку хранилища (хост → контейнер)
#   -v c:/data:c:/data
# Подключите папку шрифтов Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Запуск Docker-контейнера Aspose.Cells Cloud с токеном доступа

```powershell
# Windows Server 2022
# Режим с токеном доступа: задайте AccessToken вместе с необязательными ключами для оплаты по измерению потребления.
# Подключите папку хранилища
#   -v c:/data:c:/data
# Подключите папку шрифтов Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=вашLicensePublicKey `
  -e LicensePrivateKey=вашLicensePrivateKey `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

После запуска контейнера подтвердите работоспособность сервиса той же командой проверки состояния, что использовалась ранее.

## Справочный документ

- [Как настроить хранилище Docker-контейнера Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Устранение неполадок

- **Проверка состояния не удалась** – Убедитесь, что порт 47900 не заблокирован брандмауэром и контейнер запущен (`docker ps`).  
- **Ошибки лицензии** – Убедитесь, что значения `LicensePublicKey`, `LicensePrivateKey` или `LicenseFile` корректны и переменные среды передаются без лишних пробелов.  
- **Хранилище недоступно** – Убедитесь, что папка на хосте (`c:/data`) существует и Docker имеет разрешение на чтение/запись в неё.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Как запустить Docker-контейнер Aspose.Cells Cloud",
  "description": "Пошаговое руководство по запуску Aspose.Cells Cloud в Docker-контейнере на Windows Server 2022, включающее пробный режим, оплату по измерению потребления, оплату по лицензии и режим с токеном доступа.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, пробный режим, оплата по измерению потребления, оплата по лицензии, настройка хранилища"
}
</script>