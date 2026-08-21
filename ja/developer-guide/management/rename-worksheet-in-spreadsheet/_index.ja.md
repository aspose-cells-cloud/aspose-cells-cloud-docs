---
title: "Excel でワークシートの名前を変更する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "Excel のワークシート名を変更する方法 – シート名の変更"
linktype: "ワークシートの名前を変更する（スプレッドシート）"
type: docs
url: /ja/rename-worksheet-in-spreadsheet/
keywords: "ワークシートの名前変更, Aspose.Cells Cloud, Excel API, スプレッドシート, SDK, REST API"
description: "Aspose.Cells Cloud API を使って Excel のワークシート名を簡単に変更します。必要なパラメータの確認、cURL の例、C#、Java、Python などの SDK コードの取得方法をご紹介します。"
weight: 100
---

Aspose.Cells Cloud API を使用して、Excel ブック内のワークシート名をプログラムで変更します。シート名を変更し、タブラベルを動的に更新して、RESTful API コールでスプレッドシートの整理を自動化します。ドキュメントの標準化やワークフローの自動化に役立ちます。

## スプレッドシート API でワークシート名を変更する

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL の例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名        | 型     | 位置       | 説明                                                                                                                                                                                                     |
| ------------------- | ------ | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**     | ファイル | FormData | **必須**。名前を変更するワークシートを含む Excel ブックファイル（.xlsx、.xls など）。                                                                                                                  |
| **sourceName**      | 文字列 | クエリ    | **必須**。名前を変更したい現在のワークシート名。                                                                                                                                                       |
| **targetName**      | 文字列 | クエリ    | **必須**。ワークシートに割り当てる新しい名前。Excel の命名ルール（`:`, `\`, `?`, `*`, `[`, `]` を含まない）に従い、ブック内で一意である必要があります。                                                 |
| **outPath**         | 文字列 | クエリ    | **任意**。名前を変更したブックを保存するクラウドストレージ内のターゲットフォルダーパス。`null` または省略された場合、サービスはファイルを元のブックと同じフォルダー（またはデフォルトパス）に保存します。 |
| **outStorageName**  | 文字列 | クエリ    | **任意**。設定済みクラウドストレージサービスの名前識別子（例：`ArchiveStorage`）。省略された場合、デフォルトストレージが使用されます。                                                                    |
| **region**          | 文字列 | クエリ    | **任意**。ロケール設定（例：`ko-KR`）で、文字エンコーディングや地域固有の命名規則に影響を与える可能性があります。                                                                                         |
| **password**        | 文字列 | クエリ    | **任意**。パスワードで保護されたブックを開いて変更するために必要な復号化パスワード。ファイルが暗号化されていない場合は省略してください。                                                                |

**注意**: ワークシート名は 31 文字以内で、文字 `:`, `\`, `?`, `*`, `[`, `]` を含めることはできません。

### 応答

成功したリクエストは、ステータス情報と名前変更されたファイルへのリンクを含む JSON オブジェクトを返します。

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

| コード | 意味                 | 説明                                           |
| ------ | -------------------- | ---------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用され、応答に操作詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。       |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。     |
| 500    | Internal Server Error | 予期しないサーバーエラーが発生しました。        |

## スプレッドシート API でのワークシート名変更の使用例

- **レポート生成とブランド標準化** – 顧客向けレポートを自動生成する際、汎用ワークシート名（例：`Sheet1`）を顧客固有の名前（例：`AcmeCorp_Q1_Summary`）に変更し、プロフェッショナルな出力結果を提供します。
- **データ処理パイプラインの標準化** – ETL ワークフロー内で、不規則な名前でエクスポートされたワークシートを `Raw_Data` や `Cleaned_Data` などの標準名に変更し、後続の分析要件を満たします。
- **多言語コンテンツ配信** – ユーザーの言語設定に応じて、ワークシート名をローカライズ（例：`データ` または `Data`）し、カスタマイズされた体験を提供します。

## なぜスプレッドシート API でのワークシート名変更を使用すべきか？

- **開発者フレンドリー** – 豊富なドキュメントと複数言語向け SDK を提供し、カスタムソリューション構築よりも簡単な統合を実現します。
- **労力の削減** – ワークシート名の自動変更により、手動作業を削減します。
- **ペイ・パー・ユースモデル** – API コールごとに課金され、事前ライセンス費用が不要です。
- **サーバー保守不要** – クラウドサービスであるため、サーバーのホスティング・保守やソフトウェア更新の必要がありません。
- **自動化対応** – ワークフロー内でのドキュメント標準化を自動化します。

## SDK を使用したスプレッドシート API でのワークシート名変更の方法

### OpenAPI 仕様

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a>では、パブリックにアクセス可能なプログラミングインターフェースを詳細に説明し、Web ブラウザから直接 REST でのやり取りを可能にしています。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。次の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="応答" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 エンコード)",
  "contentType": "MIME タイプ",
  "fileDownloadName": "オプションのファイル名"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、開発を最も速く加速できます。SDK は HTTP の詳細を抽象化し、最小限のコードでワークシート名を変更できます。Aspose.Cells Cloud SDK の完全なリストは GitHub リポジトリをご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}