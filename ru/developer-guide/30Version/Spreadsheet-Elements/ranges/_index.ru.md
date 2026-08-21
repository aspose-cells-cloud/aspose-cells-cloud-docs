---
title: "Работа с диапазонами в Excel"
second_title: "Документ"
linktype: "Диапазон"
type: docs
url: /ru/ranges/
aliases: [  /ru/working-with-ranges/ ]
keywords: "Aspose.Cells, диапазон Excel, REST API, SDK, .NET, Java, Python, объединение ячеек, копирование диапазона, установка значения диапазона"
description: "Узнайте, как извлекать, изменять, стилизовать, объединять, перемещать и копировать диапазоны в Excel с помощью Aspose.Cells Cloud REST API. Включает примеры кода SDK для .NET, Java, Python и других платформ."
weight: 100
ArticleTitle: "Работа с диапазонами в Excel — документация Aspose.Cells Cloud"
---

**Диапазон** представляет собой одну ячейку, всю строку, весь столбец, непрерывный блок ячеек или трёхмерный (3‑D) диапазон, охватывающий несколько рабочих листов.

## Работа с диапазонами в файле Excel

Aspose.Cells Cloud REST API предоставляет специализированные конечные точки для каждой операции с диапазонами. В приведённом ниже списке содержатся ссылки на подробные примеры использования, а также соответствующие HTTP-методы и конечные точки для быстрого справочника.

- [Получить именованные диапазоны в книге](/cells/get-named-ranges-inside-the-workbook/) — извлекает все именованные диапазоны, определённые в книге, возвращая их адреса и область видимости. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Получить данные ячеек на основе именованного диапазона](/cells/get-cells-data-based-on-named-range/) — возвращает значения ячеек, входящих в заданный именованный диапазон. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Изменить высоту строк внутри диапазона](/cells/cells/change-heights-of-rows-inside-the-range/) — настраивает высоту каждой строки, попадающей в указанный диапазон. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Изменить ширину столбцов внутри диапазона](/cells/cells/change-widths-of-columns-inside-the-range/) — изменяет ширину всех столбцов, пересекающихся с диапазоном. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Объединить диапазон ячеек в одну ячейку](/cells/combines-a-range-of-cells-into-a-single-cell/) — объединяет выбранные ячейки в одну, сохраняя значение верхней левой ячейки. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Копировать диапазон на рабочем листе с параметрами вставки](/cells/copy-range-in-a-worksheet-with-paste-options/) — копирует исходный диапазон в целевой диапазон с возможностью выбора типа вставки (значения, форматы, формулы и т.д.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Установить стиль диапазона](/cells/set-the-style-of-the-range/) — применяет стили шрифта, заливки, границ и выравнивания ко всем ячейкам в диапазоне. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Отменить объединение объединённых ячеек диапазона](/cells/unmerge-merged-cells-of-the-range/) — отменяет предыдущую операцию объединения, восстанавливая исходные отдельные ячейки. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Переместить именованный диапазон вместе с рабочим листом Excel](/cells/move-a-named-ranged-with-a-excel-worksheet/) — перемещает именованный диапазон на новый адрес в пределах того же рабочего листа или на другой рабочий лист. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Установить значение диапазона на рабочем листе Excel](/cells/ranges/set-value/) — записывает одно значение или массив значений в указанный диапазон. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Все запросы и ответы представлены в формате JSON. Для аутентификации добавьте заголовок `Authorization` с вашим токеном доступа.
---