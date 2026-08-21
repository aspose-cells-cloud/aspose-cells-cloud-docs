---
title: "Обновление второго категориального оси диаграммы"
type: docs
url: /ru/charts/second-category-axis/update/
weight: 160
keywords: "Aspose.Cells, диаграмма, вторая категориальная ось, REST API, обновление диаграммы, Excel, облачный API"
description: "Узнайте, как обновить вторую категориальную ось диаграммы в рабочем листе Excel с помощью облачного REST API Aspose.Cells."
ArticleTitle: "Обновление второй категориальной оси диаграммы – Aspose.Cells Cloud API"
---

Этот REST API обновляет вторую категориальную ось диаграммы.

## API PostChartSecondCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе маркера JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                                |
|---------------|--------|-------------|---------------------------------------------------------|
| name          | string | path        | Имя файла Excel.                                        |
| sheetName     | string | path        | Имя рабочего листа, содержащего диаграмму.             |
| chartIndex    | integer| path        | Индекс диаграммы (начиная с 0), подлежащий обновлению.  |
| axis          | object | body        | Объект второй категориальной оси с новыми настройками. |
| folder        | string | query       | Путь к папке, где хранится файл.                        |
| storageName   | string | query       | Имя службы хранилища.                                   |

**Аутентификация** – API требует действительного токена доступа OAuth 2.0. Получите JWT-токен, следуя руководству по [аутентификации](https://docs.aspose.cloud/cells/authentication/). Включите токен в заголовок `Authorization`, как показано в примере cURL ниже.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondCategoryAxis) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondcategoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ 
        "axis": {
          /* настройки оси, например, "Title": "Новый заголовок оси", "IsVisible": true */
        }
      }'
```

*Замените `{name}`, `{sheetName}`, `{chartIndex}`, `{folder}` и `{storageName}` на ваши фактические значения. Тело запроса должно содержать объект `axis` с нужными настройками.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Успешный ответ (200)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Id": "chart_1",
    "SecondCategoryAxis": {
      "Title": "Новый заголовок оси",
      "IsVisible": true,
      /* дополнительные свойства оси */
    }
  }
}
```

**Ответы с ошибками**  

| Код состояния | Описание                                                   |
|---------------|------------------------------------------------------------|
| 400           | Неверный запрос – отсутствуют или недопустимы параметры.  |
| 401           | Неавторизован – недействительный или отсутствующий JWT-токен. |
| 404           | Не найдено – указанный файл, рабочий лист или диаграмма не существует. |
| 500           | Внутренняя ошибка сервера – непредвиденное состояние на сервере. |

```json
{
  "Code": 400,
  "Message": "Неверная полезная нагрузка запроса."
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

SDK упрощают разработку, скрывая низкоуровневые детали и позволяя сосредоточиться на бизнес-логике. Ознакомьтесь со [списком SDK Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondCategoryAxis.js" >}}
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

**Примечания и рекомендации**

* Параметр `chartIndex` индексируется с нуля: первая диаграмма на рабочем листе имеет индекс 0.  
* API поддерживает форматы рабочих книг `.xlsx` и `.xls`.  
* В объект `axis` включайте только необходимые свойства; неуказанные свойства сохраняют свои текущие значения.  
* Соблюдайте ограничения по частоте запросов (обычно 100 запросов в минуту на аккаунт), чтобы избежать ограничения скорости.