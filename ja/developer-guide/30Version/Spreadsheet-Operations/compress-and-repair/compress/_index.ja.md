---
title: "Excel ファイル内のデータを圧縮する"
ArticleTitle: "Excel ファイル内のデータを圧縮する – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "Excel ファイルを圧縮する"
type: docs
url: /ja/compress-excel-files/
aliases: [  /ja/compress/ ]
keywords: "excel ファイルを圧縮, aspose cells cloud, excel 圧縮, スプレッドシート圧縮, rest api, ファイル圧縮"
description: "Aspose.Cells Cloud REST API を使用して Excel ファイル (XLS、XLSX、XLSM、XLSB、ODS) を圧縮します。圧縮レベルの設定、複数ファイルの処理、SDK を介した統合が可能です。"
weight: 39
---

## Aspose.Cells Cloud Web サービスの PostCompress API

**前提条件:**  
- 認証には有効な JWT トークンが必要です。  
- サポートされているファイル形式は XLS、XLSX、XLSM、XLSB、ODS です。  
- 1 つのリクエストあたりの最大許容ファイルサイズは 500 MB です（サービスの制限に従います）。

この REST API は、Excel ファイル内のデータを圧縮します。

- XLS、XLSX、XLSM、XLSB、ODS の圧縮
- 複数の Excel スプレッドシートファイルを迅速に圧縮
- 圧縮レベルの選択
- 複数ファイルのサポート

### Web API エンドポイント

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

### リクエストパラメーター

| パラメーター名 | 型      | パス/クエリ文字列/HTTP ボディ | 説明                                         |
|----------------|---------|-------------------------------|----------------------------------------------|
| file           | ファイル | formData                      | アップロードするファイル                      |
| CompressLevel  | 整数    | クエリ                        | 圧縮レベル（0～100）；値が高いほど圧縮率が高くなります |

### リクエストボディパラメーター

| パラメーター名 | 型     | 説明                              |
| -------------- | ------ | --------------------------------- |
| data           | ファイル | 圧縮するワークブックファイルのバイナリ内容 |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[結合後のファイル名]",
    "Filesize" : [ファイルサイズ],
    "FileContent" : "[Base64 文字列]"
}
```

*注:* `FileContent` には、Base64 文字列としてエンコードされた圧縮されたワークブックが含まれます。この文字列の長さは圧縮後のファイルサイズに対応しており、標準の Base64 ユーティリティを使用してデコードすると、バイナリ形式の Excel ファイルを取得できます。

**HTTP ステータスコード**

| コード | 意味                      | 説明                                              |
|--------|---------------------------|---------------------------------------------------|
| 200    | OK                        | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400    | Bad Request               | パラメーターが不足しているか無効です（例：サポートされていないファイル形式）。 |
| 401    | Unauthorized              | JWT トークンが無効または不足しています。           |
| 413    | Payload Too Large         | アップロードされたファイルがサイズ制限を超えています。 |
| 500    | Internal Server Error     | サーバーで予期しないエラーが発生しました。         |

## SDK を使用して PostCompress API を活用する方法

### PostCompress API 仕様

[OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) は、パブリックにアクセス可能なプログラミングインタフェースを定義し、ウェブブラウザから直接 REST 通信を実行できるようにします。

cURL コマンドラインツールを使用すると、Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例では、cURL を使用して Cloud API にリクエストを送信する方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
# セキュアな接続には HTTPS を使用
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発を最速で加速できます。SDK は低レベルの詳細を抽象化し、プロジェクトのタスクに集中できるようにします。Aspose.Cells Cloud SDK の完全なリストについては、[GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスを呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}