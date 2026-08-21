---
title: "Aspose.Cells Cloud Excel ウェブ API - シートの種類と位置を制御して新しいシートを追加"
second_title: "ドキュメント"
articleTitle: "Excel にワークシートを追加する方法 – 特定の位置に新しいシートを挿入"
linktype: "スプレッドシートにワークシートを追加"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, ワークシート追加, aspose cells api, スプレッドシート, クラウド api, シート種別, シート位置"
description: "Aspose.Cells Cloud API を使用して、Excel ワークブックに新しいワークシート、チャートシート、マクロシートをプログラムで追加する方法を学びます。1 つの REST 呼び出しでシートの種類、名前、挿入位置を制御できます。"
weight: 100
---

Excel ファイルにワークシートをプログラムで追加し、シートの種類と位置を完全に制御します。標準ワークシート、チャートシート、マクロシートをワークブック内の任意の位置に挿入できます。この REST ベースの操作により、Excel ワークブックの自動管理と整理が可能になります。

**前提条件**

- 有効な JWT アクセストークンを持つアクティブな Aspose.Cells Cloud アカウント。
- ワークブックを保存するための設定済みクラウドストレージ名（例：`CompanyOneDrive`）。
- 対象のワークブックが指定されたストレージ内でアクセス可能である必要があります。また、パスワードで保護されている場合は、正しいパスワードを提供する必要があります。

| **シートの種類**         | 説明                                     |
| :--------------------- | :---------------------------------------- |
| **VB**                 | Visual Basic モジュール                   |
| **Worksheet**          | 通常のワークシート                        |
| **Chart**              | チャートシート                            |
| **BIFF4Macro**         | BIFF4 マクロシート                        |
| **InternationalMacro** | 国際マクロシート                          |
| **Other**              | 上記にないカスタムまたは珍しいシート種別  |
| **Dialog**             | ダイアログワークシート                    |

## **スプレッドシートにワークシートを追加する API**

### ウェブ API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメータ

| パラメータ名         | タイプ    | 位置       | 説明                                                                                                                                                                      |
| :----------------- | :------ | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Spreadsheet**    | ファイル  | FormData | **必須。** 新しいワークシートを追加する Excel ワークブック（.xlsx、.xls など）。                                                                                          |
| **sheetType**      | 文字列    | クエリ    | **任意。** 作成するシートの種類。有効な値は `worksheet`（デフォルト）、`chartsheet`、`macrosheet`、`vbmodule`、`dialog` です。                                               |
| **position**       | 整数     | クエリ    | **任意。** 新しいシートを挿入する 0 から始まるインデックス。`0` は最初のシートの前に挿入、`2` は3番目のシートとして挿入されます。省略した場合は末尾に追加されます。             |
| **sheetName**      | 文字列    | クエリ    | **任意。** 新しいワークシートの名前。ワークブック内で一意である必要があります。省略した場合、「SheetX」などのデフォルト名が生成されます。                                    |
| **outPath**        | 文字列    | クエリ    | **任意。** 変更されたワークブックを保存するクラウドストレージ内の宛先ディレクトリ。`null` または省略した場合、ワークブックはソースファイルと同じ場所、またはデフォルトパスに保存されます。 |
| **outStorageName** | 文字列    | クエリ    | **必須。** 出力ファイルを書き込む設定済みクラウドストレージの識別子（例：`CompanyOneDrive`）。                                                                             |
| **region**         | 文字列    | クエリ    | **任意。** ロケール設定（例：`ja-JP`）で、新しいワークシートの書式設定や地域ルールに影響を与える可能性があります。                                                          |
| **password**       | 文字列    | クエリ    | **任意。** パスワードで保護されたワークブックを復号化・変更するためのパスワード。ファイルが暗号化されていない場合は省略してください。                                      |

### レスポンス

成功した場合、API は更新されたワークブックファイルとともに **HTTP 200 OK**（または新規ファイル生成時は **201 Created**）を返します。

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP ステータスコード**

| コード | 意味                  | 説明                                         |
| ---- | --------------------- | -------------------------------------------- |
| 200  | OK                    | フィルターが正常に適用された。応答には操作の詳細が含まれます。 |
| 400  | Bad Request           | パラメータが不足または無効（例：サポートされていないファイル形式） |
| 401  | Unauthorized          | JWT トークンが無効または不足しています。         |
| 413  | Payload Too Large     | アップロードされたファイルがサイズ制限を超えています。     |
| 500  | Internal Server Error | サーバーで予期せぬエラーが発生しました。          |

## どこでスプレッドシートにワークシートを追加する API を使用すべきか？

- **自動レポート生成** – 財務諸表作成時に、月次ワークシート（例：`2024-05`）を動的に作成・挿入します。
- **バッチテンプレート初期化** – 販売見積りや提案書を一括生成する際、顧客やプロジェクトごとに専用の分析シートを追加します。
- **ダッシュボードの動的拡張** – 新しいデータディメンションが利用可能になったタイミングで、リアルタイムで新しいチャートシートを挿入します。
- **コンプライアンス・監査アーカイブ** – 年次監査中に証拠収集シートを自動追加し、各監査ポイントを分離して保持します。
- シートの削除については、**[シートの削除](/delete-worksheet/)** 操作を参照してください。
- シートの移動については、**[シートの移動](/move-worksheet/)** 操作を参照してください。

## なぜスプレッドシートにワークシートを追加する API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数言語向けの SDK を提供し、開発労力を削減し、豊富なドキュメントを提供します。
- **人件費削減** – 手動でのワークシート作成や繰り返しのコピー＆ペースト作業を排除します。
- **従量課金制** – 実際に実行した API 呼び出し分のみ料金が発生します。
- **メンテナンス不要** – サーバー管理、ソフトウェア更新、互換性の問題が一切ありません。

## SDK を使用してスプレッドシートにワークシートを追加する API を使用する方法

### スプレッドシートにワークシートを追加する API の仕様

[スプレッドシートにワークシートを追加する API の仕様](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST によるやり取りを実行できます。

cURL コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
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

SDK を使用すると、低レベルの詳細を抽象化し、最小限のコードでワークシートを追加できます。SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) を参照してください。

以下のコード例は、 various SDK を使用してサービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}