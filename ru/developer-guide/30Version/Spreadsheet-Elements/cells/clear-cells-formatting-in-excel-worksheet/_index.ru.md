---
title: "Очистка форматирования ячеек в листе Excel"
type: docs
url: /clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, очистка форматирования ячеек, REST API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Используйте Aspose.Cells Cloud REST API для очистки форматирования ячеек в листе Excel. Включает детали запроса, пример cURL и фрагменты кода SDK для различных языков."
ArticleTitle: "Очистка форматирования ячеек в листе Excel — API Aspose.Cells Cloud"
---

**Примечание:** Все вызовы Aspose.Cells Cloud API должны выполняться через **HTTPS**. HTTP-адреса устарели и могут быть заблокированы браузерами.

- **Метод:** POST  
- **Конечная точка:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Этот REST API очищает форматирование ячеек в файле Excel и является частью набора Aspose.Cells Cloud для очистки форматирования ячеек в листах Excel.

## API PostClearFormats

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Ответ**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Схема ответа**

| Поле   | Тип     | Описание                                                |
|--------|---------|---------------------------------------------------------|
| Code   | integer | Код HTTP-статуса, возвращаемый API (например, 200).    |
| Status | string  | Результат операции (`OK` — успех).                     |

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                                   |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит данные об операции. |
| 400 | Bad Request                 | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствующий JWT-токен.                      |
| 413 | Payload Too Large           | Загружаемый файл превышает допустимый размер.              |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                             |

## Как использовать API PostClearFormats с SDK

### Спецификация API PostClearFormats

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

Использование SDK — самый быстрый способ разработки. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также**

- [Очистка содержимого и стилей ячеек](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Установка стиля ячейки](https://docs.aspose.cloud/cells/set-cell-style)