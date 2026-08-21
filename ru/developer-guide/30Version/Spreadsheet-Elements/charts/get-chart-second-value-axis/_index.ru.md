---
title: "Получить второй осевой масштаб диаграммы"
type: docs
url: /charts/second-value-axis/get/
weight: 60
keywords: Aspose.Cells, второй осевой масштаб диаграммы, Excel, REST API, облачные технологии, API, оси диаграмм Excel
description: Получает второй осевой масштаб указанной диаграммы на рабочем листе Excel с использованием облачного REST API Aspose.Cells.
ArticleTitle: "Получить второй осевой масштаб диаграммы – Aspose.Cells Cloud API"
---

Этот REST API возвращает второй осевой масштаб диаграммы.

## API GetChartSecondValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                          |
| ------------- | ------ | ------------ | ------------------------------------------------- |
| name          | string | path         | Имя файла Excel.                                  |
| sheetName     | string | path         | Имя рабочего листа, содержащего диаграмму.       |
| chartIndex    | integer| path         | Индекс диаграммы (начинается с нуля).             |
| folder        | string | query        | Папка, в которой хранится файл.                  |
| storageName   | string | query        | Имя облачного хранилища Aspose Cloud.            |

**Необходимые условия**: Для каждого запроса в заголовке `Authorization` должен быть указан действительный токен доступа JWT, полученный с помощью OAuth2-процесса Aspose Cloud.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartSecondValueAxis) определяет публично доступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells можно использовать утилиту командной строки cURL. В следующем примере показано, как выполнить вызов облачного API с помощью cURL. Все конечные точки Aspose Cloud требуют использования HTTPS.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Axis": {
    "AxisId": 1,
    "IsVisible": true,
    "MinimumScale": 0,
    "MaximumScale": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Second Value Axis"
  }
}
```

**Поля ответа**

- **Code** — HTTP-статус выполнения операции (например, `200` — успех).  
- **Status** — текстовое описание статуса (`"OK"` — успех).  
- **Axis** — объект, содержащий сведения о втором осевом масштабе:  
  - **AxisId** — идентификатор оси.  
  - **IsVisible** — логическое значение, указывающее, отображается ли ось.  
  - **MinimumScale** — минимальное значение, отображаемое на оси.  
  - **MaximumScale** — максимальное значение, отображаемое на оси.  
  - **MajorUnit** — интервал между основными метками деления.  
  - **MinorUnit** — интервал между вспомогательными метками деления.  
  - **Title** — заголовок оси.

**Сообщения об ошибках** (не 200)

- `400 Bad Request` — недопустимые параметры или некорректный запрос.  
- `401 Unauthorized` — отсутствует или недействителен токен JWT.  
- `404 Not Found` — указанный файл, рабочий лист или диаграмма не найдены.  
- `500 Internal Server Error` — непредвиденная ошибка сервера.

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — оптимальный способ ускорить разработку. SDK берёт на себя работу с низкоуровневыми деталями, позволяя сосредоточиться на задачах проекта. Полный список облачных SDK Aspose.Cells доступен в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории на GitHub</a>.

Приведённые ниже примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartSecondValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}