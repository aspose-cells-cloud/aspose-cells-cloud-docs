---
title: "Получение заголовка диаграммы из рабочего листа"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Заголовок диаграммы"
  - "Excel"
  - "REST API"
  - "Получение заголовка диаграммы"
  - "cURL"
  - "SDK"
  - "Автоматизация диаграмм Excel"
  - "Получение заголовка диаграммы (GET)"
description: "Узнайте, как извлечь заголовок диаграммы из рабочего листа Excel с помощью Aspose.Cells Cloud REST API. Включает адрес конечной точки, параметры, аутентификацию, примеры кода на cURL и SDK."
ArticleTitle: "Получение заголовка диаграммы из рабочего листа"
---

Этот REST API позволяет получить заголовок диаграммы, хранящейся в рабочем листе книги Excel.

**Необходимые условия**: Для вызова этой конечной точки необходим действующий OAuth2/JWT-токен доступа Aspose.Cells Cloud со scope `Cells.Read`. Книга должна быть уже загружена в указанное хранилище.

## API GetWorksheetChartTitle

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Безопасность и аутентификация

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                     |
|---------------|--------|-------------|----------------------------------------------|
| name          | string | path        | Имя файла книги.                             |
| sheetName     | string | path        | Имя рабочего листа, содержащего диаграмму.  |
| chartIndex    | integer| path        | Индекс диаграммы (начинается с 0).           |
| folder        | string | query       | Путь к папке, где хранится книга.            |
| storageName   | string | query       | Имя сервиса хранилища.                       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle) определяет публично доступный программный интерфейс и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

Для простого доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки **cURL**. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "Продажи за Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Поля ответа**

| Поле                | Описание                                      |
|---------------------|-----------------------------------------------|
| `Title.Text`        | Текст, отображаемый в качестве заголовка диаграммы. |
| `Title.Font.Name`   | Семейство шрифтов, используемое для заголовка (например, _Arial_). |
| `Title.Font.Size`   | Размер шрифта в пунктах.                      |
| `Title.Font.IsBold` | Указывает, выделен ли текст заголовка жирным. |

**Коды статуса ответа**

| Код | Описание |
|-----|----------|
| 200 OK | Заголовок диаграммы успешно получен. |
| 401 Unauthorized | Аутентификация не удалась или токен отсутствует/недействителен. |
| 404 Not Found | Указанная книга, рабочий лист или диаграмма не существует. |
| 500 Internal Server Error | Произошла непредвиденная ошибка сервера. |

**Примечания**: Индекс диаграммы начинается с 0; убедитесь, что диаграмма существует. Если книга ещё не загружена, сначала загрузите её с помощью соответствующего API.

**Как извлечь заголовок в скрипте (с использованием `jq`)**

```bash
# Предполагается, что JSON-ответ сохранён в файл response.json
title=$(jq -r '.Title.Text' response.json)
echo "Заголовок диаграммы: $title"
```

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Пример на C# с использованием Aspose.Cells Cloud SDK
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Пример на Java с использованием Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// Пример на PHP с использованием Aspose.Cells Cloud SDK
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Пример на Ruby с использованием Aspose.Cells Cloud SDK
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Пример на Python с использованием Aspose.Cells Cloud SDK
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Пример на Node.js с использованием Aspose.Cells Cloud SDK
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Пример на Android (Java) с использованием Aspose.Cells Cloud SDK
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Пример на Swift с использованием Aspose.Cells Cloud SDK
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Заголовок диаграммы: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Пример на Perl с использованием Aspose.Cells Cloud SDK
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

Также вы можете обратиться к индивидуальной документации SDK для более сложных сценариев, таких как обновление или удаление заголовка диаграммы.  

**См. также**: [Обновление заголовка диаграммы](/charts/title/put/), [Удаление заголовка диаграммы](/charts/title/delete/).