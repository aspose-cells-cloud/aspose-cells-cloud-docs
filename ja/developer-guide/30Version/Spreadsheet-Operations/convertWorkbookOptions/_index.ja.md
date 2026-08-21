---
title: "ワークブック変換オプション"
second_title: "Document"
linktitle: "ワークブック変換オプション"
type: docs
url: /convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel変換, PDF, CSV, API"
description: "ワークブック変換オプション – Aspose.Cells Cloud APIを使用して、ExcelワークブックをPDF、CSV、HTMLなどに変換する設定を行います。"
weight: 79
ArticleTitle: "ワークブック変換オプション – Aspose.Cells Cloud API"
---

# ConvertWorkbookOptions プロパティ

**APIバージョン:** 23.12 (2024‑03)

`ConvertWorkbookOptions` は、Aspose.Cells Cloud 変換 API で使用されるリクエストモデルであり、Excelワークブックを他の形式（PDF、CSV、HTMLなど）に変換する方法を指定します。このオプションは、ソースファイル情報、ターゲット形式、ページ設定設定、および形式固有の保存オプションをまとめています。

| 名前                                | 型          | 説明                                                                                                   | 備考 |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | データファイルのソース: `CloudFileSystem`、`RequestFiles`、または `HttpUri`。                                            |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | ファイル名、サイズ、およびBase64エンコードされたコンテンツを示します。                                                   |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | 余白、向き、拡大縮小率などのページ設定プロパティ。                                              |       |
| **SaveOptions**                     | **Object**  | 形式固有の保存オプションオブジェクト（例: `PdfSaveOptions`、`HtmlSaveOptions`）を格納するコンテナ。                |       |
| **ConvertFormat**                   | **string**  | ターゲットファイル形式（例: **PDF**、**CSV**、**HTML**、**XLSX**、**TIFF** など）。                              |       |
| **CheckExcelRestriction**           | **boolean** | Excel固有の制限（最大行数、列数、シート名の長さなど）を適用するかどうかを取得または設定します。 |       |

**前提条件**

- Aspose.Cells Cloud 用の有効な OAuth 2.0 アクセストークンを取得していること。  
- ソースファイルがサポートされている `DataSource` タイプのいずれかでアクセス可能であること。

**クイック例**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64‑エンコードされたコンテンツ>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**APIリクエストの詳細**

変換操作は、以下のエンドポイントに対して **POST** リクエストを送信することで実行されます:

```
https://api.aspose.cloud/v3.0/cells/convert
```

必須ヘッダー:

| ヘッダー名            | 値                                 |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

リクエストボディは `ConvertWorkbookOptions` のJSON表現である必要があります（上記の例を参照）。すべてのプロパティは、選択された `ConvertFormat` で必要とされない限り、任意です。

**APIレスポンス**

正常な変換の場合、**HTTP 200 OK**（または非同期処理の場合 **202 Accepted**）が返され、変換されたファイルがレスポンスボディにストリーミングされます。レスポンスがストリーミングされる場合、`Content-Disposition` ヘッダーに推奨されるファイル名が含まれます。

非同期リクエストのJSONレスポンスの例:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**ステータスコード**

| コード | 意味                                     |
|------|------------------------------------------|
| 200  | 変換完了。ファイルが返されます。     |
| 202  | 変換が受理されました。結果は後で取得できます。 |
| 400  | 不正なリクエスト – パラメータが不足しているか、無効です。 |
| 401  | 認証エラー – トークンが無効または不足しています。 |
| 403  | アクセス拒否 – 権限が不十分です。   |
| 500  | サーバー内部エラー。                   |

**注意事項 / 制限事項**

- `CheckExcelRestriction` フラグは、最大行数（1,048,576）や列数（16,384）などのExcel制限を強制します。  
- すべてのターゲット形式がすべての `SaveOptions` プロパティをサポートしているわけではなく、サポートされていないオプションは無視されます。  
- `HttpUri` をデータソースとして使用する場合、URLは認証なしで公開的にアクセス可能である必要があります。  
- APIメソッドおよびエンドポイント情報は、開発者の理解を深め、統合エラーを減らすために追加されています。  

