---
title: "リモートスプレッドシート内のテキストを変換"
ArticleTitle: "リモートスプレッドシート内のテキストを変換 – Aspose.Cells Cloud"
second_title: "ドキュメント"
linktype: "docs"
url: /ja/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, テキスト変換, API"
description: "ワークシートの指定された範囲内のテキストを変換します。数値変換、文字置換、改行処理、アクセント付き文字の正規化を含みます。"
weight: 1000
---

## Aspose.Cells Cloud Web サービスのリモートスプレッドシート内のテキスト変換

テキストとして格納された数値を正しい数値形式に変換し、不要な文字や改行を目的の文字に置換し、アクセント付き文字をアクセントなしの同等の文字に変換することを示します。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型     | パス/クエリ文字列/HTTP ボディ | 説明 |
|----------------|--------|-------------------------------|------|
| name           | 文字列 | パス | (必須) 取得するワークブックファイルの名前。 |
| worksheet      | 文字列 | パス | スプレッドシートのワークシートを指定します。 |
| range          | 文字列 | パス | スプレッドシートのワークシート範囲を指定します。 |
| convertTextType | 文字列 | クエリ | テキストタイプの変換を示します。(必須) |
| sourceCharacters | 文字列 | クエリ | ソース文字を示します。(オプション) |
| targetCharacters | 文字列 | クエリ | 対象文字を示します。(オプション) |
| folder         | 文字列 | クエリ | (オプション) ワークブックが格納されているフォルダパス。デフォルトは null です。 |
| storageName    | 文字列 | クエリ | (オプション) カスタムクラウドストレージを使用する場合のストレージ名。省略時はデフォルトストレージが使用されます。 |
| region         | 文字列 | クエリ | スプレッドシートの地域/言語設定 (例: `en-US`, `fr-FR`)。数値フォーマット、日付解析、ロケール固有の動作に影響します。(オプション) |
| password       | 文字列 | クエリ | スプレッドシートファイルのオープンに使用するパスワード。(オプション) |

### リクエストボディパラメータ

| パラメータ名 | 型 | 説明 |
| ------------ | -- | ---- |
| - | - | - |

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "テキスト変換が正常に完了しました。",
  "Data": {
    // 更新されたセル数などの変換結果の詳細をここに追加できます。
  }
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|--------|------|------|
| 200 | OK | テキスト変換操作が正常に完了しました。 |
| 400 | Bad Request | リクエストが不正な形式であるか、必須パラメータが不足しています。 |
| 401 | Unauthorized | 認証に失敗したか、JWT トークンが不足または無効です。 |
| 413 | Payload Too Large | リクエストペイロードが許容サイズ制限を超過しています。 |
| 500 | Internal Server Error | サーバー上で予期しないエラーが発生しました。 |

## SDK を使用したリモートスプレッドシート内のテキスト変換の使用方法

### リモートスプレッドシート内のテキスト変換仕様

[リモートスプレッドシート内のテキスト変換 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 操作を実行できるようにします。

cURL コマンドラインツールを使用して、Aspose Cells Cloud Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 安全な接続に HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
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
  "Message": "テキスト変換が正常に完了しました。",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "数値が変換され、文字が置換され、改行が正規化されました。"
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
 `[TBD]`
---