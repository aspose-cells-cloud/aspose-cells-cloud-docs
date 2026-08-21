---
title: "Добавление водяного знака в файлы Excel"
second_title: "Документ"
linktype: "Add Watermark to Excel Files"
type: docs
url: /add-watermark-into-excel-files/
aliases: [/watermark/]
keywords: "добавление водяного знака в Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Узнайте, как добавить текстовый водяной знак в книги Excel с помощью Aspose.Cells Cloud REST API (v3.0). Приведён пример cURL, перечислены обязательные параметры и детали ответа."
weight: 39
ArticleTitle: "Добавление водяного знака в файлы Excel – Документация Aspose.Cells Cloud"
---

Этот REST API добавляет **водяной знак** в файлы Excel.

**Необходимые условия:** Вы должны получить действительный JWT-токен доступа и убедиться, что файл Excel находится в поддерживаемом формате (например, `.xlsx`, `.xls`).  
**Описание:** Водяной знак — это полупрозрачное текстовое наложение, применяемое к каждому листу для указания права собственности или конфиденциальности.

## API PostWatermark

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Расположение               | Описание                                                       |
|---------------|-------|----------------------------|----------------------------------------------------------------|
| `file`        | file  | formData (multipart body)  | Файл Excel, к которому будет применён водяной знак.           |
| `text`        | string| query                      | Текст водяного знака для отображения.                          |
| `color`       | string| query                      | Цвет водяного знака в формате ARGB в шестнадцатеричном виде (например, `004433ff`). |

### **Ответ**

JSON-ответ содержит массив **Files**. Для каждого объекта файла:

- **Filename** – имя обработанной рабочей книги.  
- **FileSize** – размер файла в байтах.  
- **FileContent** – содержимое файла Excel с водяным знаком, закодированное в Base64; для получения фактического файла его нужно декодировать.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[имя файла1]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[имя файла2]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[имя файла3]",
            "Filesize" : [размер файла],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                        |
|-----|-----------------------------|-----------------------------------------------------------------|
| 200 | OK                          | Водяной знак успешно применён; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен.                  |
| 413 | Payload Too Large           | Загруженный файл превышает ограничение по размеру.              |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                  |

## Как использовать API PostWatermark с SDK

### Спецификация API PostWatermark

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для вызова веб-сервисов Aspose.Cells. Пример ниже показывает полный запрос, включая обязательный заголовок аутентификации. Замените `<your‑jwt‑token>` на действительный JWT-токен доступа, полученный из точки аутентификации Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}