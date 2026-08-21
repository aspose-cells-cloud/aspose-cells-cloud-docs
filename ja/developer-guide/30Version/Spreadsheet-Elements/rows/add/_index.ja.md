---
title: "Excelワークシートに行を追加する方法"
second_title: "Document"
linktitle: "Add"
type: docs
url: /ja/rows/add/
keywords: "Aspose.Cells, 行の追加, Excel API, REST, C#, Java, Python, Node.js"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシートに単一または複数の行を追加する手順ガイド。C#、Java、Python、Node.jsのコードサンプル付き。"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用してExcelワークシートに行を追加する – 手順ガイド"
---

## Excelワークシートに行を追加する方法

この記事では、Aspose.Cells Cloud REST API を使用して、既存のワークシートに単一の空行または複数行を挿入する方法を説明します。操作を始める前に、有効なAPIキーと適切なSDKがインストールされていることを確認してください。

**前提条件**  
- [ ] 有効なサブスクリプションを持つAspose.Cells Cloudアカウント。  
- [ ] Aspose Cloudダッシュボードから生成されたAPIキー/アクセス トークン。  
- [ ] サポートされているSDK（C#、Java、Python、Node.js）のいずれかがインストール・設定済み。  

**APIリファレンス**  
- **HTTPメソッド:** `POST`  
- **エンドポイント:** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **必須のパスパラメータ:**  
  - `fileName` – クラウド上に保存されているExcelファイルの名前。  
  - `sheetName` – 行を追加するワークシートの名前。  
- **クエリパラメータ:**  
  - `startrow` – 挿入を開始する行の0から始まるインデックス。  
  - `totalRows` – 挿入する行数。  
  - `folder` – （オプション）ファイルが格納されたクラウドフォルダーのパス。  
  - `storage` – （オプション）デフォルト以外のストレージを使用する場合のストレージ名。  
- **リクエストボディ（JSON例）:**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **cURLの例**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **成功時のレスポンス（HTTP 200）:** 更新されたワークシート情報（新しい行数を含む）を返します。  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **エラーレスポンスの例（HTTP 400）:**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "無効な startrow パラメータです。0 以上の整数である必要があります。"
  }
  ```

- **ステータスコード一覧:**  

  | コード | 意味                           |
  |------|--------------------------------|
  | 200  | 行が正常に追加されました       |
  | 400  | 無効なパラメータまたは不正なJSON形式 |
  | 401  | 認証に失敗しました             |
  | 404  | ファイルまたはワークシートが見つかりません |
  | 500  | サーバーエラー                 |

以下は、行を追加する詳細な例へのリンクです：

- [Excelワークシートに空行を1行追加する方法](/cells/rows/add/row/)
- [Excelワークシートに複数行を追加する方法](/cells/rows/add/rows/)
---