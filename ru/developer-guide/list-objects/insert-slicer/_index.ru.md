---
title:  Слайсер вставки объекта списка
description:  Вставьте срез для объекта списка.
url: /ru/list-objects/insert-slicer/
weight: 20
---
 Этот REST API указывает срез вставки для объекта списка на листе Excel.

## РСЕТ API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

 Параметры запроса:

| Имя параметра| Тип| Путь/строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь||
|имя листа|Нить|Путь||
|списокОбъектИндекс|Целое число|Путь||
|индекс столбца|Целое число|Запрос||
|destCellName|Нить|Запрос||
|папка|Нить|Запрос||
|имя_хранилища|Нить|Запрос||



[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK заботится о деталях низкого уровня и позволяет вам сосредоточиться на задачах проекта. Полный список Aspose.Cells Cloud SDK можно найти в репозитории GitHub.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-служб Aspose.Cells с использованием различных SDK:
