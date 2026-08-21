---
title: "AutoFitterOptions – プロパティと使用ガイド | Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel 自動調整, 行の高さ, 結合セル, API"
description: "Aspose.Cells Cloud API の AutoFitterOptions オブジェクトを使用して、行の高さの自動調整、結合セルの処理、非表示行／列の制御、言語設定、レンダリング設定などを制御する方法を学びます。"
weight: 79
ArticleTitle: "AutoFitterOptions – Aspose.Cells Cloud 向けプロパティと使用ガイド"
---

# AutoFitterOptions プロパティ

`AutoFitterOptions` オブジェクトは、Aspose.Cells Cloud によって実行される自動行の高さ調整を細かく制御できます。結合セルの処理、非表示行／列の制御、言語固有の書式設定、またはレンダリング特有の動作について、詳細な制御が必要な場合に有用です。

**前提条件** – これらのオプションを使用するには、**Cells.ReadWrite** スコープを含む有効な OAuth 2.0 アクセストークンで認証されている必要があります。このリクエストは、v3.0 API をサポートする任意の SDK バージョンで動作します。

| 名前                         | 型          | 説明                                                                                     | 注記                                                                                                         |
| ---------------------------- | ----------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType**   | **string**  | 結合セルの自動調整方法を決定します。                                                      | 許可される値: `All`, `First`, `None`。既定値: `All`。例: `"AutoFitMergedCellsType":"All"`                      |
| **IgnoreHidden**             | **boolean** | `true` の場合、自動調整処理中に非表示の行と列が無視されます。                             | 既定値: `false`。例: `"IgnoreHidden":false`                                                                   |
| **OnlyAuto**                 | **boolean** | 手動で高さがカスタマイズされていない行のみを自動調整するかどうかを示します。               | 既定値: `false`。例: `"OnlyAuto":false`                                                                       |
| **DefaultEditLanguage**      | **string**  | ワークブックの既定の編集言語を設定します。                                                | 既定値: システム言語（例: `"en-US"`）。例: `"DefaultEditLanguage":"en-US"`                                      |
| **MaxRowHeight**             | **double**  | 行を自動調整する際に適用される最大行の高さ（ポイント単位）。`0` の場合は制限なしを意味します。 | 既定値: `0`。例: `"MaxRowHeight":0`                                                                            |
| **AutoFitWrappedTextType**   | **string**  | セル内の折り返しテキストの自動調整方法を制御します。                                      | 許可される値: `All`, `OnlyWrapped`, `None`。既定値: `All`。例: `"AutoFitWrappedTextType":"All"`                |
| **FormatStrategy**           | **string**  | 自動調整処理中に使用される書式設定戦略を指定します。                                      | 許可される値: `AutoFit`, `PreserveExisting`。既定値: `AutoFit`。例: `"FormatStrategy":"AutoFit"`               |
| **ForRendering**             | **string**  | レンダリング目的（PDF、画像など）のために自動調整を実行するかどうかを示します。           | 許可される値: `True`, `False`。既定値: `False`。例: `"ForRendering":"False"`                                   |

以下は、`AutoFitterOptions` を設定する際に API に送信可能な典型的な JSON ペイロードです。

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

これらのオプションをワークブックに適用する `cURL` リクエストの例：

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**エンドポイント参照**

| メソッド | URL                             | 必須パラメータ                  | 説明                                             |
|----------|----------------------------------|----------------------------------|--------------------------------------------------|
| PUT      | `/cells/workbook/autoFitter`     | `autoFitterOptions`（JSON ボディ） | 指定された `AutoFitterOptions` を対象ワークブックに適用します。 |
| GET      | `/cells/workbook/autoFitter`     | *なし*                          | ワークブックの現在の `AutoFitterOptions` 設定を取得します。   |

**PUT エンドポイントのリクエストパラメータ**

| パラメータ                 | 型       | 必須 | 説明                                                   |
|----------------------------|----------|------|--------------------------------------------------------|
| AutoFitMergedCellsType     | string   | はい  | 結合セルの自動調整方法（`All`, `First`, `None`）。       |
| IgnoreHidden               | boolean  | いいえ | 非表示の行／列を無視するかどうか。                      |
| OnlyAuto                   | boolean  | いいえ | 手動で高さ設定されていない行のみを調整するかどうか。     |
| DefaultEditLanguage        | string   | いいえ | 編集言語（例: `en-US`）。                               |
| MaxRowHeight               | double   | いいえ | 最大行の高さ（ポイント単位）；`0` の場合、無制限。      |
| AutoFitWrappedTextType     | string   | いいえ | 折り返しテキストの処理方法（`All`, `OnlyWrapped`, `None`）。 |
| FormatStrategy             | string   | いいえ | 書式設定戦略（`AutoFit`, `PreserveExisting`）。          |
| ForRendering               | string   | いいえ | レンダリング用に自動調整を適用するかどうか（`True`, `False`）。 |

典型的なレスポンスコード：

- **200 OK** – 処理が正常に完了しました。  
- **400 Bad Request** – 無効な JSON ペイロード、またはサポートされていない値です。  
- **401 Unauthorized** – 認証トークンが不足している、または無効です。  
- **500 Internal Server Error** – サーバーで予期しないエラーが発生しました。  

**GET レスポンスの例**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

上記の例は、Aspose.Cells Cloud API 内で `AutoFitterOptions` モデルを設定および呼び出す方法を示しています。