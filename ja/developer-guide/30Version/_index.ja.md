---
title: "Aspose.Cells Cloud 3.0 デベロッパー ガイド"
ArticleTitle: "Aspose.Cells Cloud 3.0 REST API デベロッパー ガイド – Excel ブックの作成、変換、およびスタイル設定"
second_title: "ドキュメント"
type: docs
url: /ja/developer-guide-3.0/
aliases: [  /ja/developer-guide/v3.0/ , /ja/developer-guide-v3.0/ ]
keywords: "Aspose.Cells Cloud, Excel REST API, ブック変換, チャート API, データインポート, エクスポート, PDF, CSV, JSON, デベロッパー ガイド"
description: "Aspose.Cells Cloud 3.0 REST API を使用して Excel ブックの作成、変換、スタイル設定、チャート、テーブルなどの操作方法を学習します。コードサンプルとベストプラクティスのヒントを含みます。"
weight: 150
---

## Aspose.Cells Cloud REST API の操作

**Aspose.Cells Cloud 3.0 デベロッパー ガイド** は、Excel ブックおよびワークシート操作に最もよく使用される REST API 操作について、簡潔かつ検索可能な概要を提供します。このガイドは、Excel ファイルをプログラムで作成・編集・変換・操作する必要がある開発者を対象としています。以下の一覧から必要な操作を見つけ、各リンクをクリックするとリクエスト構文、パラメータ、および実例が記載された詳細ページに移動します。このハブページでは、**Aspose.Cells Cloud REST API** のリファレンスを一元管理し、ブック関連エンドポイント、チャート処理、データのインポート・エクスポート機能などを容易に検索できるようにしています。

**前提条件:** API を使用する前に、有効な Aspose Cloud アカウント、API キーとシークレット、および開発環境に適した SDK がインストールされていることを確認してください。