## FileSource プロパティ

| プロパティ名   | プロパティ型    | Null許容 | 読み取り専用 | デフォルト値 | 説明                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | ソースタイプ（`CloudFileSystem`、`RequestFiles`、`HttpUri`）を示します。 |
| FilePath       | String        | true     | false    |               | ファイルパスの場所。                                                       |

## DbfSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | **true**の場合、数値を文字列としてエクスポートします。  |
| SaveFormat                | String        | true     | false    |               | DBFファイル用の形式識別子。               |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## DifSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | DIFファイル用の形式識別子。               |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## DocxSaveOptions プロパティ

| プロパティ名                      | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | ソースフォントが利用できない場合に使用されるフォント。          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ワークブックのデフォルトフォントが適用されているか確認します。  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ターゲット形式のフォント互換性を検証します。   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 文字レベルでのフォント置換を制御します。           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 各シートを別々のページに強制的に配置します。               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | シートのすべての列を1ページに収めます。            |
| IgnoreError                       | Boolean       | true     | false    |               | 変換中に非重大なエラーを無視します。        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 描画対象がない場合、空白ページを生成します。 |
| PageIndex                         | Integer       | true     | false    |               | エクスポートする最初のページのインデックス。                    |
| PageCount                         | Integer       | true     | false    |               | エクスポートするページ数。                            |
| PrintingPageType                  | String        | true     | false    |               | 印刷用のページタイプを指定します。                 |
| GridlineType                      | String        | true     | false    |               | グリッドラインの描画方法を決定します。                |
| TextCrossType                     | String        | true     | false    |               | テキスト描画のクロスタイプを定義します。            |
| DefaultEditLanguage               | String        | true     | false    |               | テキスト編集のデフォルト言語。                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF描画の設定。                           |
| MergeAreas                        | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。       |
| SaveFormat                        | String        | true     | false    |               | DOCXファイル用の形式識別子。                 |
| CachedFileFolder                  | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。               |
| ClearData                         | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                   |
| CreateDirectory                   | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。    |
| EnableHttpCompression             | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。           |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。           |
| SortNames                         | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 結合セルの整合性を検証します。              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。      |

## HtmlSaveOptions プロパティ

