---
title: Работа с CellsObjectOperate Task
second_title: Documen
type: docs
url: /ru/tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Cells.Cloud API для Excel работает: задача управления объектами ячеек"
weight: 20
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Работа с задачей CellsObjectOperate
---
Этот REST API управляет ячейками объекта `task`.

**OperateObject**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| OperateObjectType| нить|Рабочая книга/Лист/Параметры страницы/Cells/Диаграмма/Фигура/Объект списка/Сводная таблица/Параметры рабочей книги/Разрыв страницы|
| OperateObjectPosition| Объект||

**OperateObjectPosition**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Рабочая тетрадь| Объект||
| ИмяЛиста| нить||
| ChartIndex| целое число||
| ShapeIndex| целое число||
| ИмяЯчейки| нить||
| ListObjectIndex| целое число||


**ChartOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| ChartIndex| целое число||
| ChartType| нить||
| UpperLeftRow| целое число||
| UpperLeftColumn| целое число||
| LowerRightRow| целое число||
| Нижний правый столбец| целое число||
| Область| нить||
| IsVertical| нить| правда/ложь|
| CategoryData| нить||
| IsAutoGetSerialName| нить| правда/ложь|
| Область| Заголовок||

**ListObjectOperateParameter** 

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| ListObject| Объект||

**PageBreakOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| PageBreakType| нить||
| Индекс| Индекс||
| Ряд| целое число||
| Столбец| целое число||
| StartIndex| целое число||
| EndIndex| целое число||


**PageSetupOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| PageSetup| Объект||


**PivotTableOperateParameter**

|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Имя_ячейки_назначения| нить||
| SourceData| нить||
| ИмяТаблицы| нить||
| UseSameSource| нить| правда/ложь|
| PivotTableIndex| целое число||
| PivotFieldRows|целое число[]||
| PivotFieldColumns|целое число[]||
| PivotFieldData|целое число[]||


**ShapeOperateParameter**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Форма| Объект||


**WorkbookSettingsOperateParameter**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Настройки рабочей книги| Объект||

**Рабочий листOperateParameter**


|Имя параметра|Тип|Описание|
|:- |:- |:- |
| Имя| нить||
| Тип листа| нить||
| НовоеИмя| нить||
| Запрос на перемещение| Объект||

## ОТДЫХ API

|**API**|**Тип**|**Описание**|**Ссылка на ресурс**|
|:- |:- |:- |:- |
|/cells/task/runtask|ПОЧТА|Выполнить задачу|[PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|

 The[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) определяет общедоступный программный интерфейс и позволяет осуществлять REST-взаимодействие непосредственно из веб-браузера.

