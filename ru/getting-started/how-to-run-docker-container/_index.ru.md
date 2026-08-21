---
title: "Запуск контейнера Aspose.Cells Cloud Docker — извлечение, настройка и запуск"
second_title: "Документ"
ArticleTitle: "Как запустить контейнер Aspose.Cells Cloud Docker"
LinkTitle: "Контейнер Docker"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "Узнайте, как извлечь, настроить и запустить контейнер Aspose.Cells Cloud Docker в Windows или Linux. Включает YAML-файл Docker‑Compose, настройку лицензии, сопоставление портов и советы по устранению неполадок."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker-контейнер"
  - "Docker Compose"
  - "ключ лицензии"
  - "Excel"
  - "электронная таблица"
  - "облачный API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Технология Docker предназначена для автоматизации развёртывания приложений с использованием лёгких контейнеров. Разработчики могут использовать Docker-контейнер для упаковки приложения со всеми его библиотеками и зависимостями и развернуть всё как единый пакет.

Команда Aspose.Cells Cloud опубликовала Docker-контейнер на <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a>, чтобы облегчить его использование пользователям Docker.

**Предварительные требования** — убедитесь, что установлен Docker Engine ≥ 20.x, и что ваша операционная система (Windows 10/Server 2019/2022 или поддерживаемый дистрибутив Linux) соответствует требованиям. Дополнительно можно указать ключ лицензии для запуска в лицензионном режиме.

- Docker Engine ≥ 20.x установлен  
- Поддерживаемая ОС (Windows 10/Server 2019/2022 или дистрибутив Linux)  
- Дополнительно: ключ лицензии для лицензионного режима  

## Настройка контейнера

### Обязательные тома

| Путь монтирования в контейнере | Описание |
| :--- | :--- |
| C:\fonts | Папка с шрифтами, которые будут использоваться при рендеринге документов |
| C:\data | Папка для хранения файлов |

**Альтернатива для Linux/macOS** — используйте `/fonts` и `/data` внутри контейнера и сопоставьте их с каталогами на хосте, например `/home/user/fonts` и `/home/user/data`, при запуске контейнера.

### Параметры

| Имя | Описание |
| :--- | :--- |
| LicensePublicKey | Публичный ключ лицензии |
| LicensePrivateKey | Приватный ключ лицензии |

Если параметры **License** опущены, приложение запускается в пробном режиме.

### 1. Извлечение образа Aspose.Cells Cloud

```bash
# Извлечь конкретную версию образа Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Извлечь образ Aspose.Cells Cloud для Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Извлечь образ Aspose.Cells Cloud для Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Извлечь образ Aspose.Cells Cloud для Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Примечание:** Чтобы всегда получить последнюю версию, вы также можете извлечь тег `latest`: `docker pull aspose/cells-cloud:latest`.

### 2. Конфигурация с использованием инструмента Docker‑Compose

Вы можете записать следующую конфигурацию в файл **docker‑compose.yml**:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # хост 5000 → контейнер 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **Примечание:** Сопоставление портов `5000:80` означает, что API будет доступен по адресу `http://localhost:5000`.

### 3. Запуск Docker-контейнера через командную строку

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Устранение неполадок:**  
- **Конфликт портов:** Убедитесь, что порт 5000 на хосте свободен, либо измените сопоставление на свободный порт.  
- **Ошибка загрузки лицензии:** Проверьте, что публичный и приватный ключи корректно переданы как переменные окружения или смонтированы как файлы.  
- **Отсутствующие шрифты:** Если документы рендерятся с неправильными шрифтами, убедитесь, что каталог шрифтов смонтирован корректно и содержит необходимые файлы шрифтов.

**См. также:**  
- <a href="/cells/api/">Справочник по API</a> | <a href="/cells/license/">Руководство по активации лицензии</a> | <a href="/cells/getting-started/">Обзор начала работы</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Извлечь Docker-образ",
      "text": "Выполните `docker pull aspose/cells-cloud:<version>` для загрузки требуемого образа."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "Создать файл docker‑compose",
      "text": "Определите образ, порты, тома и переменные окружения лицензии в файле `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Запустить контейнер",
      "text": "Выполните `docker run` с соответствующими переменными окружения, монтированием томов и сопоставлением портов."
    }
  ]
}
```