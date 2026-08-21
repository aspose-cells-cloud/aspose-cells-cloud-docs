---
title: "Получение метаданных из файлов Excel"
second_title: "Документ"
linktitle: "Получение без использования хранилища"
type: docs
url: /metadata/get/
keywords: "Aspose.Cells, Excel, метаданные, REST API, облачное SDK"
description: "Получение встроенных или пользовательских метаданных из книг Excel с использованием Aspose.Cells Cloud REST API. Включает формат запроса, параметры, примеры кода SDK и обработку ошибок."
weight: 23
ArticleTitle: "Получение метаданных из файлов Excel — API Aspose.Cells Cloud"
---

Этот REST API извлекает **метаданные** из одного или нескольких файлов Excel.  
В запросе должен присутствовать заголовок `Authorization: Bearer <access_token>`, полученный с помощью потока учётных данных OAuth 2.0.

**Необходимые условия**: Для вызова этого конечного пункта необходимо иметь действующий токен доступа, полученный из конечного пункта токенов OAuth 2.0 Aspose Cloud. Пример запроса curl для получения токена:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Параметр запроса (query parameter)

| Имя параметра | Тип    | Описание                                                          |
|---------------|--------|-------------------------------------------------------------------|
| type          | string | `ALL` / `BuiltIn` / `Custom` — определяет, какие группы метаданных вернуть. |

### Параметр тела запроса (request body parameter)

| Имя параметра | Тип     | Описание                                                           |
|---------------|---------|--------------------------------------------------------------------|
| файл Excel    | файл данных | Файл Excel, передаваемый в качестве первой части многокомпонентного запроса. |

### Ответ

```json
[
  {
    "Name": "Author",
    "Value": "Иван Иванов",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Пользовательское значение",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Код | Описание                | Когда возникает                   |
|-----|-------------------------|----------------------------------|
| 200 | Успех                   | Метаданные возвращены.           |
| 400 | Неверный запрос         | Отсутствует файл или некорректный запрос. |
| 401 | Неавторизован           | Неверный или отсутствующий токен. |
| 404 | Не найдено              | Указанный файл не найден.        |
| 500 | Внутренняя ошибка сервера | Непредвиденный сбой сервера.     |

API возвращает стандартные HTTP-коды состояния вместе с объектом JSON ответа об ошибке, если применимо.

### Семейство облачных SDK

Использование SDK ускоряет разработку, скрывая низкоуровневые детали. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
---