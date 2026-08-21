---
title: "スプレッドシートの内容を検索 – Aspose.Cells Cloud API（Excelでテキストを検索）"
second_title: "ドキュメント"
article_title: "ローカルExcelスプレッドシート内でのテキスト検索 – 特定のデータを検索"
linktitle: "スプレッドシートの内容を検索"
type: docs
url: /search-spreadsheet-content/
keywords: "Aspose.Cells, Excel検索API, スプレッドシート内容検索, クラウドスプレッドシートAPI, テキスト検索"
description: "Aspose.Cells Cloud APIを使用して、ローカルExcelファイル内のテキスト、数値、数式を検索します。大文字・小文字を区別しないクエリ、ワークシート単位の検索範囲、安全な認証をサポートします。"
weight: 100
---

## **スプレッドシートの内容を検索するAPI**

Aspose.Cells Cloud APIを使用して、任意のExcelスプレッドシート内で特定のテキストをプログラムで検索します。このAPIは、クラウド上に保存されたローカルファイル内のテキスト、数値、数式を検出でき、自動化されたデータ検出、コンテンツ分析、スプレッドシート監査ワークフローを実現します。

### **Web API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

生のHTTPリクエストを使用する場合、以下のcURL例で同じリクエストを実行できます：

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ**

| パラメータ     | 型     | 位置       | 説明                                                                 |
| ------------ | ------ | ---------- | -------------------------------------------------------------------- |
| spreadsheet  | ファイル | FormData   | 検索対象のExcelファイル。                                             |
| searchText   | 文字列   | クエリ     | ワークブック内で検索するテキスト（または数値）です。                   |
| ignoringCase | 真偽値   | クエリ     | `true`に設定すると、大文字・小文字を区別せずに検索を実行します。         |
| worksheet    | 文字列   | クエリ     | 検索範囲を限定するワークシート名です。省略した場合、すべてのワークシートがスキャンされます。 |
| cellArea     | 文字列   | クエリ     | 検索範囲を制限するA1形式の範囲（例: `A1:C10`）です。                    |
| region       | 文字列   | クエリ     | サービスの地理的リージョン（例: `us-east-1`）です。                     |
| password     | 文字列   | クエリ     | 保護されたワークブックを開くために必要なパスワードです。                 |


### **レスポンス**

APIは`SearchResult`オブジェクトを返します。このオブジェクトには、一致したセルの配列が含まれます。各要素には、ワークシート名、セルアドレス、一致したテキストが提供されます。

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "合計",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "合計",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### エラーコード

- **400 Bad Request（不正なリクエスト）** – リクエストのURIまたはパラメータが無効です。
- **401 Unauthorized（認証なし）** – アクセストークンが不足しているか無効、またはクライアント認証情報が誤っています。
- **404 Not Found（見つかりません）** – 指定されたスプレッドシートにアクセスできません。
- **500 Internal Server Error（内部サーバーエラー）** – ワークブックの処理中に予期しないサーバーエラーが発生しました。

## スプレッドシートの内容検索APIはどこで使用すべきですか？

- **包括的なワークブックコンプライアンス監査** – セキュリティとコンプライアンスチェックのために、「機密条項」や「内部データ」などの機密語をワークブック全体から検索します。
- **ワークシート間のデータ関連クエリ** – 複数のワークシートに現れるプロジェクト番号や顧客名を検索し、迅速なワークシート間統合を可能にします。
- **バッチテンプレートの内容検証** – レポート生成後、`{{Date}}`などのプレースホルダーがバッチ内のExcelファイル群で正しく置換されたかを検証します。
- **履歴データのアーカイブとマイニング** – 過去のExcelファイル内から特定のイベントコードやビジネス用語を検索し、データ・アーキオロジーと分析を加速します。

## なぜスプレッドシートの内容検索APIを使用すべきですか？

- **開発者に優しい** – 多くの言語用SDKが提供されており、カスタムソリューションを構築するよりも開発作業が大幅に削減されます。
- **人件費の削減** – スプレッドシートを手動で検査する必要があるタスクを自動化します。
- **ペイ・パー・ユース** – 実際に呼び出したAPIリクエスト分のみ課金されます。
- **メンテナンス不要** – サーバーの管理、ソフトウェアの更新、互換性の問題が一切ありません。
- **複雑な書式を保持** – 結果をPDFとしてエクスポートしても、元のExcelレイアウトを保持します。

## SDKを使用してスプレッドシートのリンク切れ検索APIを活用する方法

### OpenAPI仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent)はパブリックにアクセス可能なプログラミングインターフェースを定義し、Webブラウザから直接RESTリクエストを実行できるようにします。

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、検索機能の統合が最速で実現できます。SDKはHTTPレイヤーを抽象化し、最小限のコードでAPIを呼び出せます。利用可能なSDKの完全なリストは[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまなSDKを使用して「スプレッドシートの内容検索」操作を呼び出す方法を示します：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
---