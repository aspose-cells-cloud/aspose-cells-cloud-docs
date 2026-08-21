---
title: "Excelの画像を操作する"
second_title: "ドキュメント"
linktitle: "画像"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, 画像, Aspose.Cells Cloud, REST API, 画像処理, Excel画像"
description: "Aspose.Cells Cloud REST API を使用して Excelワークシート内の画像の取得、追加、更新、削除を行う方法を学びます。C#、Java、Python など向けのコードサンプルも含まれています。"
weight: 100
ArticleTitle: "Excelの画像を操作する – Aspose.Cells Cloud ドキュメント"
---

## Excelファイル内の画像を操作する

このガイドでは、Aspose.Cells Cloud REST API を使用して Excelワークシート内の**画像**（別名：イメージ）を操作する方法を説明します。主な画像関連操作—画像の取得、追加、更新、削除—をカバーし、各タスクの詳細な例へのリンクを提供します。

**前提条件**：Aspose.Cells Cloud アカウント、有効なAPIキー、および選択した言語向けの適切なSDKがインストールされていること。

- [Excelワークシートから特定の形式の画像を取得する方法](/cells/pictures/get/) – ワークシートから、指定された形式（PNG、JPEGなど）で単一の画像を取得します。  
- [Excelワークシートからすべての画像情報を取得する方法](/cells/pictures/get-all/) – ワークシートに含まれるすべての画像のメタデータ（インデックス、名前、位置、サイズなど）を一覧表示します。  
- [Excelワークシートに画像を追加する方法](/cells/pictures/add/) – 位置とサイズを指定して、ワークシートに新しい画像を挿入します。  
- [Excelワークシート内の特定の画像を更新する方法](/cells/pictures/update/) – 既存の画像のプロパティ（例：寸法、配置）を変更します。  
- [Excelワークシートからすべての画像を削除する方法](/cells/pictures/clear/) – 単一の呼び出しでワークシートからすべての画像オブジェクトを削除します。  
- [Excelワークシートから画像を削除する方法](/cells/pictures/delete/) – インデックスで識別される単一の画像を削除します。  

**APIリファレンス**

**特定の形式の画像を取得する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエスト | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（パス）、`sheetName`（パス）、`pictureIndex`（パス）、`format`（クエリ） | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | バイナリ画像データ（PNG、JPEGなど） | 200 OK、400 Bad Request、401 Unauthorized、404 Not Found、500 Server Error |

**すべての画像情報を取得する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエスト | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（パス）、`sheetName`（パス） | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | 画像メタデータ（インデックス、名前、位置、サイズ）を含むJSON配列 | 200 OK、400、401、404、500 |

**画像を追加する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエストボディ | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（パス）、`sheetName`（パス） | `{ "image": "<base64‑エンコード済み‑画像>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Created、400、401、404、500 |

**画像を更新する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエストボディ | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（パス）、`sheetName`（パス）、`pictureIndex`（パス） | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK、400、401、404、500 |

**すべての画像を削除する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエスト | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName`（パス）、`sheetName`（パス） | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK、400、401、404、500 |

**特定の画像を削除する**

| HTTPメソッド | エンドポイント | 必須パラメータ | サンプルリクエスト | サンプルレスポンス | ステータスコード |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName`（パス）、`sheetName`（パス）、`pictureIndex`（パス） | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK、400、401、404、500 |

**関連トピック**

Aspose.Cells Cloud におけるその他の画像関連操作を確認する：  
- [図形を操作する](/cells/shapes/) – 図形の追加、編集、削除  
- [チャートを操作する](/cells/charts/) – チャートオブジェクトの作成と操作  
- [ワークシート内の画像を操作する](/cells/images/) – 生の画像ファイルの埋め込みと管理  

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Excelの画像を操作する – Aspose.Cells Cloud ドキュメント",
  "description": "Aspose.Cells Cloud REST API を使用して Excel画像を取得、追加、更新、削除するためのガイド。",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel画像, Aspose.Cells Cloud, REST API, 画像処理",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>