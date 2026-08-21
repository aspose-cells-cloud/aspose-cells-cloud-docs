---
title: "Smart Marker テンプレートで Excel レポートを構築する"
second_title: "Document"
linktype: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Workbook, SDK, API, レポート生成"
description: "Aspose.Cells Cloud REST API を使用して Smart Marker テンプレートから Excel ワークブックを生成する方法を学びます。リクエスト/レスポンスの詳細、cURL の使用例、前提条件、注意事項、および SDK のコードサンプルを含みます。"
weight: 40
ArticleTitle: "Smart Marker テンプレートで Excel レポートを構築する – Aspose.Cells Cloud API ガイド"
---

この REST API は、Smart Marker テンプレートを使用してワークブックを作成します。

## ワークブック SmartMarker API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **Smart Marker とは？**

Smart Marker とは、XML（または JSON）ファイル内のデータフィールドを Excel テンプレート内のセルにマッピングするプレースホルダー構文です。実行時に Aspose.Cells がマーカーを対応するデータで置換することで、プログラムで完全にデータが埋められたレポートを生成できます。

### **クエリパラメーター**

| パラメーター名 | 型     | 説明                                                   |
| -------------- | ------ | ------------------------------------------------------ |
| outPath        | string | 生成されたワークブックの保存先パス                     |
| folder         | string | 元のワークブックが格納されているフォルダー             |
| storageName    | string | 使用するストレージサービスの名前                       |

### **リクエストボディパラメーター**

| パラメーター名 | 型   | 説明                                     |
| -------------- | ---- | ---------------------------------------- |
| xmlFile        | file | リクエストとともにアップロードされた Smart Marker XML データファイル |

### **レスポンス**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**注意事項／制限事項:**  
- API は最大 **50 MB** の Excel ファイルをサポートします。  
- 対応フォーマットは **.xlsx**、**.xlsm**、**.xlsb** のみです。  
- アカウントごとに **1 秒あたり 20 リクエスト** のレート制限が適用されます。

**HTTP ステータスコード**

| コード | 意味                      | 説明                                                   |
|------|---------------------------|--------------------------------------------------------|
| 200  | OK                        | フィルターが正常に適用された。レスポンスには操作の詳細が含まれる。 |
| 400  | Bad Request               | パラメーターが不足または不正（例：サポートされていないファイルタイプ）。 |
| 401  | Unauthorized              | JWT トークンが不正または不足している。 |
| 413  | Payload Too Large         | アップロードされたファイルがサイズ制限を超過している。 |
| 500  | Internal Server Error     | 予期せぬサーバーエラーが発生した。 |

## ワークブック SmartMarker API の使用方法

### ワークブック SmartMarker API の仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) はパブリックにアクセス可能なプログラミングインターフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

### Aspose.Cells Cloud SDK の使用

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は cURL を使用して Cloud API を呼び出す方法を示しています。

**クイック 1 行の例**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **エラーハンドリング**

| HTTP ステータス | 説明                  | 主な原因                                                 |
| --------------- | --------------------- | -------------------------------------------------------- |
| 400             | Bad Request           | テンプレートの不足、XML の不正、パラメーターの不正など。 |
| 401             | Unauthorized          | 認証トークンが不正または不足している。                   |
| 404             | Not Found             | 指定されたワークブックまたはストレージの場所が存在しない。 |
| 500             | Internal Server Error | 予期せぬサーバーサイドの障害が発生した。                   |

**エラーレスポンスの例（400）**

```json
{
  "Code": 400,
  "Message": "XML データファイルが不足しているか、不正な形式です。"
}
```

## Cloud SDK ファミリー

SDK を使用することで開発を最適化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストについては [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}