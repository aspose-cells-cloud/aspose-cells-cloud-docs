﻿---
title: Чел
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/model/cell/
description: "Aspose.Cells Спецификация облачной модели: Cell. Легко обрабатывайте Excel и другие документы электронных таблиц с помощью таких функций, как открытие, создание, редактирование, разделение, слияние, сравнение и преобразование."
kwords: Excel, Office, Электронная таблица, Cloud REST API, Ячейка
weight: 50
---
## **клетка**

 Инкапсулирует объект, представляющий одну ячейку книги.

| Имя свойства| Тип недвижимости| Обнуляемый| Только чтение| Значение по умолчанию| Описание|
|:- |:- |:- |:- |:- |:- |
| Имя| Нить| Истинный| ЛОЖЬ|| Получает имя ячейки.|
| Ряд| Целое число| Истинный| ЛОЖЬ|| Получает номер строки (отсчитываемый от нуля) ячейки.|
| Столбец| Целое число| Истинный| ЛОЖЬ|| Получает номер столбца (отсчитываемый от нуля) ячейки.|
| Ценить| Нить| Истинный| ЛОЖЬ|| Получает значение, содержащееся в этой ячейке.|
| Тип| Нить| Истинный| ЛОЖЬ|| Представляет тип значения ячейки.|
| Формула| Нить| Истинный| ЛОЖЬ||Получает или задает формулу метода .|
| ИсФормула| логическое значение| Истинный| ЛОЖЬ|| Указывает, содержит ли указанная ячейка формулу.|
| IsMerged| логическое значение| Истинный| ЛОЖЬ|| Проверяет, является ли ячейка частью объединенного диапазона или нет.|
| IsArrayHeader| логическое значение| Истинный| ЛОЖЬ|| Указывает, что формула ячейки является формулой массива и является первой ячейкой массива.|
| ИсИнАррай| логическое значение| Истинный| ЛОЖЬ|| Указывает, является ли формула ячейки формулой массива.|
| Исеррорвалуе| логическое значение| Истинный| ЛОЖЬ|| Проверяет, является ли значение этой ячейки ошибкой.|
| Исинтабле| логическое значение| Истинный| ЛОЖЬ|| Указывает, является ли эта ячейка частью формулы таблицы.|
| Исстилесет| логическое значение| Истинный| ЛОЖЬ|| Указывает, установлен ли стиль ячейки. Если возвращается false, это означает, что эта ячейка имеет формат ячейки по умолчанию.|
| HtmlString| Нить| Истинный| ЛОЖЬ|| Получает и задает строку HTML, содержащую данные и некоторые форматы в этой ячейке.|
| Стиль| Класс:LinkElement| Истинный| ЛОЖЬ|||
| Рабочий лист| Нить| Истинный| ЛОЖЬ|| Получает родительский лист.|
| связь| Класс:Ссылка| Истинный| ЛОЖЬ|||

**Имя родителя** : [СсылкаЭлемент](/specification/model/linkelement)

