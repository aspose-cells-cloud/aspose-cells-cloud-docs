---
title: "ファイル情報"
second_title: "ドキュメント"
linktitle: "ファイル情報"
type: docs
url: /ja/file-info/
keywords: "ファイル, 情報, Excel, Aspose.Cells, クラウドAPI, メタデータ, Base64"
description: "Aspose.Cells クラウド API を使用して Excel ファイルの名前、サイズ、Base64 形式のコンテンツを取得します。リクエスト構文、サンプルコード、エラー処理を含みます。"
weight: 79
ArticleTitle: "ファイル情報 – Excel ファイルのメタデータと Base64 コンテンツ（Aspose.Cells クラウド API）"
---

## FileInfo プロパティ


| 名前            | 型     | 説明                                               |
| --------------- | ------ | -------------------------------------------------- |
| **FileName**    | string | ファイル名（拡張子を含む）。                       |
| **FileSize**    | long   | ファイルのサイズ（バイト単位）。                   |
| **FileContent** | string | Base64 エンコードされた生の Excel ファイルデータ。 |

レスポンスは、上記の表に示した3つのプロパティを含む JSON 形式で返されます。例：

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### エラー

| HTTP コード | 意味                     | 発生タイミング                           |
| ----------- | ------------------------ | ---------------------------------------- |
| 200         | OK（成功）               | 正常なレスポンス。                       |
| 401         | 認証エラー（未認証）     | 認証トークンが欠落または無効です。       |
| 404         | 見つかりません（Not Found） | 指定されたファイルが存在しません。       |
| 500         | サーバー内部エラー       | 予期しないサーバー側のエラーが発生しました。 |

各エラーについて、認証トークンの有効性を確認（401）、ファイルパスを確認（404）、またはリトライ戦略に関する一般的なエラー処理ガイドを参照（500）してください。

## 関連項目

- [ワークブックの取得](https://docs.aspose.cloud/cells/get-workbook) – ワークブックオブジェクトとそのワークシートを取得します。  
- [ファイルのダウンロード](https://docs.aspose.cloud/cells/download-file) – Base64 エンコードせずに生のファイルバイトをダウンロードします。  
- [認証の概要](https://docs.aspose.cloud/cells/authentication) – アクセストークンの取得方法と使用方法について説明します。  
---