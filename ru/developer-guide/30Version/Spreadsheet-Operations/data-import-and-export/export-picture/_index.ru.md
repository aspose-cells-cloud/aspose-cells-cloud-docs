---
title: "Экспорт изображения"
second_title: "Документ"
linktitle: "Изображение"
type: docs
url: /ru/export-excel-picture-to-different-formats/
aliases: [  /ru/export/excel-picture-to-different-formats/ ]
keywords: "Экспорт изображения, Aspose.Cells Cloud, REST API, Excel, Форматы изображений, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "Экспортируйте изображения из Excel в различные форматы изображений с помощью REST API Aspose.Cells Cloud. Сервис поддерживает SDK для множества языков программирования, включая C#, Java, PHP, Ruby, Node.js, Python, Perl, Go и Swift."
weight: 20
---

Вы можете экспортировать изображения в следующие форматы: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), и [WMF](https://docs.fileformat.com/image/Wmf/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.


### Параметры запроса

| Параметр        | Место размещения | Тип   | Обязательный | Описание                                                                 |
| --------------- | ---------------- | ----- | ------------ | ------------------------------------------------------------------------ |
| `file`          | Form‑data         | file  | Да           | Рабочая книга Excel (`.xlsx`, `.xls` и т.д.), содержащая OLE-объекты.   |
| `outputFormat`  | Query             | string| Да           | Целевой формат экспортируемых объектов (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Query             | string| Да           | Фиксированное значение `oleobject`.                                     |


### Ответ

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**Коды HTTP-статуса**

| Код  | Значение                    | Описание                                                     |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Фильтр успешно применён; ответ содержит сведения о операции. |
| 400  | Bad Request                 | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized                | Недействительный или отсутствующий JWT-токен.               |
| 413  | Payload Too Large           | Загруженный файл превышает лимит размера.                    |
| 500  | Internal Server Error       | Непредвиденная ошибка сервера.                               |

## Как использовать API PostExport с SDK

### Спецификация API PostExport

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) определяет общедоступное программное интерфейсное API и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Использование SDK Aspose.Cells Cloud

Использование SDK — наиболее эффективный способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на логике вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}