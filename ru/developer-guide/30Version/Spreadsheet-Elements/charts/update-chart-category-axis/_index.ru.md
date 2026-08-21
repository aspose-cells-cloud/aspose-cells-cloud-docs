---
title: "Обновление оси категорий диаграммы"
type: docs
url: /ru/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, диаграмма, ось категорий, REST API, Excel, облачный SDK"
description: "Обновляет ось категорий диаграммы в листе Excel с использованием облачного REST API Aspose.Cells."
ArticleTitle: "Обновление оси категорий диаграммы – Aspose.Cells Cloud API"
---

Этот REST API обновляет ось категорий диаграммы.

## API PostChartCategoryAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Безопасность и аутентификация**

Облачные API Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание |
| -------------- | ------- | -------- | ----------- |
| name           | string  | path     | Имя файла Excel. |
| sheetName      | string  | path     | Имя рабочего листа, содержащего диаграмму. |
| chartIndex     | integer | path     | Индекс диаграммы (начиная с нуля), подлежащей обновлению. |
| axis           | object  | body     | JSON-объект, определяющий свойства оси категорий. |
| folder         | string  | query    | Папка в облачном хранилище, где расположен файл (необязательно). |
| storageName    | string  | query    | Имя хранилища (необязательно). |

**Схема тела запроса — объект `axis`**

| Свойство | Тип    | Описание |
|----------|--------|-------------|
| IsAutomaticMajorUnit | boolean | Определяет, вычисляется ли основной интервал автоматически. |
| MajorUnit | number | Значение основного интервала, если `IsAutomaticMajorUnit` равно `false`. |
| IsAutomaticMinorUnit | boolean | Определяет, вычисляется ли вспомогательный интервал автоматически. |
| MinorUnit | number | Значение вспомогательного интервала, если `IsAutomaticMinorUnit` равно `false`. |
| Title | object | Настройки заголовка оси (например, `Text`, `Font`, `Visible`). |
| TickLabelPosition | string | Позиция меток делений (например, `Low`, `High`, `NextToAxis`). |
| ... | ... | Дополнительные свойства оси, определённые в спецификации API. |

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизован) | Недействительный или отсутствующий токен JWT. |
| 413  | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает ограничение по размеру. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

**Предварительные требования / Аутентификация**

Для вызова этого конечного пункта необходимо получить токен доступа JWT из службы аутентификации Aspose.Cells Cloud (`/connect/token`). Включите токен в заголовок `Authorization`, как показано в примере ниже.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Category Axis",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Пример ответа**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) определяет публично доступный программный интерфейс и позволяет выполнять взаимодействие с REST напрямую из веб-браузера.

### Примечания

* Конечная точка требует использования HTTPS; использование HTTP может вызвать предупреждения о смешанном контенте в браузерах.
* Все подставляемые значения (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) должны быть заменены реальными идентификаторами.
* Поддерживаемые типы диаграмм для обновления оси категорий указаны в справочнике по API.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Ознакомьтесь со [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список облачных SDK Aspose.Cells.

Примеры кода ниже демонстрируют, как осуществлять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}