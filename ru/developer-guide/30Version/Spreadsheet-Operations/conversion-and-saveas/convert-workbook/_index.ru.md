---
title: "Преобразование файла Excel в различные форматы"
second_title: "Документ"
linktitle: "Преобразование электронной таблицы"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "преобразование Excel, преобразование электронных таблиц, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, преобразование форматов файлов"
description: "Используйте Aspose.Cells Cloud REST API для преобразования рабочих книг Excel в различные форматы, такие как PDF, CSV, JSON и Markdown. API поддерживает множество SDK для языков программирования, включая C#, Java, Python и другие."
weight: 10
ArticleTitle: "Преобразование файла Excel в различные форматы – Руководство по API Aspose.Cells Cloud"
---

Этот REST API преобразует файл Excel в другой формат. Он поддерживает широкий спектр выходных форматов и позволяет настроить параметры страницы и сохранения перед преобразованием.

## API PostConvertWorkBook

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

Перед использованием этого API убедитесь, что у вас есть действительный JWT-токен и установлено соответствующее SDK Aspose.Cells Cloud для вашего языка программирования.

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

## Как использовать API PostConvertWorkBook с SDK

### Спецификация API PostConvertWorkBook

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) определяет общедоступное программное интерфейсное взаимодействие и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В приведённом ниже примере показано, как вызвать облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — самый быстрый способ разработки. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на проекте. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---