---
title: "Разделить файл Excel на несколько файлов"
second_title: "Документ"
linktype: "Разделить несколько файлов Excel"
type: docs
url: /ru/split-an-excel-file-to-multi-files/
aliases: [  /ru/split-excel-workbooks/ , /ru/workbook/split/ ]
keywords: "Aspose.Cells, Cloud, Excel, разделение, API, PDF, CSV, JSON"
description: "Используйте Aspose.Cells Cloud REST API для разделения многостраничных рабочих книг Excel на отдельные файлы. Поддерживаются выходные форматы, такие как PDF, CSV и JSON, доступ через SDK для Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
weight: 32
ArticleTitle: "Разделить файл Excel на несколько файлов — Документация Aspose.Cells Cloud"
---

Aspose.Cells Cloud REST API позволяет разделить многостраничные рабочие книги Excel на отдельные файлы.

**Необходимые условия**  
Перед вызовом API необходимо получить действующий JWT-токен и включить его в заголовок `Authorization` каждого запроса. Подробности см. в [руководстве по аутентификации](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API PostSplit

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение | Описание                                                        |
|---------------|--------|-------------|------------------------------------------------------------------|
| file          | file   | formData    | Загружаемая рабочая книга Excel.                                |
| format        | string | query       | Желаемый выходной формат (например, `pdf`, `csv`, `json`).      |
| password      | string | query       | Пароль для зашифрованной рабочей книги (необязательно).         |
| from          | integer| query       | Индекс первого включаемого листа (нумерация с 1).               |
| to            | integer| query       | Индекс последнего включаемого листа (включительно).             |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[имя файла 1]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[имя файла 2]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[имя файла 3]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                     |
|-----|-----------------------------|--------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр применён успешно; ответ содержит данные об операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                        |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка на стороне сервера. |

## Как использовать API PostSplit с SDK

### Спецификация API PostSplit

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) определяет публично доступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

**Коды HTTP-статуса**

| Код | Значение                        | Описание                                                         |
|-----|---------------------------------|------------------------------------------------------------------|
| 200 | OK (OK)                         | Рабочая книга успешно разделена; ответ содержит список файлов.  |
| 400 | Bad Request (Неверный запрос)   | Отсутствуют или неверны параметры (например, неподдерживаемый формат). |
| 401 | Unauthorized (Неавторизовано)   | Неверный или отсутствующий JWT-токен.                            |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Произошла непредвиденная ошибка на стороне сервера. |

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Замените xxxxx1.xlsx и xxxxx2.xlsx на пути к вашим файлам Excel
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}