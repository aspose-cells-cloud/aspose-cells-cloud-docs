---
title: "Excel の範囲の操作"
second_title: "Document"
linktitle: "範囲"
type: docs
url: /ja/ranges/
aliases: [  /ja/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel 範囲, REST API, SDK, .NET, Java, Python, セルの結合, 範囲のコピー, 範囲への値設定"
description: "Aspose.Cells Cloud REST API を使用して Excel の範囲を取得、変更、スタイル設定、結合、移動、コピーする方法を学びます。.NET、Java、Python などの SDK コードサンプルも含まれています。"
weight: 100
ArticleTitle: "Excel の範囲の操作 – Aspose.Cells Cloud ドキュメント"
---

**範囲**は、単一のセル、1 行全体、1 列全体、連続したセルのブロック、または複数のワークシートにまたがる 3 次元 (3-D) 範囲を表します。

## Excel ファイル内の範囲の操作

Aspose.Cells Cloud REST API は、各範囲操作専用のエンドポイントを提供します。以下のリストには、詳細な使用例へのリンクおよび対応する HTTP メソッドとエンドポイントが記載されています。

- [ワークブック内の名前付き範囲の取得](/cells/get-named-ranges-inside-the-workbook/) – ワークブック内に定義されたすべての名前付き範囲を取得し、そのアドレスとスコープを返します。**API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`
- [名前付き範囲に基づくセルデータの取得](/cells/get-cells-data-based-on-named-range/) – 指定された名前付き範囲に属するセルの値を返します。**API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`
- [範囲内の行の高さの変更](/cells/cells/change-heights-of-rows-inside-the-range/) – 指定された範囲内に含まれる各行の高さを調整します。**API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`
- [範囲内の列の幅の変更](/cells/cells/change-widths-of-columns-inside-the-range/) – 範囲と交差するすべての列の幅を変更します。**API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`
- [範囲内のセルを 1 つのセルに結合](/cells/combines-a-range-of-cells-into-a-single-cell/) – 選択されたセルを 1 つのセルに結合し、左上セルの値を保持します。**API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`
- [貼り付けオプションを使用してワークシート内で範囲をコピー](/cells/copy-range-in-a-worksheet-with-paste-options/) – ソース範囲を宛先範囲にコピーし、オプションで貼り付けタイプ（値、書式、数式など）を指定します。**API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`
- [範囲のスタイル設定](/cells/set-the-style-of-the-range/) – 範囲内のすべてのセルに、フォント、塗りつぶし、境界線、配置のスタイルを適用します。**API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`
- [範囲の結合セルを解除](/cells/unmerge-merged-cells-of-the-range/) – 以前の結合操作を元に戻し、元の個々のセルを復元します。**API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`
- [Excel ワークシートで名前付き範囲を移動](/cells/move-a-named-ranged-with-a-excel-worksheet/) – 名前付き範囲を同じワークシート内の新しいアドレスまたは別のワークシートに移動します。**API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`
- [Excel ワークシートで範囲の値を設定](/cells/ranges/set-value/) – 指定された範囲に単一の値または値の配列を書き込みます。**API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`

すべてのリクエストおよびレスポンスは JSON 形式です。認証には、`Authorization` ヘッダーにアクセストークンを含めてください。