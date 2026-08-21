---
title: "Работа с изображениями в Excel"
second_title: "Документ"
linktype: "Изображения"
type: docs
url: /ru/pictures/
aliases: [  /ru/working-with-pictures/ ]
keywords: "Excel, изображение, Aspose.Cells Cloud, REST API, обработка изображений, изображения Excel"
description: "Узнайте, как извлекать, добавлять, обновлять и удалять изображения в рабочих листах Excel с помощью REST API Aspose.Cells Cloud. Включены примеры кода на C#, Java, Python и других языках."
weight: 100
ArticleTitle: "Работа с изображениями в Excel – Документация Aspose.Cells Cloud"
---

## Работа с изображениями в файле Excel

В этом руководстве описано, как работать с **изображениями** (также называемыми рисунками) в рабочих листах Excel через REST API Aspose.Cells Cloud. В нём рассматриваются основные операции, связанные с изображениями — извлечение, добавление, обновление и удаление изображений в Excel — а также приведены ссылки на подробные примеры для каждой задачи.

**Необходимые условия**: аккаунт Aspose.Cells Cloud, действующий API-ключ и установленный соответствующий SDK для выбранного языка.

- [Как получить изображение в определённом формате из рабочего листа Excel.](/cells/pictures/get/) – Извлечь одно изображение в запрошенном формате (PNG, JPEG и т.д.) из рабочего листа.  
- [Как получить все данные об изображениях из рабочего листа Excel.](/cells/pictures/get-all/) – Получить метаданные всех изображений, содержащихся в рабочем листе.  
- [Как добавить изображение в рабочий лист Excel.](/cells/pictures/add/) – Вставить новое изображение в рабочий лист, указав его положение и размер.  
- [Как обновить конкретное изображение из рабочего листа Excel.](/cells/pictures/update/) – Изменить свойства (например, размеры и положение) существующего изображения.  
- [Как удалить все изображения из рабочего листа Excel.](/cells/pictures/clear/) – Удалить все объекты-изображения из рабочего листа за один вызов.  
- [Как удалить изображение из рабочего листа Excel.](/cells/pictures/delete/) – Удалить одно изображение по его индексу.  

**Справка по API**

**Получение изображения в определённом формате**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (путь), `sheetName` (путь), `pictureIndex` (путь), `format` (запрос) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Двоичные данные изображения (PNG, JPEG и т.д.) | 200 OK, 400 Неверный запрос, 401 Несанкционированный доступ, 404 Не найдено, 500 Ошибка сервера |

**Получение всех данных об изображениях**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (путь), `sheetName` (путь) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | JSON-массив с метаданными изображений (индекс, имя, положение, размер) | 200 OK, 400, 401, 404, 500 |

**Добавление изображения**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример тела запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (путь), `sheetName` (путь) | `{ "image": "<base64‑закодированное‑изображение>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Создано, 400, 401, 404, 500 |

**Обновление изображения**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример тела запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (путь), `sheetName` (путь), `pictureIndex` (путь) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Удаление всех изображений**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (путь), `sheetName` (путь) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**Удаление конкретного изображения**

| HTTP-метод | Конечная точка | Обязательные параметры | Пример запроса | Пример ответа | Коды состояния |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (путь), `sheetName` (путь), `pictureIndex` (путь) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**См. также**

Ознакомьтесь с другими операциями, связанными с изображениями, в Aspose.Cells Cloud:  
- [Работа с фигурами](/cells/shapes/) – добавление, редактирование и удаление графических фигур.  
- [Работа с диаграммами](/cells/charts/) – создание и управление объектами диаграмм.  
- [Работа с изображениями в рабочих листах](/cells/images/) – встраивание и управление исходными файлами изображений.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Работа с изображениями в Excel – Документация Aspose.Cells Cloud",
  "description": "Руководство по извлечению, добавлению, обновлению и удалению изображений Excel через REST API Aspose.Cells Cloud.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "изображения Excel, Aspose.Cells Cloud, REST API, обработка изображений",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>
---