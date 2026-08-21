---
title: "Excel のオートフィルターの操作"
second_title: "ドキュメント"
linktitle: "オートフィルター"
type: docs
url: /ja/autofilter/
aliases: [  /ja/working-with-autofilter/ ]
keywords: "オートフィルター, Aspose.Cells Cloud, Excel フィルター, 色フィルター, 日付フィルター, 動的フィルター, 数値フィルター, テキストフィルター, 空白フィルター, カスタムフィルター"
description: "Aspose.Cells Cloud API を使用して、Excel のオートフィルター（色、日付、動的、数値、テキスト、空白）の追加・編集・削除を学びましょう。複数の言語によるコードサンプルを提供しています。"
weight: 100
ArticleTitle: "Excel のオートフィルターの操作 – Aspose.Cells Cloud ドキュメント"
---

オートフィルターは、ワークシートから必要な項目のみを表示する最も迅速な方法です。この機能により、ユーザーはテキスト、数値、日付などの指定された条件に基づいてリストをフィルター処理できます。

**フィルターの種類**

Aspose.Cells Cloud は、色フィルター、日付フィルター、数値フィルター、テキストフィルター、空白フィルター、非空白フィルターなどのさまざまなフィルター種別を適用するための複数の API を提供しています。

<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>塗りつぶし色</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud は、<a href="/cells/autofilter/add-color-filter/">塗りつぶし色フィルターを追加する API</a>を提供しており、セルの塗りつぶし色プロパティに基づいてデータをフィルター処理できます。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>日付</strong></td>
    <td class="col-md-10">
      <p>2018年1月の日付を持つ行をフィルターするなど、さまざまな日付フィルターを適用できます。<a href="/cells/autofilter/add-date-filter/">日付フィルターを追加する API</a>を使用してください。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>動的日付</strong></td>
    <td class="col-md-10">
      <p>動的日付フィルターを使用すると、年を問わず特定の月（例：すべての1月の日付）に該当するセルをフィルター処理できます。<a href="/cells/autofilter/add-dynamic-filter/">動的フィルター API</a>をご参照ください。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>数値</strong></td>
    <td class="col-md-10">
      <p><a href="/cells/autofilter/add-filter/">カスタムフィルター API</a>を使用すると、数値が指定された範囲内にあるセルをフィルター処理できます。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>テキスト</strong></td>
    <td class="col-md-10">
      <p>列にテキストが含まれている場合、<a href="/cells/autofilter/add-filter/">フィルターを追加する API</a>を使用して、特定の文字列を含むセルを選択できます。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>空白</strong></td>
    <td class="col-md-10">
      <p>列が空白である行を取得するには、<a href="/cells/autofilter/match-all-blank/">すべての空白セルに一致させる API</a>を使用します。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>非空白</strong></td>
    <td class="col-md-10">
      <p>列に空白以外の値が含まれる行をフィルター処理するには、<a href="/cells/autofilter/match-all-non-blank/">すべての非空白セルに一致させる API</a>を使用します。</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>カスタムフィルター</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud は、<a href="/cells/autofilter/add-custom-filter/">カスタムフィルター API</a>を提供しており、特定の部分文字列を含む行や、特定の文字列で始まる／終わる行をフィルター処理するなどの高度なシナリオに対応しています。</p>
    </td>
  </tr>
</table>

**オートフィルターの操作**

- [Excel ワークシートに色フィルターを追加する方法](/cells/autofilter/add-color-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-color-filter/`
- [Excel ワークシートにカスタムフィルターを追加する方法](/cells/autofilter/add-custom-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-custom-filter/`
- [Excel ワークシートに日付フィルターを追加する方法](/cells/autofilter/add-date-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-date-filter/`
- [Excel ワークシートに動的フィルターを追加する方法](/cells/autofilter/add-dynamic-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-dynamic-filter/`
- [Excel ワークシートにフィルターを追加する方法](/cells/autofilter/add-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-filter/`
- [Excel ワークシートにアイコンフィルターを追加する方法](/cells/autofilter/add-icon-filter/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/add-icon-filter/`
- [Excel ワークシートから日付フィルターを削除する方法](/cells/autofilter/delete-a-date-filter/) – **メソッド:** DELETE、**エンドポイント:** `/cells/autofilter/delete-a-date-filter/`
- [Excel ワークシートからフィルターを削除する方法](/cells/delete-filter/) – **メソッド:** DELETE、**エンドポイント:** `/cells/delete-filter/`
- [Excel ワークシートからオートフィルターの説明を取得する方法](/cells/autofilter/get/) – **メソッド:** GET、**エンドポイント:** `/cells/autofilter/get/`
- [Excel ワークシートですべての空白セルに一致させる方法](/cells/autofilter/match-all-blank/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/match-all-blank/`
- [Excel ワークシートですべての非空白セルに一致させる方法](/cells/autofilter/match-all-non-blank/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/match-all-non-blank/`
- [Excel ワークシートのオートフィルターを更新する方法](/cells/autofilter/refresh/) – **メソッド:** POST、**エンドポイント:** `/cells/autofilter/refresh/`
---