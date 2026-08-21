---
title: "Обновление второго значения оси диаграммы"
ArticleTitle: "Обновление второго значения оси диаграммы – Aspose.Cells Cloud REST API"
type: docs
url: /ru/charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, Chart API, Вторая ось значений, Excel, REST, облачный SDK"
description: "Обновляет вторую ось значений диаграммы в листе Excel с использованием Aspose.Cells Cloud REST API. Включает примеры запросов, коды ответов и предварительные требования."
---

Этот REST API обновляет вторую ось значений диаграммы.

**Предварительные требования:**  
- Действующий JWT-токен доступа (см. [Руководство по аутентификации](https://docs.aspose.cloud/cells/authentication/)).  
- Целевой файл Excel должен храниться в облачном хранилище Aspose (указать `folder` и необязательно `storageName`).  
- Используется версия API v3.0; убедитесь, что базовый URL-адрес — `https://api.aspose.cloud/v3.0`.

## API PostChartSecondValueAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                        |
|--------------|--------|-------------|-------------------------------------------------|
| name         | string | path        | Имя файла Excel.                                |
| sheetName    | string | path        | Имя листа, содержащего диаграмму.              |
| chartIndex   | integer| path        | Индекс диаграммы (начиная с 0), подлежащая изменению. |
| axis         | object | body        | Параметры второй оси значений.                  |
| folder       | string | query       | Путь к папке в хранилище, где расположен файл.  |
| storageName  | string | query       | Имя сервиса хранилища.                          |

**Пример тела запроса (JSON):**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Вторичная ось"
  }
}
```

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) определяет общедоступное программное интерфейсное решение и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Некорректный или отсутствующий JWT-токен.       |
| 413 | Payload Too Large           | Загружаемый файл превышает лимит размера.        |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                   |

**См. также:**  
- [Получить второе значение оси диаграммы](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Обновить значение оси диаграммы](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют выполнение вызовов в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Пример на C# для обновления второй оси значений
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Пример на Java для обновления второй оси значений
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Пример на PHP для обновления второй оси значений
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Пример на Ruby для обновления второй оси значений
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Пример на Python для обновления второй оси значений
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Пример для Android (Java) — аналогичен фрагменту выше для Java
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Пример на Swift для обновления второй оси значений
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Пример на Perl для обновления второй оси значений
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Пример на Go для обновления второй оси значений
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}