### 目次
- [ファイル操作](#file-operations)
- [ホーム (セルの書式設定、行・列の管理)](#home-cell-formatting--rowcolumn-management)
- [挿入 (チャート、テーブル、OLE オブジェクト)](#insert-charts-tables--ole-objects)
- [ページレイアウト (改ページと設定)](#page-layout-page-breaks--setup)
- [数式 (計算と名前管理)](#formulas-calculate--names)
- [データ (大分類、フィルター、インポート)](#data-outline-filter--import)
- [レビュー (コメントと保護)](#review-comments--protection)
- [表示 (ウィンドウとズーム制御)](#view-window--zoom-controls)

### API 操作のクイック概要

| API グループ | サンプルエンドポイント | 主な操作 |
|-----------|----------------|----------------|
| **ブックの作成** | `POST /cells/workbook` | 新規空の Excel ブックを作成 |
| **ブックの変換** | `PUT /cells/workbook/convert` | Excel ファイルを PDF、CSV、JSON などに変換 |
| **チャートの追加** | `POST /cells/worksheets/{sheetName}/charts` | ワークシートに新しいチャートを挿入 |
| **テーブル管理** | `PUT /cells/worksheets/{sheetName}/tables/{tableName}` | リストオブジェクト（テーブル）を更新または削除 |
| **データのインポート** | `POST /cells/worksheets/{sheetName}/import` | CSV、JSON、画像、配列をワークシートへインポート |
| **数式の計算** | `POST /cells/workbook/calculate` | ブック内のすべての数式を再計算 |
| **フィルターの適用** | `POST /cells/worksheets/{sheetName}/filters` | 自動フィルター条件の追加または削除 |
| **ブックの保護** | `POST /cells/workbook/protect` | ブックにパスワードによる保護を適用 |

これらの頻出操作は、**Aspose.Cells Cloud Excel REST API** のコア機能をカバーし、各項目から詳細なドキュメントページへ直接リンクしています。

このクイック API 概要表の PDF 版をダウンロードし、オフラインで参照することもできます。

{{< tabs tabTotal="8" tabID="1" tabName1="ファイル" tabName2="ホーム" tabName3="挿入" tabName4="ページレイアウト" tabName5="数式" tabName6="データ" tabName7="レビュー" tabName8="表示" >}}
{{< tab tabNum="1" >}}
<div class="row">
    <div class="col-md-6">
        <p>ブック：新規作成、変換、別名で保存</p>
        <ul>
            <li><a href="/cells/create-an-empty-excel-workbook/" title="API で空の Excel ブックを作成" rel="noopener">空の Excel ブックを作成。</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-template-file/" title="テンプレートファイルからブックを作成" rel="noopener">テンプレートファイルから Excel ブックを作成。</a></li>
            <li><a href="/cells/create-excel-workbook-from-a-smartmarker-template/" title="SmartMarker テンプレートからブックを作成" rel="noopener">SmartMarker テンプレートから Excel ブックを作成。</a></li>
            <li><a href="/cells/convert/" title="Excel ブックを他の形式に変換" rel="noopener">Excel ブックを異なるファイル形式に変換。</a></li>
            <li><a href="/cells/saveas-other-formats/" title="Excel ブックを他の形式で保存" rel="noopener">Excel ブックを異なるファイル形式で保存。</a></li>
        </ul>
        <p>検索・置換</p>
        <ul>
            <li><a href="/cells/search/" title="Excel ファイル内のテキストを検索" rel="noopener">Excel ファイルからテキストを検索。</a></li>
            <li><a href="/cells/replace/" title="Excel ファイル内の値を置換" rel="noopener">Excel ファイル内の旧値を新値に置換。</a></li>
        </ul>
        <p>圧縮</p>
        <ul>
            <li><a href="/cells/compress/" title="Excel ファイルを圧縮" rel="noopener">Excel ファイルを圧縮。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>ブック：結合、分割</p>
        <ul>
            <li><a href="/cells/merge/" title="複数の Excel ブックを結合" rel="noopener">Excel ブックを結合。</a></li>
            <li><a href="/cells/split/" title="Excel ブックを個別のファイルに分割" rel="noopener">Excel ブックを分割。</a></li>
        </ul>
        <p>透かし・背景</p>
        <ul>
            <li><a href="/cells/add-background-in-workbook/" title="ブックに背景画像を追加" rel="noopener">ブックに背景を追加。</a></li>
            <li><a href="/cells/delete-background-in-workbook/" title="ブックの背景画像を削除" rel="noopener">ブックから背景を削除。</a></li>
            <li><a href="/cells/set-background-or-watermark-for-excel-worksheet/" title="ワークシートに背景または透かしを設定" rel="noopener">Excel ワークシートに背景または透かしを設定。</a></li>
            <li><a href="/cells/delete-background-or-watermark-of-excel-worksheet/" title="ワークシートの背景または透かしを削除" rel="noopener">Excel ワークシートから背景または透かしを削除。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="2" >}}
<div class="row">
    <div class="col-md-6">
        <p>セルのフォント、スタイル、条件付き書式、値</p>
        <ul>
            <li><a href="/cells/get-cell-style-from-a-worksheet/" title="ワークシートからセルスタイルを取得" rel="noopener">Excel ワークシートからセルスタイルを取得。</a></li>
            <li><a href="/cells/update-multiple-cells-style/" title="複数セルのスタイルを更新" rel="noopener">Excel ワークシート上の複数セルのスタイルを更新。</a></li>
            <li><a href="/cells/change-cell-style-in-excel-worksheet/" title="単一セルのスタイルを変更" rel="noopener">Excel ワークシート上のセルスタイルを更新。</a></li>
            <li><a href="/cells/apply-rich-text-formatting-to-a-cell/" title="セルにリッチテキスト書式を適用" rel="noopener">Excel ワークシート内のセルにリッチテキスト書式を設定。</a></li>
            <li><a href="/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/" title="セルの内容とスタイルをクリア" rel="noopener">Excel ワークシート上のセルの内容とスタイルをクリア。</a></li>
            <li><a href="/cells/working-with-conditional-formatting/" title="条件付き書式ルールを管理" rel="noopener">Excel ワークシートに条件付き書式を追加・削除・更新。</a></li>
            <li><a href="/cells/set-value-of-a-cell-in-a-worksheet/" title="セルの値を設定" rel="noopener">Excel ワークシート上のセルの値を設定。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>行／列：挿入、削除、コピー、非表示、自動調整</p>
        <ul>
            <li><a href="/cells/add-an-empty-row-in-a-worksheet/" title="ワークシートに空の行を挿入" rel="noopener">Excel ワークシートに空の行を追加。</a></li>
            <li><a href="/cells/delete-row-from-a-worksheet/" title="ワークシートから行を削除" rel="noopener">Excel ワークシートから行を削除。</a></li>
            <li><a href="/cells/copy-rows-in-excel-worksheet/" title="ワークシート内で行をコピー" rel="noopener">Excel ワークシート上で行をコピー。</a></li>
            <li><a href="/cells/hide-rows-in-excel-worksheet/" title="ワークシート内の行を非表示" rel="noopener">Excel ワークシート上で行を非表示。</a></li>
            <li><a href="/cells/auto-fit-rows-in-excel-workbooks/" title="ブック内の行を自動調整" rel="noopener">Excel ブック上で行を自動調整。</a></li>
            <li><a href="/cells/columns/add/" title="ワークシートに空の列を挿入" rel="noopener">Excel ワークシートに空の列を追加。</a></li>
            <li><a href="/cells/columns/delete/" title="ワークシートから列を削除" rel="noopener">Excel ワークシートから列を削除。</a></li>
            <li><a href="/cells/columns/copy/" title="ワークシート内で列をコピー" rel="noopener">Excel ワークシート上で列をコピー。</a></li>
            <li><a href="/cells/columns/hide/" title="ワークシート内の列を非表示" rel="noopener">Excel ワークシート上で列を非表示。</a></li>
            <li><a href="/cells/columns/autofit/" title="ブック内の列を自動調整" rel="noopener">Excel ブック上で列を自動調整。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="3" >}}
<div class="row">
    <div class="col-md-6">
        <p>チャート</p>
        <ul>
            <li><a href="/cells/add-a-chart-in-a-worksheet/" title="ワークシートにチャートを追加" rel="noopener">Excel ワークシートにチャートを追加。</a></li>
            <li><a href="/cells/delete-a-chart-from-a-worksheet/" title="ワークシートからチャートを削除" rel="noopener">Excel ワークシートからチャートを削除。</a></li>
            <li><a href="/cells/delete-all-charts-from-a-worksheet/" title="ワークシート内のすべてのチャートを削除" rel="noopener">Excel ワークシート上のすべてのチャートを削除。</a></li>
            <li><a href="/cells/convert-chart-to-image/" title="チャートを画像ファイルに変換" rel="noopener">チャートを画像に変換。</a></li>
            <li><a href="/cells/hide-chart-legend-in-a-worksheet/" title="チャート凡例を非表示" rel="noopener">Excel ワークシート上のチャート凡例を非表示。</a></li>
            <li><a href="/cells/update-chart-title-in-excel-worksheet/" title="チャートタイトルを更新" rel="noopener">Excel ワークシート上のチャートタイトルを更新。</a></li>
            <li><a href="/cells/delete-chart-title-in-a-worksheet/" title="チャートタイトルを削除" rel="noopener">ワークシート内のチャートタイトルを削除。</a></li>
        </ul>
        <p>テーブル</p>
        <ul>
            <li><a href="/cells/add-a-list-object-or-table-inside-the-worksheet/" title="ワークシートにテーブル（リストオブジェクト）を追加" rel="noopener">Excel ワークシートにリストオブジェクトを追加。</a></li>
            <li><a href="/cells/update-a-list-object-or-table-inside-the-worksheet/" title="ワークシート内のテーブルを更新" rel="noopener">Excel ワークシート上のリストオブジェクトを更新。</a></li>
            <li><a href="/cells/convert-list-object-or-table-to-range/" title="テーブルを範囲に変換" rel="noopener">リストオブジェクトを範囲に変換。</a></li>
            <li><a href="/cells/sort-table-data/" title="テーブル内のデータを並べ替え" rel="noopener">テーブルデータを並べ替え。</a></li>
        </ul>
        <p>OLE オブジェクト</p>
        <ul>
            <li><a href="/cells/add-oleobject-to-excel-worksheet/" title="ワークシートに OLE オブジェクトを追加" rel="noopener">Excel ワークシートに OLE オブジェクトを追加。</a></li>
            <li><a href="/cells/update-a-specific-oleobject-from-excel-worksheet/" title="特定の OLE オブジェクトを更新" rel="noopener">Excel ワークシート上の特定の OLE オブジェクトを更新。</a></li>
            <li><a href="/cells/convert-oleobject-to-image/" title="OLE オブジェクトを画像に変換" rel="noopener">OLE オブジェクトを画像に変換。</a></li>
            <li><a href="/cells/delete-all-oleobjects-from-excel-worksheet/" title="ワークシート内のすべての OLE オブジェクトを削除" rel="noopener">Excel ワークシート上のすべての OLE オブジェクトを削除。</a></li>
            <li><a href="/cells/delete-a-specific-oleobject-from-excel-worksheet/" title="特定の OLE オブジェクトを削除" rel="noopener">Excel ワークシート上の特定の OLE オブジェクトを削除。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>図形</p>
        <ul>
            <li><a href="/cells/add-a-shape-inside-the-worksheet/" title="ワークシートに図形を追加" rel="noopener">Excel ワークシートに図形を追加。</a></li>
            <li><a href="/cells/delete-all-shapes-inside-the-worksheet/" title="ワークシート内のすべての図形を削除" rel="noopener">Excel ワークシート上のすべての図形を削除。</a></li>
            <li><a href="/cells/delete-a-shape-by-index-inside-the-worksheet/" title="インデックスで図形を削除" rel="noopener">Excel ワークシート上でインデックスで図形を削除。</a></li>
        </ul>
        <p>ピボットテーブル</p>
        <ul>
            <li><a href="/cells/add-a-pivot-table-in-a-worksheet/" title="ワークシートにピボットテーブルを追加" rel="noopener">Excel ワークシートにピボットテーブルを追加。</a></li>
            <li><a href="/cells/delete-worksheet-pivot-tables/" title="ワークシート内のすべてのピボットテーブルを削除" rel="noopener">Excel ワークシート上のすべてのピボットテーブルを削除。</a></li>
            <li><a href="/cells/delete-worksheet-pivot-table-by-index/" title="インデックスでピボットテーブルを削除" rel="noopener">Excel ワークシート上でインデックスでピボットテーブルを削除。</a></li>
            <li><a href="/cells/update-cell-style-for-pivot-table/" title="ピボットテーブルのセルスタイルを更新" rel="noopener">Excel ワークシート上のピボットテーブルのセルスタイルを更新。</a></li>
            <li><a href="/cells/update-style-for-pivot-table/" title="ピボットテーブル全体のスタイルを更新" rel="noopener">Excel ワークシート上のピボットテーブルのスタイルを更新。</a></li>
            <li><a href="/cells/working-with-pivot-filters/" title="ピボットテーブルフィルターの操作" rel="noopener">Excel ワークシート上でピボットフィルターを操作。</a></li>
            <li><a href="/cells/hide-pivot-field-item/" title="ピボットフィールド項目を非表示" rel="noopener">Excel ワークシート上でピボットフィールド項目を非表示。</a></li>
            <li><a href="/cells/move-pivot-table/" title="ピボットテーブルをワークシート内で移動" rel="noopener">Excel ワークシート上でピボットテーブルを移動。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="4" >}}
<div class="row">
    <div class="col-md-6">
        <p>改ページ</p>
        <ul>
            <li><a href="/cells/insert-horizontal-page-break-inside-worksheet/" title="水平方向の改ページを挿入" rel="noopener">Excel ワークシートに水平方向の改ページを挿入。</a></li>
            <li><a href="/cells/insert-vertical-page-break-inside-worksheet/" title="垂直方向の改ページを挿入" rel="noopener">Excel ワークシートに垂直方向の改ページを挿入。</a></li>
            <li><a href="/cells/delete-horizontal-page-break-inside-worksheet/" title="水平方向の改ページを削除" rel="noopener">Excel ワークシートから水平方向の改ページを削除。</a></li>
            <li><a href="/cells/delete-vertical-page-break-inside-worksheet/" title="垂直方向の改ページを削除" rel="noopener">Excel ワークシートから垂直方向の改ページを削除。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>ページ設定</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="5" >}}
