---
title: "Настройка страницы рабочего листа"
second_title: "Документ"
linktitle: "Настройка страницы"
type: docs
url: /page-setup/
keywords: "Aspose.Cells, pageSetup, рабочий лист, параметры печати, поля, ориентация, размер бумаги, заголовок, подвал, масштабирование"
description: "Узнайте, как настроить макет печати рабочего листа Excel с помощью объекта PageSetup облачного решения Aspose.Cells Cloud. Включает список свойств, значения по умолчанию, диапазоны и примеры кода на C#, Java и Python."
weight: 20
ArticleTitle: "Настройка страницы рабочего листа — настройка макета печати с помощью Aspose.Cells Cloud"
---

# **PageSetup**

Параметры печати страницы Excel

## Обзор

Объект **PageSetup** определяет параметры макета печати для рабочего листа Excel, такие как поля, ориентация, масштабирование, заголовки, подвалы и другие параметры, связанные с печатью. Настройка этих свойств позволяет разработчикам создавать печатные книги, соответствующие желаемому внешнему виду и разбивке на страницы.

Ниже приведён краткий пример на C#, демонстрирующий установку распространённых свойств настройки страницы с помощью SDK облачного решения Aspose.Cells:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Инициализация клиентского API (замените на свои учётные данные)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Определение параметров PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Применение параметров к первому рабочему листу книги
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Этот фрагмент устанавливает для рабочего листа альбомную ориентацию, формат бумаги A4, центрирование содержимого и масштаб 100 %.

## Свойства

| Имя свойства          | Тип свойства | Допускает null | Только для чтения | Значение по умолчанию | Описание                                                                 |
| --------------------- | ------------- | -------------- | ---------------- | --------------------- | ------------------------------------------------------------------------ |
| BlackAndWhite         | bool          | false          | false            | false                 | Печатает рабочий лист в чёрно-белом режиме.                             |
| BottomMargin          | float         | true           | false            | 2.54 см               | Размер нижнего поля в сантиметрах.                                       |
| CenterHorizontally    | bool          | false          | false            | false                 | Центрирует лист по горизонтали при печати.                               |
| CenterVertically      | bool          | false          | false            | false                 | Центрирует лист по вертикали при печати.                                 |
| FirstPageNumber       | int           | true           | false            | 1                     | Номер первой страницы при печати листа.                                  |
| FitToPagesTall        | int           | false          | false            | 1                     | Количество страниц по высоте, до которого будет масштабироваться лист.   |
| FitToPagesWide        | int           | false          | false            | 1                     | Количество страниц по ширине, до которого будет масштабироваться лист.   |
| FooterMargin          | float         | true           | false            | 2.54 см               | Расстояние от нижнего края страницы до подвала, в сантиметрах.          |
| HeaderMargin          | float         | true           | false            | 2.54 см               | Расстояние от верхнего края страницы до заголовка, в сантиметрах.       |
| IsAutoFirstPageNumber | bool          | false          | false            | false                 | Автоматически назначает номер первой страницы.                           |
| IsHFAlignMargins      | bool          | false          | false            | true                  | Если true, поля заголовка/подвала совпадают с полями страницы.          |
| IsHFDiffFirst         | bool          | false          | false            | false                 | Указывает, что заголовок/подвал на первой странице отличается от других.|
| IsHFDiffOddEven       | bool          | false          | false            | false                 | Указывает, что заголовок/подвал на нечётных страницах отличается от чётных. |
| IsHFScaleWithDoc      | bool          | false          | false            | false                 | Масштабирует заголовок и подвал вместе с документом (Excel 2007+).      |
| IsPercentScale        | bool          | false          | false            | true                  | Если false, масштабирование управляется через FitToPagesWide и FitToPagesTall. |
| LeftMargin            | float         | true           | false            | 2.54 см               | Размер левого поля в сантиметрах.                                        |
| Order                 | string        | true           | false            | "DownThenOver"        | Порядок нумерации страниц при печати крупного листа в Excel.             |
| Orientation           | string        | false          | false            | "Portrait"            | Ориентация страницы: **Landscape** (альбомная) или **Portrait** (книжная). |
| PaperSize             | string        | true           | false            | "A4"                  | Используемый размер бумаги для печати.                                   |
| PrintArea             | string        | true           | false            | (отсутствует)         | Диапазон ячеек для печати (например, `"A1:D20"`).                        |
| PrintComments         | string        | true           | false            | "NoComments"          | Способ печати комментариев вместе с листом.                              |
| PrintCopies           | int           | true           | false            | 1                     | Количество копий для печати.                                             |
| PrintDraft            | bool          | false          | false            | false                 | Печатает лист в режиме черновика (без графики).                          |
| PrintErrors           | string        | true           | false            | "Display"             | Тип отображаемой ошибки печати.                                          |
| PrintGridlines        | bool          | false          | false            | false                 | Печатает сетку ячеек.                                                    |
| PrintHeadings         | bool          | false          | false            | false                 | Печатает заголовки строк и столбцов.                                     |
| PrintQuality          | int           | true           | false            | 600                   | Настройка качества печати (точек на дюйм).                               |
| PrintTitleColumns     | string        | true           | false            | (отсутствует)         | Столбцы, повторяющиеся слева на каждой печатной странице.               |
| PrintTitleRows        | string        | true           | false            | (отсутствует)         | Строки, повторяющиеся вверху на каждой печатной странице.                |
| RightMargin           | float         | true           | false            | 2.54 см               | Размер правого поля в сантиметрах.                                       |
| TopMargin             | float         | true           | false            | 2.54 см               | Размер верхнего поля в сантиметрах.                                      |
| Zoom                  | int           | false          | false            | 100                   | Коэффициент масштаба в процентах (10–400).                               |
| Header                | object        | true           | false            | (отсутствует)         | Конфигурация заголовка страницы.                                         |
| Footer                | object        | true           | false            | (отсутствует)         | Конфигурация подвала страницы.                                           |

## Сопутствующие объекты

- **Header** — настраивает заголовок рабочего листа.  
- **Footer** — настраивает подвал рабочего листа.  
- **PrintOptions** — дополнительные параметры печати, такие как разрывы страниц и область печати.  
---