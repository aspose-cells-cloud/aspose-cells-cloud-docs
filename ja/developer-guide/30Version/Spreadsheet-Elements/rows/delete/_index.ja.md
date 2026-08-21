---
title: "Excelワークシートでの行の削除操作"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /ja/rows/delete/
keywords: "Aspose.Cells, 行の削除, Excel API, REST, クラウド, スプレッドシート, Excel, SDK"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートで単一または複数の行を削除する方法を学びます。Android、C#、Go、Java、Node.js、Perl、PHP、Python、Ruby、Swift用のコード例を含みます。"
weight: 20
ArticleTitle: "Excelワークシートでの行の削除操作 – Aspose.Cells Cloud API ガイド"
---

## 利用可能な削除操作

以下の例では、Aspose.Cells Cloud REST API を使用して、Excelワークシートから単一の空行または複数の行を削除する方法を示します。

- [Excelワークシート上の空行を削除する方法](/cells/rows/delete/row/)
- [Excelワークシート上の複数行を削除する方法](/cells/rows/delete/rows/)

**APIリファレンス**

| 項目                | 詳細 |
|---------------------|---------------------------------------------------------------|
| **HTTPメソッド**     | DELETE |
| **エンドポイント**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **パスパラメータ**| `fileName` – Excelファイル名（必須）<br>`sheetName` – ワークシート名（必須） |
| **クエリパラメータ**| `startrow` – 削除する最初の行のインデックス（必須）<br>`totalRows` – 削除する行数（必須）<br>`storage` – クラウドストレージ名（任意）<br>`folder` – ストレージ内のフォルダーパス（任意） |
| **リクエストボディ**    | *なし* |
| **レスポンス例**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **可能なステータスコード**| 200 OK – 行の削除に成功しました<br>400 Bad Request – 無効なパラメータ<br>401 Unauthorized – 認証失敗<br>404 Not Found – ファイルまたはワークシートが見つかりません<br>500 Internal Server Error – サーバー側の問題 |

**関連項目**

- [行の追加](/cells/rows/add/)
- [行の取得](/cells/rows/get/)
- [行のコピー](/cells/rows/copy/)
- [行の非表示](/cells/rows/hide/)
- [行の概要](/cells/rows/)