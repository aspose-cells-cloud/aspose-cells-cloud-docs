---
title: "Aspose.Cells Cloud API – ファイルとフォルダー管理（アップロード、ダウンロード、コピー、移動）"
second_title: "Document"
ArticleTitle: "Excel 用クラウドファイル管理 – 効率的で安全な Excel ファイル保管およびインテリジェントな整理ソリューション"
linktitle: "ファイルとストレージ"
type: docs
url: /ja/files-and-storage/
aliases: [  /ja/working-with-files-and-storage-using-aspose-cells-cloud/ ]
keywords: "Aspose.Cells Cloud、ファイル保管 API、Excel ファイルのアップロード、Excel ファイルのダウンロード、ファイルのコピー、ファイルの移動、ファイルの削除、フォルダー管理、REST API、cURL の例"
description: "Aspose.Cells Cloud ストレージ内での Excel ファイルおよびフォルダー管理の包括的なガイドです。cURL の例、必要なパラメーター、認証に関する注意事項を含むアップロード、ダウンロード、コピー、移動、削除、およびフォルダー操作について解説します。"
weight: 100
---

Aspose.Cells Cloud は、Aspose.Cells Cloud ストレージまたはご自身で選択した任意のサードパーティクラウドストレージに保存されたファイルを操作するための包括的なヘルパー機能セットを提供します。サードパーティストレージの設定に関するご支援が必要な場合は、[Aspose Cloud UI ヘルプトピック](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics)をご参照ください。

**Aspose.Cells Cloud は、ファイル・フォルダー・ストレージ操作 API を一式提供しています。**

> **注意:** すべての API 呼び出しは **HTTPS** を使用する必要があります。JWT トークンの取得方法については、[認証ガイド](/ja/cells/authentication/) を参照してください。

**前提条件:** これらの API を使用するには、有効な Aspose Cloud アカウントが必要であり、JWT アクセストークンを取得し、ストレージ場所（Aspose Cloud ストレージまたは接続されたサードパーティストレージ）が構成されている必要があります。

**最終更新日:** 2024-12-01

## **ファイルのアップロード方法**

### アップロードファイル API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | アップロードするファイルのパス（ファイル名と拡張子を含む。例: `/folder1/Report.xlsx`） |
| file           | file   | formData | アップロードするファイル |
| storageName    | string | query  | 使用するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルが正常にアップロードされました。 |
| 400  | 不正なリクエスト – パラメーターが不足しているか、無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | ストレージが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/File/UploadFile) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### アップロードファイルの例

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使ってファイルをアップロードする方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="応答" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*注: アップロード可能なファイルの最大サイズは 100 MB です。レート制限が適用される場合があります。*

## **ファイルのダウンロード方法**

### ダウンロードファイル API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | ファイルパス（例: `/folder/Report.xlsx`） |
| storageName    | string | query  | 使用するストレージの名前 |
| versionId      | string | query  | ダウンロードするファイルバージョンの ID（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルがダウンロードされ、バイナリストリームが返されます。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | ファイルが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/File/DownloadFile) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ダウンロードファイルの例

