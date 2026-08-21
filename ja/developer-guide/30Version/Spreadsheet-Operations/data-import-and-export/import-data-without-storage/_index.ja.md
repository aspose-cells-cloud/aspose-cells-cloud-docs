---
title: "ストレージを使用せずにデータをインポート – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "ストレージを使用せずにデータをインポート"
type: docs
url: /ja/import/without-using-storage/
aliases: [  /ja/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, ストレージを使用せずにデータをインポート, Excel インポート API, REST インポート"
description: "Aspose.Cells Cloud API を使用して Excel ワークブックにストレージを使用せずにデータをインポートする方法を学びます。リクエスト形式、パラメーター、cURL の例、SDK コード、エラー処理を含みます。"
weight: 10
ArticleTitle: "ストレージを使用せずにデータをインポート – Aspose.Cells Cloud API"
---

Excel データのインポートは、多くの要因が結果に影響を与えるため、複雑になることがあります。これらのすべての要因は、**インポート**プロセス中に考慮する必要があります。Aspose.Cells Cloud を使用すると、プロフェッショナルグレードの品質で、さまざまな形式やデータタイプを Excel ファイルに簡単にインポートできます。

この REST API は、Excel ファイルに**データ**をインポートします。

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### **リクエストパラメーター:**

| パラメーター名 | 型            | 位置       | 説明                                                                                                                                     |
| -------------- | ------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| file           | file          | formData  | アップロードする Excel ファイル。                                                                                                       |
| ImportOption   | ImportOption  | JSON body | インポートするデータ、そのタイプ（例: `IntArray`, `DoubleArray`, `StringArray`）、およびワークシート内での配置を定義する JSON オブジェクト。 |

**ImportOption** パラメーターの詳細は、**ImportData オプションリファレンス** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter) を参照してください。

**前提条件:**  
有効な JWT トークンを事前に生成しておく必要があります。また、ファイルサイズはサービスの上限（通常は 100 MB）を超えてはいけません。サポートされているファイル形式には、XLS、XLSX、CSV、ODS が含まれます。プログラムによるアクセスを好む場合は、適切な SDK をインストールしてください。

### レスポンス

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP ステータスコード**

| コード | 意味                         | 説明                                             |
|------|-----------------------------|-------------------------------------------------|
| 200  | OK                          | フィルターが正常に適用されました。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request                 | パラメーターが不足しているか、無効です（例: サポートされていないファイル形式）。 |
| 401  | Unauthorized                | JWT トークンが無効または不足しています。 |
| 413  | Payload Too Large           | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error       | 予期しないサーバーエラーが発生しました。 |

**注意事項:**  
リクエストを送信する際、`Content-Type: multipart/form-data` ヘッダーは `-F` フラグによって自動的に設定されます。大きなペイロードの場合、インポート前にデータを圧縮することを検討し、一時的なエラーに対して再試行ロジックを実装してください。

## SDK を使用して PostImportData API を利用する方法

### PostImportData API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、Web ブラウザーから直接 REST アクセスを実行できるようにします。

cURL コマンドラインツールを使用して、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使用して Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*`-F` フラグは `Content-Type: multipart/form-data` を自動的に設定します。*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK を使用する

SDK を使用することは、開発を迅速化する最良の方法です。SDK は低レベルの詳細を処理し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全な一覧については、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) を確認してください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}