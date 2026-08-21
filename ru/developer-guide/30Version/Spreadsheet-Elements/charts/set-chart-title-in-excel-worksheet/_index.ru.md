---
title: "Aspose.Cells Cloud API – Добавление заголовка диаграммы в лист Excel"
type: docs
url: /ru/chart/title/add/
aliases: [  /ru/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, API заголовка диаграммы, заголовок диаграммы Excel, REST API, примеры SDK"
description: "Узнайте, как добавить или обновить заголовок диаграммы в листе Excel с помощью REST API Aspose.Cells Cloud. Включены примеры cURL, SDK, требуемые параметры, шаги аутентификации и обработка ошибок."
---

Добавляет заголовок диаграммы или делает существующий заголовок видимым.

## API PutWorksheetChartTitle

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                               |
|---------------|--------|-------------|----------------------------------------|
| name          | string | path        | Имя рабочей книги.                     |
| sheetName     | string | path        | Имя листа.                             |
| chartIndex    | integer| path        | Индекс диаграммы.                      |
| title         | string | body        | Текст заголовка диаграммы.             |
| folder        | string | query       | Папка, содержащая рабочую книгу.       |
| storageName   | string | query       | Имя хранилища.                         |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для удобного доступа к веб-сервисам Aspose.Cells. Пример ниже демонстрирует вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**Ответы об ошибках**

| HTTP-код | Пример полезной нагрузки                                                              | Описание                                                         |
|----------|---------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 400      | `{ "Code": "400", "Message": "Invalid request payload." }`                           | Неверный или неполный запрос: отсутствуют обязательные поля.    |
| 401      | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }`| Отсутствует, недействителен или просрочен токен авторизации.    |
| 404      | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`           | Указанный ресурс не найден.                                      |
| 500      | `{ "Code": "500", "Message": "Internal server error." }`                             | Внутренняя ошибка сервера.                                       |

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}