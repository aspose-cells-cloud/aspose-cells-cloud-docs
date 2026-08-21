---
title: "Excel ファイル内のテキスト コンテンツを検索して置換する"
second_title: "ドキュメント"
linktitle: "検索と置換"
type: docs
url: /search-and-replace/
aliases: [/working-with-text/, /text/]
description: "Aspose.Cells Cloud REST API を使用して、Excel ワークブックおよびワークシート内のテキストを検索・置換する方法を学びます。リクエスト形式、.NET、Java、Python 用のサンプルコード、およびエラー処理を含みます。"
keywords: "Aspose.Cells Cloud, Excel, 検索と置換, REST API, .NET, Java, Python"
weight: 20
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ファイル内のテキストを検索・置換する"
---

テキスト操作は、Excel ファイルに対して複雑な処理を伴います。この複雑さには多くの要因が関与しており、処理中に考慮すべき点も多数あります。Aspose.Cells Cloud は、さまざまなスプレッドシート形式でテキストを検索・置換するための信頼性の高い方法を提供します。

Excel ワークブックでのテキスト操作では、特定の文字列を検索して複数のシートにわたって更新することがよく必要になります。Aspose.Cells Cloud API は、サポートされているすべてのスプレッドシート形式で機能する統一された**検索と置換**操作を提供することで、このタスクを簡素化します。

## 概要

検索と置換機能を使用すると、ワークブックまたは特定のワークシート内の特定の文字列を検索し、新しい値で置換できます。この操作は、Aspose.Cells Cloud がサポートするすべての形式（**XLS、XLSX、XLSM、XLSB、ODS、CSV** など）で機能します。**検索と置換**機能を使用することで、データを迅速にクリーンアップしたり、繰り返される誤字を修正したり、ワークブック全体に一括で命名規則を適用したりできます。

## 前提条件

- 有効な **Client‑Id** と **Client‑Secret** を備えたアクティブな Aspose.Cloud アカウント。
- OAuth 2.0 認証フローにより取得したアクセストークン。
- 対象のワークブックは Aspose Cloud ストレージに保存されているか、パブリック URL からアクセス可能である必要があります。
- 必要な SDK がインストールされていること（例：Aspose.Cells‑Cloud for .NET、Java、Python）。

## API リファレンス

**メソッド:** `POST`  
**エンドポイント**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| パラメータ        | 型      | 必須 | 説明                                                                 |
| ---------------- | ------- | ---- | ------------------------------------------------------------------- |
| `fileName`       | 文字列  | はい | ワークブック名（拡張子を含む）。                                     |
| `folder`         | 文字列  | いいえ | クラウドストレージのフォルダーパス。                                |
| `storage`        | 文字列  | いいえ | ストレージ名（デフォルトでない場合）。                              |
| `sheetName`      | 文字列  | いいえ | 特定のワークシート名；省略した場合、操作はワークブック全体に適用されます。 |
| `searchString`   | 文字列  | はい | 検索するテキスト。                                                  |
| `replaceString`  | 文字列  | はい | 検索された出現箇所を置換するテキスト。                              |
| `ignoreCase`     | 真偽値  | いいえ | 大文字・小文字を区別せずに検索を実行する場合は `true` を設定します。 |
| `matchWholeCell` | 真偽値  | いいえ | セル全体が一致する場合のみ置換する場合は `true` を設定します。      |

**ヘッダー**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**リクエストボディ（JSON）**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**成功レスポンス（JSON）**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## サポートされる形式

| 形式                                | 拡張子                    |
| ----------------------------------- | ------------------------- |
| Excel ワークブック                  | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument スプレッドシート       | .ods                      |
| CSV                                 | .csv                      |
| その他の形式（Aspose.Cells がサポートするもの） | —                         |

## サンプルコード

以下は、3 つの人気のある SDK に対する最小限の例です。`{clientId}`、`{clientSecret}` およびその他のプレースホルダーを、実際の値に置き換えてください。これらのサンプルでは、**検索と置換**操作をプログラムで実行する方法を示しています。

## エラー処理とエッジケース

| HTTP コード | 意味                                             | 推奨アクション                                                       |
| ----------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| 400         | 不正リクエスト – 必須パラメータが不足しているか無効です。 | 必須フィールドとデータ型を確認してください。                         |
| 401         | 認証エラー – 無効または期限切れのトークンです。       | アクセストークンを再取得してください。                               |
| 404         | 見つかりません – ワークブックまたはワークシートが存在しません。 | ファイル名、フォルダーパス、`sheetName` を確認してください。         |
| 415         | サポートされないメディアタイプ – 無効なファイル形式です。 | アップロードされたファイルがサポートされる Excel または CSV 形式であることを確認してください。 |
| 202         | 受理済み – 処理リクエストを受け入れました。          | 非同期処理を使用している場合は、操作ステータスをポーリングしてください。 |
| 204         | コンテンツなし – 処理成功、ボディなしです。           | 置換が適用されました。追加データは返されません。                     |
| 500         | サーバー内部エラー – 予期しない失敗です。             | 少し待ってから再試行してください。問題が継続する場合は Aspose のサポートにお問い合わせください。 |

**注意事項：**  
- 大規模なワークブックはリクエストサイズ制限を超える可能性があるため、まずファイルをクラウドストレージにアップロードすることを検討してください。  
- `ignoreCase` を `true` に設定した場合、ロケール固有の大文字・小文字のマッピングが結果に影響を与える可能性がある点に注意してください。  
- `matchWholeCell` を数式付きで使用すると、数式のテキスト内での部分一致は置換されません。

## Excel ファイル内の検索と置換

- [Excel ワークブックからテキスト項目を取得する方法](/cells/workbook/get-text-items/)
- [Excel ワークシートからテキスト項目を取得する方法](/cells/worksheets/get-text-items/)
- [Excel ワークブックからテキストを検索する方法](/cells/workbook/find-text/)
- [Excel ワークシートからテキストを検索する方法](/cells/worksheets/find-text/)
- [ファイルをアップロードせずに Excel ファイルからテキストを検索する方法](/cells/search/)
- [Excel ワークブックからテキストを置換する方法](/cells/workbook/replace-text/)
- [Excel ワークシートからテキストを置換する方法](/cells/worksheets/replace-text/)
- [ファイルをアップロードせずに Excel ファイルからテキストを置換する方法](/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud API を使用して Excel ファイル内のテキストを検索・置換する",
  "description": "Aspose.Cells Cloud の検索・置換エンドポイントのドキュメント。リクエスト形式、パラメータ、例、およびエラー処理を含みます。",
  "url": "https://docs.aspose.cloud/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, 検索と置換, API, REST"
}
</script>