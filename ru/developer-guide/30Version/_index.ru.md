---
title: "Руководство разработчика Aspose.Cells Cloud 3.0"
ArticleTitle: "Руководство разработчика REST API Aspose.Cells Cloud 3.0 — создание, преобразование и форматирование рабочих книг Excel"
second_title: "Документ"
type: docs
url: /ru/developer-guide-3.0/
aliases: [  /ru/developer-guide/v3.0/ , /ru/developer-guide-v3.0/ ]
keywords: "Aspose.Cells Cloud, REST API для Excel, преобразование рабочих книг, API для диаграмм, импорт данных, экспорт, PDF, CSV, JSON, руководство разработчика"
description: "Ознакомьтесь с использованием REST API Aspose.Cells Cloud 3.0 для создания, преобразования, форматирования, создания диаграмм и таблиц в файлах Excel и многого другого. Включает примеры кода и рекомендации по лучшим практикам."
weight: 150
---

## Работа с REST API Aspose.Cells Cloud

**Руководство разработчика Aspose.Cells Cloud 3.0** содержит краткий, удобный для поиска обзор наиболее часто используемых операций REST API для рабочих книг и рабочих листов Excel. Оно предназначено для разработчиков, которым необходимо программно создавать, изменять, преобразовывать и обрабатывать файлы Excel. Используйте разделы ниже, чтобы найти нужную операцию: каждая ссылка ведёт на подробную страницу с синтаксисом запроса, параметрами и примерами. Эта центральная страница объединяет справочник **REST API Aspose.Cells Cloud**, упрощая поиск конечных точек, связанных с рабочими книгами, обработкой диаграмм, импортом и экспортом данных.

**Необходимые условия:** Перед использованием API убедитесь, что у вас есть действующая учётная запись Aspose Cloud, ключ API и секретный ключ, а также установлены соответствующие SDK для вашей среды разработки.

