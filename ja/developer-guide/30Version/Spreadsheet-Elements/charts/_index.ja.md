---
title: "Excel チャートの操作"
second_title: "ドキュメント"
linktitle: "チャート"
type: docs
url: /charts/
aliases: [/working-with-charts/]
keywords: "Aspose, Cells, Excel, チャート, API, REST, クラウド, スプレッドシート"
description: "Aspose.Cells Cloud API を使用して Excel チャートを管理する方法を学びます。チャートの取得、追加、更新、削除、および画像への変換のためのステップ・バイ・ステップ・ガイド、コード・サンプル、エラー処理について解説します。"
weight: 100
ArticleTitle: "Excel チャートの操作 – Aspose.Cells Cloud ドキュメント"
---

## Excel ファイル上のチャートの操作

**最終更新日：** 2026年7月  

Excel チャートは、データの視覚的表現であり、ユーザーがトレンドやパターンを素早く理解できるように支援します。  
Aspose.Cells Cloud API を使用すると、開発者はクラウド上に保存された Excel ワークブック内のチャートをプログラムで操作できます。API を使用することで、既存のチャートを取得したり、新しいチャートを追加したり、タイトル・軸・凡例などのプロパティを変更したり、不要なチャートを削除したり、レポートや後続処理用にチャートを画像形式に変換したりできます。以下のリンクから、各サポート対象のチャート関連操作の詳細な操作ページへ直接アクセスできます。

### クイックリファレンス

| 操作 | HTTP メソッド | エンドポイント (テンプレート) | ドキュメント |
|-----------|-------------|---------------------|---------------|
| チャートの取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [ワークシートからチャートを取得](/cells/get-chart-from-a-worksheet/) |
| チャートの追加 | POST | `/cells/{file}/worksheets/{sheet}/charts` | [ワークシートにチャートを追加](/cells/add-a-chart-in-a-worksheet/) |
| すべてのチャートを削除 | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [ワークシートからすべてのチャートを削除](/cells/delete-all-charts-from-a-worksheet/) |
| チャートの削除 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [ワークシートからチャートを削除](/cells/delete-a-chart-from-a-worksheet/) |
| チャートを画像に変換 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [チャートを画像に変換](/cells/convert-chart-to-image/) |
| チャートエリアの取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [ワークシートからチャートエリアを取得](/cells/get-chart-area-from-a-worksheet/) |
| 塗りつぶし形式の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [ワークシートのチャートエリアの塗りつぶし形式を取得](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| 凡例の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [ワークシートからチャート凡例を取得](/cells/get-chart-legend-from-a-worksheet/) |
| 凡例の更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [ワークシートでチャート凡例を更新](/cells/update-chart-legend-in-a-worksheet/) |
| 凡例を表示 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [ワークシートでチャート凡例を表示](/cells/show-chart-legend-in-a-worksheet/) |
| 凡例を非表示 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [ワークシートでチャート凡例を非表示](/cells/hide-chart-legend-in-a-worksheet/) |
| タイトルの取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [ワークシートからチャートタイトルを取得](/cells/get-chart-title-from-a-worksheet/) |
| タイトルの設定 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel ワークシートでチャートタイトルを設定](/cells/set-chart-title-in-excel-worksheet/) |
| タイトルの更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Excel ワークシートでチャートタイトルを更新](/cells/update-chart-title-in-excel-worksheet/) |
| タイトルの削除 | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [ワークシートでチャートタイトルを削除](/cells/delete-chart-title-in-a-worksheet/) |
| チャートプロパティの更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [チャートプロパティを更新](/cells/charts/properties/update/) |
| カテゴリ軸の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [チャートのカテゴリ軸を取得](/cells/charts/category-axis/get/) |
| 値軸の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [チャートの値軸を取得](/cells/charts/value-axis/get/) |
| 第2カテゴリ軸の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [チャートの第2カテゴリ軸を取得](/cells/charts/second-category-axis/get/) |
| 第2値軸の取得 | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [チャートの第2値軸を取得](/cells/charts/second-value-axis/get/) |
| カテゴリ軸の更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [チャートのカテゴリ軸を更新](/cells/charts/category-axis/update/) |
| 値軸の更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [チャートの値軸を更新](/cells/charts/value-axis/update/) |
| 第2カテゴリ軸の更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [チャートの第2カテゴリ軸を更新](/cells/charts/second-category-axis/update/) |
| 第2値軸の更新 | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [チャートの第2値軸を更新](/cells/charts/second-value-axis/update/) |

- [ワークシートからチャートを取得](/cells/get-chart-from-a-worksheet/)
- [ワークシートにチャートを追加](/cells/add-a-chart-in-a-worksheet/)
- [ワークシートからすべてのチャートを削除](/cells/delete-all-charts-from-a-worksheet/)
- [ワークシートからチャートを削除](/cells/delete-a-chart-from-a-worksheet/)
- [チャートを画像に変換](/cells/convert-chart-to-image/)
- [ワークシートからチャートエリアを取得](/cells/get-chart-area-from-a-worksheet/)
- [ワークシートのチャートエリアの塗りつぶし形式を取得](/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [ワークシートからチャート凡例を取得](/cells/get-chart-legend-from-a-worksheet/)
- [ワークシートでチャート凡例を更新](/cells/update-chart-legend-in-a-worksheet/)
- [ワークシートでチャート凡例を表示](/cells/show-chart-legend-in-a-worksheet/)
- [ワークシートでチャート凡例を非表示](/cells/hide-chart-legend-in-a-worksheet/)
- [ワークシートからチャートタイトルを取得](/cells/get-chart-title-from-a-worksheet/)
- [Excel ワークシートでチャートタイトルを設定](/cells/set-chart-title-in-excel-worksheet/)
- [Excel ワークシートでチャートタイトルを更新](/cells/update-chart-title-in-excel-worksheet/)
- [ワークシートでチャートタイトルを削除](/cells/delete-chart-title-in-a-worksheet/)
- [チャートプロパティを更新](/cells/charts/properties/update/)
- [チャートのカテゴリ軸を取得](/cells/charts/category-axis/get/)
- [チャートの値軸を取得](/cells/charts/value-axis/get/)
- [チャートの第2カテゴリ軸を取得](/cells/charts/second-category-axis/get/)
- [チャートの第2値軸を取得](/cells/charts/second-value-axis/get/)
- [チャートのカテゴリ軸を更新](/cells/charts/category-axis/update/)
- [チャートの値軸を更新](/cells/charts/value-axis/update/)
- [チャートの第2カテゴリ軸を更新](/cells/charts/second-category-axis/update/)
- [チャートの第2値軸を更新](/cells/charts/second-value-axis/update/)