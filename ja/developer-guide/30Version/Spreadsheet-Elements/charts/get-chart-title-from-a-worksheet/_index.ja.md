---
title: "ワークシートからチャートのタイトルを取得する"
type: docs
url: /charts/title/get/
aliases: [/get-chart-title-from-a-worksheet/]
weight: 120
keywords:
  - "Aspose.Cells Cloud"
  - "Chart Title"
  - "Excel"
  - "REST API"
  - "Get Chart Title"
  - "cURL"
  - "SDK"
  - "Excel chart automation"
  - "GET chart title"
description: "Aspose.Cells Cloud REST API を使用して Excel ワークシート内のチャートのタイトルを取得する方法を学びます。エンドポイント、パラメーター、認証、サンプルの cURL および SDK コードを含みます。"
ArticleTitle: "ワークシートからチャートのタイトルを取得する"
---

この REST API は、Excel ワークブックのワークシートに格納されたチャートのタイトルを取得します。

**前提条件**: このエンドポイントを呼び出すには、`Cells.Read` スコープ付きの有効な Aspose.Cells Cloud OAuth2/JWT アクセストークンが必要です。また、ワークブックはすでに指定されたストレージ場所にアップロードされている必要があります。

## GetWorksheetChartTitle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### セキュリティと認証

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必須です。

### リクエストパラメーター

| パラメーター名   | 型     | 位置   | 説明                                   |
| --------------- | ------ | ------ | --------------------------------------- |
| name            | string | path   | ワークブックファイル名。                |
| sheetName       | string | path   | チャートを含むワークシート名。          |
| chartIndex      | integer| path   | チャートの 0 から始まるインデックス。   |
| folder          | string | query  | ワークブックが格納されているフォルダーのパス。 |
| storageName     | string | query  | ストレージサービス名。                  |

[OpenAPI スペック](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChartTitle)は、パブリックに利用可能なプログラミングインターフェースを定義し、Web ブラウザーから直接 REST アクセスを可能にします。

**cURL** コマンドラインツールを使用して Aspose.Cells ウェブサービスに簡単にアクセスできます。以下の例は、cURL を使って Cloud API にリクエストを行う方法を示しています。

