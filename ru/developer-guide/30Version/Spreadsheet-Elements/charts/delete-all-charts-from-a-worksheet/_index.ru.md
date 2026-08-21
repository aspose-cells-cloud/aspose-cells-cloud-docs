---
title: "Удаление всех диаграмм из рабочего листа"
type: docs
url: /charts/clear/
aliases: [/delete-all-charts-from-a-worksheet/]
weight: 30
keywords: "Aspose.Cells, Cloud, удаление, все диаграммы, рабочий лист, REST API, DELETE, SDK"
description: "Узнайте, как удалить все диаграммы из рабочего листа с помощью Aspose.Cells Cloud REST API (v3.0). Включает адрес конечной точки, параметры, пример cURL, фрагменты кода SDK, шаги аутентификации и обработку ошибок."
ArticleTitle: "Удаление всех диаграмм из рабочего листа с помощью Aspose.Cells Cloud API"
---

Этот REST API удаляет все диаграммы из указанного рабочего листа.

**Контекст** – Удаление всех диаграмм из рабочего листа полезно, когда необходимо сбросить визуальную компоновку листа, заменить устаревшие визуализации или подготовить рабочую книгу к повторному использованию без сохранения предыдущих данных диаграмм.

Перед вызовом API убедитесь, что выполнены следующие предварительные условия:

- Доступен действительный токен JWT для аутентификации.  
- Файл рабочей книги существует в указанном месте хранения и папке.  
- Вы используете версию API **v3.0**.

## API DeleteWorksheetClearCharts

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются безопасными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                              |
| ------------- | ------ | ------------ | ------------------------------------- |
| name          | string | path         | Имя файла рабочей книги.              |
| sheetName     | string | path         | Имя рабочего листа.                   |
| folder        | string | query        | Папка, в которой хранится рабочая книга. |
| storageName   | string | query        | Имя хранилища.                        |

**Заголовки запроса**

| Заголовок       | Описание                        |
|-----------------|---------------------------------|
| Authorization   | Bearer `<jwt token>`            |
| Accept          | `application/json`              |
| Content-Type    | `application/json` (тело отсутствует) |

**Тело запроса**

Операция DELETE **не требует** тела запроса.

**Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                  |
|------|-----------------------------|-----------------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT.            |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает допустимый размер.         |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                      |

*Примеры ответов об ошибках*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Неверный параметр: требуется значение 'sheetName'."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Ошибка аутентификации. Недействительный токен JWT."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "Размер полезной нагрузки запроса превышает максимально допустимый."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "На сервере произошла непредвиденная ошибка."
}
```

## Как использовать API DeleteWorksheetClearCharts с SDK

### Спецификация API DeleteWorksheetClearCharts

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```


{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Использование SDK Aspose.Cells Cloud

Использование SDK — это лучший способ ускорить разработку при необходимости **удаления всех диаграмм** из рабочего листа. SDK берёт на себя работу с низкоуровневыми деталями и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}