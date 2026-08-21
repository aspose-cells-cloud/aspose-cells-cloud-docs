---
title: "リモートスプレッドシート内の文字を削除"
ArticleTitle: "リモートスプレッドシート内の文字を削除 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "リモートスプレッドシート内の文字を削除"
type: docs
url: /ja/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, 文字の削除, テキスト処理"
description: "リモートスプレッドシートの選択された範囲内のすべてのセルから、ユーザー定義の文字、事前定義された記号セット、または任意の部分文字列を削除します。ただし、数式、書式設定、データ検証は保持されます。"
weight: 100
---

## Aspose.Cells Cloud Web サービスの「リモートスプレッドシート内の文字を削除」機能

リモートスプレッドシートの選択された範囲内のすべてのセルから、ユーザー定義の文字、事前定義された記号セット、または任意の部分文字列を削除します。ただし、数式、書式設定、データ検証は保持されます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

### リクエストパラメータ

| パラメータ名        | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                                         |
|---------------------|---------|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | パス                          | (必須) 取得するワークブックファイルの名前。                                                                                                                 |
| worksheet           | string  | パス                          | スプレッドシートのワークシートを指定します。                                                                                                                 |
| range               | string  | パス                          | スプレッドシートのワークシート範囲を指定します。                                                                                                            |
| removeTextMethod    | string  | クエリ                        | テキスト削除メソッドのタイプを指定します。                                                                                                                  |
| characterSets       | string  | クエリ                        | 文字セットを指定します。                                                                                                                                    |
| removeCustomValue   | string  | クエリ                        | 削除するカスタム値を指定します。                                                                                                                            |
| caseSensitive       | boolean | クエリ                        | 有効な場合、`Substring` モードおよび `CustomChars` に影響を与えます。                                                                                       |
| folder              | string  | クエリ                        | (任意) ワークブックが保存されているフォルダのパス。既定値は null です。                                                                                     |
| storageName         | string  | クエリ                        | (任意) カスタムクラウドストレージを使用する場合のストレージ名。省略した場合は既定のストレージが使用されます。                                               |
| region              | string  | クエリ                        | スプレッドシートの地域/言語設定（例：`en-US`、`fr-FR`）。数値の書式設定、日付の解析、ロケール固有の動作に影響を与えます。                                   |
| password            | string  | クエリ                        | スプレッドシートファイルを開くためのパスワード。                                                                                                            |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| *なし*       | *なし* | この操作ではリクエストボティは必要ありません。 |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "文字が正常に削除されました。",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**レスポンスステータスコード**

| コード | 意味             | 説明                                                                 |
|--------|------------------|----------------------------------------------------------------------|
| 200    | OK               | 文字が正常に削除され、ワークブックが更新されました。                 |
| 400    | Bad Request      | 1 つ以上のパラメータが不足しているか、無効です。                     |
| 401    | Unauthorized     | 認証に失敗しました – JWT トークンが不足しているか、無効です。        |
| 413    | Payload Too Large| リクエストサイズが許容上限を超えています。                           |
| 500    | Internal Server Error | サーバー側で予期せぬエラーが発生しました。                         |

## SDK を使用した「リモートスプレッドシート内の文字を削除」の使用方法

### リモートスプレッドシート内の文字を削除する仕様

[リモートスプレッドシート内の文字を削除する API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST によるやり取りを実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にアクセスする方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 安全な接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "文字が正常に削除されました。",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a> をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---