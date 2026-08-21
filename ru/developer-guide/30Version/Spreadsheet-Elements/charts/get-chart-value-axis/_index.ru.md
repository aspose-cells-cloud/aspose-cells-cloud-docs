---
title: "Получить ось значений диаграммы"
type: docs
url: /charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Ось значений диаграммы, REST API, Excel, Cloud SDK, Получить ось значений диаграммы
description: "Aspose.Cells Cloud REST API — получить ось значений диаграммы в рабочей книге Excel."
ArticleTitle: "Получить ось значений диаграммы — Aspose.Cells Cloud REST API"
---

Этот REST API позволяет получить ось значений диаграммы. Он является частью **Aspose.Cells Cloud REST API** и работает с рабочими книгами Excel, хранящимися в облаке.

См. также конечную точку **[Получить ось категорий диаграммы](/charts/category-axis/get/)**.

## API GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Местоположение | Описание                                                  |
|---------------|--------|---------------|-----------------------------------------------------------|
| name          | string | path          | Имя файла Excel (включая расширение).                     |
| sheetName     | string | path          | Имя рабочего листа, содержащего диаграмму.               |
| chartIndex    | integer| path          | Индекс диаграммы на рабочем листе (начинается с нуля).    |
| folder        | string | query         | Папка в облачном хранилище, где расположен файл.          |
| storageName   | string | query         | Имя сервиса хранилища (например, Aspose Cloud).           |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
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
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Значения",
    "Format": {
      "NumberFormat": "Общий",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Возможные HTTP-коды состояния**

| Код | Описание                                                                 |
|-----|--------------------------------------------------------------------------|
| 200 | Успех — информация об оси значений возвращена.                           |
| 400 | Неверный запрос — отсутствуют обязательные параметры или они недопустимы.|
| 401 | Неавторизован — отсутствует или недействителен токен аутентификации.     |
| 404 | Не найдено — указанная рабочая книга, рабочий лист или диаграмма не существует. |
| 500 | Внутренняя ошибка сервера — произошла непредвиденная ошибка на сервере.  |

Ответ содержит детальный объект `ValueAxis` со свойствами, такими как `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` и `Format`. В полной реализации могут быть предоставлены дополнительные детали форматирования.

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK берет на себя низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Примеры кода ниже демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
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