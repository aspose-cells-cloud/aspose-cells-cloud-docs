---
title: "Параметры преобразования рабочей книги"
second_title: "Документ"
linktitle: "Параметры преобразования рабочей книги"
type: docs
url: /ru/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, преобразование Excel, PDF, CSV, API"
description: "Параметры преобразования рабочей книги — настройка преобразования рабочей книги Excel в PDF, CSV, HTML и другие форматы с использованием API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "Параметры преобразования рабочей книги – API Aspose.Cells Cloud"
---

# Свойства ConvertWorkbookOptions

**Версия API:** 23.12 (2024‑03)

`ConvertWorkbookOptions` — это модель запроса, используемая API преобразования Aspose.Cells Cloud для указания способа трансформации рабочей книги Excel в другой формат (PDF, CSV, HTML и т.д.). Она объединяет информацию об исходном файле, целевой формат, настройки страницы и параметры сохранения, специфичные для формата.

| Имя                                 | Тип         | Описание                                                                                                           | Примечания |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------ | ---------- |
| **DataSource**                      | **Object**  | Источник данных файла: `CloudFileSystem`, `RequestFiles` или `HttpUri`.                                            |            |
| **[FileInfo](/ru/cells/file-info/)** | **Object**  | Описывает имя файла, его размер и содержимое в кодировке base64.                                                   |            |
| **[PageSetup](/ru/cells/page-setup/)** | **Object**  | Свойства настройки страницы, такие как поля, ориентация и масштаб.                                                 |            |
| **SaveOptions**                     | **Object**  | Контейнер для объектов параметров сохранения, специфичных для формата (например, `PdfSaveOptions`, `HtmlSaveOptions`). |            |
| **ConvertFormat**                   | **string**  | Целевой формат файла (например, **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF** и т.д.).                              |            |
| **CheckExcelRestriction**           | **boolean** | Получает или задаёт, следует ли применять ограничения, специфичные для Excel (максимальное количество строк, столбцов, длина имени листа и т.д.). |            |

**Предварительные требования**

- Получите действительный токен доступа OAuth 2.0 для Aspose.Cells Cloud.  
- Убедитесь, что исходный файл доступен через один из поддерживаемых типов `DataSource`.

**Быстрый пример**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64‑кодированное‑содержимое>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**Детали запроса API**

Операция преобразования выполняется с помощью **POST**-запроса к конечной точке:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Обязательные заголовки:

| Заголовок             | Значение                           |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

Тело запроса должно быть JSON-представлением `ConvertWorkbookOptions` (см. пример выше). Все свойства являются необязательными, если они не требуются выбранным значением `ConvertFormat`.

**Ответ API**

При успешном преобразовании возвращается **HTTP 200 OK** (или **202 Accepted** для асинхронной обработки) с преобразованным файлом, передаваемым в теле ответа. При потоковой передаче ответа заголовок `Content-Disposition` содержит предложенное имя файла.

Пример JSON-ответа для асинхронного запроса:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Коды состояния**

| Код | Значение                                     |
|-----|----------------------------------------------|
| 200 | Преобразование завершено; файл возвращён.    |
| 202 | Преобразование принято; результат будет доступен позже. |
| 400 | Неверный запрос — отсутствуют или некорректны параметры. |
| 401 | Неавторизован — неверный или отсутствующий токен. |
| 403 | Запрещено — недостаточно прав.              |
| 500 | Внутренняя ошибка сервера.                   |

**Примечания / Ограничения**

- Флаг `CheckExcelRestriction` применяет ограничения Excel, такие как максимальное количество строк (1 048 576) и столбцов (16 384).  
- Не все целевые форматы поддерживают каждое свойство `SaveOptions`; неподдерживаемые параметры игнорируются.  
- При использовании `HttpUri` в качестве источника данных URL должен быть общедоступным и не требовать аутентификации.  
- Информация о методе API и конечной точке добавлена для повышения ясности разработчиков и снижения вероятности ошибок при интеграции.  

## Свойства FileSource

