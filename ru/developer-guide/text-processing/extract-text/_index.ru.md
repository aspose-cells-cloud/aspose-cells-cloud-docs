---
title: "Aspose.Cells Cloud Web API – Извлечение текста"
second_title: "Aspose.Cells Cloud – Онлайн-короткие коды"
linktitle: "Извлечение текста"
type: docs
url: /ru/extract-text/
keywords: "Aspose.Cells Cloud, извлечение текста, Excel API, извлечение текста из ячеек, REST API"
description: "Извлекайте подстроки, числа или символы из ячеек Excel с помощью API Aspose.Cells Cloud. Поддерживает извлечение до/после текста, извлечение по позиции и вывод в новый диапазон напрямую."
weight: 100
ArticleTitle: "Документация API Aspose.Cells Cloud для извлечения текста"
---

Извлекает подстроки, символы или числа из ячейки электронной таблицы в другую ячейку, исключая необходимость использования сложных формул FIND, MIN, LEFT или RIGHT.

## **API ExtractText**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Параметры запроса API **extractText**

| Имя параметра   | Тип    | Расположение        | Описание                                                                                                                     |
| ---------------- | ------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | File    | FormData           | Загрузите файл электронной таблицы.                                                                                                    |
| extractTextType  | String  | Query              | Перечисление, указывающее режим извлечения. Допустимые значения: `Before`, `After`, `BeforePosition`, `AfterPosition`.                      |
| beforeText       | String  | Query              | Текст, который должен находиться **перед** извлекаемой подстрокой. Используется при `extractTextType=Before`.                                   |
| afterText        | String  | Query              | Текст, который должен находиться **после** извлекаемой подстроки. Используется при `extractTextType=After`.                                     |
| beforePosition   | Integer | Query              | Количество символов, возвращаемых с левой стороны ячейки. Используется при `extractTextType=BeforePosition`.                      |
| afterPosition    | Integer | Query              | Количество символов, возвращаемых с правой стороны ячейки. Используется при `extractTextType=AfterPosition`.                      |
| outPositionRange | String  | Query              | Целевой диапазон (например, `Sheet1!A1`), в который будет записан извлечённый текст.                                                  |
| worksheet        | String  | Query              | Имя рабочего листа, содержащего исходную ячейку.                                                                            |
| range            | String  | Query              | Исходная ячейка или диапазон (например, `A1`).                                                                                          |
| outPath          | String  | Query _(опционально)_ | Путь к папке в хранилище, куда будет сохранена результирующая рабочая книга. Если не указан, результат возвращается в теле ответа. |
| outStorageName   | String  | Query              | Имя хранилища, которое будет использоваться для выходного файла.                                                                                 |
| region           | String  | Query              | Настройка региона электронной таблицы (например, `US`, `EU`).                                                                                  |
| password         | String  | Query              | Пароль для открытия защищённой рабочей книги.                                                                                      |

**Пример запроса cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx"
```

### **Ответ**

При успешном выполнении запроса API возвращает JSON-полезную нагрузку, содержащую извлечённый текст и адрес ячейки, в которую он был записан:

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

Если параметр `outPath` указан, ответ содержит только сообщение о статусе; рабочая книга записывается в указанный путь.

**Пример ответа при отсутствии параметра `outPath`**

```json
{
  "Code": 200,
  "Status":"OK"
}
```

### Коды ошибок

- **200 OK** – извлечение завершено успешно.  
- **202 Accepted** – запрос принят для асинхронной обработки.  
- **400 Bad Request** – неверный URI API Aspose.Cells Cloud или отсутствуют обязательные параметры.  
- **401 Unauthorized** – неверный токен доступа, client ID или client secret.  
- **404 Not Found** – указанный файл электронной таблицы не может быть доступен.  
- **500 Server Error** – произошла непредвиденная ошибка при обработке рабочей книги.

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ExtractText) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Используйте SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает все внутренние детали, позволяя вам просто реализовать функцию **извлечения текста** для ячеек с минимальным количеством кода. Ознакомьтесь с [репозиторием GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода иллюстрируют, как делать вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{<tab tabNum="1" >}}

```csharp
// Пример на C# – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="2" >}}

```java
// Пример на Java – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="3" >}}

```php
// Пример на PHP – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="4" >}}

```ruby
# Пример на Ruby – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="5" >}}

```javascript
// Пример на Node.js – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="6" >}}

```python
# Пример на Python – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="7" >}}

```perl
# Пример на Perl – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{<tab tabNum="8" >}}

```go
// Пример на Go – извлечение текста (код опущен для краткости)
```

{{</tab>}}

{{< /tabs >}}