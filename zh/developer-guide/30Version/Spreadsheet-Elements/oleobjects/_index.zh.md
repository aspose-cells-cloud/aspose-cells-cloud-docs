---
title: "处理 Excel OLE 对象"
second_title: "文档"
linktitle: "OleObjects"
type: docs
url: /zh/oleobjects/
aliases: [  /zh/working-with-oleobjects/ ]
keywords: "OLE, Excel, Aspose.Cells, API, 云"
description: "使用 Aspose.Cells Cloud REST API 在 Excel 工作表中检索、添加、更新、删除和转换 OLE 对象。提供适用于 Java、.NET、Python、PHP、Ruby、Go、Node.js、Perl、Swift 和 Android 的 SDK。"
weight: 100
ArticleTitle: "处理 Excel OLE 对象——检索、添加、更新、删除和转换 OLE 对象指南"
---

**如何在 Excel 工作表中处理 OLE 对象**

Aspose.Cells Cloud REST API 提供了一整套操作，用于以编程方式管理 OLE 对象。以下是对每项操作的简明参考，包括 HTTP 方法、端点模式、所需参数以及简要示例响应。

- [如何从 Excel 工作表中获取 OLE 对象](/zh/cells/oleobjects/get/)
  - **方法：** `GET`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）、`oleObjectIndex`（整数）  
  - **示例响应：**  
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

- [如何向 Excel 工作表中添加 OLE 对象](/zh/cells/oleobjects/add/)
  - **方法：** `POST`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）、`oleObject`（二进制或 Base64 编码）、`imageFormat`（可选）  
  - **示例请求体：** multipart/form-data，包含文件流。  
  - **示例响应：** `201 Created`，并包含新 OLE 对象的 location 响应头。

- [如何更新 Excel 工作表中的特定 OLE 对象](/zh/cells/oleobjects/update/)
  - **方法：** `PUT`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）、`oleObjectIndex`（整数）、`oleObject`（更新后的内容）  
  - **示例响应：** `200 OK`，返回更新后的对象元数据。

- [如何将 Excel 工作表中的 OLE 对象转换为图像](/zh/cells/oleobjects/convert/)
  - **方法：** `GET`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）、`oleObjectIndex`（整数）、`format`（例如 `png`、`jpeg`）  
  - **示例响应：** 转换后的 OLE 对象的二进制图像流。

- [如何删除 Excel 工作表中的所有 OLE 对象](/zh/cells/oleobjects/clear/)
  - **方法：** `DELETE`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）  
  - **示例响应：** `204 No Content`，表示所有 OLE 对象已被移除。

- [如何删除 Excel 工作表中的特定 OLE 对象](/zh/cells/oleobjects/delete/)
  - **方法：** `DELETE`  
  - **端点：** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **参数：** `fileName`（字符串）、`sheetName`（字符串）、`oleObjectIndex`（整数）  
  - **示例响应：** `204 No Content`，确认该对象已被删除。
---