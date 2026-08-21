---
title: "ConvertWorksheetToPdf"
ArticleTitle: "ワークシートをPDFに変換する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, ワークシートをPDFに変換, API"
description: "Aspose.Cells Cloud を使用してスプレッドシートファイルのワークシートを PDF に変換します。"
weight: 10
---

## Aspose.Cells Cloud Web サービスの ConvertWorksheetToPdf

このメソッドは、ローカルファイルシステムからスプレッドシートファイルを読み込み、そのワークシートを PDF ファイルに変換して変換結果を返します。ソースファイルのパスとターゲットフォーマットを正しく指定する必要があります。また、ソースファイルの読み込みおよび該当する場合は変換後のファイルの書き込みを行うための適切な権限が設定されていることを確認してください。変換処理はクラウドサーバー上で完全に実行されるため、クラウドストレージや外部ダウンロードは一切必要ありません。

主な特徴として、クラウドネイティブな変換、クラウドリソースの負荷軽減、および簡略化されたワークフローが挙げられます。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が要求されます。

### リクエストパラメータ

| パラメータ名     | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                                   |
|------------------|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                                                                                         |
| worksheet        | 文字列   | クエリ                        | スプレッドシートのワークシート名。                                                                                                     |
| outPath          | 文字列   | クエリ                        | （オプション）ワークブックを保存するフォルダーパス。デフォルトは null です。                                                           |
| outStorageName   | 文字列   | クエリ                        | 出力ファイルのストレージ名。                                                                                                           |
| fontsLocation    | 文字列   | クエリ                        | カスタムフォントを使用します。                                                                                                         |
| AutoRowsFit      | 真偽値  | クエリ                        | （オプション）ワークシート内のすべての行を自動調整します。                                                                             |
| AutoColumnsFit   | 真偽値  | クエリ                        | （オプション）ワークシート内のすべての列を自動調整します。                                                                             |
| region           | 文字列   | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値書式、日付解析、地域固有の動作に影響を与えます。                           |
| password         | 文字列   | クエリ                        | スプレッドシートファイルを開くためのパスワード。                                                                                       |

### リクエストボディパラメータ

| パラメータ名 | 型   | 説明 |
| ------------ | ---- | ---- |
| [TBD]        |      |      |

### **レスポンス**

```json
{
  "file": "<生成された PDF のバイナリストリーム>"
}
```

**レスポンスのステータスコード**

| コード | 意味             | 説明                                     |
|--------|------------------|------------------------------------------|
| 200    | OK               | ワークシートが正常に PDF に変換され、ファイルストリームとして返されました。 |
| 400    | Bad Request      | 無効なリクエストパラメータまたは不正な URL です。 |
| 401    | Unauthorized     | 認証に失敗したか、資格情報が提供されていません。 |
| 404    | Not Found        | ソースファイルにアクセスできません。     |
| 413    | Payload Too Large | アップロードされたファイルが許可されたサイズ制限を超えています。 |
| 500    | Internal Server Error | 変換中にスプレッドシートで異常が発生しました。 |

## ConvertWorksheetToPdf を SDK で使用する方法

### ConvertWorksheetToPdf の仕様

[ConvertWorksheetToPdf API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) は、公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用することで、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# 安全な接続には HTTPS を使用します
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<生成された PDF のバイナリストリーム>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---