---
title: "Замена текста в файлах Excel"
second_title: "Документ"
linktitle: "Замена без использования хранилища"
type: docs
url: /ru/replace/
keywords: "замена текста в Excel, Aspose.Cells Cloud, REST API, замена в электронных таблицах, API, замена текста в файле Excel"
description: "Используйте REST API Aspose.Cells Cloud для замены существующего текста новыми значениями в файлах Excel. Поддерживает SDK для C#, Java, Python, Node.js, PHP, Ruby, Go и Perl."
weight: 80
---


## REST API

Этот REST API заменяет данные в файлах Excel.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Безопасность и аутентификация

API Aspose.Cells Cloud безопасны и требуют [аутентификации на основе токена JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Параметры запроса

| Имя параметра | Тип   | Расположение         | Описание                                         |
|--------------|-------|---------------------|--------------------------------------------------|
| **file**     | файл  | formData (multipart) | Обрабатываемый файл Excel.                      |
| **text**     | строка | query               | Текстовая строка, подлежащая замене.            |
| **newtext**  | строка | query               | Текст замены.                                   |
| **password** | строка | query               | Пароль для защищённой рабочей книги (необязательно). |
| **sheetname**| строка | query               | Имя целевого листа (необязательно).             |

### **Ответ**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[имя файла1]",
      "Filesize" : [размер файла],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[имя файла2]",
      "Filesize" : [размер файла],
      "FileContent" : "[Base64String]"
    },
    {
      "Filename" : "[имя файла3]",
      "Filesize" : [размер файла],
      "FileContent" : "[Base64String]"
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий токен JWT. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostReplace с SDK

### Спецификация API PostReplace

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

---