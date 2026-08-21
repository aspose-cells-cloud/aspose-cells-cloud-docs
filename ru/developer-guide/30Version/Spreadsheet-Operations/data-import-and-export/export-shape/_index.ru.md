---
title: "Экспорт фигур"
second_title: "Документ"
linktitle: "Фигура"
type: docs
url: /ru/export-excel-shape-to-different-formats/
aliases: [  /ru/export/excel-shape-to-different-formats/ ]
keywords: "Экспорт фигур, Aspose.Cells Cloud, экспорт фигур Excel, форматы изображений, REST API, SDK"
description: "Узнайте, как экспортировать фигуры Excel в различные форматы изображений (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) с использованием Aspose.Cells Cloud REST API и SDK."
weight: 20
ArticleTitle: "Экспорт фигур – Aspose.Cells Cloud"
---

Экспорт фигур из Excel позволяет повторно использовать диаграммный контент в различных платформах и приложениях. **Необходимые условия:** действительный JWT-токен доступа и исходный файл Excel для загрузки.

Вы можете экспортировать фигуры в следующие форматы: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## API PostExport

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.


### Параметры запроса

| Имя параметра | Тип   | Путь/Строка запроса/HTTP-тело | Обязательный | Описание |
|---------------|-------|-------------------------------|-------------|----------|
| file          | file  | formData                      | Да          | Файл для загрузки |
| objectType    | string | query                        | Да          | Тип экспортируемого объекта. Для экспорта диаграмм используйте `chart`. Допустимые значения включают `shape`, `worksheet`, `picture` и др. |
| format        | string | query                        | Да          | Желаемый выходной формат. Поддерживаемые значения: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Пример запроса**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Ответ

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... дополнительные объекты файлов ...
  ]
}
```

*Типичные объемы содержимого файлов в кодировке Base64 варьируются от нескольких сотен байт до нескольких мегабайт в зависимости от размеров изображения и используемого формата.*

**Коды HTTP-статуса**

| Код | Значение                | Описание |
|-----|-------------------------|----------|
| 200 | OK (ОК)                 | Фигуры успешно экспортированы; в ответе содержится список файлов. |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры запроса. |
| 401 | Unauthorized (Неавторизован) | Недопустимый или отсутствующий токен доступа. |
| 413 | Payload Too Large (Слишком большой Payload) | Загруженный файл превышает лимит размера. |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |


## Как использовать API PostExport с SDK

### Спецификация API PostExport

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет публично доступное программное интерфейсное описание и позволяет выполнять взаимодействие с REST API прямо из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как вызвать облачный API с помощью cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ разработки для Aspose.Cells Cloud. SDK абстрагирует низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}