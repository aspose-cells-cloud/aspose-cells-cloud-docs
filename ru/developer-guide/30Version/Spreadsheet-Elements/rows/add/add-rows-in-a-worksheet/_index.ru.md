---
title: "Добавление нескольких строк в рабочий лист Excel"
ArticleTitle: "Добавление нескольких строк в рабочий лист Excel с использованием API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Строки"
type: docs
url: /ru/rows/add/rows/
keywords: "Aspose.Cells Cloud, вставка строк, рабочий лист Excel, REST API, SDK, добавление нескольких строк"
description: "Узнайте, как использовать REST API Aspose.Cells Cloud для вставки нескольких строк в рабочий лист Excel. В этом руководстве описаны конечная точка API, параметры запроса, примеры команд cURL и примеры использования SDK."
weight: 20
---

Этот REST API добавляет несколько новых строк в рабочий лист Excel.

## API PutInsertWorksheetRows

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### **Параметры запроса**

| Имя параметра  | Тип     | Местоположение | Описание                                                                 |
| --------------- | ------- | ------------- | ------------------------------------------------------------------------ |
| name            | string  | path          | Имя рабочей книги.                                                       |
| sheetName       | string  | path          | Имя рабочего листа.                                                      |
| startrow        | integer | query         | Индекс первой вставляемой строки (**с нуля**).                           |
| totalRows       | integer | query         | Количество вставляемых строк.                                            |
| updateReference | boolean | query         | Необходимо ли обновлять ссылки на ячейки после вставки (`true` или `false`). |
| folder          | string  | query         | Папка, содержащая документ.                                              |
| storageName     | string  | query         | Имя хранилища.                                                           |

**Предварительные требования**  
Рабочая книга должна уже существовать в указанном хранилище (или папке) перед вызовом этой операции.

**Аутентификация**  
API требует действительный токен JWT. Включите его в заголовок `Authorization`, как показано в примере cURL ниже.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) определяет доступный для публичного использования программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует вызов Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Примечание:** Эта операция `PUT` не требует тело запроса; пустой JSON-объект (`{}`) можно отправить, если клиентская библиотека требует наличие полезной нагрузки.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Возможные коды ответа*  

- **200 OK** – строки успешно вставлены.  
- **400 Bad Request** – недопустимые параметры (например, отрицательный индекс строки).  
- **401 Unauthorized** – отсутствует или недействителен токен JWT.  
- **404 Not Found** – указанная рабочая книга или рабочий лист не найдены.  
- **500 Internal Server Error** – непредвиденная ошибка сервера.

{{< /tab >}}

{{< /tabs >}}

Дополнительные операции со строками см. на смежных страницах: **Удаление строк**, **Получение строк** и **Копирование строк**.

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK берет на себя обработку низкоуровневых деталей, позволяя сосредоточиться на вашем проекте. Пожалуйста, ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}