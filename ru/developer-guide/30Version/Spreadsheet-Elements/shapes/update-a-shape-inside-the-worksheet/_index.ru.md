---
title: "Обновление фигуры на листе Excel"
second_title: "Документ"
linktype: "Обновление"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "обновление фигуры в Excel через API, Aspose.Cells Cloud, обновление фигуры Excel, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Узнайте, как обновить фигуру на листе Excel с помощью REST API Aspose.Cells Cloud. Включает HTTPS-конечную точку, данные по аутентификации, схему DTO, пошаговое руководство, пример cURL и примеры кода SDK для различных языков."
ArticleTitle: "Обновление фигуры на листе Excel — API Aspose.Cells Cloud"
weight: 31
---

Этот REST API обновляет фигуру на листе Excel.

## Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Параметры запроса

| Имя параметра   | Тип     | Местоположение | Описание                                                                                      |
| ---------------- | ------- | -------------- | ---------------------------------------------------------------------------------------------- |
| **name**         | string  | path           | Имя файла рабочей книги.                                                                       |
| **sheetName**    | string  | path           | Имя листа, содержащего фигуру.                                                                  |
| **shapeindex**   | integer | path           | Индекс фигуры (начиная с нуля) на листе.                                                       |
| **dto**          | object  | body           | Объект передачи данных фигуры, содержащий обновлённые свойства (см. _Схему DTO_ ниже).         |
| **folder**       | string  | query          | Папка, в которой хранится рабочая книга.                                                       |
| **storageName**  | string  | query          | Имя облачного хранилища Aspose Cloud.                                                           |

### Схема DTO

Объект `dto` содержит свойства, которые можно обновить. Все поля являются необязательными, если не указано иное.

| Поле                | Тип     | Обязательное | Описание                                                                           |
| -------------------- | ------- | ------------ | ---------------------------------------------------------------------------------- |
| **Name**            | string  | Нет          | Новое имя фигуры.                                                                  |
| **UpperLeftRow**    | integer | Нет          | Индекс строки верхнего левого угла фигуры.                                         |
| **UpperLeftColumn** | integer | Нет          | Индекс столбца верхнего левого угла фигуры.                                        |
| **Width**           | integer | Нет          | Ширина фигуры (в пунктах).                                                         |
| **Height**          | integer | Нет          | Высота фигуры (в пунктах).                                                         |
| **RotationAngle**   | integer | Нет          | Угол поворота в градусах.                                                          |
| **IsHidden**        | boolean | Нет          | `true`, чтобы скрыть фигуру.                                                       |
| **IsLocked**        | boolean | Нет          | `true`, чтобы заблокировать фигуру.                                                |
| **Font**            | object  | Нет          | Параметры шрифта (см. OpenAPI-спецификацию для подсвойств).                        |
| **...**             | …       | Нет          | Дополнительные свойства, такие как `HtmlText`, `AlternativeText`, `ZOrderPosition` и др. |

> Полный список доступен в официальной OpenAPI-спецификации: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Заголовки запроса

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(JWT-токен, полученный на этапе _Аутентификации_)_

### Тело запроса (пример)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Пример с использованием cURL (инструмент командной строки)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Ответ

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Обработка ошибок** – API может возвращать следующие коды состояния:

| Код | Значение              | Типичная причина                                     |
| ---- | --------------------- | ---------------------------------------------------- |
| 400  | Bad Request           | Неверный JSON или отсутствуют обязательные поля.    |
| 401  | Unauthorized          | Отсутствует или недействителен JWT-токен.           |
| 404  | Not Found             | Рабочая книга, лист или индекс фигуры не найдены.    |
| 500  | Internal Server Error | Непредвиденная ошибка на стороне сервера.            |

**Примеры ответов об ошибках**

*400 – Bad Request*

```json
{
  "Code": 400,
  "Message": "Неверный полезный запрос. Поле 'Name' превышает максимальную длину."
}
```

*401 – Unauthorized*

```json
{
  "Code": 401,
  "Message": "Ошибка аутентификации. Недействительный или просроченный JWT-токен."
}
```

*404 – Not Found*

```json
{
  "Code": 404,
  "Message": "Указанная рабочая книга, лист или индекс фигуры не найдены."
}
```

*500 – Internal Server Error*

```json
{
  "Code": 500,
  "Message": "На сервере произошла непредвиденная ошибка."
}
```

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}