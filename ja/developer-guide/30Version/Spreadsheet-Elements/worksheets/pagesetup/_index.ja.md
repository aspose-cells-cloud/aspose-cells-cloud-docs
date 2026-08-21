---
title: "ワークシートのページ設定"
second_title: "Document"
linktitle: "ページ設定"
type: docs
url: /ja/page-setup/
keywords: "Aspose.Cells, pageSetup, ワークシート, 印刷設定, 余白, 向き, 用紙サイズ, ヘッダー, フッター, 拡大縮小"
description: "Aspose.Cells CloudのPageSetupオブジェクトを使用してExcelワークシートの印刷レイアウトを設定する方法を学びます。プロパティ一覧、デフォルト値、範囲、およびC#、Java、Python用のコードサンプルを含みます。"
weight: 20
ArticleTitle: "ワークシートのページ設定 – Aspose.Cells Cloudで印刷レイアウトを設定する"
---

# **PageSetup**

Excelの印刷ページ設定

## 概要

**PageSetup** オブジェクトは、余白、向き、拡大縮小、ヘッダー、フッターなど、Excelワークシートの印刷レイアウトオプションを定義します。これらのプロパティを設定することで、開発者は目的の外観とページ分割を実現する印刷可能なワークブックを作成できます。

以下は、Aspose.Cells Cloud SDKを使用して一般的なページ設定プロパティを設定するC#の短い例です：

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// APIクライアントを初期化（資格情報を自分のものに置き換えてください）
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// PageSetup設定を定義
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// ワークブックの最初のワークシートに設定を適用
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

このスニペットは、ワークシートを横向きに設定し、A4用紙を使用し、コンテンツを中央配置し、100％の拡大縮小率を適用します。

## プロパティ

| プロパティ名              | プロパティ型 | null許容 | 読み取り専用 | デフォルト値     | 説明                                                                 |
| ------------------------- | ------------ | -------- | ------------ | ---------------- | -------------------------------------------------------------------- |
| BlackAndWhite             | bool         | false    | false        | false            | ワークシートを白黒モードで印刷します。                               |
| BottomMargin              | float        | true     | false        | 2.54 cm          | 下部余白のサイズ（センチメートル単位）。                             |
| CenterHorizontally        | bool         | false    | false        | false            | 印刷時にシートを水平方向に中央配置します。                           |
| CenterVertically          | bool         | false    | false        | false            | 印刷時にシートを垂直方向に中央配置します。                           |
| FirstPageNumber           | int          | true     | false        | 1                | シートが印刷される際に使用される最初のページ番号。                   |
| FitToPagesTall            | int          | false    | false        | 1                | ワークシートが拡大縮小される高さのページ数。                         |
| FitToPagesWide            | int          | false    | false        | 1                | ワークシートが拡大縮小される幅のページ数。                           |
| FooterMargin              | float        | true     | false        | 2.54 cm          | ページ下部からフッターまでの距離（センチメートル単位）。             |
| HeaderMargin              | float        | true     | false        | 2.54 cm          | ページ上部からヘッダーまでの距離（センチメートル単位）。             |
| IsAutoFirstPageNumber     | bool         | false    | false        | false            | 最初のページ番号を自動的に割り当てます。                             |
| IsHFAlignMargins          | bool         | false    | false        | true             | trueの場合、ヘッダー/フッターの余白がページの余白と一致します。      |
| IsHFDiffFirst             | bool         | false    | false        | false            | 最初のページのヘッダー/フッターが他のページと異なることを示します。  |
| IsHFDiffOddEven           | bool         | false    | false        | false            | 奇数ページと偶数ページのヘッダー/フッターが異なることを示します。    |
| IsHFScaleWithDoc          | bool         | false    | false        | false            | ドキュメントと一緒にヘッダーとフッターを拡大縮小します（Excel 2007以降）。 |
| IsPercentScale            | bool         | false    | false        | true             | falseの場合、`FitToPagesWide`および`FitToPagesTall`が拡大縮小を制御します。 |
| LeftMargin                | float        | true     | false        | 2.54 cm          | 左側の余白のサイズ（センチメートル単位）。                           |
| Order                     | string       | true     | false        | "DownThenOver"   | 大きなワークシートを印刷する際にExcelがページに番号を付ける順序。    |
| Orientation               | string       | false    | false        | "Portrait"       | ページの向き：**Landscape**（横向き）または**Portrait**（縦向き）。 |
| PaperSize                 | string       | true     | false        | "A4"             | 印刷に使用される用紙サイズ。                                         |
| PrintArea                 | string       | true     | false        | （なし）         | 印刷するセル範囲（例："A1:D20"）。                                   |
| PrintComments             | string       | true     | false        | "NoComments"     | シートにコメントを印刷する方法。                                     |
| PrintCopies               | int          | true     | false        | 1                | 印刷する部数。                                                       |
| PrintDraft                | bool         | false    | false        | false            | ドラフトモードでワークシートを印刷します（グラフィックなし）。       |
| PrintErrors               | string       | true     | false        | "Display"        | 表示される印刷エラーの種類。                                         |
| PrintGridlines            | bool         | false    | false        | false            | セルの罫線を印刷します。                                             |
| PrintHeadings             | bool         | false    | false        | false            | 行見出しと列見出しを印刷します。                                     |
| PrintQuality              | int          | true     | false        | 600              | 印刷品質設定（dpi）。                                                |
| PrintTitleColumns         | string       | true     | false        | （なし）         | 各印刷ページの左側に繰り返す列。                                     |
| PrintTitleRows            | string       | true     | false        | （なし）         | 各印刷ページの上部に繰り返す行。                                     |
| RightMargin               | float        | true     | false        | 2.54 cm          | 右側の余白のサイズ（センチメートル単位）。                           |
| TopMargin                 | float        | true     | false        | 2.54 cm          | 上部の余白のサイズ（センチメートル単位）。                           |
| Zoom                      | int          | false    | false        | 100              | 拡大縮小率（％単位、10–400％）。                                     |
| Header                    | object       | true     | false        | （なし）         | ページヘッダー設定。                                                 |
| Footer                    | object       | true     | false        | （なし）         | ページフッター設定。                                                 |

## 関連オブジェクト

- **Header** – ワークシートのヘッダーを設定します。
- **Footer** – ワークシートのフッターを設定します。
- **PrintOptions** – ページ区切りや印刷範囲など、追加の印刷関連設定。  
---