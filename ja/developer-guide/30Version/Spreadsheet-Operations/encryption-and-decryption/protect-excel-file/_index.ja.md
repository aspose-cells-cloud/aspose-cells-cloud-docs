---
title: "Aspose.Cells Cloud API を使用して Excel ワークブックを保護する"
second_title: "ドキュメント"
linktitle: "Excel ファイルを保護する"
type: docs
url: /protect-excel-file/
aliases: [/protect-excel-workbooks/, /workbook/protect/]
keywords: "Aspose.Cells, Excel の保護, API, REST, SDK"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークブックを保護する方法を学びます。認証手順、クエリパラメータおよびボディパラメータ、cURL リクエスト、および C#、Java、PHP、Ruby、Node.js、Python、Perl、Go 向けの SDK コードサンプルを含みます。"
weight: 30
ArticleTitle: "Aspose.Cells Cloud API を使用して Excel ワークブックを保護する"
---

この REST API は Excel ワークブックを**保護**し、Aspose.Cells Cloud を使用してパスワードおよび保護オプションで Excel ワークブックを安全に保護できるようにします。

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### クエリパラメータ

| パラメータ名 | 型     | 説明                                                    |
|------------|--------|---------------------------------------------------------|
| folder     | string | ソースワークブックを含むフォルダー。（オプション）         |
| storageName| string | ストレージロケーションの名前。（オプション；デフォルト = "Default"） |

### リクエストボディパラメータ

| パラメータ名     | 型                        | 説明                                            |
|----------------|---------------------------|-------------------------------------------------|
| protection     | WorkbookProtectionRequest | ワークブックの保護設定を定義するオブジェクト。     |

#### WorkbookProtectionRequest

| パラメータ名     | 型     | 説明                                                                                                                                      |
|----------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------|
| ProtectionType | string | 適用する保護のタイプ。許可される値（大文字・小文字を区別しない）：**ALL**、**CONTENTS**、**NONE**、**OBJECTS**、**SCENARIOS**、**STRUCTURE**、**WINDOWS**。 |
| Password       | string | 保護用に設定するオプションのパスワード。                                                                                                    |

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                          | 説明                                                     |
|------|-------------------------------|----------------------------------------------------------|
| 200  | OK                            | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request                   | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized                  | JWT トークンが無効または不足している。                               |
| 413  | Payload Too Large             | アップロードされたファイルがサイズ制限を超えた。                     |
| 500  | Internal Server Error         | 予期しないサーバーエラーが発生した。                                 |

## SDK を使用して PostProtectDocument API を利用する方法

### 前提条件

API を呼び出す前に、以下の手順を完了していることを確認してください。

- **JWT アクセストークンを取得する**：セキュリティセクションで説明されている認証フローに従って取得します。  
- **ワークブックをアップロードする**：Aspose Cloud ストレージにワークブックをアップロードするか、ターゲットフォルダーに既に存在することを確認します。  
- **ストレージ名を確認する**（指定しない場合のデフォルトは `"Default"`）および保護したいファイルの正確なファイル名を把握します。

### PostProtectDocument API 仕様

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI 仕様</a>は、パブリックにアクセス可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 相互作用を実行できるようにします。

### 例：cURL を使用してワークブックを保護する

1. **前提条件 / 認証**で説明されている手順に従ってアクセストークンを取得します。  
2. リクエストを実行します：

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   レスポンスには、保護が成功したことを確認するステータスオブジェクトが含まれます。

### Aspose.Cells Cloud SDK を使用する

SDK を使用すると、Aspose.Cells Cloud に対する開発を最速で行えます。SDK は低レベルの詳細を抽象化し、ビジネスロジックの開発に集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、<a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub リポジトリ</a>をご覧ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### サンプルの完全レスポンス

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```