---
title: "範囲を CSV に変換"
ArticleTitle: "範囲を CSV に変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktype: "docs"
url: /cells/convert/range/csv
aliases: []
keywords: "変換, csv, 範囲, Aspose.Cells"
description: "ローカルドライブ上のスプレッドシートの指定範囲を CSV ファイルに変換します。"
weight: 1
---

## Aspose.Cells Cloud Web サービスの範囲を CSV に変換

この操作は、ローカルファイルシステムからスプレッドシートファイルを読み込み、指定された範囲を CSV 形式に変換して、変換結果を直接返します。この API はクラウドサーバー上で完全に処理されるため、クラウドストレージへの中間アップロードは不要です。API は、カスタムフォント、行/列の自動調整、ロケール設定、パスワードで保護されたワークブックなどのオプションパラメータをサポートしています。

### Web API エンドポイント

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名   | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                                                                                                            |
|----------------|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet    | ファイル | FormData                      | スプレッドシートファイルをアップロードします。                                                                                         |
| worksheet      | 文字列   | クエリ                        | スプレッドシートのワークシート名。**必須**。                                                                                           |
| range          | 文字列   | クエリ                        | セル範囲（例: `A1:C10`）。**必須**。                                                                                                   |
| outPath        | 文字列   | クエリ                        | （オプション）ワークブックが保存されるフォルダーパス。既定値は null です。                                                            |
| outStorageName | 文字列   | クエリ                        | 出力ファイルのストレージ名。                                                                                                           |
| fontsLocation  | 文字列   | クエリ                        | カスタムフォントを使用します。                                                                                                         |
| AutoRowsFit    | 真偽値  | クエリ                        | （オプション）ワークシート内のすべての行を自動調整します。                                                                            |
| AutoColumnsFit | 真偽値  | クエリ                        | （オプション）ワークシート内のすべての列を自動調整します。                                                                            |
| region         | 文字列   | クエリ                        | スプレッドシートの地域/言語設定（例: `en-US`, `fr-FR`）。数値の書式、日付の解析、地域固有の動作に影響します。                           |
| password       | 文字列   | クエリ                        | スプレッドシートファイルを開くためのパスワード。                                                                                       |

### リクエストボディパラメータ

| パラメータ名 | 型  | 説明 |
| ------------ | --- | ---- |
| なし         | N/A | リクエストボディパラメータはありません。 |

### **レスポンス**

```json
{
  "ResponseFile": "バイナリファイルストリーム（CSV コンテンツ）"
}
```

**レスポンスステータスコード**

| コード | 意味 | 説明 |
|------|------|------|
| 200 | OK | 範囲の変換に成功し、CSV ファイルがレスポンスボディに返されます。 |
| 400 | Bad Request | 無効な URL、または必須パラメータが欠落しています。 |
| 401 | Unauthorized | 認証に失敗したか、資格情報が提供されていません。 |
| 413 | Payload Too Large | リクエストペイロードが許容サイズ制限を超過しています。 |
| 500 | Internal Server Error | スプレッドシートが変換データの取得中に異常が発生しました。 |

## SDK を使用して範囲を CSV に変換する方法

### 範囲を CSV に変換の仕様

[範囲を CSV に変換 API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できます。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64エンコードされたCSVコンテンツ"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK を使用する

SDK を使用すると、開発を最も迅速に進めることができます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose Cells Cloud Web サービスを呼び出す方法を示しています：
`[TBD]`
---