### Содержание
- [Операции с файлами](#file-operations)
- [Домашняя (Форматирование ячеек и управление строками/столбцами)](#home-cell-formatting--rowcolumn-management)
- [Вставка (Диаграммы, таблицы и OLE-объекты)](#insert-charts-tables--ole-objects)
- [Макет страницы (Разрывы страниц и настройки)](#page-layout-page-breaks--setup)
- [Формулы (Вычисление и именованные диапазоны)](#formulas-calculate--names)
- [Данные (Структура, фильтрация и импорт)](#data-outline-filter--import)
- [Просмотр (Комментарии и защита)](#review-comments--protection)
- [Вид (Окна и масштаб)](#view-window--zoom-controls)

### Краткое резюме API

| Группа API | Пример конечной точки | Основное действие |
|-----------|----------------|----------------|
| **Создание рабочей книги** | `POST /cells/workbook` | Создать новую пустую рабочую книгу Excel |
| **Преобразование рабочей книги** | `PUT /cells/workbook/convert` | Преобразовать файл Excel в PDF, CSV, JSON и др. |
| **Добавление диаграммы** | `POST /cells/worksheets/{sheetName}/charts` | Вставить новую диаграмму в рабочий лист |
| [Управление таблицами](/cells/add-a-list-object-or-table-inside-the-worksheet/) | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | Обновить или удалить объект списка (таблицу) |
| **Импорт данных** | `POST /cells/worksheets/{sheetName}/import` | Импортировать CSV, JSON, изображения или массивы в рабочий лист |
| **Вычисление формул** | `POST /cells/workbook/calculate` | Пересчитать все формулы в рабочей книге |
| **Применение фильтров** | `POST /cells/worksheets/{sheetName}/filters` | Добавить или удалить критерии автофильтра |
| **Защита рабочей книги** | `POST /cells/workbook/protect` | Применить парольную защиту к рабочей книге |

Эти часто используемые операции охватывают основные функции **REST API Aspose.Cells Cloud для Excel**, а также содержат прямые ссылки на подробные страницы документации.

Вы можете загрузить PDF-версию таблицы краткого резюме API для использования в автономном режиме.

{{< tabs tabTotal="8" tabID="1" tabName1="Файл" tabName2="Домашняя" tabName3="Вставка" tabName4="Макет страницы" tabName5="Формулы" tabName6="Данные" tabName7="Просмотр" tabName8="Вид" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>Рабочая книга: создание, преобразование, сохранение в другом формате</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="Создать пустую рабочую книгу Excel через API" rel="noopener">Создать пустую рабочую книгу Excel.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="Создать рабочую книгу из шаблонного файла" rel="noopener">Создать рабочую книгу Excel из шаблонного файла.</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="Создать рабочую книгу из шаблона с использованием SmartMarker" rel="noopener">Создать рабочую книгу Excel из шаблона SmartMarker.</a></li>
            <li><a href="/cells/convert/" title="Преобразовать рабочую книгу Excel в другой формат" rel="noopener">Преобразовать рабочую книгу Excel в различные форматы файлов.</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Сохранить рабочую книгу Excel в другом формате" rel="noopener">Сохранить рабочую книгу Excel в различных форматах файлов.</a></li>
        </ul>
        <p>Поиск и замена</p>
        <ul>
            <li><a href="/cells/search/" title="Поиск текста в файлах Excel" rel="noopener">Найти текст в файлах Excel.</a></li>
            <li><a href="/cells/replace/" title="Замена значений в файлах Excel" rel="noopener">Заменить старые значения новыми в файлах Excel.</a></li>
        </ul>
        <p>Сжатие</p>
        <ul>
            <li><a href="/cells/compress/" title="Сжать файлы Excel" rel="noopener">Сжать файлы Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Рабочая книга: объединение и разделение</p>
        <ul>
            <li><a href="/cells/merge/" title="Объединить несколько рабочих книг Excel" rel="noopener">Объединить рабочие книги Excel.</a></li>
            <li><a href="/cells/split/" title="Разделить рабочую книгу Excel на отдельные файлы" rel="noopener">Разделить рабочие книги Excel.</a></li>
        </ul>
        <p>Водяные знаки</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="Добавить фоновое изображение в рабочую книгу" rel="noopener">Добавить фон в рабочую книгу.</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="Удалить фоновое изображение из рабочей книги" rel="noopener">Удалить фон из рабочей книги.</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="Установить фон или водяной знак на рабочем листе" rel="noopener">Установить фон или водяной знак на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="Удалить фон или водяной знак с рабочего листа" rel="noopener">Удалить фон или водяной знак с рабочего листа Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>Шрифты, стили, условное форматирование и значения ячеек</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="Получить стиль ячейки с рабочего листа" rel="noopener">Получить стиль ячейки с рабочего листа Excel.</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="Обновить стили нескольких ячеек" rel="noopener">Обновить стили нескольких ячеек на рабочем листе Excel.</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="Изменить стиль одной ячейки" rel="noopener">Обновить стиль ячейки на рабочем листе Excel.</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="Применить форматирование RTF к ячейке" rel="noopener">Установить форматирование Rich Text для ячейки на рабочем листе Excel.</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="Очистить содержимое и стили ячеек" rel="noopener">Очистить содержимое и стили ячеек на рабочем листе Excel.</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="Управление правилами условного форматирования" rel="noopener">Добавить, удалить и обновить условное форматирование на рабочем листе Excel.</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="Задать значение ячейки" rel="noopener">Задать значение ячейки на рабочем листе Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Строки/столбцы: добавление, удаление, копирование, скрытие и автонастройка</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="Вставить пустую строку в рабочий лист" rel="noopener">Добавить пустую строку на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="Удалить строку из рабочего листа" rel="noopener">Удалить строку с рабочего листа Excel.</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="Скопировать строки в пределах рабочего листа" rel="noopener">Скопировать строки на рабочем листе Excel.</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="Скрыть строки на рабочем листе" rel="noopener">Скрыть строки на рабочем листе Excel.</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="Автонастроить строки в рабочей книге" rel="noopener">Автонастроить строки в рабочей книге Excel.</a></li>
            <li><a href="/cells/columns/add/" title="Вставить пустой столбец в рабочий лист" rel="noopener">Добавить пустой столбец на рабочем листе Excel.</a></li>
            <li><a href="/cells/columns/delete/" title="Удалить столбец из рабочего листа" rel="noopener">Удалить столбец с рабочего листа Excel.</a></li>
            <li><a href="/cells/columns/copy/" title="Скопировать столбцы в пределах рабочего листа" rel="noopener">Скопировать столбцы на рабочем листе Excel.</a></li>
            <li><a href="/cells/columns/hide/" title="Скрыть столбцы на рабочем листе" rel="noopener">Скрыть столбцы на рабочем листе Excel.</a></li>
            <li><a href="/cells/columns/autofit/" title="Автонастроить столбцы в рабочей книге" rel="noopener">Автонастроить столбцы в рабочей книге Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>Диаграммы</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="Добавить диаграмму на рабочий лист" rel="noopener">Добавить диаграмму на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="Удалить диаграмму с рабочего листа" rel="noopener">Удалить диаграмму с рабочего листа Excel.</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="Удалить все диаграммы с рабочего листа" rel="noopener">Удалить все диаграммы с рабочего листа Excel.</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="Преобразовать диаграмму в файл изображения" rel="noopener">Преобразовать диаграмму в изображение.</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="Скрыть легенду диаграммы" rel="noopener">Скрыть легенду диаграммы на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="Обновить заголовок диаграммы" rel="noopener">Обновить заголовок диаграммы на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="Удалить заголовок диаграммы" rel="noopener">Удалить заголовок диаграммы на рабочем листе.</a></li>
        </ul>
        <p>Таблицы</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="Добавить таблицу (объект списка) на рабочий лист" rel="noopener">Добавить объект списка на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="Обновить таблицу на рабочем листе" rel="noopener">Обновить объект списка на рабочем листе Excel.</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="Преобразовать таблицу в диапазон" rel="noopener">Преобразовать объект списка в диапазон.</a></li>
            <li><a href="/cells/sort-table-data/" title="Сортировать данные в таблице" rel="noopener">Сортировать данные в таблице.</a></li>
        </ul>
        <p>OLE-объекты</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="Добавить OLE-объект на рабочий лист" rel="noopener">Добавить OLE-объект на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="Обновить конкретный OLE-объект" rel="noopener">Обновить конкретный OLE-объект на рабочем листе Excel.</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="Преобразовать OLE-объект в изображение" rel="noopener">Преобразовать OLE-объект в изображение.</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="Удалить все OLE-объекты с рабочего листа" rel="noopener">Удалить все OLE-объекты с рабочего листа Excel.</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="Удалить конкретный OLE-объект" rel="noopener">Удалить конкретный OLE-объект на рабочем листе Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Фигуры</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="Добавить фигуру на рабочий лист" rel="noopener">Добавить фигуру на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="Удалить все фигуры с рабочего листа" rel="noopener">Удалить все фигуры с рабочего листа Excel.</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="Удалить фигуру по индексу" rel="noopener">Удалить фигуру по индексу на рабочем листе Excel.</a></li>
        </ul>
        <p>Сводные таблицы</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="Добавить сводную таблицу на рабочий лист" rel="noopener">Добавить сводную таблицу на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="Удалить все сводные таблицы с рабочего листа" rel="noopener">Удалить все сводные таблицы с рабочего листа Excel.</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="Удалить сводную таблицу по индексу" rel="noopener">Удалить сводную таблицу по индексу на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="Обновить стиль ячейки в сводной таблице" rel="noopener">Обновить стиль ячейки сводной таблицы на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="Обновить общий стиль сводной таблицы" rel="noopener">Обновить стиль сводной таблицы на рабочем листе Excel.</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="Работа с фильтрами сводных таблиц" rel="noopener">Работа с фильтрами сводных таблиц на рабочем листе Excel.</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="Скрыть элемент поля сводной таблицы" rel="noopener">Скрыть элементы поля сводной таблицы на рабочем листе Excel.</a></li>
            <li><a href="/cells/move-pivot-table/" title="Переместить сводную таблицу в пределах рабочего листа" rel="noopener">Переместить сводную таблицу на рабочем листе Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>Разрывы страниц</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="Вставить горизонтальный разрыв страницы" rel="noopener">Вставить горизонтальный разрыв страницы на рабочем листе Excel.</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="Вставить вертикальный разрыв страницы" rel="noopener">Вставить вертикальный разрыв страницы на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="Удалить горизонтальный разрыв страницы" rel="noopener">Удалить горизонтальный разрыв страницы на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="Удалить вертикальный разрыв страницы" rel="noopener">Удалить вертикальный разрыв страницы на рабочем листе Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Настройка страницы</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>Вычисление</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="Вычислить все формулы в рабочей книге" rel="noopener">Вычислить все формулы в рабочей книге Excel.</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="Вычислить формулу конкретной ячейки" rel="noopener">Вычислить формулы ячеек в рабочей книге Excel.</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="Вычислить формулу на рабочем листе" rel="noopener">Вычислить формулу на рабочем листе Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Именованные диапазоны</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>Структура (группировка)</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="Сгруппировать строки на рабочем листе" rel="noopener">Сгруппировать строки на рабочем листе Excel.</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="Разгруппировать строки на рабочем листе" rel="noopener">Разгруппировать строки на рабочем листе Excel.</a></li>
        </ul>
        <p>Фильтрация</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="Добавить фильтр для столбца" rel="noopener">Добавить фильтр для столбца на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="Удалить фильтр для столбца" rel="noopener">Удалить фильтр для столбца на рабочем листе Excel.</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="Удалить фильтр по дате" rel="noopener">Удалить фильтр по дате на рабочем листе Excel.</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="Добавить иконный фильтр" rel="noopener">Добавить иконный фильтр на рабочем листе Excel.</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="Добавить фильтр по дате" rel="noopener">Добавить фильтр по дате на рабочем листе Excel.</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="Фильтровать данные с помощью автофильтра" rel="noopener">Отфильтровать данные с помощью автофильтра на рабочем листе Excel.</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="Фильтровать 10 лучших элементов списка" rel="noopener">Отфильтровать 10 лучших элементов списка на рабочем листе Excel.</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="Найти все пустые ячейки" rel="noopener">Найти все пустые ячейки в списке на рабочем листе Excel.</a></li>
        </ul>
        <p>Сортировка</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="Сортировать данные на рабочем листе" rel="noopener">Сортировать данные на рабочем листе Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Импорт данных</p>
        <ul>
            <li><a href="/cells/import/" title="Импортировать данные в файлы Excel" rel="noopener">Импортировать данные в файлы Excel.</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="Импортировать CSV-данные на рабочий лист" rel="noopener">Импортировать CSV-данные на рабочий лист Excel.</a></li>
            <li><a href="/cells/import/picture/" title="Импортировать изображение на рабочий лист" rel="noopener">Импортировать изображение на рабочий лист Excel.</a></li>
            <li><a href="/cells/import/double-array/" title="Импортировать массив double на рабочий лист" rel="noopener">Импортировать массив double на рабочий лист Excel.</a></li>
            <li><a href="/cells/import/integer-array/" title="Импортировать массив integer на рабочий лист" rel="noopener">Импортировать массив integer на рабочий лист Excel.</a></li>
            <li><a href="/cells/import/string-array/" title="Импортировать массив строк на рабочий лист" rel="noopener">Импортировать массив строк на рабочий лист Excel.</a></li>
            <li><a href="/cells/import/with-using-storage/" title="Импортировать данные с использованием хранилища" rel="noopener">Импортировать данные в рабочий лист Excel с использованием хранилища.</a></li>
            <li><a href="/cells/import/without-using-storage/" title="Импортировать данные без использования хранилища" rel="noopener">Импортировать данные в рабочий лист Excel без использования хранилища.</a></li>
        </ul>
        <p>Сборка данных</p>
        <ul>
            <li><a href="/cells/assembly/" title="Собрать данные в файлах Excel" rel="noopener">Собрать данные в файлах Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>Комментарии</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="Добавить комментарий к ячейке" rel="noopener">Добавить комментарий к ячейке на рабочем листе Excel.</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="Обновить комментарий ячейки" rel="noopener">Обновить комментарий на рабочем листе Excel.</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="Удалить все комментарии с рабочего листа" rel="noopener">Удалить все комментарии с рабочего листа Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Изменения</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Защитить рабочую книгу Excel" rel="noopener">Защитить рабочую книгу Excel.</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Снять защиту с рабочей книги Excel" rel="noopener">Снять защиту с рабочей книги Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>Окна</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="Закрепить области на рабочем листе" rel="noopener">Закрепить области на рабочем листе Excel.</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="Отменить закрепление областей на рабочем листе" rel="noopener">Отменить закрепление областей на рабочем листе Excel.</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="Скрыть рабочий лист" rel="noopener">Скрыть рабочий лист Excel.</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="Показать скрытый рабочий лист" rel="noopener">Показать скрытый рабочий лист Excel.</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>Масштаб</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="Задать масштаб рабочего листа" rel="noopener">Задать масштаб на рабочем листе Excel.</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}