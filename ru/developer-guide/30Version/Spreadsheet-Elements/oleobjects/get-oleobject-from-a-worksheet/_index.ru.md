---
title: "Получение OLE-объекта из рабочего листа Excel – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Получить"
type: docs
url: /ru/oleobjects/get/
aliases: [/ru/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole object, excel, worksheet, get ole object, rest api"
description: "Извлечение OLE-объекта (изображения, диаграммы или встроенного файла) из рабочего листа с использованием Aspose.Cells Cloud REST API. Включает HTTPS-адрес, необходимые параметры, пример cURL и код SDK на нескольких языках."
ArticleTitle: "Получение OLE-объекта из рабочего листа Excel – Aspose.Cells Cloud API"
weight: 10
---

Этот REST API извлекает **OLE-объект** из рабочего листа Excel.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификацию на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Описание                                                      |
|---------------|--------|----------------|---------------------------------------------------------------|
| name          | string | path           | Имя документа.                                                |
| sheetName     | string | path           | Имя рабочего листа.                                           |
| objectNumber  | integer| path           | Номер объекта внутри рабочего листа.                          |
| format        | string | query          | Желаемый формат экспорта объекта (например, `png`, `jpeg`).  |
| folder        | string | query          | Папка, содержащая документ.                                   |
| storageName   | string | query          | Имя используемого хранилища.                                  |

### Параметры хранилища

- **folder** – указывает подпапку в хранилище по умолчанию, где находится рабочая книга.
- **storageName** – переопределяет имя хранилища по умолчанию, если рабочая книга хранится в другом месте.

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервиса Aspose.Cells. В приведённом ниже примере показано, как запросить OLE-объект в виде изображения PNG.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Ответ с бинарными данными изображения

Если параметр `format` задан как тип изображения (например, `png`), API возвращает бинарные данные изображения с заголовком:

```
Content-Type: image/png
```

_(Файл изображения передаётся напрямую клиенту.)_

### Ответ с метаданными в формате JSON

Если параметр `format` опущен или установлен в значение `json`, API возвращает JSON-полезную нагрузку с описанием OLE-объекта:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Ответы об ошибках

| HTTP-статус | Код ошибки | Описание                                            |
|-------------|------------|-----------------------------------------------------|
| 400         | BadRequest | Отсутствуют или недопустимы параметры запроса.    |
| 401         | Unauthorized | Недействительный или отсутствующий токен JWT.     |
| 404         | NotFound   | Рабочая книга, рабочий лист или OLE-объект не найдены. |
| 500         | ServerError | Непредвиденная ошибка сервера.                     |

**Пример ответа с кодом 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "Запрошенный OLE-объект с номером 0 не найден на рабочем листе 'Sheet1'."
}
```

## Семейство облачных SDK

Использование SDK — самый быстрый способ интеграции API. SDK обрабатывают низкоуровневые детали, позволяя вам сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}