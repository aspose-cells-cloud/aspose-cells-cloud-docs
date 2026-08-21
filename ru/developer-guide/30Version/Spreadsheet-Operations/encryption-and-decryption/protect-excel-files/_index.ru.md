---
title: "Защита файлов Excel"
second_title: "Документ"
linktype: "Шифрование файлов Excel"
type: docs
url: /protect-excel-files/
aliases:
  [
    /protect/without-storage/,
    /protect/without-using-storage/,
    /protect/without-using-storage/,
  ]
keywords: "Aspose.Cells, API защиты Excel, шифрование рабочей книги Excel, безопасность облачных электронных таблиц, REST API"
description: "Используйте REST API Aspose.Cells Cloud для защиты файлов Excel. В этом руководстве показано, как зашифровать рабочие книги с помощью HTTP POST, cURL и SDK для множества языков программирования (по состоянию на 2026 год)."
weight: 40
---

Этот REST API защищает файлы Excel.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Параметры запроса

| Имя параметра | Тип   | Местоположение            | Описание                              |
| ------------- | ----- | ------------------------- | ------------------------------------- |
| file          | file  | formData (тело)           | Загружаемый файл                      |
| password      | string| строка запроса (`password`) | Пароль, используемый для защиты рабочей книги |

### Ответ


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "защищённое имя файла: smaple1.xlsx",
      "FileSize": размер,
      "FileContent": "-----Base64-строка sample1-----"
    },
    {
      "Filename": "защищённое имя файла: sample2.xlsx",
      "FileSize": размер,
      "FileContent": "-----Base64-строка sample2-----"
    }
  ]
}
```

**Коды HTTP-статусов**

| Код | Значение                    | Описание                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (ОК)                    | Фильтр успешно применён; ответ содержит детали операции. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизован) | Неверный или отсутствующий JWT-токен. |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает ограничение по размеру. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostProtect с SDK

### Спецификация API PostProtect

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-строка sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-строка sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Обработка ошибок**

– API может возвращать следующие коды состояния:

| HTTP-код | Значение                                 | Пример JSON-сообщения об ошибке                    |
| -------- | ---------------------------------------- | -------------------------------------------------- |
| 400      | Неверный запрос (например, отсутствует файл) | `{"Code":400,"Message":"Файл обязателен."}`        |
| 401      | Неавторизован (неверный или отсутствующий токен) | `{"Code":401,"Message":"Неверный токен доступа."}` |
| 403      | Запрещено (недостаточно прав)           | `{"Code":403,"Message":"Доступ запрещён."}`       |
| 500      | Внутренняя ошибка сервера               | `{"Code":500,"Message":"Непредвиденная ошибка сервера."}` |

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK берёт на себя работу с низкоуровневыми деталями, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен на [GitHub-репозитории](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}