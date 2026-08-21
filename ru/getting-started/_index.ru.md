---
---
title: "Начало работы с Aspose.Cells Cloud API — обработка файлов Excel за 3 простых шага"
second_title: "Документ"
ArticleTitle: "Начало работы с Aspose.Cells Cloud"
linktitle: "Начало работы"
type: docs
url: /ru/getting-started/
description: "Узнайте, как загружать, преобразовывать и скачивать файлы Excel с помощью REST API Aspose.Cells Cloud за три простых шага. Включены примеры кода cURL."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, преобразование электронных таблиц, Excel в PDF, облачная электронная таблица, API Aspose.Cells Cloud"
---

- [Обзор](/cells/overview/)
- [Быстрый старт](/cells/quickstart/)
- [Доступные SDK](/cells/available-sdks/)
- [Поддерживаемые платформы](/cells/supported-platforms/)
- [Поддерживаемые форматы файлов](/cells/supported-file-formats/)
- [Оценка Aspose.Cells Cloud](/cells/evaluate-aspose-cells/)
- [Тарифный план](/cells/pricing-plan/)
- [Техническая поддержка](/cells/technical-support/)
- [Как запустить Docker-контейнер](/cells/how-to-run-docker-container/)

**Руководство по началу работы**

Перед началом работы убедитесь, что у вас есть действующий **API-ключ Aspose Cloud** и **имя хранилища**. Эти учетные данные необходимы для всех последующих вызовов API.

**Шаг 1: Загрузка файла Excel**  
Загрузите исходную рабочую книгу в облачное хранилище Aspose Cloud.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*Тело запроса*: файл отправляется в виде двоичного потока (`application/octet‑stream`).  
*Обязательные параметры*:

- `path` — путь в хранилище, по которому будет сохранен файл (например, `folder/sample.xlsx`).

**Шаг 2: Преобразование рабочей книги в PDF**  
Отправьте запрос на преобразование после загрузки файла.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*Обязательные параметры*:

- `name` — имя загруженной рабочей книги (например, `sample.xlsx`).
- `format` — целевой формат (`pdf`).
- `outputPath` — путь в хранилище для сохранения преобразованного файла (например, `folder/result.pdf`).

*Пример полезной нагрузки ответа* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**Шаг 3: Скачивание преобразованного PDF**  
Получите результирующий PDF из хранилища.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*Обязательные параметры*:

- `outputPath` — путь к PDF, созданному на предыдущем шаге.

**Краткая сводка примеров запросов и ответов**

| Операция | HTTP-метод | Конечная точка (пример) | Параметры | Статус успеха |
|----------|------------|------------------------|-----------|---------------|
| Загрузка | PUT        | /cells/storage/file/{path} | `path` (местоположение в хранилище) | 200 OK |
| Преобразование | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Скачивание | GET        | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Распространенные коды ошибок**

- **400 Bad Request** — отсутствуют или некорректны параметры запроса.  
- **401 Unauthorized** — недействительный или отсутствующий токен доступа.  
- **404 Not Found** — указанный файл или путь не существует.  
- **500 Internal Server Error** — непредвиденная ошибка сервера; повторите попытку или обратитесь в службу поддержки.