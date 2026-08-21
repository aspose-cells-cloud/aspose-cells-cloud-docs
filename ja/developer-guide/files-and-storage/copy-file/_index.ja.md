---
title: "Aspose.Cells Cloud ファイルコピー API - クラウド上で Excel ファイルを高速にコピーおよび一括処理するためのインターフェース"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースの Excel ファイル管理ソリューション – Aspose.Cells Copy File API の一括コピー機能の詳細解説"
linktype: "docs"
url: /ja/copy-file/
keywords: "Aspose.Cells, CopyFile API, Excel ファイルのコピー, クラウドストレージ, REST API"
description: "Aspose.Cells Cloud CopyFile API を使用して、Excel ファイルを効率的に複製し、複数のストレージ間で管理する方法を学びます。"
weight: 100
---

**copyFile** API を使用すると、ユーザーは指定されたソースパスから宛先パスへ Excel ファイルを複製でき、さまざまなストレージオプションをサポートします。

## **Excel API: ファイルのコピー**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

### **copyFile** API のリクエストパラメータは以下の通りです

| パラメータ名       | タイプ   | パス/クエリ文字列/HTTP ボディ | 説明                                         |
| ----------------- | -------- | ----------------------------- | -------------------------------------------- |
| srcPath           | 文字列型 | パス                          | コピーするファイルのソースパス               |
| destPath          | 文字列型 | クエリ                        | ファイルを保存する宛先パス                   |
| srcStorageName    | 文字列型 | クエリ                        | ソースストレージの名前                       |
| destStorageName   | 文字列型 | クエリ                        | 宛先ストレージの名前                         |
| versionId         | 文字列型 | クエリ                        | コピーするファイルのオプション版 ID           |

### **レスポンス**

成功時は、この操作はコンテンツを返しません。一般的な HTTP ステータスコードは以下の通りです。

**HTTP ステータスコード**

| コード | 意味                 | 説明                                                       |
| ------ | -------------------- | ---------------------------------------------------------- |
| 200    | OK（正常終了）       | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request（不正なリクエスト） | 必要なパラメータが不足しているか、無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized（認証エラー） | JWT トークンが無効または不足しています。                   |
| 413    | Payload Too Large（ペイロードが大きすぎます） | アップロードされたファイルがサイズ制限を超えています。     |
| 500    | Internal Server Error（内部サーバーエラー） | 予期しないサーバーエラーが発生しました。                   |

## SDK を使用してコピー ファイル API を活用する方法

### コピー ファイル API の仕様

[Copy File API Specification（コピー ファイル API の仕様）](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) は、Web ブラウザから直接 REST 経由でインタラクションを行うための公開可能なプログラミングインターフェースを提供します。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も迅速になります。最小限のコードでスプレッドシートのテーブルデータを画像に変換できます。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。