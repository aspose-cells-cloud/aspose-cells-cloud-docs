---
title: "Aspose.Cells Trim Content API – Excel からスペースと改行を削除"
second_title: "ドキュメント"
linktitle: "コンテンツのトリム"
type: docs
url: /spreadsheet-trim-content/
keywords: "Aspose.Cells, Trim Content API, Excel データクリーニング, Excel でスペースを削除, 改行削除, スプレッドシートデータクリーニング"
description: "Aspose.Cells Cloud の PostTrimContent API を使用して、Excel セル内の余分なスペース、改行、不要な文字を自動的にクリーニングします。エンドポイント、リクエスト形式、サンプルコード、エラー処理について学びます。"
weight: 100
---

## **Excel Web API: PostTrimContent**

**PostTrimContent** API は、スプレッドシート内の指定された範囲内でコンテンツを処理し、トリム（余白や不要な文字の削除）を行います。選択されたセルの内容から余分なスペース、改行、その他の不要な文字を削除するため、データ入力のクリーニングやスプレッドシートのフォーマットの一貫性を保つのに役立ちます。

```http
POST https://api.aspose.cloud/v3.0/cells/trimcontent
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。


### **機能の説明**

- **効率性** – 指定された範囲内でのみコンテンツをトリムし、ワークシート全体に対して不要な操作を行うことを避け、時間とリソースを節約します。
- **柔軟性** – 処理対象のセル範囲をユーザーが正確に定義でき、さまざまなデータセットや要件に対応します。
- **データの整合性** – 余分なスペースや改行を削除し、分析やレポート用の一貫性があり信頼性の高いデータを維持します。
- **使いやすさ** – 最小限のセットアップで簡単に統合でき、開発者からエンドユーザーまで幅広く利用可能です。

### **リクエストパラメータ**

| パラメータ名       | 型    | 位置   | 説明                                                                 |
| ------------------ | ----- | ------ | -------------------------------------------------------------------- |
| trimContentOptions | クラス | 本文   | コンテンツをどのようにトリムするかを指定するオプション（例：対象範囲、トリムモード）。 |

### **レスポンス**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[結合されたファイル名]",
    "Filesize" : [ファイルサイズ],
    "FileContent" : "[Base64文字列]"
}
```

**HTTP ステータスコード**

| コード | 意味            | 説明                                               |
|------|-----------------|----------------------------------------------------|
| 200  | OK              | フィルターが正常に適用された。レスポンスには操作の詳細が含まれます。 |
| 400  | Bad Request     | パラメータが不足または無効（例：サポートされていないファイル形式）。 |
| 401  | Unauthorized    | JWT トークンが無効または不足しています。             |
| 413  | Payload Too Large | アップロードされたファイルがサイズ制限を超えています。 |
| 500  | Internal Server Error | サーバー内で予期しないエラーが発生しました。        |

## SDK を使用した PostRemoveCharacters API の使用方法

### PostRemoveCharacters API の仕様

[OpenAPI 仕様](https://reference.aspose.cloud/cells/#/TextProcessingController/PostTrimContent) はパブリックにアクセス可能なプログラミングインターフェースを定義しており、Web ブラウザから直接 REST 通信を実行できます。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、開発 speed を大幅に向上させることができます。SDK は低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全な一覧については [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています：

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostTrimContent.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostTrimContent.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostTrimContent.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostTrimContent.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostTrimContent.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostTrimContent.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostTrimContent.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostTrimContent.go" >}}
{{</ tab>}}
{{< /tabs >}}

_最終更新日: 2026-03-30_