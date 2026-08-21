---
title: "Получение фигуры по индексу на листе Excel"
second_title: "Документ"
linktype: "Получить"
type: docs
url: /ru/shapes/get/
aliases: [  /ru/get-a-shape-by-index-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud, API фигур Excel, получение фигуры по индексу, фигура листа, REST API, извлечение фигур, Aspose.Cells SDK"
description: "Извлечение фигуры по её индексу с листа Excel с помощью REST API Aspose.Cells Cloud. Включает синтаксис запроса, параметры, данные ответа и примеры SDK."
weight: 20
ArticleTitle: "Получение фигуры по индексу на листе Excel – Документация Aspose.Cells Cloud"
---

Этот REST API извлекает фигуру (включая её растровые данные или метаданные) с листа Excel.

## API GetWorksheetShape

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Необходимые условия**  
- Действующий маркер доступа Aspose Cloud (Bearer JWT).  
- Рабочая книга должна находиться в вашем облачном хранилище Aspose Cloud или в указанной папке.  

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе маркера JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                            |
|---------------|--------|-------------|-----------------------------------------------------|
| name          | string | path        | Имя документа Excel.                                |
| sheetName     | string | path        | Имя листа, содержащего фигуру.                      |
| shapeindex    | integer| path        | Индекс фигуры на листе (начинается с 0).            |
| folder        | string | query       | Путь к папке, где сохранён документ.                |
| storageName   | string | query       | Имя сервиса хранилища.                              |

**Примечание:** `shapeindex` — индексация начинается с 0; первая фигура имеет индекс 0. Убедитесь, что рабочая книга сохранена в указанной `folder` и `storageName`, если вы не используете хранилище по умолчанию.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Исправленная конечная точка и путь
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Возможные коды HTTP-статуса**

| Код | Описание |
|------|-------------|
| **200 OK** | Фигура успешно получена. |
| **400 Bad Request** | Запрос имеет некорректный формат или отсутствуют обязательные параметры. |
| **401 Unauthorized** | Аутентификация не удалась или маркер отсутствует/недействителен. |
| **404 Not Found** | Указанная рабочая книга, лист или индекс фигуры не найдены. |
| **500 Internal Server Error** | Произошла непредвиденная ошибка сервера. |

**Типичные ошибки:** Использование некорректного домена верхнего уровня (`api.aspose.com`) или устаревшего сегмента `/autoshapes/` приведёт к ошибке 404. Всегда используйте сегмент `/shapes/` с доменом `api.aspose.cloud`.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

См. также документацию по смежным операциям: **[Добавление фигуры](/shapes/add/)** и **[Обновление фигуры](/shapes/update/)**.