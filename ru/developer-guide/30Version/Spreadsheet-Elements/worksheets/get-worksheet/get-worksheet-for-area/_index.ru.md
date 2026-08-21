---
title: "Экспорт области рабочего листа в PNG, PDF, CSV — Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Область"
type: docs
url: /ru/worksheets/area-to-different-formats/
aliases: [  /ru/get-worksheet-for-area/ ]
keywords: "Aspose.Cells, экспорт области рабочего листа, PNG, PDF, CSV, конвертация Excel, REST API, SDK"
description: "Узнайте, как экспортировать определённый диапазон ячеек из рабочего листа Excel в форматы PNG, PDF, CSV и более чем в 20 других форматов с помощью Aspose.Cells Cloud REST API или SDK (C#, Java, Python и др.)."
weight: 230
ArticleTitle: "Экспорт области рабочего листа в PNG, PDF, CSV с помощью Aspose.Cells Cloud API — Полное руководство"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API позволяет конвертировать указанную область рабочего листа в различные форматы файлов. Поддерживаемые форматы: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

В данном руководстве показано, как экспортировать **конкретный диапазон ячеек** из рабочего листа Excel в PNG, PDF, CSV и более чем 20 других форматов с помощью Aspose.Cells Cloud API. Дополнительные сведения о смежных операциях, таких как экспорт всего рабочего листа или конвертация книги, см. на страницах **[Экспорт всего рабочего листа](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** и **[Конвертация книги в PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## REST API

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) определяет общедоступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

### Параметры запроса

| Параметр             | Тип    | Обязательный | Описание                                      |
|----------------------|--------|-------------|-----------------------------------------------|
| `name`               | string | Да          | Имя файла книги.                              |
| `sheetName`          | string | Да          | Имя целевого рабочего листа.                  |
| `format`             | string | Да          | Желаемый выходной формат (png, pdf, csv и др.).|
| `area`               | string | Нет         | Диапазон экспортируемых ячеек (например, `B3:K8`). |
| `verticalResolution`| int    | Нет         | Вертикальное разрешение (DPI) для растровых форматов. |
| `horizontalResolution`| int  | Нет         | Горизонтальное разрешение (DPI) для растровых форматов. |
| `folder`             | string | Нет         | Папка облачного хранилища, содержащая файл.   |
| `storage`            | string | Нет         | Имя сервиса хранилища.                        |

### Успешный ответ

* **200 OK** – Возвращает запрошенный файл в бинарном формате (PNG, PDF, CSV и др.).

### Ответы об ошибках

| Код состояния | Описание                                         |
|---------------|--------------------------------------------------|
| 400           | Неверный запрос — отсутствующие или некорректные параметры. |
| 401           | Неавторизован — отсутствует или недействителен токен аутентификации. |
| 404           | Не найдено — указанная книга или рабочий лист не существуют. |
| 500           | Внутренняя ошибка сервера — непредвиденное состояние на сервере. |

**Пример ошибочного ответа**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "Неверный формат параметра 'area'. Ожидаемый формат: B3:K8."
  }
}
```

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Преобразованное изображение (бинарный PNG)

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на логике вашего проекта. Полный список SDK Aspose.Cells Cloud см. в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

В приведённых ниже примерах кода показано, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}