{{< tabs tabTotal="2" tabID="13" tabName13="リクエスト" tabName14="応答" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<バイナリデータ>"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: 応答にはファイルのバイナリストリームが含まれます。cURL を使用する場合は、出力をファイルに保存してください（`-o filename.xlsx`）。*

## **ファイルの削除方法**

### ファイル削除 API 情報

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | ファイルパス（例: `/folder/Report.xlsx`） |
| storageName    | string | query  | 使用するストレージの名前 |
| versionId      | string | query  | 削除するファイルバージョンの ID（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルが正常に削除されました。 |
| 400  | 不正なリクエスト – パラメーターが不足しているか、無効です。 |
| 401  | 認証エラー – JWT トークンが無効です。 |
| 404  | ファイルが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/File/DeleteFile) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ファイル削除の例

{{< tabs tabTotal="2" tabID="15" tabName15="リクエスト" tabName16="応答" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: ファイルを削除すると、元に戻すことはできません。必要に応じてバックアップを取得してください。*

## **ファイルのコピー方法**

### ファイルコピー API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

リクエストパラメーターは以下の通りです。

| パラメーター名   | 型     | 位置   | 説明 |
|------------------|--------|--------|------|
| srcPath          | string | path   | 元のファイルパス（例: `/folder/Source.xlsx`） |
| destPath         | string | query  | 先のファイルパス（例: `/folder/Destination.xlsx`） |
| srcStorageName   | string | query  | 元のストレージ名（オプション） |
| destStorageName  | string | query  | 先のストレージ名（オプション） |
| versionId        | string | query  | コピーするファイルバージョン ID（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルが正常にコピーされました。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | 元のファイルが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/File/CopyFile) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ファイルコピーの例

{{< tabs tabTotal="2" tabID="17" tabName17="リクエスト" tabName18="応答" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: コピー操作では、元のファイルは削除されません。*

## **ファイルの移動方法**

### ファイル移動 API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

リクエストパラメーターは以下の通りです。

| パラメーター名   | 型     | 位置   | 説明 |
|------------------|--------|--------|------|
| srcPath          | string | path   | 元のファイルパス（例: `/folder/Source.xlsx`） |
| destPath         | string | query  | 先のファイルパス（例: `/folder/Destination.xlsx`） |
| srcStorageName   | string | query  | 元のストレージ名（オプション） |
| destStorageName  | string | query  | 先のストレージ名（オプション） |
| versionId        | string | query  | 移動するファイルバージョン ID（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルが正常に移動されました。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | 元のファイルが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/File/MoveFile) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ファイル移動の例

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="応答" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: ファイルを移動すると、ファイルのバージョン履歴が保持されます。*

## **フォルダーの作成方法**

### フォルダー作成 API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | 作成するフォルダーのパス（例: `folder1/folder2/`） |
| storageName    | string | query  | 使用するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | フォルダーが正常に作成されました。 |
| 400  | 不正なリクエスト – パスまたはパラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### フォルダー作成の例

{{< tabs tabTotal="2" tabID="3" tabName3="リクエスト" tabName4="応答" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*注: フォルダーのパスは大文字・小文字を区別します。*

## **フォルダー内のファイル一覧を取得する方法**

### ファイル一覧取得 API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | フォルダーのパス（例: `/folder`） |
| storageName    | string | query  | 使用するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルおよびサブフォルダーの一覧が返されます。 |
| 400  | 不正なリクエスト – パスが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | フォルダーが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ファイル一覧取得の例

{{< tabs tabTotal="2" tabID="5" tabName5="リクエスト" tabName6="応答" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*注: 応答には、指定されたパス内のファイルおよびサブフォルダーの両方が一覧表示されます。*

## **フォルダーの削除方法**

### フォルダー削除 API 情報

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型      | 位置   | 説明 |
|----------------|---------|--------|------|
| path           | string  | path   | フォルダーのパス（例: `/folder`） |
| storageName    | string  | query  | 使用するストレージの名前 |
| recursive      | boolean | query  | フォルダーを再帰的に削除する場合は `true` を設定します。 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | フォルダーが正常に削除されました。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | フォルダーが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### フォルダー削除の例

{{< tabs tabTotal="2" tabID="7" tabName7="リクエスト" tabName8="応答" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: `recursive=true` を指定してフォルダーを削除すると、そのフォルダー内のすべての内容が完全に削除されます。*

## **フォルダーのコピー方法**

### フォルダーコピー API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

リクエストパラメーターは以下の通りです。

| パラメーター名   | 型     | 位置   | 説明 |
|------------------|--------|--------|------|
| srcPath          | string | path   | 元のフォルダーのパス（例: `/src`） |
| destPath         | string | query  | 先のフォルダーのパス（例: `/dst`） |
| srcStorageName   | string | query  | 元のストレージ名（オプション） |
| destStorageName  | string | query  | 先のストレージ名（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | フォルダーが正常にコピーされました。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | 元のフォルダーが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### フォルダーコピーの例

{{< tabs tabTotal="2" tabID="21" tabName21="リクエスト" tabName22="応答" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: コピー操作では、元のフォルダーと同一の内容を持つ新しいフォルダーが作成されます。*

## **フォルダーの移動方法**

### フォルダー移動 API 情報

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

リクエストパラメーターは以下の通りです。

| パラメーター名   | 型     | 位置   | 説明 |
|------------------|--------|--------|------|
| srcPath          | string | path   | 元のフォルダーのパス（例: `/folder`） |
| destPath         | string | query  | 先のフォルダーのパス（例: `/dst`） |
| srcStorageName   | string | query  | 元のストレージ名（オプション） |
| destStorageName  | string | query  | 先のストレージ名（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | フォルダーが正常に移動されました。 |
| 400  | 不正なリクエスト – パラメーターが無効です。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | 元のフォルダーが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### フォルダー移動の例

{{< tabs tabTotal="2" tabID="23" tabName23="リクエスト" tabName24="応答" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*注: フォルダーを移動すると、内部構造およびファイルバージョンが保持されます。*

## **ストレージの存在を確認する方法**

### ストレージ存在確認 API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| storageName    | string | path   | 確認するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ストレージの存在情報が返されます（`true` または `false`）。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | ストレージが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ストレージ存在確認の例

{{< tabs tabTotal="2" tabID="33" tabName33="リクエスト" tabName34="応答" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **ファイルまたはフォルダーの存在を確認する方法**

### オブジェクト存在確認 API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | ファイルまたはフォルダーのパス（例: `/file.xlsx` または `/folder`） |
| storageName    | string | query  | 確認するストレージの名前 |
| versionId      | string | query  | ファイルバージョン ID（オプション） |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | 存在情報が返されます。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | ファイルまたはフォルダーが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### オブジェクト存在確認の例

{{< tabs tabTotal="2" tabID="37" tabName37="リクエスト" tabName38="応答" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **ディスク使用量を確認する方法**

### ディスク使用量確認 API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| storageName    | string | query  | 照会するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ディスク使用量情報が返されます。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ディスク使用量確認の例

{{< tabs tabTotal="2" tabID="40" tabName40="リクエスト" tabName41="応答" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **ファイルバージョンを取得する方法**

### ファイルバージョン取得 API 情報

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

リクエストパラメーターは以下の通りです。

| パラメーター名 | 型     | 位置   | 説明 |
|----------------|--------|--------|------|
| path           | string | path   | ファイルパス（例: `/file.xlsx`） |
| storageName    | string | query  | 照会するストレージの名前 |

**HTTP 応答**

| コード | 説明 |
|--------|------|
| 200  | ファイルバージョン一覧が返されます。 |
| 401  | 認証エラー – JWT トークンが無効または不足しています。 |
| 404  | ファイルが見つかりません。 |
| 500  | サーバー内部エラー。 |

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザーから直接 REST 経由で操作できます。

### ファイルバージョン取得の例

{{< tabs tabTotal="2" tabID="46" tabName46="リクエスト" tabName47="応答" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}