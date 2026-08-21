---
title: "Работа с OLE-объектами в Excel"
second_title: "Документ"
linktitle: "OleObjects"
type: docs
url: /ru/oleobjects/
aliases: [/ru/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Используйте Aspose.Cells Cloud REST API для извлечения, добавления, обновления, удаления и преобразования OLE-объектов в листах Excel. Доступны SDK для Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift и Android."
weight: 100
ArticleTitle: "Работа с OLE-объектами в Excel – Руководство по извлечению, добавлению, обновлению, удалению и преобразованию OLE-объектов"
---

**Как работать с OLE-объектами в листе Excel**

Aspose.Cells Cloud REST API предоставляет полный набор операций для программного управления OLE-объектами. Ниже приведено краткое описание каждой операции, включая HTTP-метод, шаблон конечной точки, необходимые параметры и пример ответа.

- [Как получить OLE-объект из листа Excel](/ru/cells/oleobjects/get/)
  - **Метод:** `GET`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Параметры:** `fileName` (строка), `sheetName` (строка), `oleObjectIndex` (целое число)  
  - **Пример ответа:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Как добавить OLE-объект в лист Excel](/ru/cells/oleobjects/add/)
  - **Метод:** `POST`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Параметры:** `fileName`, `sheetName`, `oleObject` (двоичные данные или base64), `imageFormat` (необязательный)  
  - **Пример тела запроса:** multipart/form‑data с потоком файла.  
  - **Пример ответа:** `201 Created` с заголовком Location новой OLE-ссылки.

- [Как обновить конкретный OLE-объект в листе Excel](/ru/cells/oleobjects/update/)
  - **Метод:** `PUT`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Параметры:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (обновлённое содержимое)  
  - **Пример ответа:** `200 OK` с метаданными обновлённого объекта.

- [Как преобразовать OLE-объект в изображение в листе Excel](/ru/cells/oleobjects/convert/)
  - **Метод:** `GET`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Параметры:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (например, `png`, `jpeg`)  
  - **Пример ответа:** Двоичный поток изображения преобразованного OLE-объекта.

- [Как удалить все OLE-объекты в листе Excel](/ru/cells/oleobjects/clear/)
  - **Метод:** `DELETE`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Параметры:** `fileName`, `sheetName`  
  - **Пример ответа:** `204 No Content`, указывающий, что все OLE-объекты были удалены.

- [Как удалить конкретный OLE-объект в листе Excel](/ru/cells/oleobjects/delete/)
  - **Метод:** `DELETE`  
  - **Конечная точка:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Параметры:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Пример ответа:** `204 No Content`, подтверждающий удаление объекта.