<div class="row">
    <div class="col-md-6">
        <p>計算</p>
        <ul>
            <li><a href="/cells/calculate-all-formulas-in-a-workbook/" title="ブック内のすべての数式を計算" rel="noopener">Excel ブック内のすべての数式を計算。</a></li>
            <li><a href="/cells/calculate-cells-formula/" title="特定のセルの数式を計算" rel="noopener">Excel ブック内のセルの数式を計算。</a></li>
            <li><a href="/cells/calculate-formula-in-a-worksheet/" title="ワークシート内の数式を計算" rel="noopener">Excel ワークシート上の数式を計算。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>名前（名前付き範囲）</p>
        <ul>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="6" >}}
<div class="row">
    <div class="col-md-6">
        <p>大分類（アウトライン）</p>
        <ul>
            <li><a href="/cells/group-rows-in-excel-worksheet/" title="ワークシートで行をグループ化" rel="noopener">Excel ワークシートで行をグループ化。</a></li>
            <li><a href="/cells/ungroup-rows-in-excel-worksheet/" title="ワークシートで行のグループ化を解除" rel="noopener">Excel ワークシートで行のグループ化を解除。</a></li>
        </ul>
        <p>フィルター</p>
        <ul>
            <li><a href="/cells/add-a-filter-for-a-filter-column/" title="列にフィルターを追加" rel="noopener">Excel ワークシートで列にフィルターを追加。</a></li>
            <li><a href="/cells/delete-a-filter-for-a-filter-column/" title="列フィルターを削除" rel="noopener">Excel ワークシートで列フィルターを削除。</a></li>
            <li><a href="/cells/remove-a-date-filter/" title="日付フィルターを削除" rel="noopener">Excel ワークシートで日付フィルターを削除。</a></li>
            <li><a href="/cells/add-an-icon-filter/" title="アイコンフィルターを追加" rel="noopener">Excel ワークシートにアイコンフィルターを追加。</a></li>
            <li><a href="/cells/add-date-filter-in-a-worksheet/" title="日付フィルターを追加" rel="noopener">Excel ワークシートに日付フィルターを追加。</a></li>
            <li><a href="/cells/filter-data-by-using-an-autofilter/" title="オートフィルターでデータをフィルター" rel="noopener">Excel ワークシートでオートフィルターを使用してデータをフィルター。</a></li>
            <li><a href="/cells/filter-the-top-10-items-in-the-list/" title="上位 10 件の項目をフィルター" rel="noopener">Excel ワークシートでリストの上位 10 件の項目をフィルター。</a></li>
            <li><a href="/cells/match-all-blank-cells-in-the-list/" title="空白セルすべてに一致" rel="noopener">Excel ワークシートでリスト内の空白セルすべてに一致。</a></li>
        </ul>
        <p>並べ替え</p>
        <ul>
            <li><a href="/cells/sort-worksheet-data/" title="ワークシートデータを並べ替え" rel="noopener">Excel ワークシートでデータを並べ替え。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>データのインポート</p>
        <ul>
            <li><a href="/cells/import/" title="Excel ファイルへデータをインポート" rel="noopener">Excel ファイルへデータをインポート。</a></li>
            <li><a href="/cells/import-CSV-data-into-worksheet/" title="ワークシートへ CSV データをインポート" rel="noopener">Excel ワークシートへ CSV データをインポート。</a></li>
            <li><a href="/cells/import/picture/" title="ワークシートへ画像をインポート" rel="noopener">Excel ワークシートへ画像をインポート。</a></li>
            <li><a href="/cells/import/double-array/" title="ワークシートへ倍精度浮動小数点配列をインポート" rel="noopener">Excel ワークシートへ倍精度浮動小数点配列をインポート。</a></li>
            <li><a href="/cells/import/integer-array/" title="ワークシートへ整数配列をインポート" rel="noopener">Excel ワークシートへ整数配列をインポート。</a></li>
            <li><a href="/cells/import/string-array/" title="ワークシートへ文字列配列をインポート" rel="noopener">Excel ワークシートへ文字列配列をインポート。</a></li>
            <li><a href="/cells/import/with-using-storage/" title="ストレージを使用してデータをインポート" rel="noopener">ストレージを使用して Excel ワークシートへデータをインポート。</a></li>
            <li><a href="/cells/import/without-using-storage/" title="ストレージを使用せずにデータをインポート" rel="noopener">ストレージを使用せずに Excel ワークシートへデータをインポート。</a></li>
        </ul>
        <p>アセンブリ（データ集約）</p>
        <ul>
            <li><a href="/cells/assembly/" title="Excel ファイル内でデータをアセンブリ" rel="noopener">Excel ファイル内でデータをアセンブリ。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="7" >}}
