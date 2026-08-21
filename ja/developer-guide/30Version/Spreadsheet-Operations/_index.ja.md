---
title: "スプレッドシート操作"
second_title: "ドキュメント"
type: docs
url: /ja/spreadsheet-operations/
keywords: "Aspose Cells Cloud, Excel API, スプレッドシート操作, 自動フィット, バッチ処理, ファイル保護, 変換, インポート・エクスポート, テキスト処理"
description: "Aspose.Cells Cloud REST API を使用して、自動フィット、バッチ変換、保護、結合、検索と置換などのスプレッドシート操作を実行する方法を学びます。簡潔な使用ノートとコードサンプルのガイドを含みます。"
weight: 100
ArticleTitle: "スプレッドシート操作 – Aspose.Cells Cloud API ガイド"
---

スプレッドシート操作では、**Aspose.Cells Cloud**（v3.0）を使用して Excel ブックで実行できる最も一般的な操作について、簡潔なガイドを提供します。列の幅や行の高さを自動調整する必要がある場合や、ファイルをバッチ処理する必要がある場合、ワークシートを保護する必要がある場合、またはテキストを操作する必要がある場合でも、REST API は Python、C#、Java などの言語で動作する専用エンドポイントを提供します。以下の一覧は、各操作の詳細なドキュメントへのリンクと、すぐに始められるようにするための簡潔な使用ノートを含んでいます。

**前提条件**：これらのエンドポイントを呼び出すには、有効な Aspose.Cells Cloud API キーが必要であり、`Authorization` ヘッダー（`Bearer <access-token>`）を含める必要があります。例では API バージョン v3.0 を前提としています。

- **[オートフィッターオプション](/ja/cells/auto-fitter-options/)** – 列の幅と行の高さを自動的に調整します。`POST /cells/{file}/worksheets/{sheet}/autoFitColumns`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/autoFitColumns
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "autoFitOptions": {
      "autoFitType": "All",
      "autoFitMergedCells": true
    }
  }
  ```
- **[Excel ファイルのバッチ処理：変換、ロック、保護、分割、およびロック解除](/ja/cells/batch/)** – 最大 100 ファイルまで、1 回のリクエストで一括操作（変換、ロック、保護、分割、ロック解除）を実行します。`POST /cells/batch`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/batch
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "tasks": [
      { "file": "Book1.xlsx", "action": "convert", "format": "pdf" },
      { "file": "Book2.xlsx", "action": "protect", "password": "Secret123" }
    ]
  }
  ```
- **[Excel ファイルの圧縮と修復](/ja/cells/compress-and-repair-excel-files/)** – ファイルサイズを縮小し、構造上の問題を修正します。`POST /cells/{file}/compressAndRepair`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/compressAndRepair
  Authorization: Bearer {access-token}
  ```
- **[Excel ファイルを他の形式に変換または別の形式で保存](/ja/cells/conversion-and-save-as/)** – Excel を PDF、CSV、HTML などに変換するか、出力形式を変更します。`GET /cells/{file}/saveAs`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Financials.xlsx/saveAs?format=pdf
  Authorization: Bearer {access-token}
  ```
- **[ワークブック変換オプション](/ja/cells/convert-workbook-options/)** – ページサイズ、レンダリングオプション、パスワード保護などの変換設定を微調整します。`POST /cells/{file}/convert`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/convert
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "format": "pdf",
    "options": {
      "pageSetup": { "orientation": "landscape" },
      "pdfSaveOptions": { "compressImages": true }
    }
  }
  ```
- **[Excel ファイルの作成または Excel レポートの構築](/ja/cells/creating-files-and-reports/)** – 新規ワークブックをゼロから、またはテンプレートから生成します。`PUT /cells/{newFile}`  
  ```http
  PUT https://api.aspose.cloud/v3.0/cells/NewReport.xlsx
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "templateFile": "Template.xlsx",
    "dataSource": { "name": "Q1 Sales", "value": 12345 }
  }
  ```
- **[Excel ファイルへのデータのインポートと Excel ファイルからのデータのエクスポート](/ja/cells/data-import-and-export/)** – CSV、JSON、またはデータベースからデータを読み込み、ワークシートデータをエクスポートします。`POST /cells/{file}/importData`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Orders.xlsx/importData
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "importOptions": {
      "source": "json",
      "jsonData": [{ "OrderId": 1, "Amount": 250.0 }]
    }
  }
  ```
- **[Excel ファイルの暗号化、復号化、および電子署名](/ja/cells/protect/)** – パスワード保護、暗号化、または電子署名を適用します。`POST /cells/{file}/encrypt`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Sensitive.xlsx/encrypt
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "password": "StrongPass!23",
    "encryptionType": "Standard"
  }
  ```
- **[ファイル情報](/ja/cells/file-info/)** – サイズ、形式、作成日などのメタデータを取得します。`GET /cells/{file}/info`  
  ```http
  GET https://api.aspose.cloud/v3.0/cells/Archive.xlsx/info
  Authorization: Bearer {access-token}
  ```
- **[Excel ファイルの結合と分割](/ja/cells/merge-and-split/)** – 複数のワークブックを 1 つのファイルに結合するか、ワークブックを個別のファイルに分割します。`POST /cells/merge` / `POST /cells/split`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/merge
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "files": ["Q1.xlsx", "Q2.xlsx"],
    "outputFile": "FullYear.xlsx"
  }
  ```
- **[Excel ファイル内のテキストコンテンツの検索と置換](/ja/cells/search-and-replace/)** – ワークシート全体で文字列を検索して置換します。`POST /cells/{file}/searchReplace`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Report.xlsx/searchReplace
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "text": "Draft",
    "newText": "Final",
    "options": { "matchCase": false }
  }
  ```
- **[Excel テキスト処理：テキストの追加、文字の削除、テキストのトリミング、単語のケース変更など](/ja/cells/text-processing/)** – セル値に対して高度なテキスト操作を実行します。`POST /cells/{file}/textProcessing`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Notes.xlsx/textProcessing
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "trim", "range": "A1:A10" },
      { "type": "toUpper", "range": "B1:B5" }
    ]
  }
  ```
- **[Excel ファイルへの透かしの挿入または背景の設定](/ja/cells/watermark-and-background/)** – 画像またはテキストの透かしを追加し、ワークシートの背景を設定します。`POST /cells/{file}/watermark`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Presentation.xlsx/watermark
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "type": "text",
    "text": "Confidential",
    "fontSize": 36,
    "color": "FF0000"
  }
  ```
- **[Excel ファイルの操作：数式の計算、オートフィット、オブジェクトのクリアなど](/ja/cells/workbook/)** – 数式の計算、オブジェクトのクリア、オートフィットなどの一般的なワークブックタスクを実行します。`POST /cells/{file}/workbookOperations`  
  ```http
  POST https://api.aspose.cloud/v3.0/cells/Analytics.xlsx/workbookOperations
  Authorization: Bearer {access-token}
  Content-Type: application/json

  {
    "operations": [
      { "type": "calculateFormula" },
      { "type": "clearObjects", "objectType": "charts" }
    ]
  }
  ```