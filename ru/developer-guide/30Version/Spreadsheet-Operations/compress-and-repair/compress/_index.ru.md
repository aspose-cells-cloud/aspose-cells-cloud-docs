---
title: "Сжатие данных в файле Excel"
ArticleTitle: "Сжатие данных в файле Excel – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Сжатие файлов Excel"
type: docs
url: /compress-excel-files/
aliases: [/compress/]
keywords: "сжатие файла Excel, Aspose Cells Cloud, сжатие Excel, сжатие электронных таблиц, REST API, сжатие файлов"
description: "Сжимайте файлы Excel (XLS, XLSX, XLSM, XLSB, ODS) с помощью REST API Aspose.Cells Cloud. Настраивайте уровень сжатия, обрабатывайте несколько файлов и интегрируйтесь через SDK."
weight: 39
---

## API PostCompress веб-сервисов Aspose.Cells Cloud

**Необходимые условия:**  
- Для аутентификации требуется действительный JWT-токен.  
- Поддерживаемые форматы файлов: XLS, XLSX, XLSM, XLSB и ODS.  
- Максимальный допустимый размер файла: 500 МБ на запрос (ограничения сервиса могут варьироваться).

Этот REST API сжимает данные в файле Excel.

- Сжатие XLS, XLSX, XLSM, XLSB, ODS  
- Быстрое сжатие нескольких файлов электронных таблиц Excel  
- Выбор уровня сжатия  
- Поддержка нескольких файлов  

### Конечная точка веб-API

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### Параметры запроса

| Имя параметра | Тип    | Путь/Строка запроса/Тело HTTP-запроса | Описание                                                |
|---------------|--------|----------------------------------------|----------------------------------------------------------|
| file          | file   | formData                               | Файл для загрузки                                        |
| CompressLevel | integer | query                                  | Уровень сжатия (0–100); более высокие значения означают более сильное сжатие |

### Параметр тела запроса

| Имя параметра | Тип | Описание                                            |
| ------------- | --- | --------------------------------------------------- |
| data          | file | Двоичное содержимое файла рабочей книги для сжатия. |

### **Ответ**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[имя объединённого файла]",
    "Filesize" : [размер файла],
    "FileContent" : "[Base64String]"
}
```

*Примечание:* `FileContent` содержит сжатую рабочую книгу, закодированную в формате Base64. Длина строки соответствует размеру сжатого файла; вы можете декодировать её с помощью стандартных средств Base64, чтобы получить двоичный файл Excel.

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK                          | Фильтр применён успешно; ответ содержит подробности операции. |
| 400 | Bad Request                 | Отсутствующие или некорректные параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Неверный или отсутствующий JWT-токен.                     |
| 413 | Payload Too Large           | Загруженный файл превышает лимит размера.                 |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                            |

## Как использовать API PostCompress с SDK

### Спецификация API PostCompress

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
# Используйте HTTPS для безопасного подключения
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ ускорить разработку. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с помощью различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}
---