---
title: "Обновить заголовок диаграммы в рабочей тетради Excel"
type: docs
url: /ru/charts/title/update/
aliases: [  /ru/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, заголовок диаграммы, обновление, облачный SDK
description: Узнайте, как обновить заголовок диаграммы в рабочей тетради Excel с помощью Aspose.Cells Cloud REST API, cURL и различных SDK.
ArticleTitle: "Обновить заголовок диаграммы в рабочей тетради Excel – документация Aspose.Cells Cloud"
---

Этот REST API обновляет заголовок диаграммы.

**Необходимые условия:** У вас должен быть действующий аккаунт Aspose Cloud и JWT-токен для авторизации. Типичные шаги включают:

- Зарегистрироваться в аккаунте Aspose Cloud.  
- Получить JWT-токен через endpoint аутентификации.  
- Убедитесь, что целевая рабочая тетрадь сохранена в поддерживаемом облачном хранилище (по умолчанию или пользовательском).

## API PostWorksheetChartTitle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Все вызовы API должны выполняться по протоколу **HTTPS**, чтобы избежать предупреждений о смешанном содержимом.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                         |
| ------------- | ------ | ------------ | -------------------------------- |
| name          | string | path         | Имя рабочей тетради.             |
| sheetName     | string | path         | Имя рабочего листа.              |
| chartIndex    | integer| path         | Индекс диаграммы (начинается с 0)|
| title         | string | body         | Новый заголовок диаграммы.       |
| folder        | string | query        | Папка рабочей тетради.           |
| storageName   | string | query        | Имя хранилища.                   |

### Коды состояния ответа

| Код | Описание                                              |
| --- | ----------------------------------------------------- |
| 200 | OK — заголовок диаграммы успешно обновлён.            |
| 400 | Bad Request — отсутствуют или некорректны параметры. |
| 401 | Unauthorized — недействительный или отсутствующий JWT-токен. |
| 404 | Not Found — рабочая тетрадь, рабочий лист или диаграмма не найдены. |
| 500 | Internal Server Error — непредвиденная ошибка сервера. |

**Примечание:** Индекс диаграммы (`chartIndex`) начинается с 0; первая диаграмма на рабочем листе имеет индекс `0`.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Биржа ценных бумаг"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a> для получения полного списка SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}