---
title: "Excel ファイルの圧縮と修復"
second_title: "Document"
type: docs
url: /compress-and-repair-excel-files/
linktitle: "圧縮と修復"
keywords: "Aspose.Cells, Excel 圧縮, Excel 修復, クラウド API, Excel ファイルサイズの削減, 損傷したワークブックの復元, Excel ファイルの圧縮, Excel ワークブックの修復"
description: "Aspose.Cells Cloud API を使って大規模な Excel ワークブックを圧縮し、損傷したファイルを修復する方法を学びます。ステップ・バイ・ステップの例、サポート言語、ベストプラクティスを紹介します。"
weight: 100
ArticleTitle: "Excel ファイルの圧縮と修復 – Aspose.Cells Cloud API"
---

Excel ワークブックを圧縮すると、未使用のスタイル、画像、共有文字列を削除してファイルサイズを縮小します。一方、修復は損傷したワークブックの整合性を回復します。Aspose.Cells Cloud API は、これらの操作それぞれに専用のエンドポイントを提供しています。

- **[Excel ファイル内のデータを圧縮する](https://docs.aspose.cloud/cells/compress-excel-files/)**
- **[Excel ファイルを修復する](https://docs.aspose.cloud/cells/repair-excel-files/)**

**ワークブック圧縮 API**  
**Compress** 操作は、シンプルな POST リクエストを使用します。以下に完全なリクエスト／レスポンス仕様を示します。

| メソッド | エンドポイント | 必須パラメータ | リクエスト本文 | サンプルレスポンス | 一般的なステータスコード |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/compress` | `file`（バイナリ）— 圧縮対象のワークブック；オプションの `outPath`（文字列）— 保存先パス | *なし*（ファイルは multipart/form‑data として送信） | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**ワークブック修復 API**  
**Repair** 操作も POST リクエストを使用します。その仕様は以下の通りです。

| メソッド | エンドポイント | 必須パラメータ | リクエスト本文 | サンプルレスポンス | 一般的なステータスコード |
|--------|----------|---------------------|--------------|-----------------|----------------------|
| POST   | `/cells/repair` | `file`（バイナリ）— 損傷したワークブック；オプションの `outPath`（文字列）— 修復後のファイル保存先 | *なし*（ファイルは multipart/form‑data として送信） | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

これらの表により、開発者は他のページを閲覧することなく、直接 API を呼び出すために必要な情報を得ることができます。

**その他のリソース**  
- 未使用の行や列を削除するなどの高度なオプションについては、完全な **[Excel ファイルの圧縮](/compress-excel-files/)** ガイドをご覧ください。  
- トラブルシューティングのヒントやエラーコードの解説については、**[Excel ファイルの修復](/repair-excel-files/)** ドキュメントをご確認ください。  
- Aspose.Cells Cloud API のより広範な理解のために、**[ファイル情報の取得](/file-info/)** や **[スプレッドシート操作](/spreadsheet-operations/)** などの関連操作もご参照ください。