---
title: "Aspose.Cells Cloud – テーブルを HTML に変換"
description: "Aspose.Cells Cloud API を使用して Excel テーブルを HTML に迅速に変換 – セキュアで、書式を保持し、統合が容易です。"
keywords: "Aspose.Cells, Excel から HTML へ, テーブルを HTML に変換, クラウド API, スプレッドシート変換"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /ja/convert-table-to-html/
type: docs
---

**クイック概要** – このエンドポイントは、ローカルの Excel ワークブックを読み取り、指定された**テーブル**を抽出し、**HTML** ファイルに変換して、ダウンロード可能なストリームとして結果を返します。Aspose Cloud ストレージへの中間アップロードは不要です。

## ConvertTableToHTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| 名前               | 位置       | 型        | 必須   | 説明                                                                                      |
| ------------------ | ---------- | --------- | ------ | ----------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data  | `File`    | **Yes** | 変換対象のテーブルを含む Excel ワークブック。                                               |
| **worksheet**      | クエリー   | `String`  | **Yes** | テーブルを含むワークシートの名前。                                                          |
| **tableName**      | クエリー   | `String`  | **Yes** | 変換するテーブルの正確な名前。                                                              |
| **outPath**        | クエリー   | `String`  | いいえ  | HTML ファイルを保存する Aspose Cloud ストレージ内のフォルダーパス（オプション）。            |
| **outStorageName** | クエリー   | `String`  | いいえ  | 出力ファイル用のストレージ名（オプション）。                                                |
| **fontsLocation**  | クエリー   | `String`  | いいえ  | 変換に必要なカスタムフォントを含むフォルダーのパス。                                         |
| **region**         | クエリー   | `String`  | いいえ  | ロケール識別子（例: `ja-JP`、`en-US`、`fr-FR`）。数値や日付の書式に影響します。              |
| **password**       | クエリー   | `String`  | いいえ  | 保護されたワークブックを開くためのパスワード。                                              |
| **AutoRowsFit**    | クエリー   | `Boolean` | いいえ  | ワークシート内のすべての行を自動調整するかどうか（`true`/`false`）。                        |
| **AutoColumnsFit** | クエリー   | `Boolean` | いいえ  | ワークシート内のすべての列を自動調整するかどうか（`true`/`false`）。                        |

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

| コード | 意味                 | 説明                                                     |
| ------ | -------------------- | -------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメーターが不足しているか無効です（例: サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWT トークンが無効または不足しています。                 |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。   |
| 500    | Internal Server Error| サーバーで予期しないエラーが発生しました。               |

## Convert Table to HTML API を使用するタイミング

- **動的ウェブコンテンツ** – 価格表、スケジュール、製品リストなどをウェブページや CMS に直接埋め込みます。
- **メールテンプレート** – メールクライアント間で一貫して表示される、注文要約やレポート用の HTML スニペットを生成します。
- **ダッシュボードとレポートツール** – 完全なワークブックを読み込んだり、重いグリッドコンポーネントを使用することなく、ライブのスプレッドシートデータを表示します。
- **ドキュメントプレビュー** – 特定のスプレッドシートセクションの、書式を保持した迅速なプレビューを提供します。

## SDK を使用して Convert Table to HTML API を利用する方法

### Convert Table to HTML API 仕様

[Convert Table to HTML API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) はパブリックにアクセス可能なプログラミングインターフェースを提供し、ウェブブラウザーから直接 REST によるやり取りが可能です。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスを簡単に利用できます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速です。最小限のコードでスプレッドシートのテーブルデータを CSV ファイルに変換できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリー](https://github.com/aspose-cells-cloud)をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

---