| プロパティ名                    | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | HTML出力にページヘッダーを含めます。            |
| ExportPageFooters               | Boolean       | true     | false    |               | HTML出力にページフッターを含めます。            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | 行と列の見出しをエクスポートします。                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | すべてのワークシートを1つのHTMLファイルに表示します。          |
| ImageOptions                    | Class         | true     | false    |               | 画像描画を制御する設定。               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | 全ワークブックを1つのHTMLファイルとして保存します。          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | 隠しワークシートをエクスポートに含めます。            |
| ExportGridLines                 | Boolean       | true     | false    |               | HTML出力にグリッドラインを描画します。               |
| PresentationPreference          | Boolean       | true     | false    |               | HTMLをプレゼンテーションモード向けに最適化します。                |
| CellCssPrefix                   | String        | true     | false    |               | セル用に生成されたCSSクラス名に追加されるプレフィックス。 |
| TableCssId                      | String        | true     | false    |               | 生成されたHTMLテーブルのID属性。           |
| IsFullPathLink                  | Boolean       | true     | false    |               | リソース用にフルパスのハイパーリンクを生成します。        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | 各ワークシートのCSSを個別のファイルに配置します。      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | 類似の境界線スタイルを統合してCSSサイズを削減します。     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | 空の `<td>` 要素を強制的に結合します。             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | HTMLにセル座標（例: A1）を含めます。    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | 必要に応じて追加の見出し行/列を追加します。       |
| ExportHeadings                  | Boolean       | true     | false    |               | 行と列の見出しをエクスポートします。                     |
| ExportFormula                   | Boolean       | true     | false    |               | 計算された値ではなく数式を表示します。         |
| AddTooltipText                  | Boolean       | true     | false    |               | セルのコメントを含むツールチップを追加します。                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | 空のデータ用のプレースホルダ行を含めます。            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | 使用されていないCSSスタイルを削除します。                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | ドキュメントレベルのプロパティをHTMLのメタタグに書き込みます。  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | ワークシートレベルのプロパティをHTMLに書き込みます。           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | ワークブックレベルのプロパティをHTMLに書き込みます。            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | フレーム用のスクリプトとプロパティを含めます。          |
| AttachedFilesDirectory          | String        | true     | false    |               | 添付ファイル用のディレクトリパス。                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | 添付ファイル用のURLプレフィックス。                       |
| Encoding                        | String        | true     | false    |               | HTMLファイルの文字エンコーディング。                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | アクティブなワークシートのみをエクスポートします。                   |
| ExportChartImageFormat          | String        | true     | false    |               | 埋め込みチャート用の画像形式。               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | 画像をBase64文字列としてエンコードします。                    |
| HiddenColDisplayType            | String        | true     | false    |               | 隠し列の表示方法。                    |
| HiddenRowDisplayType            | String        | true     | false    |               | 隠し行の表示方法。                       |
| HtmlCrossStringType             | String        | true     | false    |               | クロス文字列データの描画方法を決定します。        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | 画像を一時ディレクトリにエクスポートします。             |
| PageTitle                       | String        | true     | false    |               | 生成されたHTMLページのタイトル。              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | セル値に含まれるHTMLタグを解析します。             |
| CellNameAttribute               | String        | true     | false    |               | セル参照を保持する属性名。        |
| SaveFormat                      | String        | true     | false    |               | HTMLファイル用の形式識別子。                |
| CachedFileFolder                | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。              |
| ClearData                       | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                  |
| CreateDirectory                 | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。   |
| EnableHttpCompression           | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。           |
| RefreshChartCache               | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。           |
| SortNames                       | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | 結合セルの整合性を検証します。              |
| MergeAreas                      | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                 |
| SortExternalNames               | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。     |

## ImageSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | チャート描画用の画像形式。             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG出力に埋め込まれた画像に割り当てられる名前。    |
| HorizontalResolution      | Integer       | true     | false    |               | エクスポートされた画像の水平DPI。              |
| ImageFormat               | String        | true     | false    |               | ターゲット画像形式（PNG、JPGなど）。              |
| IsCellAutoFit             | Boolean       | true     | false    |               | セル内容を画像サイズに自動調整します。         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 各ワークシートを別々のページに描画します。         |
| OnlyArea                  | Boolean       | true     | false    |               | ワークシートの定義済み領域のみをエクスポートします。    |
| PrintingPage              | String        | true     | false    |               | 印刷に使用されるページレイアウト。                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 印刷中にステータスダイアログを表示します。             |
| Quality                   | Integer       | true     | false    |               | JPEG画像の圧縮品質（0～100）。       |
| TiffCompression           | String        | true     | false    |               | TIFF画像の圧縮タイプ。                  |
| VerticalResolution        | Integer       | true     | false    |               | エクスポートされた画像の垂直DPI。                |
| SaveFormat                | String        | true     | false    |               | 画像ファイル用の形式識別子。             |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## JsonSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | エクスポートするワークシート領域を定義します。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 最初の行に列見出しが含まれているかを示します。 |
| ExportAsString            | Boolean       | true     | false    |               | すべての値を文字列としてエクスポートします。                           |
| Indent                    | String        | true     | false    |               | インデントに使用される文字列（例: 2つのスペース）。          |
| SaveFormat                | String        | true     | false    |               | JSONファイル用の形式識別子。                    |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                      |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。               |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                  |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。         |

## MarkdownSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | マークダウンファイルの文字エンコーディング。                    |
| FormatStrategy            | String        | true     | false    |               | マークダウンのフォーマットに使用される戦略（例: GitHub、CommonMark）。 |
| LineSeparator             | String        | true     | false    |               | 使用する改行文字（文字列）。                              |
| SaveFormat                | String        | true     | false    |               | マークダウンファイル用の形式識別子。                    |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                      |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                          |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。           |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。                   |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。                   |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                      |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                         |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。            |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。             |

## OoxmlSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | エクスポートされたファイルにセル名を含めます。            |
| UpdateZoom                | Boolean       | true     | false    |               | 出力ドキュメントのズームレベルを更新します。       |
| EnableZip64               | Boolean       | true     | false    |               | 大きなファイル用にZIP64拡張機能を有効にします。            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | OOXMLをOLEオブジェクトとして埋め込みます。                       |
| CompressionType           | String        | true     | false    |               | 適用される圧縮の種類（例: Normal、Maximum）。 |
| SaveFormat                | String        | true     | false    |               | OOXMLファイル用の形式識別子。               |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。              |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                  |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。   |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。           |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。           |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。              |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                 |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。     |

## PclSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | 使用するフォントの完全な名前。                      |
| fontPclName               | String        | true     | false    |               | PCL固有のフォント名。                            |
| SaveFormat                | String        | true     | false    |               | PCLファイル用の形式識別子。               |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## PDFSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | ドキュメントタイトルをPDFタイトルとして使用します。            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | ドキュメントの論理構造を保持します。     |
| EmfRenderSetting          | String        | true     | false    |               | EMF画像の描画設定。                   |
| CustomPropertiesExport    | String        | true     | false    |               | カスタムドキュメントプロパティのエクスポートを制御します。       |
| OptimizationType          | String        | true     | false    |               | PDF最適化の種類（例: Size、Speed）。        |
| Producer                  | String        | true     | false    |               | PDF生成アプリケーションの名前。                |
| PDFCompression            | String        | true     | false    |               | PDFストリーム用の圧縮アルゴリズム。               |
| FontEncoding              | String        | true     | false    |               | 埋め込みフォントに使用されるエンコーディング。                    |
| Watermark                 | Class         | true     | false    |               | PDFに適用される透かし設定。               |
| CalculateFormula          | Boolean       | true     | false    |               | エクスポート前に数式を計算します。                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | PDF描画用のフォント互換性を検証します。      |
| Compliance                | String        | true     | false    |               | PDF/AまたはPDF/X準拠レベル。                     |
| DefaultFont               | String        | true     | false    |               | ソースフォントが利用できない場合に使用されるフォント。         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 各ワークシートを個別のPDFページに配置します。        |
| PrintingPageType          | String        | true     | false    |               | 印刷用のページタイプを指定します。                |
| SecurityOptions           | Class         | true     | false    |               | パスワードや権限などのセキュリティ設定。 |
| desiredPPI                | Integer       | true     | false    |               | 望ましいピクセル每インチ解像度。                  |
| jpegQuality               | Integer       | true     | false    |               | JPEG画像の品質（0～100）。                          |
| ImageType                 | String        | true     | false    |               | ラスタライズに使用される画像タイプ。                   |
| SaveFormat                | String        | true     | false    |               | PDFファイル用の形式識別子。                 |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。              |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                  |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。   |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。           |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。           |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。              |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                 |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。     |

## PptxSaveOptions プロパティ

| プロパティ名                      | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | エクスポート時に隠し行をスキップします。                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | 行の種類に基づいてフォントサイズの調整を制御します。       |
| ExportViewType                    | String        | true     | false    |               | エクスポートするビュー（スライド、ノート）を決定します。        |
| DefaultFont                       | String        | true     | false    |               | ソースフォントが利用できない場合に使用されるフォント。           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ワークブックのデフォルトフォントが適用されているか確認します。   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ターゲット形式のフォント互換性を検証します。    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 文字レベルでのフォント置換を制御します。            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 各ワークシートを個別のスライドに配置します。             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | シートのすべての列を1つのスライドに収めます。            |
| IgnoreError                       | Boolean       | true     | false    |               | 変換中に非重大なエラーを無視します。         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 描画対象がない場合、空白スライドを生成します。 |
| PageIndex                         | Integer       | true     | false    |               | エクスポートする最初のスライドのインデックス。                    |
| PageCount                         | Integer       | true     | false    |               | エクスポートするスライド数。                            |
| PrintingPageType                  | String        | true     | false    |               | 印刷用のページタイプを指定します。                  |
| GridlineType                      | String        | true     | false    |               | グリッドラインの描画方法を決定します。                 |
| TextCrossType                     | String        | true     | false    |               | テキスト描画のクロスタイプを定義します。             |
| DefaultEditLanguage               | String        | true     | false    |               | テキスト編集のデフォルト言語。                     |
| EmfRenderSetting                  | String        | true     | false    |               | EMF描画の設定。                            |
| MergeAreas                        | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                   |
| SortExternalNames                 | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。        |
| SaveFormat                        | String        | true     | false    |               | PPTXファイル用の形式識別子。                  |
| CachedFileFolder                  | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                |
| ClearData                         | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                    |
| CreateDirectory                   | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。     |
| EnableHttpCompression             | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。             |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。             |
| SortNames                         | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。       |

## SqlScriptSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | ターゲットテーブルが既に存在するか確認します。          |
| ColumnTypeMap             | String        | true     | false    |               | 列名とSQLデータ型のマッピング。               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | すべての行をスキャンして列のタイプを推測します。                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | 生成された行間に空白行を挿入します。             |
| Separator                 | String        | true     | false    |               | 列を区切る文字列（例: カンマ、タブ）。      |
| OperatorType              | String        | true     | false    |               | 使用するSQL演算子（INSERT、UPDATEなど）。                |
| PrimaryKey                | Integer       | true     | false    |               | 主キーとして機能する列のインデックス。               |
| CreateTable               | Boolean       | true     | false    |               | CREATE TABLE文を生成します。                      |
| IdName                    | String        | true     | false    |               | 識別子列の名前。                           |
| StartId                   | Integer       | true     | false    |               | 自動インクリメントIDの開始値。                 |
| TableName                 | String        | true     | false    |               | ターゲットデータベーステーブルの名前。                       |
| ExportAsString            | Boolean       | true     | false    |               | すべての値を文字列としてエクスポートします。                           |
| ExportArea                | Class         | true     | false    |               | エクスポートするワークシート領域を定義します。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 最初の行に列見出しが含まれているかを示します。 |
| SaveFormat                | String        | true     | false    |               | SQLスクリプトファイル用の形式識別子。              |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                      |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。               |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                  |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。         |

## SvgSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | エクスポートするワークシートのインデックス。                  |
| ChartImageType            | String        | true     | false    |               | チャート描画用の画像形式。             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG出力に埋め込まれた画像に割り当てられる名前。    |
| HorizontalResolution      | Integer       | true     | false    |               | エクスポートされたSVGの水平DPI。                |
| ImageFormat               | String        | true     | false    |               | ラスタ要素用のターゲット画像形式。           |
| IsCellAutoFit             | Boolean       | true     | false    |               | セル内容をSVGサイズに自動調整します。           |
| OnePagePerSheet           | Boolean       | true     | false    |               | 各ワークシートを個別のSVGページに描画します。     |
| OnlyArea                  | Boolean       | true     | false    |               | ワークシートの定義済み領域のみをエクスポートします。    |
| PrintingPage              | String        | true     | false    |               | 印刷に使用されるページレイアウト。                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 印刷中にステータスダイアログを表示します。             |
| Quality                   | Integer       | true     | false    |               | ラスタ画像の圧縮品質。             |
| TiffCompression           | String        | true     | false    |               | SVGに埋め込まれたTIFF画像の圧縮タイプ。  |
| VerticalResolution        | Integer       | true     | false    |               | エクスポートされたSVGの垂直DPI。                  |
| SaveFormat                | String        | true     | false    |               | SVGファイル用の形式識別子。               |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## TxtSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | 使用されるクォートの種類（例: 二重引用符、一重引用符）。                            |
| Separator                 | String        | true     | false    |               | 列の区切り文字（例: カンマ、タブ）。                          |
| SeparatorString           | String        | true     | false    |               | 1文字以上が必要な場合に区切り文字として使用される完全な文字列。 |
| AlwaysQuoted              | Boolean       | true     | false    |               | すべてのフィールドをクォートするように強制します。                                         |
| SaveFormat                | String        | true     | false    |               | TXTファイル用の形式識別子。                                    |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                                 |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                                     |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。                              |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。                              |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                                 |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                                    |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。                        |

