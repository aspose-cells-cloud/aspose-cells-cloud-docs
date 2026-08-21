---
title: "Создание пустой рабочей книги Excel"
second_title: "Документ"
linktitle: "Пустая рабочая книга"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, пустая рабочая книга, REST API, SDK"
description: "Узнайте, как создать пустую рабочую книгу Excel с помощью Aspose.Cells Cloud REST API. Примеры на cURL и SDK."
weight: 20
ArticleTitle: "Создание пустой рабочей книги Excel с помощью Aspose.Cells Cloud API"
---

Этот REST API создает **пустую рабочую книгу**.

## API PutWorkbookCreate

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе токена JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Описание                                                       |
|---------------|--------|----------------------------------------------------------------|
| templateFile  | string | Путь к шаблонной рабочей книге, используемой в качестве основы (необязательно). |
| dataFile      | string | Путь к файлу данных для заполнения рабочей книги (необязательно). |
| isWriteOver   | boolean | `true` — перезаписать существующий файл; `false` — иначе.      |
| folder        | string | Папка назначения для созданной рабочей книги (необязательно).  |
| storageName   | string | Имя используемого сервиса хранения.                            |

### Параметр тела запроса

| Имя параметра | Тип | Описание                                   |
|---------------|-----|--------------------------------------------|
| data          | file | Двоичное содержимое создаваемого файла рабочей книги. |

### **Ответ**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Условие возврата                        |
|-----|-----------------------------|-----------------------------------------|
| 200 OK | Рабочая книга успешно создана | Нормальный сценарий выполнения           |
| 201 Created | Рабочая книга создана (альтернативный ответ) | Когда API возвращает статус «создано» |
| 400 Bad Request | Некорректные параметры | Ошибка со стороны клиента               |
| 401 Unauthorized | Отсутствует или недействителен токен | Ошибка аутентификации                  |
| 409 Conflict | Файл существует, а `isWriteOver=false` | Конфликт с существующим файлом         |

## Как использовать API PutWorkbookCreate с SDK

### Спецификация API PutWorkbookCreate

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для доступа к веб-сервисам Aspose.Cells. Добавьте заголовок `Authorization` с действительным токеном OAuth2/JWT. Для пустой рабочей книги тело запроса является необязательным; если необходимо загрузить файл, добавьте `--data-binary @empty.xlsx`, как показано ниже.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Создать пустую рабочую книгу с именем newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Пропустите эту строку для действительно пустой рабочей книги
```

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

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}