---
title: "Получение диаграммы из рабочего листа"
type: docs
url: /charts/get/
aliases: [/get-chart-from-a-worksheet/]
weight: 10
keywords: "Aspose.Cells Cloud, получение диаграммы, рабочий лист, REST API, Excel, API диаграмм, извлечение диаграммы, диаграмма Excel"
description: "Получение информации о диаграмме, включая метаданные и формат экспорта, из рабочего листа с использованием REST API Aspose.Cells Cloud."
ArticleTitle: "Получение диаграммы из рабочего листа – API Aspose.Cells Cloud"
---

Этот REST API извлекает информацию о диаграмме.

**Необходимые условия** – Для вызова этого эндпоинта у вас должна быть действующая учетная запись Aspose.Cells Cloud, активное хранилище и JWT-токен доступа. Получите токен, следуя инструкциям в руководстве по аутентификации, прежде чем отправлять какие-либо запросы к API.

## API GetWorksheetChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации посредством JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                |
| ------------- | ------ | ------------ | --------------------------------------- |
| name          | string | path         | Имя файла Excel.                        |
| sheetName     | string | path         | Имя рабочего листа, содержащего диаграмму. |
| chartNumber   | integer| path         | Индекс диаграммы (начиная с 0) для извлечения. |
| format        | string | query        | Желаемый формат экспорта (например, png, jpeg). |
| folder        | string | query        | Путь к папке, где сохранён документ.    |
| storageName   | string | query        | Имя сервиса хранилища.                  |

### **Ответ**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                              |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK (Успех)                  | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.        |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает предельный размер.         |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                        |

## Как использовать API GetWorksheetChart с SDK

### Спецификация API GetWorksheetChart

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать инструмент командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы к облачному API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}