## XlsSaveOptions & XlsbSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | エクスポート中に正確なセルの色を保持します。         |
| WpsCompatibility          | Boolean       | true     | false    |               | WPS Officeとの互換性を有効にします。             |
| SaveFormat                | String        | true     | false    |               | XLS/XLSBファイル用の形式識別子。          |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。            |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                |
| CreateDirectory           | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。 |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。         |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。         |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。            |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。               |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。   |

## XmlSaveOptions プロパティ

| プロパティ名              | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | エクスポートに含めるワークシートインデックスのリスト。      |
| ExportArea                | Class         | true     | false    |               | エクスポートするワークシート領域を定義します。                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 最初の行に列見出しが含まれているかを示します。 |
| XmlMapName                | String        | true     | false    |               | ワークシートに適用されたXMLマップの名前。            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | シート名をXML要素名として使用します。             |
| DataAsAttribute           | Boolean       | true     | false    |               | セルデータを要素ではなくXML属性としてエクスポートします。 |
| SaveFormat                | String        | true     | false    |               | XMLファイル用の形式識別子。                     |
| CachedFileFolder          | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。                  |
| ClearData                 | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                      |
| CreateDirectory           | String        | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。       |
| EnableHttpCompression     | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。               |
| RefreshChartCache         | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。               |
| SortNames                 | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 結合セルの整合性を検証します。                  |
| MergeAreas                | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                     |
| SortExternalNames         | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。         |

## XpsSaveOptions プロパティ

| プロパティ名                      | プロパティ型  | Null許容 | 読み取り専用 | デフォルト値 | 説明                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | ソースフォントが利用できない場合に使用されるフォント。          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | ワークブックのデフォルトフォントが適用されているか確認します。  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | ターゲット形式のフォント互換性を検証します。   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 文字レベルでのフォント置換を制御します。           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 各ワークシートを個別のXPSページに配置します。         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | シートのすべての列を1ページに収めます。            |
| IgnoreError                       | Boolean       | true     | false    |               | 変換中に非重大なエラーを無視します。        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 描画対象がない場合、空白ページを生成します。 |
| PageIndex                         | Integer       | true     | false    |               | エクスポートする最初のページのインデックス。                    |
| PageCount                         | Integer       | true     | false    |               | エクスポートするページ数。                            |
| PrintingPageType                  | String        | true     | false    |               | 印刷用のページタイプを指定します。                 |
| GridlineType                      | String        | true     | false    |               | グリッドラインの描画方法を決定します。                |
| TextCrossType                     | String        | true     | false    |               | テキスト描画のクロスタイプを定義します。            |
| DefaultEditLanguage               | String        | true     | false    |               | テキスト編集のデフォルト言語。                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF描画の設定。                           |
| MergeAreas                        | Boolean       | true     | false    |               | 可能な場合、隣接するセルを結合します。                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 外部名前付き参照を並べ替えます。                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArtオブジェクトを最新バージョンに更新します。       |
| SaveFormat                        | String        | true     | false    |               | XPSファイル用の形式識別子。                  |
| CachedFileFolder                  | String        | true     | false    |               | 一時キャッシュファイル用のフォルダー。               |
| ClearData                         | Boolean       | true     | false    |               | 保存前に既存のデータをクリアします。                   |
| CreateDirectory                   | Boolean       | true     | false    |               | ターゲットディレクトリが存在しない場合は作成します。    |
| EnableHttpCompression             | Boolean       | true     | false    |               | レスポンスのHTTP圧縮を有効にします。            |
| RefreshChartCache                 | Boolean       | true     | false    |               | 保存前にキャッシュされたチャートデータを更新します。            |
| SortNames                         | Boolean       | true     | false    |               | 名前付き範囲をアルファベット順に並べ替えます。                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 結合セルの整合性を検証します。               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 変換中にExcel固有の制限を適用します。     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 出力ファイルのドキュメントプロパティを暗号化します。      |
---