---
title: "Aspose.Cells Cloud Upload File API – クラウド内でのファイル高速アップロード用インターフェース"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Upload File API – クラウド内でのファイル高速アップロード用インターフェース"
linktitle: "Upload File"
type: docs
url: /ja/upload-file/
keywords: "Aspose.Cells, ファイルアップロード, Excel API, クラウドストレージ, REST API"
description: "Aspose.Cells Cloud API を使用したファイルアップロードのガイド。リクエストパラメータ、HTTP ステータスコード、エラー処理、およびコード例をカバーします。"
weight: 100
---

**uploadFile** API により、開発者はファイルをクラウドストレージに直接アップロードし、Aspose Cells で処理できます。

## **Aspose Cells API: ファイルのアップロード**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>を要求します。

```bash
-H "Authorization: Bearer {access_token}"
```

### uploadFile API のリクエストパラメータは以下の通りです

| パラメータ名    | 型     | パス/クエリ文字列/HTTP ボディ | 説明                                                                                   |
| :-------------- | :----- | :---------------------------- | :------------------------------------------------------------------------------------- |
| UploadFiles     | File   | FormData                      | クラウドストレージへファイルをアップロードします。                                   |
| path            | String | Path                          | クラウドストレージ内の宛先パス。ファイルをアップロードするパスを指定します。         |
| storageName     | String | Query                         | ファイルがアップロードされるストレージの名前です。                                   |

### **レスポンス**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["ファイルアップロード結果"],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["アップロードされたファイル名のリスト"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["エラーのリスト"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

この API は以下の HTTP ステータスコードを返します：

| ステータスコード              | 説明                                       |
| ----------------------------- | ------------------------------------------ |
| **200 OK**                    | ファイルが正常にアップロードされました。   |
| **400 Bad Request**           | 無効なパラメータまたは不正な形式のリクエスト。 |
| **401 Unauthorized**          | 認証トークンが不足している、または無効です。 |
| **403 Forbidden**             | 指定されたストレージに対する権限が不足しています。 |
| **500 Internal Server Error** | 予期しないサーバーエラーが発生しました。   |

## SDK を使用したファイルアップロード API の使い方

### OpenAPI スペック

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/FileController/UploadFile) により、API の詳細な説明が提供され、開発者が Web ブラウザから直接 API を操作できます。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスへ簡単にアクセスできます。以下の例では、cURL を使用してクラウド API へリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を活用すると、低レベルの詳細処理が SDK 側で管理されるため、開発者はプロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud)をご覧ください。

以下のコード例では、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**関連項目**

- [Download File API](/download-file/) – クラウドストレージからファイルを取得します。
- [Copy File API](/copy-file/) – クラウドストレージ内でファイルを複製します。
- [Delete File API](/delete-file/) – クラウドストレージからファイルを削除します。