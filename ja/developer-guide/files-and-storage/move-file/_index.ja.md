---
title: "Aspose.Cells Cloud ファイル移動 API – クラウド内でのファイルを高速に移動するためのインターフェース"
second_title: "ドキュメント"
ArticleTitle: "クラウドベースの Excel ファイル効率管理ソリューション – クラウド内でのファイルを高速に移動するためのインターフェース"
linktitle: "ファイルの移動"
type: docs
url: /ja/move-file/
keywords: "Aspose.Cells, ファイル移動 API, クラウドストレージ, Excel API, ファイル管理"
description: "Aspose.Cells Cloud ストレージ内でフォルダ間でファイルを移動する方法 – v4.0 ファイル移動 API のエンドポイント、パラメータ、使用例、および SDK リンク。"
weight: 100
---

**moveFile** API は、Aspose.Cells Cloud ストレージ内でファイルをある場所から別の場所へ移動します。これにより、ファイルの整理やストレージの効率的な管理が可能になります。

## **Excel API：ファイルの移動**

### Web API

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **moveFile** API のリクエストパラメータ

| パラメータ名      | 型     | パス/クエリ文字列/HTTP ボディ | 説明                                      |
| ----------------- | ------ | ----------------------------- | ----------------------------------------- |
| srcPath           | String | Path                          | 移動対象のファイルのソースパス。          |
| destPath          | String | Query                         | ファイルの移動先パス。                    |
| srcStorageName    | String | Query                         | ソースストレージ名（該当する場合）。      |
| destStorageName   | String | Query                         | 移動先ストレージ名（該当する場合）。      |
| versionId         | String | Query                         | ファイルのバージョン ID（該当する場合）。 |

### **レスポンス**

成功したリクエストは、空の JSON ボディを含む **HTTP 200 OK** を返します。

```json
{}
```

**HTTP ステータスコード**

| HTTP コード | HTTP ステータス         | 説明                                               |
| ----------- | ----------------------- | -------------------------------------------------- |
| 200         | OK                      | Web API が正常に呼び出された。応答には操作の詳細が含まれます。 |
| 400         | Bad Request             | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401         | Unauthorized            | JWT トークンが無効または不足しています。           |
| 413         | Payload Too Large       | アップロードされたファイルがサイズ制限を超えています。 |
| 500         | Internal Server Error   | 予期しないサーバーエラーが発生しました。            |

## OpenAPI 仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/FileController/MoveFile) は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells Web サービスに簡単にアクセスできます。以下の例は、cURL を使用してクラウド API を呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

SDK を使用することで、開発を迅速化できます。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。