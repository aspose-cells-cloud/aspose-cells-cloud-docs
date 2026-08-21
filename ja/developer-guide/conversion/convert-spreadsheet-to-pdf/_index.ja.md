---
title: "Aspose.Cells Cloud Web API – スプレッドシートを PDF に変換"
second_title: "ドキュメント"
ArticleTitle: "Aspose.Cells Cloud API を使用してローカルのスプレッドシートを PDF に変換する方法"
linktitle: "スプレッドシートを PDF に変換"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, スプレッドシートから PDF への変換, Excel 変換, クラウド API, PDF 生成, REST API, v4.0"
description: "ローカルのスプレッドシートを Aspose.Cells Cloud API を使用して PDF に変換するステップ・バイ・ステップ・ガイド。リクエスト構文、パラメータ、レスポンスの詳細、エラー処理、実用的なユースケースを含みます。"
weight: 100
---

**ConvertSpreadsheetToPdf** エンドポイントは、ローカルドライブからアップロードされたスプレッドシートファイルを読み込み、Aspose.Cells Cloud サーバー上で処理し、結果として得られた PDF ドキュメントをバイナリ・ストリームとしてクライアントに返します。このクラウド・ネイティブな変換により、ソース・ファイルをストレージにアップロードする必要がなくなり、リソースの消費を削減し、PDF をクライアントに直接返すことでワークフローを簡素化します。サポートされるフォーマットは、基盤となるライブラリに依存します。API はファイルの存在、権限、変換の整合性を検証し、無効な入力または処理エラーが発生した場合は適切な HTTP エラーをスローします。

## **スプレッドシートを PDF に変換する API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **セキュリティと認証**

Aspose.Cells Cloud API はセキュアであり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエスト・パラメータ**

| パラメータ名     | 型     | 位置       | 必須/任意 | 説明                                                                                                                                                                                                 |
| :--------------- | :----- | :--------- | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | ファイル | FormData   | 必須      | 変換するソース・スプレッドシート・ファイル（XLS、XLSX、CSV など）。有効で読み取り可能なファイルである必要があります。最大サイズは 100 MB です。例：`myWorkbook.xlsx`。                                  |
| outPath          | 文字列  | クエリ     | 任意      | 変換された PDF をサーバー上に保存する宛先フォルダのパス（保存したい場合）。省略した場合、ファイルはレスポンスに直接返されます。例：`/output/reports/`。                                               |
| outStorageName   | 文字列  | クエリ     | 任意      | 宛先ストレージサービスの名前（例：`MyCloudStorage`）。`outPath` を使用し、かつストレージがデフォルトでない場合にのみ必要です。                                                                        |
| fontsLocation    | 文字列  | クエリ     | 任意      | PDF 内のテキスト描画を正しく行うための、サーバー上のカスタムフォントフォルダのパス。例：`/fonts/custom/`。                                                                                             |
| region           | 文字列  | クエリ     | 任意      | スプレッドシートの地域/言語設定（例：`en-US`、`fr-FR`）。数値書式、日付解析、ロケール固有の動作に影響を与えます。                                                                                      |
| password         | 文字列  | クエリ     | 任意      | 保護されたスプレッドシートを開くために必要なパスワード。ファイルが暗号化されていない場合は省略してください。                                                                                          |

### **レスポンス**

成功レスポンス（200 OK）  
Content-Type: application/pdf  
Content-Disposition: attachment; filename="converted.pdf"  
Content-Length: `<バイト単位のサイズ>`

ボディ：生成された PDF ファイルのバイナリ・ストリーム

**HTTP ステータス・コード**

| コード | 意味               | 説明                                         |
| ------ | ------------------ | -------------------------------------------- |
| 200    | OK                 | 変換が正常に完了し、レスポンスに PDF が含まれます。 |
| 400    | Bad Request        | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized       | JWT トークンが無効または不足しています。        |
| 413    | Payload Too Large  | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error | サーバーで予期せぬエラーが発生しました。       |

## どこでスプレッドシートを PDF に変換する API を使用すべきか？

- **自動レポート・パイプライン** – 毎日生成される Excel レポートを PDF に変換し、手動ステップなしでアーカイブやメール配信を行います。
- **ドキュメント管理システム** – 変換後、PDF を DMS に直接保存し、元のスプレッドシートはクライアント側にのみ保持します。
- **オン・ザ・フライ・エクスポートを備えたウェブ・アプリケーション** – ブラウザ内で編集しているスプレッドシートの PDF 版をエンド・ユーザーがダウンロードできるようにし、クラウド変換を使用してレイアウトを保持します。
- **規制コンプライアンス** – 監査トレイル用に財務スプレッドシートの不変 PDF スナップショットを生成し、ソース・ファイルがクライアント環境を一切離れないようにします。
- **クロス・フォーマット変換ワークフロー** – [スプレッドシートを CSV に変換する API](/convert-spreadsheet-to-csv/) などの他の変換エンドポイントと組み合わせて、複数フォーマットのアーカイブを作成します。

## なぜスプレッドシートを PDF に変換する API を使用すべきか？

- **アップロード不要ワークフロー** – ソース・ファイルをクラウド・ストレージにアップロードする必要がありません。変換はアップロードされたストリームから直接行われ、帯域幅とストレージコストを節約します。
- **高忠実度の描画** – Aspose.Cells は、PDF への変換時に複雑な数式、チャート、書式を保持し、デスクトップ版 Excel と同等の出力を実現します。
- **スケーラブルなクラウド実行** – Aspose のクラウド・インフラストラクチャを活用し、クライアントのハードウェアに依存せず、高速かつ信頼性の高い変換を実現します。
- **シンプルな REST インターフェース** – オプションのクエリ・パラメータ付きの単一の `PUT` リクエストで、ダウンロード可能な PDF ストリームが返されるため、任意の言語での統合が容易です。

## SDK を使用してスプレッドシートを PDF に変換する API を使用する方法

### スプレッドシートを PDF に変換する API 仕様

[スプレッドシートを PDF に変換する API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) は、ウェブ・ブラウザから直接 REST 通信を実行するための公開可能なプログラミング・インターフェースを提供します。

cURL コマンドライン・ツールを使用すると、Aspose.Cells ウェブ・サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API に呼び出しを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

SDK を使用すると、低レベルの詳細を抽象化し、短いコードでスプレッドシートを別のスプレッドシートに統合できるため、開発が最速で行えます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブ・サービスとやり合う方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}