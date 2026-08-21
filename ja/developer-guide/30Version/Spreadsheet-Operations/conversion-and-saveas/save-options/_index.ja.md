---
title: "保存オプション"
second_title: "ドキュメント"
linktype: "保存オプション"
type: docs
url: /ja/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Workbook, REST API, ファイル形式, PDF, CSV, JSON, HTTP圧縮, チャートキャッシュ, 名前付き範囲, ディレクトリ作成"
description: "Aspose.Cells Cloud REST API の SaveOptions プロパティについて説明します。これにより、開発者は HTTP 圧縮、チャートキャッシュの更新、自動ディレクトリ作成などの複数のファイル形式やオプションに応じてワークブックの保存動作を設定できます。"
weight: 79
ArticleTitle: "保存オプション – Aspose.Cells Cloud REST API ドキュメント"
---

# SaveOptions プロパティ

SaveOptions を使用すると、Aspose.Cells Cloud REST API を使ってワークブックを保存する際の動作を制御できます。これらのオプションを設定することで、HTTP 圧縮の有効化、出力形式の指定、一時ストレージの管理、チャートキャッシュの更新や自動ディレクトリ作成などの追加動作の制御が可能になります。

**前提条件**  
- 認証済みの Aspose.Cells Cloud セッション（OAuth 2.0 または JWT）。  
- 保存前に、API を通じて対象のワークブックをロードまたは作成しておく必要があります。

| 名前                      | 型         | 説明                                                                                       | 備考       |
| ------------------------- | ---------- | ------------------------------------------------------------------------------------------ | ---------- |
| **EnableHTTPCompression** | **bool?**  | 応答に対して HTTP 圧縮を有効にします。                                                     | [オプション] |
| **SaveFormat**            | **string** | ワークブックを保存する際のターゲットファイル形式を指定します。                             | [オプション] |
| **ClearData**             | **bool?**  | ファイル保存後にワークブックのデータをクリアします。                                       | [オプション] |
| **CachedFileFolder**      | **string** | 大量データを一時的に格納するために使用されるキャッシュファイルフォルダです。               | [オプション] |
| **ValidateMergedAreas**   | **bool?**  | ファイル保存前に結合セル領域を検証するかどうかを示します。既定値は `false` です。         | [オプション] |
| **RefreshChartCache**     | **bool?**  | 保存前にチャートキャッシュのデータを更新します。                                           | [オプション] |
| **CreateDirectory**       | **bool?**  | `true` の場合、ディレクトリが存在しない場合はファイル保存前に自動的に作成されます。        | [オプション] |
| **SortNames**             | **bool?**  | 名前付き範囲を保存時にアルファベット順に並べ替えます。                                     | [オプション] |

**リクエスト**  
- **メソッド:** `POST`（または操作に応じて `PUT`）  
- **エンドポイント:** `/cells/workbook/save`  
- **ヘッダー:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **本文:** `SaveOptions` モデル（上記の表）の JSON 表現に、ワークブックのデータまたは参照を加えたもの。

**レスポンス例**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "ワークブックが正常に保存されました。"
}
```

**HTTP ステータスコード**

| コード | 意味                        | 説明                                           |
|--------|-----------------------------|------------------------------------------------|
| 200    | OK                          | フィルターが正常に適用され、応答に操作の詳細が含まれます。 |
| 400    | Bad Request                 | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized                | JWT トークンが無効または不足しています。        |
| 413    | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error       | 予期しないサーバーエラーが発生しました。        |

**備考 / 注意事項**  
- **CreateDirectory** を `true` に設定すると、API はターゲットフォルダが存在しない場合に自動的に作成します。  
- **EnableHTTPCompression** を有効にすると、大きなワークブックのペイロードサイズを削減できますが、クライアントが gzip/deflate のデコードをサポートしている必要があります。  
- **RefreshChartCache** は、チャートがワークブック生成以降に変更された可能性のある動的データに依存している場合に使用してください。