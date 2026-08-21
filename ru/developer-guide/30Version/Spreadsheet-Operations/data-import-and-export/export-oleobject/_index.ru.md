---
title: "Экспорт OLE-объекта — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "OLE-объект"
type: docs
url: /ru/export-excel-ole-object/
aliases: [  /ru/export/excel-ole-object/ ]
keywords: "Aspose.Cells, OLE-объект, экспорт, Excel, облачный API, PDF, PNG, DOCX, PPTX"
description: "Экспортируйте OLE-объекты из рабочей книги Excel с помощью Aspose.Cells Cloud API. Узнайте формат запроса, параметры, примеры cURL и обработку ошибок."
weight: 20
ArticleTitle: "Экспорт OLE-объекта — Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.


### Параметры запроса

| Параметр         | Местоположение | Тип   | Обязательный | Описание                                                                 |
| ---------------- | -------------- | ----- | ------------ | ------------------------------------------------------------------------ |
| `file`           | Form‑data      | файл  | Да           | Рабочая книга Excel (`.xlsx`, `.xls` и т.д.), содержащая OLE-объекты.   |
| `outputFormat`   | Query          | строка| Да           | Целевой формат экспортируемых объектов (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`     | Query          | строка| Да           | Фиксированное значение `oleobject`.                                     |


### Ответ

Успешный запрос возвращает JSON-объект со списком экспортированных файлов:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                      |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK (OK)                     | Фильтр применён успешно; ответ содержит данные о операции.   |
| 400 | Bad Request (Неверный запрос)| Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано)| Недействительный или отсутствующий токен JWT.                |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает допустимый размер. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Как использовать API PostExport с SDK

### Спецификация API PostExport

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия прямо из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Что такое OLE-объект?

**OLE-объект (Object Linking and Embedding)** встраивает внешнее содержимое — такое как документы Word, слайды PowerPoint, изображения или другие файлы — внутрь рабочей книги Excel. При экспорте вложенное содержимое извлекается и сохраняется в запрошенном выходном формате.

### Обзор конечной точки

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – должно быть установлено в значение `oleobject`.
- `format` – желаемый выходной формат (например, `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

В приведённых ниже примерах кода показано, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---