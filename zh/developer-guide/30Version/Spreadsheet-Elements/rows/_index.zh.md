---
title: "处理 Excel 行 — Aspose.Cells Cloud API"
ArticleTitle: "处理 Excel 行 — Aspose.Cells Cloud API"
second_title: "文档"
linktitle: "行"
type: docs
url: /zh/rows/
aliases: [  /zh/working-with-rows/ ]
keywords: "Aspose.Cells, Excel 行, REST API, 电子表格操作"
description: "使用 Aspose.Cells Cloud REST API 处理 Excel 文件中的行。支持 Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby 和 Swift。"
weight: 100
---

## 在 Excel 文件中处理行

**最后更新时间：2026 年 7 月**

- [如何获取 Excel 工作表中的行信息](/cells/rows/get/row/)
- [如何在 Excel 工作表中添加空行](/cells/rows/add/row/)
- [如何在 Excel 工作表中复制行](/cells/rows/copy/)
- [如何在 Excel 工作表中隐藏行](/cells/rows/hide/)
- [如何在 Excel 工作表中取消隐藏行](/cells/rows/unhide/)
- [如何在 Excel 工作表中对行进行分组](/cells/rows/group/)
- [如何在 Excel 工作表中取消行分组](/cells/rows/ungroup/)
- [如何从工作表中删除行](/cells/rows/delete/)

常见行操作的快速 API 参考：

| 操作         | HTTP 方法 | 端点                                                                   | 关键参数                                       |
|--------------|-----------|------------------------------------------------------------------------|------------------------------------------------|
| [获取行](https://docs.aspose.cloud/cells/rows/get/row/)     | GET       | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`            |
| [添加行](https://docs.aspose.cloud/cells/rows/add/row/)     | POST      | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                           |
| [复制行](https://docs.aspose.cloud/cells/rows/copy/)      | POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [删除行](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE    | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`            |
| [隐藏行](https://docs.aspose.cloud/cells/rows/hide/)      | POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`                       |
| [取消隐藏行](https://docs.aspose.cloud/cells/rows/unhide/) | POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`                       |
| [分组行](https://docs.aspose.cloud/cells/rows/group/)    | POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`                       |
| [取消分组行](https://docs.aspose.cloud/cells/rows/ungroup/)| POST      | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`                       |

**请求 / 响应详情**

- **获取行**  
  *请求*：无需请求体。  
  *响应（200）*：  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *错误*：400 Bad Request（索引无效），404 Not Found（文件或工作表不存在）。

- **添加行**  
  *请求体（JSON）*：  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *响应（201）*：  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *错误*：400 Bad Request（缺少或无效参数），401 Unauthorized。

- **复制行**  
  *请求体（JSON）*：  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *响应（200）*：  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *错误*：400 Bad Request，404 Not Found。

- **删除行**  
  *请求*：无需请求体。  
  *响应（200）*：  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *错误*：400 Bad Request，404 Not Found。

- **隐藏行**  
  *请求体（JSON）*：  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *响应（200）*：`{ "Code": "Success", "Status": "Rows hidden" }`  
  *错误*：400 Bad Request。

- **取消隐藏行** — 请求体与 *隐藏行* 相同；响应相同，状态为 “Rows unhidden”。

- **分组行** — 请求体与 *隐藏行* 相同；响应状态为 “Rows grouped”。

- **取消分组行** — 请求体与 *隐藏行* 相同；响应状态为 “Rows ungrouped”。

所有操作均需有效的 OAuth 2.0/JWT 访问令牌及相应版本的 SDK。