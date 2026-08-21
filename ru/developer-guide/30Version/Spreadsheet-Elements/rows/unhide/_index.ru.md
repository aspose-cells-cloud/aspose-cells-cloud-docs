---
title: "Отменить скрытие строк на листе Excel"
second_title: "Документ"
linktitle: "Отменить скрытие"
type: docs
url: /ru/rows/unhide/
aliases: [  /ru/unhide-rows-in-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, отменить скрытие строк, REST API, электронная таблица, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, Aspose.Cells Cloud REST API"
description: "Используйте Aspose.Cells Cloud REST API для отмены скрытия строк на листе Excel. API доступно через множество SDK, включая .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl и Swift."
weight: 50
ArticleTitle: "Отменить скрытие строк на листе Excel с помощью Aspose.Cells Cloud API"
---

Этот REST API отменяет скрытие строк на листе Excel.

**Необходимые условия:** Получите действительный JWT-токен доступа из службы аутентификации Aspose Cloud и убедитесь, что целевая рабочая книга загружена в поддерживаемое хранилище перед вызовом этой конечной точки.

## API PostUnhideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип    | Расположение | Описание                                          |
| ------------- | ------ | ----------- | ------------------------------------------------- |
| name          | string | path        | Имя рабочей книги.                                |
| sheetName     | string | path        | Имя листа.                                        |
| startrow      | integer | query      | Индекс первой строки (начиная с 0) для отмены скрытия. |
| totalRows     | integer | query      | Количество строк для отмены скрытия.              |
| height        | number | query       | Высота строки (по умолчанию 15.0).               |
| folder        | string | query       | Папка документа.                                  |
| storageName   | string | query       | Имя хранилища.                                    |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

**Аутентификация**  
Все запросы должны проходить аутентификацию с использованием JWT-токена доступа, полученного из службы аутентификации Aspose Cloud. Включите токен в заголовок `Authorization: Bearer <jwt token>`.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# Примечание: тело POST-запроса для этой конечной точки пусто
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

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                          |
|-----|----------------------------|--------------------------------------------------|
| 200 | OK (OK)                    | Фильтр успешно применён; ответ содержит подробности операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Некорректный или отсутствующий JWT-токен.        |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

Для подробной устранения неполадок см. [Руководство по обработке ошибок](/ru/error-handling/).

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}