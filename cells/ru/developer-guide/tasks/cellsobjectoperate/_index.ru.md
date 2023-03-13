---
title: Работа с CellsObjectOperate Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API для Excel работа: задача работы объекта ячейки"
weight: 20
---
Этот REST API управляет объектами ячеек `task`.

**ОперироватьОбъект**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| ОперативныйОбъектТип| нить| Книга/Рабочий лист/PageSetup/Cells/Диаграмма/Форма/ListObject/Сводная таблица/WorkbookSettings/PageBreak|
| OperateObjectPosition| Объект||

**OperateObjectPosition**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Рабочая тетрадь| Объект||
| имя листа| нить||
| индекс диаграммы| целое число||
| ShapeIndex| целое число||
| CellName| нить||
| ИндексОбъектаСписка| целое число||


**ChartOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| индекс диаграммы| целое число||
| Тип диаграммы| нить||
| верхний левый ряд| целое число||
|Верхняя левая колонка| целое число||
| нижняя правая строка| целое число||
| Нижняя правая колонка| целое число||
| Область| нить||
| IsVertical| нить| правда/ложь|
| КатегорияДанные| нить||
| Исаутожетсериалнаме| нить| правда/ложь|
| Область| Заголовок||

**ListObjectOperateParameter** 

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| СписокОбъект| Объект||

**PageBreakOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| PageBreakType| нить||
| Индекс| Индекс||
| Ряд| целое число||
| Столбец| целое число||
| Начальный индекс| целое число||
| EndIndex| целое число||


**PageSetupOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Настройка страницы| Объект||


**PivotTableOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| DestCellName| нить||
| Источник данных| нить||
| ИмяТаблицы| нить||
| UseSameSource| нить| правда/ложь|
| индекс сводной таблицы| целое число||
| PivotFieldRows|целое []||
| PivotFieldColumns|целое []||
|PivotFieldData|целое []||


**Параметр ShapeOperate**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Форма| Объект||


**WorkbookSettingsOperateParameter**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| WorkbookSettings| Объект||

**Рабочий листОперацияПараметр**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Имя| нить||
| Тип листа| нить||
| Новое имя| нить||
| MovingRequest| Объект||

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/ячейки/задача/runtask|ПОЧТА|Выполнить задачу|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет общедоступный программный интерфейс и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

