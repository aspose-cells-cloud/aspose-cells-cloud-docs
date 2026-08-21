---
title: "Удаление фонового изображения из книги Excel"
second_title: "Документ"
linktitle: "Удалить"
type: docs
url: /ru/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells удаление фона, Excel API удаление фона, Aspose.Cells Cloud, DELETE /cells background"
description: "Удаление фонового изображения из книги Excel с помощью API Aspose.Cells Cloud. Изучите конечную точку DELETE, необходимые параметры, пример cURL и код SDK на C#, Java, Python и других языках."
weight: 170
ArticleTitle: "Удаление фонового изображения из книги Excel с помощью API Aspose.Cells Cloud"
---

Этот REST API удаляет фоновое изображение книги Excel.

## API DeleteWorkbookBackground

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud безопасны и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Описание                                         | Обязательный |
| -------------- | ------ | ------------------------------------------- | -------- |
| folder         | string | Папка, содержащая исходную книгу. | Нет       |
| storageName    | string | Имя используемого сервиса хранилища.         | Нет       |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP-коды состояния**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр успешно применён; ответ содержит подробности операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)                | Недействительный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой полезный груз)           | Загружаемый файл превышает лимит размера. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |

## Как использовать API DeleteWorkbookBackground с SDK

### Спецификация API DeleteWorkbookBackground

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание, позволяющее выполнять взаимодействие с REST напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Приведённый ниже пример демонстрирует полный DELETE-запрос с необходимым заголовком аутентификации; тело запроса не требуется.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы получить полный список SDK Aspose.Cells Cloud.

Приведённые ниже примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}