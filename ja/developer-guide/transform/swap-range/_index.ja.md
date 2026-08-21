---
title: "Aspose.Cells Cloud – 列、行、範囲の入れ替え（v4.0）"
second_title: "ドキュメント"
ArticleTitle: "Excel の列、行、セル間でデータを交換／入れ替え"
linktype: "範囲の入れ替え"
type: docs
url: /ja/swap-range/
keywords: "Aspose Cells、Excel API、範囲の入れ替え、クラウドスプレッドシート"
description: "Aspose.Cells Cloud API を使用して Excel ファイル内の列、行、または範囲を入れ替えます。1回のリクエストで書式、数式、セル参照を保持したまま実行可能です。"
weight: 100
---

Aspose.Cells Cloud API を使用すると、Excel ファイル内の任意の2つの列、行、範囲、またはセル間でデータを自動的に交換できます。範囲の入れ替え API は、すべての書式、数式、セル参照を保持したまま、正確にデータを入れ替えられる機能を提供します。複雑なデータ再編成、バッチ処理、エンタープライズワークフロー向けのシームレスなクラウド統合をサポートします。

## **範囲の入れ替え API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **セキュリティと認証**

Aspose.Cells Cloud API は安全であり、<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT トークンベースの認証</a>が必要です。

```bash
-H "Authorization: Bearer {access_token}"
```

### **リクエストパラメーター**

| パラメーター名     | 型     | 位置       | 説明                                                                                                                                     |
| ------------------ | ------ | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | ファイル | FormData   | **必須。** 元となる Excel ワークブックファイル（`.xlsx`、`.xls`）。                                                                      |
| **worksheet1**     | 文字列  | クエリ     | **必須。** 最初のデータ領域を含むワークシート名。                                                                                         |
| **range1**         | 文字列  | クエリ     | **必須。** `worksheet1` 内で入れ替えるセル範囲（例：`A1:D10`）。                                                                           |
| **worksheet2**     | 文字列  | クエリ     | **必須。** 2番目のデータ領域を含むワークシート名（`worksheet1` と同じでも可）。                                                             |
| **range2**         | 文字列  | クエリ     | **必須。** `worksheet2` 内で入れ替えるセル範囲（例：`F1:I10`）。**重要：** `range1` と `range2` は同じ寸法である必要があります。           |
| **outPath**        | 文字列  | クエリ     | **オプション。** 変更後のワークブックを保存するクラウドストレージフォルダー。                                                              |
| **outStorageName** | 文字列  | クエリ     | **必須。** 設定済みのクラウドストレージサービス名（例：`MyCompanyStorage`）。                                                             |
| **region**         | 文字列  | クエリ     | **オプション。** 書式設定に影響を与える可能性のあるロケール設定（例：`en-US`、`ja-JP`）。                                                  |
| **password**       | 文字列  | クエリ     | **オプション。** 暗号化されたスプレッドシートを復号化するためのパスワード。暗号化されていない場合は省略可能です。                         |

**リクエストのサンプル（cURL）**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **レスポンス**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**注意事項：**  
- API は変更後のワークブックをファイルストリームとして返します。`outPath` を指定した場合、ファイルは指定されたクラウドストレージの場所にも保存されます。  
- 範囲の寸法が一致しない場合、**400 Bad Request** エラーが発生します。

### エラーコード

| コード                 | 説明                                                         |
| -------------------- | ------------------------------------------------------------ |
| **400 Bad Request**  | 無効なリクエスト URI、または範囲の寸法が一致しません。         |
| **401 Unauthorized** | 無効または期限切れのアクセストークン、またはクライアント ID／シークレットが正しくありません。 |
| **404 Not Found**    | 指定されたスプレッドシートファイルにアクセスできません。       |
| **500 Server Error** | ワークブックの処理中に内部エラーが発生しました。               |

## 範囲の入れ替え API の使用例

- **財務モデルの再編成** – 数式や条件付き書式を保持したまま、データブロックを再編成（例：Q3の予測をQ4に移動）。
- **データパイプラインとETL処理** – 最終出力の前に、ステージングワークシート内の生データ範囲とクリーニング済みデータ範囲を入れ替え。
- **エラー修正とデータ復旧** – 手動でのコピー・貼り付けなしで、誤って配置されたデータを素早く修正。

## 範囲の入れ替え API の利点

- **開発者向け** – 複数言語向け SDK が提供されており、カスタムソリューションを構築するよりも開発労力を大幅に削減。
- **人件費削減** – データの再配置を自動化し、手動での集約作業の必要性を低減。
- **従量課金制** – 実際に実行した API コールのみに課金されます。
- **メンテナンス不要** – サーバー管理が不要で、ソフトウェア更新や互換性の懸念もありません。

## SDK を使用した範囲の入れ替え API の利用方法

### 範囲の入れ替え API の仕様

[範囲の入れ替え API 仕様](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) は公開可能なプログラミングインターフェースを定義し、Web ブラウザから直接 REST 通信を実行可能にします。

### Aspose.Cells Cloud SDK の使用

SDK を使用すると、低レベルの詳細を抽象化できるため、開発が最も速く、簡潔なコードで範囲を入れ替えられます。Aspose.Cells Cloud SDK の完全な一覧は [GitHub リポジトリ](https://github.com/aspose-cells-cloud) をご確認ください。

以下のコード例は、さまざまな SDK を使用して Aspose.Cells Web サービスを呼び出す方法を示しています。

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---