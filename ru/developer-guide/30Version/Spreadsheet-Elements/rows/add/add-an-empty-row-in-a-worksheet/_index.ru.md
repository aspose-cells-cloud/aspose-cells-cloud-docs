---
title: "Добавление пустой строки в рабочий лист Excel"
ArticleTitle: "Добавление пустой строки в рабочий лист Excel с помощью API Aspose.Cells Cloud"
second_title: "Документ"
linktitle: "Строка"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, добавление пустой строки, рабочий лист, REST API, вставка строки, облачная электронная таблица"
description: "Используйте REST API Aspose.Cells Cloud для вставки пустой строки в рабочий лист Excel. Поддерживает множество SDK (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) для быстрой разработки."
weight: 20
---

Этот REST API добавляет новую строку в рабочий лист Excel. Он вставляет пустую строку по указанному индексу (начинается с нуля).

**Необходимые условия:**  
- В заголовке `Authorization` должен быть указан действующий токен доступа Aspose Cloud (Bearer JWT).  
- Целевая рабочая книга должна быть загружена в облачное хранилище Aspose Cloud, а параметры `folder` и `storageName` должны указывать на её расположение.

**Примечания:**  
- Индекс строки (`rowIndex`) нумеруется с нуля; вставка по индексу 0 добавляет строку в начало рабочего листа.  
- Максимальное количество строк в рабочем листе Excel составляет 1 048 576; попытка вставить строку за пределами этого лимита приведёт к

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Местоположение | Описание                                                   |
| ------------- | ------ | -------------- | ---------------------------------------------------------- |
| name          | string | path           | Имя файла рабочей книги.                                   |
| sheetName     | string | path           | Имя рабочего листа.                                        |
| rowIndex      | integer| path           | Нулевой индекс, по которому будет вставлена новая строка. |
| folder        | string | query          | Путь к папке в хранилище, где находится рабочая книга.    |
| storageName   | string | query          | Имя облачного хранилища Aspose Cloud, которое следует использовать. |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) определяет общедоступное программное интерфейсное описание и позволяет выполнять взаимодействие по REST напрямую из веб-браузера.

Вы можете легко использовать утилиту командной строки cURL для доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует, как делать вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Примечание:** Все конечные точки Aspose.Cells Cloud используют HTTPS. Для рабочих вызовов используйте защищённую схему `https://`.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр применён успешно; в ответе содержатся детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                 |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер.         |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                        |

*Пример ответа об ошибке (например, если индекс строки выходит за пределы допустимого диапазона):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Индекс строки вне допустимого диапазона. Максимально допустимое количество строк: 1048576."
}
```

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории на GitHub</a>.

Примеры кода ниже демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}