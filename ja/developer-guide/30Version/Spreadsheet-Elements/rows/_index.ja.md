---
title: "Excelの行を操作する – Aspose.Cells Cloud API"
ArticleTitle: "Excelの行を操作する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "行"
type: docs
url: /rows/
aliases: [/working-with-rows/]
keywords: "Aspose.Cells, Excelの行, REST API, スプレッドシート操作"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイル内の行を操作します。Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift をサポートしています。"
weight: 100
---

## Excel ファイルの行を操作する

**最終更新日：2026年7月**

- [Excelワークシート上で行の情報を取得する方法](/cells/rows/get/row/)
- [Excelワークシート上に空の行を追加する方法](/cells/rows/add/row/)
- [Excelワークシート上で行をコピーする方法](/cells/rows/copy/)
- [Excelワークシート上で行を隠す方法](/cells/rows/hide/)
- [Excelワークシート上で隠された行を表示する方法](/cells/rows/unhide/)
- [Excelワークシート上で行をグループ化する方法](/cells/rows/group/)
- [Excelワークシート上で行のグループ化を解除する方法](/cells/rows/ungroup/)
- [ワークシートから行を削除する方法](/cells/rows/delete/)

よく使う行操作のためのクイック API リファレンス：

| 操作 | HTTP メソッド | エンドポイント | 主なパラメータ |
|-------------|-------------|------------------------------------------------------------------------|----------------------------------------|
| [行の取得](https://docs.aspose.cloud/cells/rows/get/row/)     | GET         | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [行の追加](https://docs.aspose.cloud/cells/rows/add/row/)     | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [行のコピー](https://docs.aspose.cloud/cells/rows/copy/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [行の削除](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE      | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [行の隠す](https://docs.aspose.cloud/cells/rows/hide/)      | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [行の表示](https://docs.aspose.cloud/cells/rows/unhide/)  | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [行のグループ化](https://docs.aspose.cloud/cells/rows/group/)    | POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [行のグループ化解除](https://docs.aspose.cloud/cells/rows/ungroup/)| POST        | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**リクエスト／レスポンスの詳細**

- **行の取得**  
  *リクエスト*: リクエストボディは不要です。  
  *レスポンス (200)*:  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *エラー*: 400 Bad Request（無効なインデックス）、404 Not Found（ファイルまたはシートが存在しません）。

- **行の追加**  
  *リクエストボディ (JSON)*:  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *レスポンス (201)*:  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *エラー*: 400 Bad Request（パラメータが不足または無効）、401 Unauthorized。

- **行のコピー**  
  *リクエストボディ (JSON)*:  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *レスポンス (200)*:  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *エラー*: 400 Bad Request、404 Not Found。

- **行の削除**  
  *リクエスト*: リクエストボディは不要です。  
  *レスポンス (200)*:  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *エラー*: 400 Bad Request、404 Not Found。

- **行の隠す**  
  *リクエストボディ (JSON)*:  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *レスポンス (200)*: `{ "Code": "Success", "Status": "Rows hidden" }`  
  *エラー*: 400 Bad Request。

- **行の表示** – ペイロードは「行の隠す」と同一、レスポンスは同一で、ステータスは「Rows unhidden」。

- **行のグループ化** – ペイロードは「行の隠す」と同一、レスポンスステータスは「Rows grouped」。

- **行のグループ化解除** – ペイロードは「行の隠す」と同一、レスポンスステータスは「Rows ungrouped」。

すべての操作には、有効な OAuth 2.0/JWT アクセストークンおよび適切な SDK バージョンが必要です。  

---