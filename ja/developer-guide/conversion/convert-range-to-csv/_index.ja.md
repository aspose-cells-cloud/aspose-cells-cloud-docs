---
title: "Excel 範囲を CSV に変換 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "ローカルスプレッドシートの範囲を CSV ファイルに変換する方法：ステップ・バイ・ステップ・ガイド"
linktitle: "範囲を CSV に変換"
type: docs
url: /ja/convert-range-to-csv/
keywords: "Aspose Cells, 範囲を CSV に変換, Excel を CSV に変換, Excel API, クラウドスプレッドシート, 変換, Excel, CSV, Aspose.Cells, クラウド API"
description: "Aspose.Cells Cloud REST API を使用して、ローカル Excel ワークブック (XLSX または XLS) の特定の範囲を CSV に変換する方法を学びます。リクエスト構文、パラメーター、エラー処理、SDK の例を含みます。"
---

Aspose.Cells Cloud API を使用して、ローカル Excel ファイルから特定の範囲を CSV にエクスポートします。

## **範囲を CSV に変換する API**

### 前提条件
このエンドポイントを呼び出すには、有効な Aspose Cloud の **クライアント ID** と **クライアント シークレット** を持っていること、**JWT アクセストークン** を取得していること、およびソース スプレッドシートが **XLSX** または **XLS** 形式であることを確認してください。

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**cURL の例**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a> を必要とします。

### **リクエストパラメーター**

| パラメーター名     | タイプ   | パス/クエリ文字列/HTTPボディ | 説明                                                                 |
| :---------------- | :------- | :--------------------------- | :------------------------------------------------------------------- |
| Spreadsheet       | ファイル | FormData                     | スプレッドシート ファイルをアップロードします。                      |
| worksheet         | 文字列   | クエリ                       | スプレッドシートのワークシート名を指定します。                       |
| range             | 文字列   | クエリ                       | セル範囲を指定します (例: A1:C10)。                                  |
| outPath           | 文字列   | クエリ                       | ワークブックを保存するフォルダーのパスです (オプション)。デフォルトは null です。 |
| outStorageName    | 文字列   | クエリ                       | 出力ストレージの名前です。                                           |
| fontsLocation     | 文字列   | クエリ                       | 必要に応じてカスタムフォントを指定します。                           |
| region            | 文字列   | クエリ                       | スプレッドシートの地域設定を定義します。                             |
| password          | 文字列   | クエリ                       | スプレッドシート ファイルを開くために必要なパスワードです。          |

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

_返される CSV コンテンツの例 (最初の数行):_

```csv
Name,Date,Amount
John Doe,2023-01-15,1250.00
Jane Smith,2023-01-16,980.50
```

**HTTP ステータスコード**

| コード | 意味                   | 説明                                                     |
| ------ | ---------------------- | -------------------------------------------------------- |
| 200    | OK                     | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | リクエストエラー       | パラメーターが不足しているか無効です (例: サポートされていないファイル形式)。 |
| 401    | 認証エラー             | JWT トークンが無効または不足しています。                 |
| 413    | ペイロードが大きすぎます | アップロードされたファイルがサイズ制限を超えています。   |
| 500    | サーバー内部エラー     | 予期しないサーバー エラーが発生しました。                |

## 範囲を CSV に変換する API の使用例

### **1. データのエクスポートと移行のシナリオ**

- **データベース連携**: 特定の Excel 範囲をデータベース システムに直接エクスポートします。
- **アプリケーション連携**: 選択したスプレッドシートデータを SaaS アプリケーションに提供します。
- **システム移行**: 古典的なシステムと最新のシステム間で特定のデータ範囲を移行します。
- **クロスプラットフォーム共有**: 複数のプラットフォーム間で焦点を絞ったデータ サブセットを共有します。

### **2. レポートと分析**

- **ターゲットレポート**: 特定のレポート セクションを CSV にエクスポートし、焦点を絞った分析を実施します。
- **ダッシュボードデータフィード**: 特定のデータ範囲を BI ダッシュボード ツールに提供します。
- **パフォーマンス指標**: KPI 範囲を抽出し、パフォーマンス追跡システムに供給します。
- **財務レポート**: 財務諸表セクションを外部監査用にエクスポートします。

### **3. 開発とテスト**

- **テストデータ管理**: テスト目的で特定のデータ範囲をエクスポートします。
- **開発環境**: 開発チームとサンプルデータ範囲を共有します。
- **API テスト**: 特定のスプレッドシート セクションから CSV テストデータを生成します。
- **プロトタイプ開発**: アプリケーション プロトタイプ用に焦点を絞ったデータセットを提供します。

### **4. ビジネス運用**

- **選択的データ共有**: 外部パートナーと特定のデータ範囲を共有します。
- **部分データバックアップ**: 重要なデータ範囲を CSV 形式でバックアップします。
- **部門間データ転送**: 部門間で特定のデータを共有します。
- **コンプライアンスレポート**: コンプライアンス提出用に規制データ範囲をエクスポートします。

### **5. 自動化ワークフロー**

- **スケジュールされた範囲エクスポート**: 特定の範囲をスケジュールに基づいて自動的にエクスポートします。
- **トリガーに基づく抽出**: ビジネスイベントやトリガーに基づいて範囲をエクスポートします。
- **ワークフロー連携**: 範囲エクスポートをビジネスプロセスワークフローに統合します。
- **バッチ範囲処理**: 複数の特定の範囲をバッチ処理で処理します。

## なぜ範囲を CSV に変換する API を使用すべきなのか？

- ワークブックを事前にアップロードせずにスプレッドシート範囲を変換できるため、ストレージ容量を節約し、コストを削減できます。
- 既存の Aspose.Cells Cloud SDK を使用することで、迅速に開発を完了できます。
- **シンプルな統合**: 明確なドキュメントが整った REST API。
- **スケーラブルなアーキテクチャ**: 小規模からエンタープライズ規模まで、あらゆる規模の操作に対応可能です。

## SDK を使用して範囲を CSV に変換する API をどのように使用するか？

### OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV) では、パブリックにアクセス可能な API を定義しており、Web ブラウザーから直接 REST による操作が可能になります。

## Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、最小限のコードでデータ範囲を CSV ファイルに変換できます。  
Aspose.Cells Cloud SDK の完全な一覧は、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) で確認できます。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。Gist からの読み込みがブロックされた場合は、リポジトリから直接例をダウンロードできます。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}

---