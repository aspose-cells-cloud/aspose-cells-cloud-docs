---
title: "Excel の範囲を PDF、PNG、CSV にエクスポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
ArticleTitle: "リモートスプレッドシートの範囲を他の形式にエクスポートする方法：ステップ・バイ・ステップ・ガイド"
linktitle: "範囲を形式としてエクスポート"
type: docs
url: /ja/export-range-as-format/
keywords: "Aspose Cells、Excel 範囲のエクスポート、PDF、PNG、CSV、Cloud API、スプレッドシート変換"
description: "Aspose.Cells Cloud に保存された特定の Excel 範囲を PDF、PNG、CSV またはその他の形式に変換する方法を学びます。エンドポイントの詳細、パラメーター、リクエストのサンプル、レスポンス処理、エラー情報が含まれます。"
weight: 100
---

クラウド上のスプレッドシート／Excel 範囲を形式ファイルとしてエクスポートします。形式ファイルはクラウド上に保存するか、ローカルストレージへエクスポートできます。

## 範囲を形式としてエクスポート API

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベース認証</a>が必要です。

### リクエストパラメーター

| パラメーター名     | タイプ   | 位置     | 説明                                                                                                                                                        |
| :----------------- | :----- | :------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | 文字列 | パス     | (必須) 取得するワークブックファイルの名前。                                                                                                                  |
| **worksheet**      | 文字列 | パス     | スプレッドシートのワークシート名。                                                                                                                          |
| **range**          | 文字列 | パス     | 変換する範囲（例: `A1:C12`）。                                                                                                                               |
| **format**         | 文字列 | クエリ   | (必須) 出力先の形式（例: `pdf`、`png`、`svg`）。                                                                                                             |
| **folder**         | 文字列 | クエリ   | (オプション) ワークブックが格納されているフォルダーのパス。                                                                                                  |
| **storageName**    | 文字列 | クエリ   | (オプション) カスタムクラウドストレージを使用する場合のストレージ名。                                                                                        |
| **outPath**        | 文字列 | クエリ   | (オプション) クラウドストレージ内の出力ファイルのパス。                                                                                                      |
| **outStorageName** | 文字列 | クエリ   | (オプション) 出力ファイルのストレージ名。                                                                                                                    |
| **fontsLocation**  | 文字列 | クエリ   | (オプション) カスタムフォントの場所。                                                                                                                        |
| **region**         | 文字列 | クエリ   | (オプション) スプレッドシートの地域／言語設定（例: `en-US`、`fr-FR`）。数値書式、日付解析、ロケール固有の動作に影響します。                                    |
| **password**       | 文字列 | クエリ   | (オプション) スプレッドシートファイルを開くために必要なパスワード。                                                                                          |

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

| コード | 意味                 | 説明                                                             |
| ------ | -------------------- | ---------------------------------------------------------------- |
| 200    | OK（成功）           | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | パラメーターが不足しているか無効（例: 未対応のファイル形式）。        |
| 401    | Unauthorized（未認証）      | JWT トークンが無効または不足している。                              |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。               |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラー。                                          |

## 範囲を他の形式にエクスポートする API を使用するシナリオ

### データエクスポートと移行シナリオ

- **データベース連携** – 特定の Excel 範囲をデータベースシステムに直接エクスポート。
- **アプリケーション連携** – 選択したスプレッドシートデータを SaaS アプリケーションに供給。
- **システム移行** – 古いシステムとモダンなシステム間で特定のデータ範囲を転送。
- **クロスプラットフォーム共有** – 異なるプラットフォーム間で限定的なデータサブセットを共有。

### レポーティングと分析

- **ターゲットレポーティング** – 特定のレポートセクションを分析用に他の形式にエクスポート。
- **ダッシュボードデータフィード** – 特定のデータ範囲を BI ダッシュボードツールに提供。
- **パフォーマンスメトリクス** – パフォーマンス追跡システム用に KPI 範囲を抽出。
- **財務レポーティング** – 監査用に財務諸表のセクションをエクスポート。

### 開発とテスト

- **テストデータ管理** – テスト目的で特定のデータ範囲をエクスポート。
- **開発環境** – 開発チームとサンプルデータ範囲を共有。
- **API テスト** – 特定のスプレッドシートセクションから CSV テストデータを生成。
- **プロトタイプ開発** – アプリケーションプロトタイプ用に限定的なデータセットを提供。

### ビジネスオペレーション

- **選択的データ共有** – 外部パートナーと特定のデータ範囲を共有。
- **部分的データバックアップ** – 重要なデータ範囲を選択した形式でバックアップ。
- **部署間データ転送** – 部署間で特定のデータを共有。
- **コンプライアンスレポーティング** – コンプライアンス提出用に規制データ範囲をエクスポート。

### 自動化ワークフロー

- **スケジュール付き範囲エクスポート** – 定期的に特定の範囲を自動エクスポート。
- **トリガーベースの抽出** – ビジネスイベントやトリガーに応じて範囲をエクスポート。
- **ワークフロー連携** – 範囲エクスポートをビジネスプロセスワークフローに統合。
- **バッチ範囲処理** – 複数の特定範囲をバッチ処理で操作。

## なぜ範囲を他の形式にエクスポートする API を使用すべきか？

- **開発者フレンドリー** – Aspose.Cells Cloud は複数の言語向け SDK ライブラリを提供し、充実したドキュメントにより迅速な開発を可能にします。カスタムのチャート描画ソリューションを構築する場合と比べ、開発負担を大幅に削減します。
- **人件費削減** – ドキュメント統合専任スタッフの必要が減ります。
- **ペイ・パー・ユース** – 前払い不要で、実際に使用した API コール分だけ課金されます。
- **サーバー保守不要** – サーバーの保守やソフトウェア更新が不要で、互換性の問題もありません。
- **複雑な Excel 書式を保持** – 出力ファイルは元のスプレッドシートの書式を維持します。

## SDK を使用してスプレッドシート範囲を形式としてエクスポート API を使用する方法

### 範囲を形式としてエクスポート API の仕様

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">範囲を形式としてエクスポート API の仕様</a>は、パブリックに利用可能なプログラミングインターフェースを提供し、Web ブラウザーから直接 REST 操作を実行できます。

cURL コマンドラインツールを使用すると、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は cURL を使用してクラウド API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

SDK を使用すると、低レベルの詳細が抽象化されるため、最も迅速な開発が可能です。簡潔なコードでスプレッドシート範囲を形式ファイルとしてエクスポートできます。Aspose.Cells Cloud SDK の完全な一覧は <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub リポジトリ</a>をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}