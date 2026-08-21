---
title: "Импорт данных без использования хранилища — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Импорт данных без хранилища"
type: docs
url: /ru/import/without-using-storage/
aliases: [  /ru/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, импорт данных без хранилища, API импорта Excel, REST-импорт"
description: "Узнайте, как импортировать данные в рабочую книгу Excel без использования хранилища с помощью Aspose.Cells Cloud API. Включает формат запроса, параметры, пример cURL, код SDK и обработку ошибок."
weight: 10
ArticleTitle: "Импорт данных без использования хранилища — Aspose.Cells Cloud API"
---

Импорт данных в Excel может быть сложным, поскольку на результат влияет множество факторов. Все эти факторы следует учитывать во время процесса **импорта**. Aspose.Cells Cloud упрощает импорт различных форматов и типов данных в файл Excel с качеством профессионального уровня.

Этот REST API импортирует **данные** в файл Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud являются защищёнными и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса:**

| Имя параметра | Тип          | Местоположение  | Описание                                                                                                                                     |
| -------------- | ------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| file           | файл          | formData  | Файл Excel для загрузки.                                                                                                                       |
| ImportOption   | ImportOption  | JSON-тело | JSON-объект, определяющий импортируемые данные, их тип (например, `IntArray`, `DoubleArray`, `StringArray`) и место размещения в листе. |

Параметры **ImportOption** описаны в справочнике по параметру **ImportData** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Необходимые условия:**  
JWT-токен должен быть сгенерирован заранее, а размер файла не должен превышать лимит сервиса (обычно 100 МБ). Поддерживаемые форматы файлов: XLS, XLSX, CSV и ODS. Если вы предпочитаете программный доступ, убедитесь, что установлен соответствующий SDK.

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                     | Описание                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (ОК)                          | Фильтр применён успешно; ответ содержит детали операции. |
| 400  | Bad Request (Неверный запрос)                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано)                | Неверный или отсутствующий JWT-токен. |
| 413  | Payload Too Large (Слишком большой payload)           | Загруженный файл превышает ограничение по размеру. |
| 500  | Internal Server Error (Внутренняя ошибка сервера)       | Непредвиденная ошибка сервера. |

**Примечания:**  
При отправке запроса заголовок `Content-Type: multipart/form-data` устанавливается автоматически с помощью флага `-F`. Для больших объёмов данных рекомендуется сжимать данные перед импортом и реализовывать логику повторных попыток для устранения временных ошибок.

## Как использовать API PostImportData с SDK

### Спецификация API PostImportData

[OpenAPI-спецификация](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как делать вызовы в Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*Флаг `-F` автоматически устанавливает `Content-Type: multipart/form-data`.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали и позволяет сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}