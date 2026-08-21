---
title: "Получить формат заливки области диаграммы – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /ru/charts/chart-area/fill-format/get/
aliases: [  /ru/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Область диаграммы"
  - "Формат заливки"
  - "REST API"
  - "Excel"
description: "Получить формат заливки (цвет, узор, градиент) области диаграммы в рабочей книге Excel через Aspose.Cells Cloud API. Включает пример cURL, фрагменты кода SDK, шаги аутентификации и детали ответа."
ArticleTitle: "Получить формат заливки области диаграммы Aspose.Cells Cloud API v3.0"
---

Этот REST API возвращает информацию о формате заливки **области диаграммы**.

**Предварительные требования**  
Для вызова этого конечного пункта требуется действующий токен OAuth/JWT. Получите токен, следуя процедуре аутентификации Aspose.Cells Cloud, и включите его в заголовок `Authorization` в виде `Bearer <jwt token>`. Если вы используете один из SDK, убедитесь, что SDK настроен с вашими `client_id` и `client_secret` перед вызовом метода.

## API GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                              |
|---------------|--------|-------------|---------------------------------------|
| name          | string | path        | Имя рабочей книги.                    |
| sheetName     | string | path        | Имя рабочего листа.                   |
| chartIndex    | integer| path        | Индекс диаграммы.                     |
| folder        | string | query       | Папка, содержащая рабочую книгу.      |
| storageName   | string | query       | Имя хранилища.                        |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**Примечания**  
- Успешный вызов возвращает HTTP 200 с деталями формата заливки.  
- HTTP 401 указывает на ошибку аутентификации (недействительный или отсутствующий токен).  
- HTTP 404 возвращается, если указанная рабочая книга, рабочий лист или индекс диаграммы не существует.  
- HTTP 500 означает ошибку на стороне сервера; повторите запрос или свяжитесь со службой поддержки, если проблема сохраняется.

| Код | Значение                                             |
|-----|------------------------------------------------------|
| 200 | Успех – формат заливки возвращён                    |
| 401 | Неавторизован – недействительный или отсутствующий токен |
| 404 | Не найдено – рабочая книга, рабочий лист или диаграмма не найдены |
| 500 | Внутренняя ошибка сервера                            |

См. также конечные пункты **Get Chart Area Border** (Получить границу области диаграммы) и **Get Chart Title** (Получить заголовок диаграммы).

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Ознакомьтесь со списком всех SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---