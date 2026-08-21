---
title: "Excel のコメントの操作"
second_title: "Document"
linktype: "コメント"
type: docs
url: /comments/
aliases: [/working-with-comments/]
keywords: "Aspose.Cells Cloud, Excel コメント API, スプレッドシート コメント, REST API"
description: "Aspose.Cells Cloud REST API v3.0 を使用して、Excel のコメントを追加、取得、更新、削除する方法を、コード例、前提条件、エラー処理を交えて学びます。"
weight: 100
ArticleTitle: "Excel のコメントの操作 – Aspose.Cells Cloud API ガイド"
---

Excel ブックを作成する際、ユーザーはさまざまな理由でコメントを追加できます。よくある用途の一つは、セル内の数式を説明することです。特に、ファイルを他者と共有する場合に有効です。また、コメントはリマインダーや共同作業者へのメモ、他のブックとのクロス参照手段としても活用できます。一度コメントを追加した後、Excel では、好みのスタイルに合わせてコメント ボックスのサイズ変更、形状変更、書式設定が可能です。コメント管理をマスターすることで、この機能を最大限に活用できます。

**前提条件**

- アクティブな Aspose.Cells Cloud アカウント。  
- OAuth 2.0 を通じて取得した有効な **アクセストークン**。  
- API バージョン **v3.0**（本ガイドで使用するエンドポイントは、このバージョンに属します）。  
- オプション：リクエスト構築を簡略化するため、お使いの言語向けの Aspose.Cells SDK。

**バージョン**

以下の例では、**Aspose.Cells Cloud REST API v3.0** を対象としています。今後の API リリースでは、追加のパラメーターが導入されたり、応答構造が変更される可能性があります。最新の API 参照情報をご確認ください。

**コメントの追加**

コメントを追加するには、以下のエンドポイントに **POST** リクエストを送信します：

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**パス パラメーター**

| パラメーター | 型     | 必須   | 説明                                     |
|-------------|--------|--------|------------------------------------------|
| `file`      | 文字列 | はい   | ブック ファイル名（拡張子を含む）。      |
| `sheet`     | 文字列 | はい   | コメントを追加するワークシート名。       |

**リクエスト本文のスキーマ**

| フィールド    | 型     | 必須   | 説明                                     |
|--------------|--------|--------|------------------------------------------|
| `CellName`   | 文字列 | はい   | A1 形式のセル アドレス（例：**B2**）。   |
| `Comment`    | 文字列 | はい   | 保存するコメントのテキスト。              |
| `Author`     | 文字列 | いいえ | コメント作成者の名前。                    |

**リクエスト本文のサンプル**

```json
{
  "CellName": "B2",
  "Comment": "レビューが必要です",
  "Author": "John Doe"
}
```

**成功時の応答サンプル**（`200 OK`）

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "John Doe",
    "HtmlComment": "レビューが必要です",
    "Note": "レビューが必要です"
  }
}
```

**共通のエラー コード**

| コード | 意味                                 |
|--------|--------------------------------------|
| 400    | 無効なセル アドレスまたはリクエスト本文 |
| 401    | 認証エラー – トークンが不足または無効   |
| 404    | ブックまたはワークシートが見つからない |

**コメントの取得**

ワークシートのすべてのコメントを取得するには：

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**パス パラメーター**

| パラメーター | 型     | 必須   | 説明                     |
|-------------|--------|--------|--------------------------|
| `file`      | 文字列 | はい   | ブック ファイル名。      |
| `sheet`     | 文字列 | はい   | ワークシート名。         |

**応答のサンプル**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "初期値",
      "Note": "初期値"
    },
    {
      "CellName": "B2",
      "Author": "John Doe",
      "HtmlComment": "レビューが必要です",
      "Note": "レビューが必要です"
    }
  ]
}
```

**コメントの更新**

既存のコメントを変更するには、**PUT** リクエストを送信します。コメントは、ワークシートのコメント コレクションにおける **インデックス**（0 から始まる）で識別されます。

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**パス パラメーター**

| パラメーター     | 型     | 必須   | 説明                             |
|-----------------|--------|--------|----------------------------------|
| `file`          | 文字列 | はい   | ブック ファイル名。              |
| `sheet`         | 文字列 | はい   | ワークシート名。                 |
| `commentIndex`  | 整数   | はい   | 更新するコメントの 0 から始まるインデックス。 |

**リクエスト本文のスキーマ**

| フィールド   | 型     | 必須   | 説明                     |
|-------------|--------|--------|--------------------------|
| `Comment`   | 文字列 | はい   | 新しいコメントのテキスト。 |
| `Author`    | 文字列 | いいえ | 更新された作成者名（オプション）。 |

**リクエスト本文のサンプル**

```json
{
  "Comment": "更新されたノート テキスト",
  "Author": "John Doe"
}
```

応答は、**コメントの追加**の応答と同様の構造になります。

**コメントの削除**

インデックスで単一のコメントを削除する場合：

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**パス パラメーター**

| パラメーター     | 型     | 必須   | 説明                             |
|-----------------|--------|--------|----------------------------------|
| `file`          | 文字列 | はい   | ブック ファイル名。              |
| `sheet`         | 文字列 | はい   | ワークシート名。                 |
| `commentIndex`  | 整数   | はい   | 削除するコメントの 0 から始まるインデックス。 |

正常に削除された場合、次のような応答が返されます：

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**すべてのコメントを削除**

ワークシートからすべてのコメントをクリアする場合：

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**パス パラメーター**

| パラメーター | 型     | 必須   | 説明                     |
|-------------|--------|--------|--------------------------|
| `file`      | 文字列 | はい   | ブック ファイル名。      |
| `sheet`     | 文字列 | はい   | ワークシート名。         |

**エラー処理のガイドライン**

- **404 Not Found** – ブック ID、ワークシート名、コメントインデックスが正しいか確認してください。  
- **400 Bad Request** – JSON の構文および必須フィールド（`CellName`、`Comment`）を確認してください。  
- **429 Too Many Requests** – 指数的バックオフを実装し、`Retry-After` ヘッダーに従ってください。

**まとめ**

- Excel のコメントは、[セルにメモを追加したり、数式を説明する](/cells/comments/add/)ために使用されます。  
- Excel では、ワークシート上でコメントの[編集](/cells/comments/update/)、[削除](/cells/comments/delete/)、[表示](/cells/comments/get/)または[非表示](/cells/comments/update/)を柔軟に操作できます。  
- また、コメント ボックスの[サイズ変更](/cells/comments/update/)や[移動](/cells/comments/update/)も可能です。  

その他のスプレッドシート要素の操作方法については、[セルの操作](/cells/working-with-cells/)に関するガイドをご参照ください。