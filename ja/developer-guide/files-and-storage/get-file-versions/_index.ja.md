---
title: "Aspose.Cells Cloud Get File Versions API – ファイルのバージョン履歴を迅速に取得"
second_title: "Document"
ArticleTitle: "クラウドベースのExcel管理 – Aspose.Cells Cloudでファイルのバージョン履歴を素早く取得"
linktype: "docs"
url: /ja/get-file-versions/
keywords: "Aspose Cells API, ファイルのバージョン, スプレッドシートのバージョン管理, クラウドストレージ API, REST, Excelファイルの履歴"
description: "Aspose.Cells Cloudに保存された任意のExcelファイルのバージョン履歴を完全な一覧で取得します。ストレージの選択、認証、詳細なエラーコードをサポートします。"
weight: 100
---

Aspose.Cells Cloudに保存された特定のスプレッドシートのバージョンレコードの完全な一覧を取得します。このエンドポイントにより、開発者は変更の追跡、修正の監査、およびバージョン管理ワークフローの実装をクラウドストレージから直接行えます。

**GetFileVersions** APIは、Aspose.Cells Cloudに保存された指定されたスプレッドシートのすべてのバージョンレコードを返します。これにより、各ファイルの完全な変更履歴を保持できます。

## **Excel API: ファイルのバージョンを取得**

### Web API

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud APIは安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWTトークンベースの認証</a>を必要とします。

### **GetFileVersions** APIのリクエストパラメータ

| パラメータ名     | 型     | 位置   | 説明                                                                                      |
|------------------|--------|--------|-------------------------------------------------------------------------------------------|
| `path`           | String | Path   | **必須。** バージョンを取得するファイルの完全なパス。                                     |
| `storageName`    | String | Query  | オプション。ファイルを含むストレージの名前。省略された場合、デフォルトのストレージが使用されます。 |

### **レスポンス**

```json
{
  "Name": "FileVersions",
  "Description": [
    "指定されたドキュメントのファイルバージョン一覧を含みます。"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["ファイルバージョンの詳細のコレクション。"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

正常終了した場合、APIは上記のように`Value`配列（ファイルバージョンオブジェクトの配列）を含むJSONペイロードとともに**HTTP 200 OK**を返します。

**HTTPステータスコード**

| コード | 意味                 | 説明                                                            |
| ------ | -------------------- | --------------------------------------------------------------- |
| 200    | OK                   | フィルターが正常に適用され、レスポンスに操作の詳細が含まれます。 |
| 400    | Bad Request          | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized         | JWTトークンが無効または不足しています。                          |
| 413    | Payload Too Large    | アップロードされたファイルがサイズ制限を超えています。           |
| 500    | Internal Server Error| サーバーで予期しないエラーが発生しました。                       |

## OpenAPI仕様

[OpenAPI仕様](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)は、Webブラウザから直接RESTインタラクションを実行するための包括的なプログラミングインターフェースを提供します。

cURLコマンドラインツールを使用すると、Aspose.Cellsウェブサービスに簡単にアクセスできます。以下の例では、cURLを使用してクラウドAPIを呼び出す方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKの使用

SDKを使用すると、低レベルの複雑さが抽象化されるため、開発者はコア機能に集中できます。Aspose.Cells Cloud SDKの完全な一覧については、[GitHubリポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまなプログラミング言語でAspose.Cellsウェブサービスとやり取りする方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}