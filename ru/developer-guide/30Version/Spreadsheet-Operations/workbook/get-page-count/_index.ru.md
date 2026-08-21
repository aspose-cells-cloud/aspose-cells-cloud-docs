---
title: "Получить количество страниц из файла Excel"
second_title: "Документ"
linktitle: "Страницы"
type: docs
url: /ru/get-page-count-from-an-excel-file/
aliases: [  /ru/workbook/page-count/ , /ru/workbook/get/page-count/ ]
keywords: "Aspose.Cells, Cloud API, количество страниц Excel, постраничная разбивка книги"
description: "Получить общее количество страниц для печати в книге Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает формат запроса, необходимые параметры, пример cURL, схему ответа, обработку ошибок и фрагменты кода SDK для различных языков программирования."
weight: 10
version: "v3.0"
ArticleTitle: "Получить количество страниц из файла Excel с помощью Aspose.Cells Cloud API"
---

Этот REST API возвращает **количество страниц** для книги.

## Безопасность и аутентификация
Aspose.Cells Cloud API защищены и требуют [аутентификацию на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Обязательный | Описание                                 |
| ------------- | ------ | -------------- | ------------ | ---------------------------------------- |
| name          | string | path           | Да           | Имя документа Excel.                     |
| folder        | string | query          | Нет          | Папка, содержащая документ.              |
| storageName   | string | query          | Нет          | Имя хранилища, которое следует использовать. |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к REST API Aspose.Cells. Пример ниже демонстрирует, как вызвать конечную точку с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Замените `YourFile.xlsx` на фактическое имя книги, которую вы хотите запросить.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Схема ответа

| HTTP-статус | Тип данных | Описание                                               |
| ----------- | ---------- | ------------------------------------------------------ |
| 200         | integer    | Общее количество страниц для печати в книге (например, `13`). |
| 4xx‑5xx     | JSON       | Объект ошибки (см. раздел _Обработка ошибок_).         |

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берет на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах вашего проекта. Пожалуйста, ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), где представлен полный список облачных SDK Aspose.Cells.

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Обработка ошибок

| HTTP-статус | Описание                                    | Пример тела JSON                                                                 |
| ----------- | ------------------------------------------- | ------------------------------------------------------------------------------- |
| 401         | Недействительный или отсутствующий JWT-токен. | `{ "Code": "InvalidAuthenticationToken", "Message": "Access token is missing or invalid." }` |
| 404         | Указанная книга не найдена.                 | `{ "Code": "FileNotFound", "Message": "The requested file does not exist." }`  |
| 400         | Неверный запрос — отсутствуют обязательные параметры. | `{ "Code": "BadRequest", "Message": "Required parameter 'name' is missing." }` |
| 500         | Внутренняя ошибка сервера.                  | `{ "Code": "InternalError", "Message": "An unexpected error occurred." }`      |
---