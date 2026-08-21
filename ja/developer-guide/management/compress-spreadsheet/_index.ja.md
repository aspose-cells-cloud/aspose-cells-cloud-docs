---
title: "Aspose.Cells Cloud Excel圧縮Web API – スプレッドシートファイルサイズをプログラムで削減"
second_title: "ドキュメント"
ArticleTitle: "Excelファイルを圧縮する方法 – スプレッドシートサイズを削減しパフォーマンスを最適化"
linktitle: "スプレッドシートの圧縮"
type: docs
url: /compress-spreadsheet/
keywords: "Excel圧縮, Aspose.Cells Cloud, スプレッドシートサイズ削減, API, ワークブック最適化"
description: "Aspose.Cells Cloud API を使用して Excel ワークブックを圧縮する方法を学びます。ステップ・バイ・ステップの例、パラメータ、認証、およびベストプラクティスを取得します。"
weight: 100
---

Aspose.Cells Cloud API を使用して、Excel スプレッドシートをプログラムで圧縮し、ファイルサイズを削減します。未使用データの削除、埋め込みオブジェクトの圧縮、書式設定のクリーニングにより、ワークブックのパフォーマンスを最適化します。この RESTful API により、Excel ファイルの自動圧縮・最適化ワークフローを実現できます。

## **スプレッドシート圧縮 API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### リクエストパラメータ

| パラメータ名     | 型     | Path/Query/String/HTTP Body | 説明                                                                                                                                  |
| --------------- | ------ | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | ファイル | FormData                    | **必須。** 圧縮対象のソース Excel ワークブックファイル（`.xlsx`、`.xls` など）。                                                      |
| level           | 整数   | Query                       | **任意。** 圧縮強度（0 = 最速／最低圧縮、9 = 最遅／最高圧縮）。指定しない場合、バランスの取れたデフォルト値（5）が適用されます。          |
| outPath         | 文字列 | Query                       | **任意。** クラウドストレージ内の保存先フォルダパス。指定しない場合、ファイルはソースワークブックと同じフォルダに保存されます。         |
| outStorageName  | 文字列 | Query                       | **必須。** 設定済みクラウドストレージサービスの識別子（例: `CorporateDrive`）。                                                       |
| region          | 文字列 | Query                       | **任意。** ロケール設定（例: `de-DE`）。地域固有のデータ処理に影響を与える可能性があります。                                            |
| password        | 文字列 | Query                       | **任意。** 保護されたスプレッドシートを復号化するためのパスワード。ファイルが暗号化されていない場合は空白のままにしてください。          |

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

| コード | 意味             | 説明                                                              |
| ------ | ---------------- | ----------------------------------------------------------------- |
| 200    | OK               | 圧縮処理が正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request      | パラメータが不足または無効（例: 未対応のファイル形式）。          |
| 401    | Unauthorized     | JWT トークンが無効または不足。                                    |
| 413    | Payload Too Large| アップロードされたファイルがサイズ制限を超えた。                  |
| 500    | Internal Server Error | サーバー側で予期せぬエラーが発生しました。                        |

## スプレッドシート圧縮 API の使用ケース

- **自動レポート配信** – 月次財務報告書をメール送信前に圧縮し、配信成功率を高め、受信者の利便性を向上させます。
- **ユーザーによるファイルアップロードの最適化** – アップロードされた Excel ファイルをバックグラウンドで圧縮し、クラウドストレージの容量を節約し、ストレージコストを削減します。
- **データパイプライン処理およびマイグレーション** – ETL 処理中に生成される中間 Excel ファイルを圧縮し、ネットワーク転送速度を向上させ、一時ストレージの負荷を軽減します。

## なぜスプレッドシート圧縮 API を使用すべきなのか

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、豊富なドキュメントにより迅速な開発を可能にします。
- **人件費削減** – ドキュメントを手動で統合するための専任スタッフが不要になります。
- **従量課金制** – 初期投資は不要で、実際に実行した API コール分のみ課金されます。
- **サーバー保守不要** – サーバーの保守やソフトウェア更新、互換性の問題が一切ありません。

## SDK を使用したスプレッドシート圧縮 API の利用方法

### スプレッドシート圧縮 API の仕様

[スプレッドシート圧縮 API 仕様](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) は、REST インタラクション用の公開インターフェースを提供し、Web ブラウザから直接 API を呼び出すことができます。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例では、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
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

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化し、わずか数行のコードでスプレッドシートを圧縮できるため、開発が最速で行えます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご参照ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスと連携する方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}