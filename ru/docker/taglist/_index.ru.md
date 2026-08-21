---
title: "Метки образов Docker Aspose.Cells Cloud"
second_title: "Документ"
ArticleTitle: "Метки образов Docker Aspose.Cells Cloud"
linktitle: "Метки образов"
type: docs
url: /ru/docker/tag-list/
description: "Найдите актуальные метки образов Docker Aspose.Cells Cloud для Windows Server (2016–2022) и Linux. Получите команды загрузки, сведения об архитектуре и примечания по обновлению в одном месте."
weight: 30
keywords:
  - "Метки образов Docker Aspose.Cells Cloud"
  - "Команды docker pull"
  - "Метки Docker для Windows Server"
  - "Метки Docker для Linux"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud предоставляет готовые к запуску образы Docker для Windows Server (2016, 2019, 2022) и Linux.  
Каждый образ снабжается **меткой**, которая однозначно идентифицирует выпуск продукта и целевую операционную систему.  
Используйте указанные ниже метки для загрузки нужного образа, а также обратитесь к примерам загрузки и запуска для быстрого старта.

*Последнее обновление: 2026-07-01*

**Необходимые условия:** Убедитесь, что установлен Docker Engine версии 20.10 или выше, и у вас есть действующий лицензионный ключ Aspose.Cells Cloud. Образы собираются для указанных версий Windows Server или для Linux x64.

## Образы Windows Server 2016 ##

Метки | Архитектура | Dockerfile | Примечание
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile не опубликован — подробности сборки см. в [заметках о выпуске](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016). | Для Windows Server 2016 новые метки не планируются; это последний выпущенный выпуск.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Дополнительные ресурсы: [Загрузка Docker](/cells/docker/downloads/), [Заметки о выпуске](/cells/release-notes/), [Необходимые условия](/cells/docker/prerequisites/).  
Дополнительные сведения см. в разделе [Обзор Docker](/cells/docker/).

## Образы Windows Server 2019 ##

Метки | Архитектура | Dockerfile | Примечание
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile не опубликован — подробности сборки см. в [заметках о выпуске](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019). | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Дополнительные ресурсы: [Загрузка Docker](/cells/docker/downloads/), [Заметки о выпуске](/cells/release-notes/), [Необходимые условия](/cells/docker/prerequisites/).  
Дополнительные сведения см. в разделе [Обзор Docker](/cells/docker/).

## Образы Windows Server 2022 ##

Метки | Архитектура | Dockerfile | Примечание
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile не опубликован — подробности сборки см. в [заметках о выпуске](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022). | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Дополнительные ресурсы: [Загрузка Docker](/cells/docker/downloads/), [Заметки о выпуске](/cells/release-notes/), [Необходимые условия](/cells/docker/prerequisites/).  
Дополнительные сведения см. в разделе [Обзор Docker](/cells/docker/).

## Образы Linux ##

Метки | Архитектура | Dockerfile | Примечание
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile не опубликован — подробности сборки см. в [заметках о выпуске](https://github.com/aspose-cells/dockerfiles/tree/main/linux). | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Дополнительные ресурсы: [Загрузка Docker](/cells/docker/downloads/), [Заметки о выпуске](/cells/release-notes/), [Необходимые условия](/cells/docker/prerequisites/).  
Дополнительные сведения см. в разделе [Обзор Docker](/cells/docker/).

**Журнал изменений версий**

Метка | Изменения
---|---
`ltsc2016.23.5.0` | Последний выпуск для Windows Server 2016; включает исправления безопасности и улучшения производительности.
`ltsc2019.25.10.0` | Обновлено до Aspose.Cells 25.10.0; добавлена поддержка новых формул и исправлены ошибки.
`ltsc2022.25.10.0` | То же, что и метка 2019, оптимизировано для среды выполнения Windows Server 2022.
`linux.25.10.0` | Базовый образ Linux с Aspose.Cells 25.10.0; включает обновленные зависимости и специфические оптимизации для Linux.