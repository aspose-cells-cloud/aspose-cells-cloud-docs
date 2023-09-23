---
title:  Объект списка удалить дубликаты
second_title: Aspose.Cells Cloud Documen
linktitle: Удалить дубликат
type: docs
keywords: list object(table) remove duplicates 
url: /ru/list-objects/remove-duplicates/
description:  Удалите дубликаты в объекте списка.
weight: 20
---
 Этот REST API указывает на удаление дубликатов в объекте списка.

## РСЕТ API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 Параметры запроса:

| Имя параметра| Тип| Путь/строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
|имя|Нить|Путь||
|имя листа|Нить|Путь||
|списокОбъектИндекс|Целое число|Путь||
|папка|Нить|Запрос||
|имя_хранилища|Нить|Запрос||



[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) определяет общедоступный интерфейс программирования и позволяет выполнять взаимодействие с REST непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как позвонить на Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
