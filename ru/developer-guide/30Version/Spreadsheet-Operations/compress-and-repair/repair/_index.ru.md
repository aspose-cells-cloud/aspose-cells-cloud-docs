---
title: "Восстановление файлов Excel"
second_title: "Документ"
type: docs
linktitle: "Восстановление файлов Excel"
url: /ru/repair-excel-files/
keywords: "Aspose Cells, API для восстановления Excel, поврежденный XLSX, восстановление электронных таблиц, облачный API"
description: "Используйте облачный REST API Aspose.Cells для восстановления поврежденных файлов Excel (XLS, XLSX, XLSM, XLSB, ODS). Загрузите один или несколько файлов, выберите формат выходного файла и получите восстановленные файлы в формате Base64. Установка не требуется."
weight: 39
---

Этот REST API позволяет **восстанавливать** файлы Excel.

- Восстанавливайте файлы XLS, XLSX, XLSM, XLSB, ODS и другие форматы электронных таблиц.  
- Поддерживается загрузка нескольких файлов в одном запросе.

Aspose.Cells Cloud для восстановления Excel позволяет онлайн-восстанавливать данные из поврежденных файлов Excel без установки какого-либо программного обеспечения. Поврежденные файлы Excel создают проблемы, так как их невозможно открыть. Вы можете воспользоваться приложением Aspose.Cells Cloud для восстановления Excel, чтобы извлечь данные из таких файлов.

## REST API

Конечная точка **Repair Excel Files** восстанавливает поврежденные файлы электронных таблиц и возвращает восстановленное содержимое.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра | Тип   | Расположение                     | Описание |
|---------------|--------|----------------------------------|----------|
| file          | file   | formData (multipart)             | Файл для загрузки |
| format        | string | query                            | Желаемый выходной формат. Если не указан (null), выходной формат по умолчанию совпадает с форматом входного файла. |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[имя файла]",
    "Filesize" : [размер файла],
    "FileContent" : "[Base64String]"
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                            |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400 | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Недействительный или отсутствующий JWT-токен. |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера. |

## Как использовать API PostRepair с SDK

### Спецификация API PostRepair

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

При успешном выполнении сервис возвращает HTTP 200 с JSON-полезной нагрузкой, содержащей массив `Files`. В случае ошибок API использует стандартные HTTP-коды статуса:

- **400 Bad Request** — Недопустимые параметры или неподдающийся восстановлению файл.  
- **401 Unauthorized** — Отсутствует или недействителен JWT-токен.  
- **413 Payload Too Large** — Загруженный файл превышает допустимый размер.  
- **500 Internal Server Error** — Непредвиденная ошибка на стороне сервера.

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы получить полный список SDK для Aspose.Cells Cloud.

В следующих примерах кода показано, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}