---
title: "リモート Excel スプレッドシートのテキストを検索する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "リモート Excel スプレッドシート内のテキストを検索 – 特定のデータを抽出"
linktype: "リモートスプレッドシートの内容を検索"
type: docs
url: /ja/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel 検索 API, クラウドスプレッドシート, テキスト検索, REST"
description: "Aspose.Cells Cloud を使用してクラウドストレージに保存された Excel ファイル内にあるテキスト、数値、数式を検索します。大文字・小文字を区別しない検索、フォルダー選択、パスワード保護されたワークブックのサポートを提供します。"
weight: 100
---

### **リモートスプレッドシートの内容を検索する API**

Aspose.Cells Cloud API を使用して、任意の Excel スプレッドシート内から特定のテキストをプログラムで検索します。クラウドストレージに保存されたファイル内にあるテキスト、数値、数式を検索できます。この RESTful API は、自動化されたデータ検出、コンテンツ分析、スプレッドシート監査ワークフローを実現します。

### **Web API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ:**

| パラメータ名   | 型      | パス / クエリ文字列 / HTTP ボディ | 説明                                                                                                                                                      |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | 文字列  | パス                       | **必須**。テキスト検索を実行する Excel ワークブックのファイル名（拡張子を含む）。例: `sales_data.xlsx`。                         |
| searchText     | 文字列  | クエリ                     | **必須**。ワークブック全体またはワークシート上で検索する正確な文字列、数値、または部分的な内容。                                                 |
| ignoringCase   | 真偽値  | クエリ                     | **オプション**。大文字・小文字の区別を指定します。`true` に設定すると大文字・小文字を区別しない検索（例: “Report” が “REPORT” にマッチ）になります。既定値は `false` です。                    |
| folder         | 文字列  | クエリ                     | **オプション**。対象ワークブックを含むクラウドストレージ内のディレクトリパス。省略した場合、ルートフォルダーが前提となります。                            |
| storageName    | 文字列  | クエリ                     | **オプション**。カスタム設定されたクラウドストレージサービスの名前識別子。指定しない場合、API はアカウントに関連付けられた既定のストレージを使用します。 |
| region         | 文字列  | クエリ                     | **オプション**。検索時に適用されるロケール設定（例: `es-ES`）。これにより、テキストの正規化や照合ルールに影響を与える可能性があります。                              |
| password       | 文字列  | クエリ                     | **オプション**。パスワード保護された Excel ファイルにアクセスするために必要な復号化パスワード。ファイルが暗号化されていない場合はこのパラメータを省略してください。                      |

**用語集**

- **searchText** – 検索対象の正確な文字列。部分一致も可能です。
- **ignoringCase** – `true` に設定すると大文字・小文字を区別しない検索が有効になります。`false` の場合は大文字・小文字を区別します。
- **folder** – ワークブックを含むディレクトリのパス。
- **storageName** – カスタムストレージ設定の識別子。
- **region** – テキスト比較ルールに影響を与えるロケールコード。
- **password** – 保護されたワークブックの復号化に使用するパスワード。

### **レスポンス**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

レスポンスには、検索されたテキストが見つかったセル（`CellName`）のリストと、ワークシート名、マッチしたテキストが含まれます。マッチする項目が見つからない場合でも、`Cells` 配列は空になりますが、HTTP 200 OK が返されます。

### エラーコード

- **400 Bad Request** – 無効な Aspose.Cells Cloud API の URI。  
  ```json
  {"code":400,"message":"Invalid request URI"}
  ```
- **401 Unauthorized** – 無効なアクセストークン、クライアント ID、またはクライアントシークレット。  
  ```json
  {"code":401,"message":"Invalid access token"}
  ```
- **404 Not Found** – スプレッドシートファイルにアクセスできません。  
  ```json
  {"code":404,"message":"File not found"}
  ```
- **500 Server Error** – 予期しない状態により、API がリクエストを完了できませんでした。  
  ```json
  {"code":500,"message":"Internal server error"}
  ```

## スプレッドシートの内容検索 API の使用例

- **包括的なワークブックコンプライアンス監査** – 企業のデータセキュリティおよびコンプライアンスチェックのために、Excel ファイル全体を素早くスキャンし、機密性の高い用語（例: “Confidential Clause”, “Internal Data”）をすべて特定します。
- **ワークシート間のデータ関連クエリ** – プロジェクト情報が複数のワークシートに分散している場合、特定のプロジェクト番号や顧客名を検索し、関連データを即座に特定できます。
- **バッチテンプレートの内容検証** – 自動レポート生成後、複数の Excel ファイルをバッチでスキャンし、すべてのプレースホルダー（例: `{{Date}}`）が正しく置換されたことを確認し、レポートの完全性と正確性を保証します。
- **履歴データのアーカイブとマイニング** – 古いファイルを分析し、特定のイベントコードやビジネス用語を検索して、データ考古学の観点から過去のビジネスロジックを素早く把握します。

## なぜスプレッドシートの内容検索 API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向けの SDK ライブラリを提供し、豊富なドキュメントにより迅速な開発を実現します。カスタムソリューションを構築する場合と比べ、大幅に開発工数を削減できます。
- **人件費の削減** – 繰り返し検索タスクを自動化し、開発者が手動のデータ抽出作業から解放されます。
- **従量課金制** – 初期投資不要。実際に使用した API コールのみに課金されます。
- **メンテナンス不要** – Aspose がサーバー、アップデート、互換性を管理するため、アプリケーションロジックに集中できます。
- **複雑な Excel 書式を保持** – 結果を元のスタイルを保持した、広くアクセス可能な PDF 形式でエクスポート可能です。

## SDK を使用したスプレッドシート API のリンク切れ検索の使い方

### OpenAPI 仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI 仕様</a> はパブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST API 操作を実行できるようにします。

### Aspose.Cells Cloud SDK の使用

SDK を使用することで、開発 speed を最大限に引き上げられます。SDK は内部処理を処理するため、最小限のコードでスプレッドシート内のセルに検索内容を実装できます。Aspose.Cells Cloud SDK の完全なリストについては、<a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}
---