{{< tabs tabTotal="2" tabID="11" tabName11="リクエスト" tabName12="レスポンス" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/charts/0/title" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Title": {
    "Text": "売上 Q1",
    "Font": {
      "Name": "Arial",
      "Size": 12,
      "IsBold": true
    }
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**レスポンスフィールド**

| フィールド            | 説明                                      |
| --------------------- | ----------------------------------------- |
| `Title.Text`          | チャートタイトルとして実際に表示されるテキスト。 |
| `Title.Font.Name`     | タイトルに使用されるフォントファミリー（例: _Arial_）。 |
| `Title.Font.Size`     | フォントサイズ（ポイント単位）。          |
| `Title.Font.IsBold`   | タイトルテキストが太字かどうかを示します。 |

**レスポンスステータスコード**

| コード | 説明 |
|--------|------|
| 200 OK | チャートタイトルの取得に成功しました。 |
| 401 Unauthorized | 認証に失敗したか、トークンが不足または無効です。 |
| 404 Not Found | 指定されたワークブック、ワークシート、またはチャートが存在しません。 |
| 500 Internal Server Error | 予期しないサーバーエラーが発生しました。 |

**注意事項**: チャートインデックスは 0 から始まります。チャートが存在することを確認してください。ワークブックがアップロードされていない場合は、先に適切な API を使用してアップロードしてください。

**スクリプトでタイトルを抽出する方法（`jq` を使用）**

```bash
# JSON レスポンスを response.json に保存したと仮定
title=$(jq -r '.Title.Text' response.json)
echo "Chart title: $title"
```

## Cloud SDK ファミリー

SDK を使用すると、開発を高速化できます。SDK が低レベルの詳細を処理するため、プロジェクトのタスクに集中できます。Aspose.Cells Cloud SDK の完全なリストは [GitHub リポジトリー](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells ウェブサービスにリクエストを行う方法を示しています。

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// C# による Aspose.Cells Cloud SDK の使用例
var config = new Configuration
{
    AccessToken = "<jwt token>",
    BasePath = "https://api.aspose.cloud"
};
var api = new ChartsApi(config);
var response = api.GetWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, folder: "", storageName: "");
Console.WriteLine(response.Title.Text);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Java による Aspose.Cells Cloud SDK の使用例
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
System.out.println(response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
<?php
// PHP による Aspose.Cells Cloud SDK の使用例
$config = new Aspose\Cells\Configuration();
$config->setAccessToken('<jwt token>');
$config->setHost('https://api.aspose.cloud');
$apiInstance = new Aspose\Cells\Api\ChartsApi($config);
$response = $apiInstance->getWorksheetChartTitle('Book1.xlsx', 'Sheet1', 0, '', '');
echo $response->getTitle()->getText();
?>
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Ruby による Aspose.Cells Cloud SDK の使用例
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '<jwt token>'
config.host = 'https://api.aspose.cloud'

api_instance = AsposeCellsCloud::ChartsApi.new
result = api_instance.get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '')
puts result.title.text
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Python による Aspose.Cells Cloud SDK の使用例
from asposecellscloud import ChartsApi, Configuration

config = Configuration()
config.access_token = "<jwt token>"
config.host = "https://api.aspose.cloud"

api_instance = ChartsApi(config)
response = api_instance.get_worksheet_chart_title("Book1.xlsx", "Sheet1", 0, "", "")
print(response.title.text)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

```javascript
// Node.js による Aspose.Cells Cloud SDK の使用例
const { ChartsApi, Configuration } = require('asposecellscloud');

let config = new Configuration();
config.accessToken = "<jwt token>";
config.basePath = "https://api.aspose.cloud";

let apiInstance = new ChartsApi(config);
apiInstance.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "", (error, data) => {
    if (error) console.error(error);
    else console.log(data.title.text);
});
```

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Android (Java) による Aspose.Cells Cloud SDK の使用例
Configuration config = new Configuration();
config.setAccessToken("<jwt token>");
config.setBasePath("https://api.aspose.cloud");
ChartsApi api = new ChartsApi(config);
ChartTitleResponse response = api.getWorksheetChartTitle("Book1.xlsx", "Sheet1", 0, "", "");
Log.d("ChartTitle", response.getTitle().getText());
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Swift による Aspose.Cells Cloud SDK の使用例
import AsposeCellsCloud

let config = Configuration()
config.accessToken = "<jwt token>"
config.host = "https://api.aspose.cloud"

let api = ChartsApi(configuration: config)
api.getWorksheetChartTitle(name: "Book1.xlsx", sheetName: "Sheet1", chartIndex: 0, folder: "", storageName: "") { result, error in
    if let title = result?.title?.text {
        print("Chart title: \(title)")
    }
}
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Perl による Aspose.Cells Cloud SDK の使用例
use AsposeCellsCloud::ChartsApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new();
$config->{access_token} = '<jwt token>';
$config->{host} = 'https://api.aspose.cloud';

my $api_instance = AsposeCellsCloud::ChartsApi->new($config);
my $result = $api_instance->get_worksheet_chart_title('Book1.xlsx', 'Sheet1', 0, '', '');
print $result->{title}{text}, "\n";
```

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "e1b22ed45ca780faa3231c3a8c60ddd4" >}}

{{< /tab >}}

{{< /tabs >}}

さらに高度なシナリオ（チャートタイトルの更新や削除など）については、各 SDK のドキュメントを参照してください。

**関連項目**: [チャートタイトルの更新](/charts/title/put/)、 [チャートタイトルの削除](/charts/title/delete/)。