<div class="row">
    <div class="col-md-6">
        <p>コメント</p>
        <ul>
            <li><a href="/cells/add-a-comment-to-a-cell-in-a-worksheet/" title="セルにコメントを追加" rel="noopener">Excel ワークシート上のセルにコメントを追加。</a></li>
            <li><a href="/cells/update-a-comment-in-excel-workbook/" title="セルコメントを更新" rel="noopener">Excel ワークシート上のコメントを更新。</a></li>
            <li><a href="/cells/delete-all-comments-in-a-worksheet/" title="ワークシート内のすべてのコメントを削除" rel="noopener">Excel ワークシート上のすべてのコメントを削除。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>変更</p>
        <ul>
            <li><a href="/cells/protect-excel-workbooks/" title="Excel ブックを保護" rel="noopener">Excel ブックを保護。</a></li>
            <li><a href="/cells/unprotect-excel-workbooks/" title="Excel ブックの保護を解除" rel="noopener">Excel ブックの保護を解除。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}
{{< tab tabNum="8" >}}
<div class="row">
    <div class="col-md-6">
        <p>ウィンドウ</p>
        <ul>
            <li><a href="/cells/freeze-panes-in-excel-worksheet/" title="ワークシートでペインを固定" rel="noopener">Excel ワークシートでペインを固定。</a></li>
            <li><a href="/cells/unfreeze-panes-in-excel-worksheet/" title="ワークシートでペインの固定を解除" rel="noopener">Excel ワークシートでペインの固定を解除。</a></li>
            <li><a href="/cells/hide-excel-worksheets/" title="ワークシートを非表示" rel="noopener">Excel ワークシートを非表示。</a></li>
            <li><a href="/cells/unhide-excel-worksheets/" title="ワークシートの非表示を解除" rel="noopener">Excel ワークシートの非表示を解除。</a></li>
        </ul>
    </div>
    <div class="col-md-6">
        <p>ズーム</p>
        <ul>
            <li><a href="/cells/set-zoom-in-excel-worksheet/" title="ワークシートのズーム率を設定" rel="noopener">Excel ワークシートでズーム率を設定。</a></li>
        </ul>
    </div>
</div>
{{< /tab >}}

{{< /tabs >}}
---