---
title: "Получить ось категорий диаграммы"
type: docs
url: /charts/category-axis/get/
weight: 60
keywords: "Aspose.Cells, ось категорий диаграммы, Excel, REST API, облачное хранилище, OAuth2, документация API"
description: "Получает ось категорий диаграммы в листе Excel с использованием REST API Aspose.Cells Cloud."
ArticleTitle: "Получить ось категорий диаграммы – документация API Aspose.Cells Cloud"
---

Этот REST API позволяет получить **ось категорий** диаграммы.  
Для вызова этого endpoint необходимо предоставить действительный токен доступа OAuth 2.0, а рабочая книга должна быть сохранена в облачном хранилище Aspose.

**Предварительные требования**  
Перед использованием этого endpoint убедитесь, что:  

- Получен и действителен токен OAuth 2.0 для сервисов Aspose Cloud.  
- Файл рабочей книги загружен в облачное хранилище Aspose (в папку по умолчанию или в указанную папку).  
- Используется версия API **v3.0**, как указано в URL запроса.  
- Приложение, выполняющее вызов, имеет разрешение на чтение рабочей книги и доступ к её листам.

## API GetChartCategoryAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

**Контекст** — удаление всех диаграмм с листа полезно, когда необходимо сбросить визуальное оформление листа, заменить устаревшие визуализации или подготовить рабочую книгу к повторному использованию без сохранения предыдущих данных диаграмм.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Расположение | Описание                                            |
| ------------- | ------ | ------------ | --------------------------------------------------- |
| name          | string | path         | Имя файла рабочей книги.                            |
| sheetName     | string | path         | Имя листа, содержащего диаграмму.                   |
| chartIndex    | integer| path         | Индекс диаграммы (от 0), ось которой запрашивается.|
| folder        | string | query        | Путь к папке в хранилище, где расположена рабочая книга. |
| storageName   | string | query        | Имя сервиса хранилища (если отличается от стандартного). |

### **Ответ**

```json
{
  "Code": 200,
  "Status": "OK",
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий токен JWT. |
| 413 | Payload Too Large           | Загружаемый файл превышает допустимый размер. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API GetChartCategoryAxis с SDK

### Спецификация API GetChartCategoryAxis

<a href="https://apireference.aspose.cloud/cells/#/Charts/GetChartCategoryAxis" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для доступа к веб-сервисам Aspose.Cells Cloud можно использовать утилиту командной строки cURL. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis" \
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
  "CategoryAxis": {
    "AxisBetweenCategories": true,
    "AxisLine": {
      "IsVisible": true,
      "Weight": 1.0
    },
    "MajorTickMark": "Cross",
    "MinorTickMark": "None",
    "Title": {
      "Text": "Category Axis",
      "IsVisible": true
    },
    "Labels": {
      "IsAutoRotation": false,
      "RotationAngle": 0,
      "IsVisible": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:

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
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartCategoryAxis.js" >}}
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