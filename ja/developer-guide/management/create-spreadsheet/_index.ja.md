---
title: "スプレッドシート API の作成 – Aspose.Cells Cloud (v5.0) | Excel ファイルの生成"
second_title: "ドキュメント"
ArticleTitle: "新しい Excel スプレッドシートの作成方法 – 空白またはテンプレートベースのファイルを生成する"
linktype: "スプレッドシートの作成"
type: docs
url: /ja/create-spreadsheet/
keywords: "Aspose.Cells, スプレッドシート API, Excel 作成, クラウド, XLSX, ODS, CSV, テンプレート, SDK, 自動化"
description: "Aspose.Cells Cloud API (v5.0) を使用して、空白またはテンプレートベースの Excel ワークブックを作成する方法を学びます。エンドポイント、パラメータ、エラーコード、認証手順、SDK の使用例を含みます。"
weight: 100
---

Aspose.Cells Cloud API を使用して、プログラムで新しい Excel スプレッドシートを作成します。空白のワークブックを生成するか、カスタムテンプレートからファイルをインスタンス化できます。この RESTful API は、Excel ファイルの自動作成を可能にし、レポート生成、ドキュメント自動化、データ処理ワークフローに最適です。

## **スプレッドシート API の作成**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名       | 型     | 位置     | 説明                                                                                                                                              |
| ------------------ | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | 文字列 | クエリ   | **必須**。新規スプレッドシートのファイル形式（例: `XLSX`, `XLS`, `ODS`, `CSV`）。                                                                |
| **template**       | 文字列 | クエリ   | **オプション**。クラウドストレージに保存されたテンプレートファイルの名前（例: `invoice_template.xlsx`）。省略した場合、空白のワークブックが作成されます。 |
| **outPath**        | 文字列 | クエリ   | **オプション**。生成されたファイルを保存するクラウドストレージ内のターゲットフォルダーパス。`null` または省略した場合、スプレッドシートはデフォルトの場所に保存されます。 |
| **outStorageName** | 文字列 | クエリ   | **必須**。設定済みクラウドストレージの識別子（例: `MyDrive`）。                                                                                   |
| **region**         | 文字列 | クエリ   | **オプション**。ロケール設定（例: `fr-FR`）で、日付・数値・通貨のデフォルト形式を決定します。                                                       |
| **password**       | 文字列 | クエリ   | **オプション**。暗号化されたテンプレートファイルのパスワード。テンプレートが保護されていない場合は空のままにしてください。                           |

### レスポンス

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                            |
| ------ | -------------------- | --------------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足している。                            |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えた。                  |
| 500    | Internal Server Error| サーバーで予期せぬエラーが発生しました。                           |

## スプレッドシート API の使用場面

- **自動レポートシステムの初期化** – 毎日／毎週の自動化サイクルの開始時に、空白ワークブックを作成するか、標準テンプレートからレポートファイルを生成します。
- **ユーザー自サービスポータル** – 顧客がテンプレート（見積もり、プロジェクトスケジュールなど）を選択し、カスタマイズされた Excel ファイルを即座にダウンロードできるようにします。
- **バッチデータのエクスポートと配布** – エクスポートされたデータセットごとに一貫した形式で個別のワークブックを生成し、後続の配布・処理を容易にします。

シートの追加やセルへのデータ入力など、その後の操作については、**シート追加 API**、**セル更新 API**、**ワークブックエクスポート API** を参照してください。

## なぜスプレッドシート API を使用すべきか？

- **開発者向け** – 複数言語用の SDK ライブラリと豊富なドキュメントを提供し、カスタムソリューションの構築よりも簡単な統合を実現します。
- **作業効率の向上** – ドキュメントの統合処理を自動化し、手動作業を削減します。
- **従量課金制** – 事前のライセンス費用なしで、API 使用量に基づいて課金されます。
- **マネージドサービス** – API は完全にホストされており、オンプレミスサーバーの保守やソフトウェアアップデートの必要がありません。

## SDK を使用したスプレッドシート API の使い方

### スプレッドシート API の仕様

[スプレッドシート API の仕様](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet)は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を可能にします。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使ってクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード済み)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化して、簡潔なコードでスプレッドシートを構築できるため、開発が最も迅速に行えます。Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---