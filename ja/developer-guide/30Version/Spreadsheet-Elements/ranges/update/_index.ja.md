---
title: "Excelワークシートの範囲コンテンツを更新する方法"
second_title: "ドキュメント"
linktitle: "更新"
type: docs
url: /ja/ranges/update/
keywords: "Excel, 範囲の更新, Aspose.Cells Cloud, REST API, スプレッドシート, 範囲のスタイル, 範囲の値, 行の高さ, 列の幅"
description: "Aspose.Cells Cloud REST APIを使用してExcelワークシートの範囲コンテンツを更新します。対応するSDKを通じて、スタイル、値、行の高さ、列の幅を変更します。"
weight: 20
ArticleTitle: "Excelワークシートの範囲コンテンツを更新する方法 – Aspose.Cells Cloudドキュメント"
---

## Excelワークシートで範囲コンテンツを更新する際の作業手順

更新操作を使用する前に、有効なAspose.Cells Cloud APIトークンが取得でき、対象のワークブックがクラウドストレージ内に保存されていることを確認してください。このAPIは、Android、.NET、Go、Java、Node.js、Perl、PHP、Python、Ruby、およびSwift向けのSDKを介して利用可能です。

以下に、4つの主要な更新アクションの概要を簡潔に示します。この表は、開発者向けに各操作のHTTPメソッド、エンドポイントのパターン、主なパラメーター、および通常の成功時のレスポンスを素早く参照できるようにします。

| アクション        | HTTPメソッド | エンドポイントのパターン                                                                              | 主なパラメーター            | 200‑OK レスポンス          |
|-------------------|--------------|-------------------------------------------------------------------------------------------------------|----------------------------|----------------------------|
| スタイルを設定     | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style` オブジェクト        | 更新された範囲のスタイル    |
| 値を設定          | POST         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values` 配列              | 更新された範囲の値          |
| 行の高さ          | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` 数値              | 更新された行の高さ          |
| 列の幅            | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` 数値               | 更新された列の幅            |

このページでは、以下の4つの主要な更新アクションへの素早いアクセス方法を提供します：ワークシート上の範囲のスタイルを設定する方法、範囲の値を設定する方法、行の高さを調整する方法、および列の幅を調整する方法。

- [Excelワークシート上の範囲のスタイルを設定する方法](/cells/ranges/update/style/)  
- [Excelワークシート上の範囲の値を設定する方法](/cells/ranges/update/values/)  
- [Excelワークシート上の範囲の行の高さを設定する方法](/cells/ranges/update/row-height/)  
- [Excelワークシート上の範囲の列の幅を設定する方法](/cells/ranges/update/column-width/)  
---