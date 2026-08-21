---
title: "列のグループ化 – Aspise.Cells Cloud API ドキュメント"
description: "Aspose.Cells Cloud REST API (v3.0) を使用して、Excelワークシート内のワークシート列をグループ化します。リクエスト構文、パラメータ、cURL および SDK の使用例、および応答の詳細を含みます。"
keywords: "Aspose.Cells, 列のグループ化, Excel API, REST, クラウドSDK"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Excelワークシートで列をグループ化する

**APIバージョン:** v3.0  
**操作:** `PostGroupWorksheetColumns` – ワークシート内の列をグループ化します。

---

## 概要

このREST APIを使用すると、ワークシート内の列の範囲をグループ化できます。グループ化された列は表示・非表示を切り替えることができ、Microsoft Excelと同様に折りたたみ可能なセクションを作成できます。

---

## 前提条件

- Aspose Cloud 認証サービスから取得した有効な**JWT アクセストークン**。  
- ワークブックは、Aspose.Cells Cloud がアクセス可能な場所（デフォルトストレージまたはカスタムストレージ名）に保存されていること。  
- 必要な SDK バージョン（SDK を使用する場合）： API バージョン **v3.0** をサポートする最新リリース。  

---

## 認証

すべてのリクエストには **Bearer トークン** 認証が必要です。

```http
Authorization: Bearer <access_token>
```

トークンの取得方法の詳細については、[JWT 認証ガイド](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) を参照してください。

---

## HTTP リクエスト

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| パラメータ | 位置 | 必須 | 説明 |
|-----------|------|------|-------------|
| `name` | パス | はい | ワークブックのファイル名（例: `test.xlsx`）。 |
| `sheetName` | パス | はい | グループ化する列を含むワークシート名。 |
| `firstIndex` | クエリ | はい | グループに含める最初の列の 0 から始まるインデックス。 |
| `lastIndex` | クエリ | はい | グループに含める最後の列の 0 から始まるインデックス。 |
| `hide` | クエリ | いいえ | `true` の場合、グループ化された列は非表示になります。それ以外の場合は表示されたままです。 |
| `folder` | クエリ | いいえ | ワークブックを含むフォルダへのパス。 |
| `storageName` | クエリ | いいえ | ファイルが配置されているストレージサービスの名前。 |

---

## リクエスト例（cURL）

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **注意:** リクエストは**HTTPS**を使用しており、通信は暗号化されます。

---

## 応答

### 成功（200）

| フィールド | 型 | 説明 |
|--------|---------|-------------|
| `Code` | 整数型 | HTTP ステータスコード（`200`）。 |
| `Status` | 文字列 | 操作のテキストによるステータス（`OK`）。 |

**例**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### エラー（例: 400 Bad Request）

| フィールド | 型 | 説明 |
|--------------|---------|-------------|
| `Code` | 整数型 | HTTP ステータスコード（`400`、`401`、`404`、`500` など）。 |
| `Status` | 文字列 | テキストによるステータス（`Error`）。 |
| `ErrorMessage` | 文字列 | 問題の読みやすい説明。 |
| `ErrorCode` | 文字列 | エラーのプログラム識別子。 |

**例 – Bad Request**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "無効な列インデックスです。",
  "ErrorCode": "InvalidParameter"
}
```

---

## SDK 使用例

以下のスニペットは、サポートされている SDK を使用して **ワークシート列のグループ化** 操作を呼び出す方法を示しています。

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## 備考

- **グループ化の動作:** API は列グループを作成し、Excel で展開または折りたたむことができます。`hide=true` を設定すると、グループは直ちに折りたたまれます。  
- **0 から始まるインデックス:** `firstIndex` および `lastIndex` はともに **0** から始まります。ワークシートの最初の列のインデックスは 0 です。  
- **ストレージに関する考慮事項:** ワークブックがデフォルト以外のストレージにある場合、`folder` および `storageName` の両方のクエリパラメータを指定する必要があります。  

---

## 関連項目

- [認証 – JWT トークンベース](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [ワークシート列のグループ化用 OpenAPI 仕様](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [Aspose.Cells Cloud SDK（GitHub）](https://github.com/aspose-cells-cloud)  
- [Excelワークシートで行をグループ化する](/rows/group/)  

---

> *図:* ![Excelワークシートでグループ化された列を示すスクリーンショット](./images/group-columns.png){: .img-fluid alt="Excelワークシートでグループ化された列を示すスクリーンショット" }

*上記のプレースホルダ画像は、列のグループ化の視覚的結果を示す実際のスクリーンショットに置き換える必要があります。*