| Имя свойства   | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                                                 |
| -------------- | ------------ | --------------- | ---------------- | --------------------- | ------------------------------------------------------------------------ |
| FileSourceType | String       | true            | false            |                       | Указывает тип источника (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath       | String       | true            | false            |                       | Путь к файлу.                                                            |

## Свойства DbfSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| ExportAsString            | Boolean      | true            | false            |                       | Если **true**, числовые значения экспортируются как строки. |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов DBF.                |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства DifSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов DIF.                |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства DocxSaveOptions

| Имя свойства                      | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                               |
| --------------------------------- | ------------ | --------------- | ---------------- | --------------------- | ------------------------------------------------------ |
| DefaultFont                       | String       | true            | false            |                       | Шрифт, используемый, когда исходный шрифт недоступен. |
| CheckWorkbookDefaultFont          | Boolean      | true            | false            |                       | Проверяет, применяется ли шрифт по умолчанию для рабочей книги. |
| CheckFontCompatibility            | Boolean      | true            | false            |                       | Проверяет совместимость шрифтов для целевого формата. |
| IsFontSubstitutionCharGranularity | Boolean      | true            | false            |                       | Управляет заменой шрифтов на уровне символов.         |
| OnePagePerSheet                   | Boolean      | true            | false            |                       | Принудительно размещает каждый лист на отдельной странице. |
| AllColumnsInOnePagePerSheet       | Boolean      | true            | false            |                       | Помещает все столбцы листа на одну страницу.          |
| IgnoreError                       | Boolean      | true            | false            |                       | Игнорирует некритические ошибки при преобразовании.    |
| OutputBlankPageWhenNothingToPrint | Boolean      | true            | false            |                       | Генерирует пустую страницу, если нечего отображать.    |
| PageIndex                         | Integer      | true            | false            |                       | Индекс первой страницы для экспорта.                   |
| PageCount                         | Integer      | true            | false            |                       | Количество страниц для экспорта.                       |
| PrintingPageType                  | String       | true            | false            |                       | Указывает тип страницы для печати.                     |
| GridlineType                      | String       | true            | false            |                       | Определяет способ отрисовки сетки.                    |
| TextCrossType                     | String       | true            | false            |                       | Определяет тип переноса текста.                        |
| DefaultEditLanguage               | String       | true            | false            |                       | Язык по умолчанию для редактирования текста.          |
| EmfRenderSetting                  | String       | true            | false            |                       | Настройки рендеринга EMF.                              |
| MergeAreas                        | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.       |
| SortExternalNames                 | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                  |
| UpdateSmartArt                    | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.       |
| SaveFormat                        | String       | true            | false            |                       | Идентификатор формата для файлов DOCX.                 |
| CachedFileFolder                  | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                         | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.        |
| CreateDirectory                   | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.        |
| EnableHttpCompression             | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                       |
| RefreshChartCache                 | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                         | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.           |
| ValidateMergedAreas               | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.      |
| CheckExcelRestriction             | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.        |
| EncryptDocumentProperties         | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.          |

## Свойства HtmlSaveOptions

| Имя свойства                    | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean      | true            | false            |                       | Включает заголовки страниц в HTML-вывод.            |
| ExportPageFooters               | Boolean      | true            | false            |                       | Включает нижние колонтитулы в HTML-вывод.           |
| ExportRowColumnHeadings         | Boolean      | true            | false            |                       | Экспортирует заголовки строк и столбцов.             |
| ShowAllSheets                   | Boolean      | true            | false            |                       | Показывает все рабочие листы в одном HTML-файле.     |
| ImageOptions                    | Class        | true            | false            |                       | Настройки, управляющие рендерингом изображений.     |
| SaveAsSingleFile                | Boolean      | true            | false            |                       | Сохраняет всю рабочую книгу как один HTML-файл.      |
| ExportHiddenWorksheet           | Boolean      | true            | false            |                       | Включает скрытые рабочие листы в экспорт.             |
| ExportGridLines                 | Boolean      | true            | false            |                       | Отрисовывает сеточные линии в HTML-выводе.           |
| PresentationPreference          | Boolean      | true            | false            |                       | Оптимизирует HTML для режима презентации.            |
| CellCssPrefix                   | String       | true            | false            |                       | Префикс, добавляемый к именам CSS-классов для ячеек. |
| TableCssId                      | String       | true            | false            |                       | Атрибут ID для созданной HTML-таблицы.                |
| IsFullPathLink                  | Boolean      | true            | false            |                       | Генерирует полные пути гиперссылок на ресурсы.       |
| ExportWorksheetCSSSeparately    | Boolean      | true            | false            |                       | Размещает CSS каждого листа в отдельном файле.       |
| ExportSimilarBorderStyle        | Boolean      | true            | false            |                       | Объединяет похожие стили границ для уменьшения размера CSS. |
| MergeEmptyTdForcely             | Boolean      | true            | false            |                       | Принудительно объединяет пустые элементы `<td>`.      |
| ExportCellCoordinate            | Boolean      | true            | false            |                       | Включает координаты ячеек (например, A1) в HTML.     |
| ExportExtraHeadings             | Boolean      | true            | false            |                       | Добавляет дополнительные заголовочные строки/столбцы при необходимости. |
| ExportHeadings                  | Boolean      | true            | false            |                       | Экспортирует заголовки строк и столбцов.              |
| ExportFormula                   | Boolean      | true            | false            |                       | Показывает формулы вместо вычисленных значений.     |
| AddTooltipText                  | Boolean      | true            | false            |                       | Добавляет всплывающие подсказки с комментариями ячеек. |
| ExportBogusRowData              | Boolean      | true            | false            |                       | Включает строки-заполнители для пустых данных.       |
| ExcludeUnusedStyles             | Boolean      | true            | false            |                       | Удаляет неиспользуемые CSS-стили.                     |
| ExportDocumentProperties        | Boolean      | true            | false            |                       | Записывает свойства документа в HTML-мета-теги.     |
| ExportWorksheetProperties       | Boolean      | true            | false            |                       | Записывает свойства рабочего листа в HTML.           |
| ExportWorkbookProperties        | Boolean      | true            | false            |                       | Записывает свойства рабочей книги в HTML.            |
| ExportFrameScriptsAndProperties | Boolean      | true            | false            |                       | Включает скрипты и свойства для фреймов.             |
| AttachedFilesDirectory          | String       | true            | false            |                       | Путь к папке для вложенных файлов.                    |
| AttachedFilesUrlPrefix          | String       | true            | false            |                       | Префикс URL для вложенных файлов.                     |
| Encoding                        | String       | true            | false            |                       | Кодировка символов для HTML-файла.                    |
| ExportActiveWorksheetOnly       | Boolean      | true            | false            |                       | Экспортирует только активный рабочий лист.            |
| ExportChartImageFormat          | String       | true            | false            |                       | Формат изображения, используемый для встроенных диаграмм. |
| ExportImagesAsBase64            | Boolean      | true            | false            |                       | Кодирует изображения как строки Base64.              |
| HiddenColDisplayType            | String       | true            | false            |                       | Как отображаются скрытые столбцы.                     |
| HiddenRowDisplayType            | String       | true            | false            |                       | Как отображаются скрытые строки.                      |
| HtmlCrossStringType             | String       | true            | false            |                       | Определяет, как отображаются переносимые строки.     |
| IsExpImageToTempDir             | Boolean      | true            | false            |                       | Экспортирует изображения во временную папку.         |
| PageTitle                       | String       | true            | false            |                       | Заголовок для созданной HTML-страницы.               |
| ParseHtmlTagInCell              | Boolean      | true            | false            |                       | Парсит HTML-теги, содержащиеся в значениях ячеек.    |
| CellNameAttribute               | String       | true            | false            |                       | Имя атрибута, содержащего ссылку на ячейку.           |
| SaveFormat                        | String       | true            | false            |                       | Идентификатор формата для HTML-файлов.                |
| CachedFileFolder                  | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                         | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.       |
| CreateDirectory                   | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.       |
| EnableHttpCompression             | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                      |
| RefreshChartCache                 | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                         | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.          |
| ValidateMergedAreas               | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.     |
| MergeAreas                        | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames                 | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction             | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt                    | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties         | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства ImageSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| ChartImageType            | String       | true            | false            |                       | Формат изображения, используемый для рендеринга диаграмм. |
| EmbeddedImageNameInSvg    | String       | true            | false            |                       | Имя, присваиваемое встроенным изображениям в SVG-выводе. |
| HorizontalResolution      | Integer      | true            | false            |                       | Горизонтальное разрешение (DPI) экспортируемого изображения. |
| ImageFormat               | String       | true            | false            |                       | Целевой формат изображения (PNG, JPG и т.д.).        |
| IsCellAutoFit             | Boolean      | true            | false            |                       | Автоматически подгоняет содержимое ячейки под размер изображения. |
| OnePagePerSheet           | Boolean      | true            | false            |                       | Рендерит каждый рабочий лист на отдельной странице.   |
| OnlyArea                  | Boolean      | true            | false            |                       | Экспортирует только заданную область рабочего листа. |
| PrintingPage              | String       | true            | false            |                       | Макет страницы, используемый для печати.             |
| PrintWithStatusDialog     | Boolean      | true            | false            |                       | Показывает диалоговое окно состояния во время печати. |
| Quality                   | Integer      | true            | false            |                       | Качество сжатия для изображений JPEG (0‑100).        |
| TiffCompression           | String       | true            | false            |                       | Тип сжатия для изображений TIFF.                     |
| VerticalResolution        | Integer      | true            | false            |                       | Вертикальное разрешение (DPI) экспортируемого изображения. |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов изображений.        |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства JsonSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                               |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ------------------------------------------------------ |
| ExportArea                | Class        | true            | false            |                       | Определяет область рабочего листа для экспорта.       |
| HasHeaderRow              | Boolean      | true            | false            |                       | Указывает, содержит ли первая строка заголовки столбцов. |
| ExportAsString            | Boolean      | true            | false            |                       | Экспортирует все значения как строки.                  |
| Indent                    | String       | true            | false            |                       | Строка, используемая для отступов (например, два пробела). |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для JSON-файлов.                |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.       |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.       |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                      |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.          |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.     |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства MarkdownSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                                   |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------------- |
| Encoding                  | String       | true            | false            |                       | Кодировка символов для markdown-файла.                     |
| FormatStrategy            | String       | true            | false            |                       | Стратегия форматирования markdown (например, GitHub, CommonMark). |
| LineSeparator             | String       | true            | false            |                       | Символ(ы) разрыва строки, используемые для вывода.         |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для markdown-файлов.                 |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов.    |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.           |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.           |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                          |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.              |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.         |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.           |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                     |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.           |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.           |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.              |

## Свойства OoxmlSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean      | true            | false            |                       | Включает имена ячеек в экспортируемый файл.          |
| UpdateZoom                | Boolean      | true            | false            |                       | Обновляет масштаб в выходном документе.              |
| EnableZip64               | Boolean      | true            | false            |                       | Включает расширения ZIP64 для больших файлов.        |
| EmbedOoxmlAsOleObject     | Boolean      | true            | false            |                       | Встраивает OOXML как OLE-объект.                     |
| CompressionType           | String       | true            | false            |                       | Тип применяемого сжатия (например, Normal, Maximum). |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов OOXML.               |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства PclSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| fontFullName              | String       | true            | false            |                       | Полное имя используемого шрифта.                    |
| fontPclName               | String       | true            | false            |                       | Имя шрифта, специфичное для PCL.                     |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов PCL.                |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства PDFSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean      | true            | false            |                       | Использует заголовок документа как заголовок PDF.   |
| ExportDocumentStructure   | Boolean      | true            | false            |                       | Сохраняет логическую структуру документа.           |
| EmfRenderSetting          | String       | true            | false            |                       | Настройки рендеринга изображений EMF.                |
| CustomPropertiesExport    | String       | true            | false            |                       | Управляет экспортом пользовательских свойств документа. |
| OptimizationType          | String       | true            | false            |                       | Тип оптимизации PDF (например, Size, Speed).         |
| Producer                  | String       | true            | false            |                       | Имя приложения-производителя PDF.                    |
| PDFCompression            | String       | true            | false            |                       | Алгоритм сжатия для потоков PDF.                     |
| FontEncoding              | String       | true            | false            |                       | Кодировка, используемая для встроенных шрифтов.      |
| Watermark                 | Class        | true            | false            |                       | Настройки водяного знака, применяемые к PDF.         |
| CalculateFormula          | Boolean      | true            | false            |                       | Вычисляет формулы перед экспортом.                   |
| CheckFontCompatibility    | Boolean      | true            | false            |                       | Проверяет совместимость шрифтов для рендеринга PDF.  |
| Compliance                | String       | true            | false            |                       | Уровень соответствия PDF/A или PDF/X.                 |
| DefaultFont               | String       | true            | false            |                       | Шрифт, используемый, когда исходный шрифт недоступен. |
| OnePagePerSheet           | Boolean      | true            | false            |                       | Размещает каждый рабочий лист на отдельной странице PDF. |
| PrintingPageType          | String       | true            | false            |                       | Указывает тип страницы для печати.                   |
| SecurityOptions           | Class        | true            | false            |                       | Параметры безопасности, такие как пароли и разрешения. |
| desiredPPI                | Integer      | true            | false            |                       | Желаемое разрешение в пикселях на дюйм.              |
| jpegQuality               | Integer      | true            | false            |                       | Качество изображения JPEG (0‑100).                   |
| ImageType                 | String       | true            | false            |                       | Тип изображения, используемый для растеризации.      |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для PDF-файлов.                |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства PptxSaveOptions

| Имя свойства                      | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                              |
| --------------------------------- | ------------ | --------------- | ---------------- | --------------------- | ----------------------------------------------------- |
| IgnoreHiddenRows                  | Boolean      | true            | false            |                       | Пропускает скрытые строки при экспорте.               |
| AdjustFontSizeForRowType          | String       | true            | false            |                       | Управляет изменением размера шрифта в зависимости от типа строки. |
| ExportViewType                    | String       | true            | false            |                       | Определяет, какой вид (слайд, заметки) экспортировать. |
| DefaultFont                       | String       | true            | false            |                       | Шрифт, используемый, когда исходный шрифт недоступен. |
| CheckWorkbookDefaultFont          | Boolean      | true            | false            |                       | Проверяет, применяется ли шрифт по умолчанию для рабочей книги. |
| CheckFontCompatibility            | Boolean      | true            | false            |                       | Проверяет совместимость шрифтов для целевого формата. |
| IsFontSubstitutionCharGranularity | Boolean      | true            | false            |                       | Управляет заменой шрифтов на уровне символов.        |
| OnePagePerSheet                   | Boolean      | true            | false            |                       | Размещает каждый рабочий лист на отдельном слайде.    |
| AllColumnsInOnePagePerSheet       | Boolean      | true            | false            |                       | Помещает все столбцы листа на один слайд.             |
| IgnoreError                       | Boolean      | true            | false            |                       | Игнорирует некритические ошибки при преобразовании.   |
| OutputBlankPageWhenNothingToPrint | Boolean      | true            | false            |                       | Генерирует пустой слайд, если нечего отображать.      |
| PageIndex                         | Integer      | true            | false            |                       | Индекс первого слайда для экспорта.                   |
| PageCount                         | Integer      | true            | false            |                       | Количество слайдов для экспорта.                      |
| PrintingPageType                  | String       | true            | false            |                       | Указывает тип страницы для печати.                    |
| GridlineType                      | String       | true            | false            |                       | Определяет способ отрисовки сетки.                   |
| TextCrossType                     | String       | true            | false            |                       | Определяет тип переноса текста.                       |
| DefaultEditLanguage               | String       | true            | false            |                       | Язык по умолчанию для редактирования текста.         |
| EmfRenderSetting                  | String       | true            | false            |                       | Настройки рендеринга EMF.                             |
| MergeAreas                        | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames                 | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| UpdateSmartArt                    | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| SaveFormat                        | String       | true            | false            |                       | Идентификатор формата для файлов PPTX.                |
| CachedFileFolder                  | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                         | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.       |
| CreateDirectory                   | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.       |
| EnableHttpCompression             | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                      |
| RefreshChartCache                 | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                         | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.          |
| ValidateMergedAreas               | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.     |
| CheckExcelRestriction             | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.       |
| EncryptDocumentProperties         | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства SqlScriptSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                                |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ------------------------------------------------------- |
| CheckIfTableExists        | Boolean      | true            | false            |                       | Проверяет, существует ли целевая таблица уже.          |
| ColumnTypeMap             | String       | true            | false            |                       | Сопоставление имён столбцов с типами данных SQL.       |
| CheckAllDataForColumnType | Boolean      | true            | false            |                       | Сканирует все строки для вывода типов столбцов.        |
| AddBlankLineBetweenRows   | Boolean      | true            | false            |                       | Вставляет пустую строку между сгенерированными строками. |
| Separator                 | String       | true            | false            |                       | Строка, используемая как разделитель столбцов (например, запятая, табуляция). |
| OperatorType              | String       | true            | false            |                       | SQL-оператор, используемый (INSERT, UPDATE и т.д.).    |
| PrimaryKey                | Integer      | true            | false            |                       | Индекс столбца, являющегося первичным ключом.          |
| CreateTable               | Boolean      | true            | false            |                       | Генерирует оператор CREATE TABLE.                      |
| IdName                    | String       | true            | false            |                       | Имя столбца идентификатора.                            |
| StartId                   | Integer      | true            | false            |                       | Начальное значение для автоувеличивающихся ID.         |
| TableName                 | String       | true            | false            |                       | Имя целевой таблицы базы данных.                       |
| ExportAsString            | Boolean      | true            | false            |                       | Экспортирует все значения как строки.                  |
| ExportArea                | Class        | true            | false            |                       | Определяет область рабочего листа для экспорта.        |
| HasHeaderRow              | Boolean      | true            | false            |                       | Указывает, содержит ли первая строка заголовки столбцов. |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов SQL-скриптов.         |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.        |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.        |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                       |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.           |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.      |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.       |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                  |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.        |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.       |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.          |

## Свойства SvgSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| SheetIndex                | Integer      | true            | false            |                       | Индекс экспортируемого рабочего листа.               |
| ChartImageType            | String       | true            | false            |                       | Формат изображения, используемый для рендеринга диаграмм. |
| EmbeddedImageNameInSvg    | String       | true            | false            |                       | Имя, присваиваемое встроенным изображениям в SVG-выводе. |
| HorizontalResolution      | Integer      | true            | false            |                       | Горизонтальное разрешение (DPI) экспортируемого SVG. |
| ImageFormat               | String       | true            | false            |                       | Целевой формат изображения для растровых элементов.  |
| IsCellAutoFit             | Boolean      | true            | false            |                       | Автоматически подгоняет содержимое ячейки под размер SVG. |
| OnePagePerSheet           | Boolean      | true            | false            |                       | Рендерит каждый рабочий лист на отдельной странице SVG. |
| OnlyArea                  | Boolean      | true            | false            |                       | Экспортирует только заданную область рабочего листа. |
| PrintingPage              | String       | true            | false            |                       | Макет страницы, используемый для печати.             |
| PrintWithStatusDialog     | Boolean      | true            | false            |                       | Показывает диалоговое окно состояния во время печати. |
| Quality                   | Integer      | true            | false            |                       | Качество сжатия для растровых изображений.           |
| TiffCompression           | String       | true            | false            |                       | Тип сжатия для изображений TIFF, встроенных в SVG.   |
| VerticalResolution        | Integer      | true            | false            |                       | Вертикальное разрешение (DPI) экспортируемого SVG.   |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для SVG-файлов.                 |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.       |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.       |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                      |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.          |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.     |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства TxtSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                                              |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | --------------------------------------------------------------------- |
| QuoteType                 | String       | true            | false            |                       | Тип кавычек (например, двойные, одинарные).                           |
| Separator                 | String       | true            | false            |                       | Символ-разделитель столбцов (например, запятая, табуляция).           |
| SeparatorString           | String       | true            | false            |                       | Полная строка, используемая как разделитель, если требуется более одного символа. |
| AlwaysQuoted              | Boolean      | true            | false            |                       | Принудительно заключает все поля в кавычки.                           |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для TXT-файлов.                                 |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов.               |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.                       |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.                       |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                                      |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением.            |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.                          |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.                     |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.                      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.                      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.                      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.                         |

## Свойства XlsSaveOptions и XlsbSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                             |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ---------------------------------------------------- |
| MatchColor                | Boolean      | true            | false            |                       | Сохраняет точные цвета ячеек при экспорте.          |
| WpsCompatibility          | Boolean      | true            | false            |                       | Включает совместимость с WPS Office.                |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для файлов XLS/XLSB.           |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.      |
| CreateDirectory           | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.      |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                     |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.         |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.    |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.      |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |

## Свойства XmlSaveOptions

| Имя свойства              | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                                |
| ------------------------- | ------------ | --------------- | ---------------- | --------------------- | ------------------------------------------------------- |
| SheetIndexes              | Array        | true            | false            |                       | Список индексов рабочих листов для включения в экспорт. |
| ExportArea                | Class        | true            | false            |                       | Определяет область рабочего листа для экспорта.         |
| HasHeaderRow              | Boolean      | true            | false            |                       | Указывает, содержит ли первая строка заголовки столбцов. |
| XmlMapName                | String       | true            | false            |                       | Имя XML-карты, применённой к рабочему листу.           |
| SheetNameAsElementName    | Boolean      | true            | false            |                       | Использует имя листа в качестве имени XML-элемента.    |
| DataAsAttribute           | Boolean      | true            | false            |                       | Экспортирует данные ячеек как XML-атрибуты вместо элементов. |
| SaveFormat                | String       | true            | false            |                       | Идентификатор формата для XML-файлов.                  |
| CachedFileFolder          | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                 | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.        |
| CreateDirectory           | String       | true            | false            |                       | Создаёт целевую папку, если она не существует.        |
| EnableHttpCompression     | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                       |
| RefreshChartCache         | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                 | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.           |
| ValidateMergedAreas       | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.      |
| MergeAreas                | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.       |
| SortExternalNames         | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                  |
| CheckExcelRestriction     | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.        |
| UpdateSmartArt            | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.       |
| EncryptDocumentProperties | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.           |

## Свойства XpsSaveOptions

| Имя свойства                      | Тип свойства | Может быть null | Только для чтения | Значение по умолчанию | Описание                                              |
| --------------------------------- | ------------ | --------------- | ---------------- | --------------------- | ----------------------------------------------------- |
| DefaultFont                       | String       | true            | false            |                       | Шрифт, используемый, когда исходный шрифт недоступен. |
| CheckWorkbookDefaultFont          | Boolean      | true            | false            |                       | Проверяет, применяется ли шрифт по умолчанию для рабочей книги. |
| CheckFontCompatibility            | Boolean      | true            | false            |                       | Проверяет совместимость шрифтов для целевого формата. |
| IsFontSubstitutionCharGranularity | Boolean      | true            | false            |                       | Управляет заменой шрифтов на уровне символов.        |
| OnePagePerSheet                   | Boolean      | true            | false            |                       | Размещает каждый рабочий лист на отдельной странице XPS. |
| AllColumnsInOnePagePerSheet       | Boolean      | true            | false            |                       | Помещает все столбцы листа на одну страницу.         |
| IgnoreError                       | Boolean      | true            | false            |                       | Игнорирует некритические ошибки при преобразовании.  |
| OutputBlankPageWhenNothingToPrint | Boolean      | true            | false            |                       | Генерирует пустую страницу, если нечего отображать.  |
| PageIndex                         | Integer      | true            | false            |                       | Индекс первой страницы для экспорта.                  |
| PageCount                         | Integer      | true            | false            |                       | Количество страниц для экспорта.                      |
| PrintingPageType                  | String       | true            | false            |                       | Указывает тип страницы для печати.                    |
| GridlineType                      | String       | true            | false            |                       | Определяет способ отрисовки сетки.                   |
| TextCrossType                     | String       | true            | false            |                       | Определяет тип переноса текста.                       |
| DefaultEditLanguage               | String       | true            | false            |                       | Язык по умолчанию для редактирования текста.         |
| EmfRenderSetting                  | String       | true            | false            |                       | Настройки рендеринга EMF.                             |
| MergeAreas                        | Boolean      | true            | false            |                       | Объединяет соседние ячейки, когда это возможно.      |
| SortExternalNames                 | Boolean      | true            | false            |                       | Сортирует внешние именованные ссылки.                 |
| UpdateSmartArt                    | Boolean      | true            | false            |                       | Обновляет объекты SmartArt до последней версии.      |
| SaveFormat                        | String       | true            | false            |                       | Идентификатор формата для файлов XPS.                 |
| CachedFileFolder                  | String       | true            | false            |                       | Папка, используемая для временных кэшированных файлов. |
| ClearData                         | Boolean      | true            | false            |                       | Очищает существующие данные перед сохранением.       |
| CreateDirectory                   | Boolean      | true            | false            |                       | Создаёт целевую папку, если она не существует.       |
| EnableHttpCompression             | Boolean      | true            | false            |                       | Включает HTTP-сжатие для ответа.                      |
| RefreshChartCache                 | Boolean      | true            | false            |                       | Обновляет кэшированные данные диаграмм перед сохранением. |
| SortNames                         | Boolean      | true            | false            |                       | Сортирует именованные диапазоны по алфавиту.          |
| ValidateMergedAreas               | Boolean      | true            | false            |                       | Проверяет объединённые ячейки на согласованность.     |
| CheckExcelRestriction             | Boolean      | true            | false            |                       | Применяет ограничения Excel при преобразовании.       |
| EncryptDocumentProperties         | Boolean      | true            | false            |                       | Шифрует свойства документа в выходном файле.         |