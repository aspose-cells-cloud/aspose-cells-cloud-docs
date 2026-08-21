---
title: "Преобразование листа в PDF, PNG, CSV и другие форматы – Aspose.Cells Cloud API"
second_title: "Документ"
linktitle: "Преобразование листа"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, преобразование листа, REST API, cURL, SDK, PDF, PNG, CSV"
description: "Узнайте, как преобразовать отдельный лист из рабочей книги Excel в PDF, PNG, CSV и более 15 других форматов с помощью Aspose.Cells Cloud REST API. Приведены примеры cURL, фрагменты кода SDK и полная справка по параметрам."
weight: 130
ArticleTitle: "Преобразование листа в PDF, PNG, CSV и другие форматы – Aspose.Cells Cloud API"
---

**API для преобразования листов** — конечная точка `GET /cells/{name}/worksheets/{sheetName}` преобразует отдельный лист (лист внутри рабочей книги Excel) в другой файловый формат.

> **Необходимое условие:** Перед вызовом данной конечной точки у вас должен быть действительный JWT-токен и рабочая книга, сохранённая в поддерживаемом хранилище Aspose Cloud.

Поддерживаемые **импортируемые** форматы (из которых можно считать лист):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Поддерживаемые **только для экспорта** форматы (в которые можно сохранить лист):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST API

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) описывает публично доступный интерфейс.

### **Параметры запроса**

| Параметр                 | Тип     | Обязательный | Значение по умолчанию | Допустимые значения                                                  | Описание                                            |
| ------------------------ | ------- | ------------ | --------------------- | -------------------------------------------------------------------- | --------------------------------------------------- |
| **format**               | string  | Да           | –                     | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (см. поддерживаемый список) | Целевой формат вывода.                              |
| **verticalResolution**   | integer | Нет          | 96                    | 72‑600                                                               | Вертикальное разрешение (DPI) для вывода изображения. |
| **horizontalResolution** | integer | Нет          | 96                    | 72‑600                                                               | Горизонтальное разрешение (DPI) для вывода изображения. |
| **password**             | string  | Нет          | –                     | –                                                                    | Пароль для открытия защищённой рабочей книги.       |
| **folder**               | string  | Нет          | –                     | –                                                                    | Облачная папка, в которой хранится исходная рабочая книга. |
| **storage**              | string  | Нет          | –                     | –                                                                    | Имя хранилища (например, «Default»).                |

### Ответ

| Код статуса | Описание                                                                  | Тип возвращаемых данных    |
| ----------- | ------------------------------------------------------------------------- | -------------------------- |
| **200**     | Преобразование успешно завершено; возвращается двоичный поток преобразованного файла. | `application/octet-stream` |
| **400**     | Неверный запрос — отсутствуют или недопустимы параметры.                 | Объект ошибки JSON         |
| **401**     | Неавторизованный доступ — недействительный или отсутствующий JWT-токен. | Объект ошибки JSON         |
| **404**     | Не найдено — рабочая книга или лист не существуют.                       | Объект ошибки JSON         |
| **500**     | Внутренняя ошибка сервера — непредвиденное завершение.                   | Объект ошибки JSON         |

#### Пример запроса (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Пример ответа

```
Преобразованное изображение (двоичный поток)
```

## Семейство облачных SDK

Использование SDK — самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на вашем проекте. Полный список облачных SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют вызов веб-служб Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---