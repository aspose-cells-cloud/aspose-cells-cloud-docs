---
title: "Aspose.Cells Cloud Excel：ワークシートを移動する Web API — シートの位置をプログラムで変更"
second_title: "ドキュメント"
ArticleTitle: "Excel でワークシートを移動する方法 — シートの順序と位置を再編成"
linktitle: "スプレッドシート内のワークシートを移動"
type: docs
url: /ja/move-worksheet-in-spreadsheet/
keywords: "ワークシート移動 API、シート再編成 API、シート順序変更 API、Excel タブ管理 API、Aspose Cells REST API、シート配置の自動化、ワークブック整理 API、スプレッドシート構造 API、クラウド Excel 自動化、一括シート再編成"
description: "Excel ワークブック内でワークシートを移動し、シート順序を再編成してワークブック構造を最適化する方法を学びましょう。ワークシートの位置を変更し、タブを再配置してワークフローを効率化し、プロフェッショナルなスプレッドシート管理のためにシート整理を自動化します。"
weight: 100
---

Aspose.Cells Cloud API を使用して、Excel ワークブック内でワークシートをプログラムで移動します。RESTful API 呼び出しでシートの位置を変更し、タブの順序を並べ替え、ワークブック構造を最適化します。スプレッドシート整理の自動化や標準化されたワークブックレイアウトの作成に最適です。

## **スプレッドシート内のワークシートを移動する API**

### Web API

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet?sheetName={sheetName}&position={position}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメータ:**

| パラメータ名     | タイプ    | パス／クエリ文字列／HTTP 本文 | 説明                                                                                                                                                      |
| :--------------- | :-------- | :--------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル  | FormData                     | **必須**。再配置対象のワークシートを含むソース Excel ワークブックファイル（.xlsx、.xls など）。                                                         |
| worksheet        | 文字列    | クエリ                       | **必須**。移動対象のワークシートの正確な名前（例：`Summary`、`RawData_2024`）。                                                                         |
| position         | 整数      | クエリ                       | **必須**。ワークシートの新しい 0 から始まるインデックス位置。例：`0` は先頭、`2` は 3 番目のシートに移動します。                                         |
| outPath          | 文字列    | クエリ                       | **任意**。再編成されたワークブックを保存するクラウドストレージ内の宛先フォルダーパス。`null` または省略された場合、デフォルトでソースファイルのディレクトリに保存されます。 |
| outStorageName   | 文字列    | クエリ                       | **必須**。出力ファイルを保存するクラウドストレージサービスの名前識別子（例：`TeamDrive`）。                                                              |
| region           | 文字列    | クエリ                       | **任意**。適用するロケール設定（例：`es-MX`）。保存操作中に一部の書式設定ルールに影響を与える可能性があります。                                          |
| password         | 文字列    | クエリ                       | **任意**。パスワード保護されたワークブックを開いて編集するために必要な復号化パスワード。ファイルが暗号化されていない場合は省略可能です。               |

### **レスポンス**

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

| コード | 意味             | 説明                                     |
| ------ | ---------------- | ---------------------------------------- |
| 200    | OK               | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized     | JWT トークンが無効または不足している。     |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超過している。 |
| 500    | Internal Server Error | サーバーで予期せぬエラーが発生した。     |

## スプレッドシート内のワークシートを移動する API の使用例

- **標準化されたレポート生成**：月次・四半期レポートが自動生成された後、`Summary`（概要）または`Executive Overview`（経営陣向け概要）ワークシートをワークブックの先頭に移動し、ファイルを開いた際に主要な結論が最初に表示されるようにします。
- **データ処理パイプライン**：ETL 処理で複数のデータソースから取得した生データワークシートを処理した後、クリーニング・変換された`Processed_Data`ワークシートをワークブック内の論理的な位置（例：中盤）に移動し、元のデータと分析結果を明確な構造で配置します。
- **ユーザー定制ファイルの提供**：ユーザーが設定画面で好むレイアウト（例：チャートページを先頭に配置）を選択した後、システムがその選択に基づいてワークブック内のワークシート順序を自動的に再編成し、カスタマイズされたファイルを提供します。

## なぜスプレッドシート内のワークシートを移動する API を使用すべきなのか？

- **開発者フレンドリー**：Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、迅速な開発が可能で、包括的なドキュメントも整っています。カスタムソリューションを構築する場合と比較して、開発工数を大幅に削減できます。
- **人件費削減**：ドキュメントの統合作業を担う人的リソースの必要性を低減します。
- **従量課金制**：初期投資不要。実際に使用した API 呼び出し分のみの課金です。
- **メンテナンスコストゼロ**：サーバーのメンテナンス、ソフトウェアのアップデート、互換性の問題に対応する必要がありません。

## SDK を使用してスプレッドシート内のワークシートを移動する API を利用する方法

### スプレッドシート内のワークシートを移動する API の仕様

[スプレッドシート内のワークシートを移動する API の仕様](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) はパブリックに利用可能なプログラミングインターフェースを提供し、Web ブラウザから直接 REST と対話することを容易にします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheet/move?sheetName=Sheet1&destIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
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

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も速く、簡潔なコードでスプレッドシート内のワークシートを移動できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。  
以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}