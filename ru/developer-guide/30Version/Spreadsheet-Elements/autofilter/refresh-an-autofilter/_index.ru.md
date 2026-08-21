---
title: "Обновление автозаполнения в листе Excel"
second_title: "Документ"
linktype: "Обновить автозаполнение"
type: docs
url: /ru/autofilter/refresh/
aliases: [  /ru/refresh-an-autofilter/ ]
weight: 100
keywords: "Aspose.Cells, AutoFilter, обновление, Excel, API, REST"
description: "Обновите существующее автозаполнение на листе Excel с помощью Aspose.Cells Cloud REST API. Включает примеры cURL и SDK для C#, Java, Python и других."
ArticleTitle: "Обновление автозаполнения в листе Excel"
---

### Что делает операция **обновления**?

Вызов конечной точки повторно применяет текущие критерии фильтрации после изменения данных листа (например, добавления или удаления строк). Операция не изменяет определение фильтра; она просто обновляет отображение и возвращает ответ с состоянием.

### REST API

Этот REST API обновляет автозаполнение на листе Excel (версия API — **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud безопасны и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                            |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK (ОК)                     | Фильтр успешно применён; ответ содержит данные о выполнении. |
| 400  | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT.     |
| 413  | Payload Too Large (Слишком большой объём данных) | Загруженный файл превышает допустимый размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

*Примеры ответов с ошибками*  

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Неверный параметр: лист с именем sheetName не найден."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Ошибка аутентификации. Токен JWT отсутствует или недействителен."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "Загруженный файл превышает максимально допустимый размер."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "На сервере произошла непредвиденная ошибка."
}
```

## Как использовать API PostWorksheetAutoFilterRefresh с SDK

### Спецификация API PostWorksheetAutoFilterRefresh

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Ознакомьтесь со [списком SDK Aspose.Cells Cloud на GitHub](https://github.com/aspose-cells-cloud).

Ниже приведены примеры кода, показывающие, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}