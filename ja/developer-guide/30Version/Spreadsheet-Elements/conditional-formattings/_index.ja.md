---
title: "Excel 条件付き書式の操作"
second_title: "Document"
linktitle: "条件付き書式"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, 条件付き書式, Aspose.Cells Cloud, API"
description: "Aspose.Cells Cloud API for Excel は、条件付き書式ルールの取得・追加・変更・クリアを行うためのエンドポイントを提供し、ワークシートデータの動的視覚的分析を可能にします。"
weight: 100
ArticleTitle: "Excel 条件付き書式の操作 – API ガイド"
---

Excel の条件付き書式では、セルの値に応じて特定の色でセルを強調表示できます。

条件付き書式を使用することで、データの視覚的探索と分析、重要な問題の検出、パターンやトレンドの特定が容易になります。

条件付き書式では、興味深いセルやセル範囲を強調表示したり、異常値を強調表示したり、データに応じたデータバーや色スケール、アイコンセットを使用してデータを視覚化したりすることが簡単にできます。

条件付き書式では、指定した条件に基づいてセルの表示形式を変更します。条件が真（TRUE）の場合、セル範囲が書式設定されます。条件が偽（FALSE）の場合、セル範囲は変更されません。組み込み条件は多数用意されていますが、独自の条件（**TRUE** または **FALSE** を評価する数式を使用したものも含む）を作成することもできます。

Aspose.Cells Cloud API では、条件付き書式ルールをプログラムで管理するための一連のエンドポイントが提供されています。以下の操作が利用可能です。

- **ワークシートの条件付き書式を取得** – ワークシートに適用されたすべての条件付き書式ルールを取得します。  
  - **メソッド:** `GET`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **パラメータ:** `fileName`（文字列、必須）、`sheetName`（文字列、必須）、およびオプションのクエリパラメータ（`folder`、`storageName` など）  
  - **cURL の例:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **条件付き書式を取得** – 指定した ID で特定の条件付き書式ルールを返します。  
  - **メソッド:** `GET`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **パラメータ:** `index`（整数、必須）でルールの位置を識別します。  
  - **cURL の例:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **書式条件用のセル範囲を追加** – 指定した条件付き書式が適用されるセル範囲を追加します。  
  - **メソッド:** `POST`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **リクエストボディ（JSON）:** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **cURL の例:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **書式条件用の条件を追加** – 既存の書式ルールに新しい条件（例：値、数式）を定義します。  
  - **メソッド:** `POST`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **リクエストボディ（JSON）:** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **cURL の例:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **書式条件を追加** – タイプやスタイルを含む完全な条件付き書式ルールを作成します。  
  - **メソッド:** `POST`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **リクエストボディ（JSON）:**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **cURL の例:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **すべての条件付き書式をクリア** – 対象ワークシートからすべての条件付き書式ルールを削除します。  
  - **メソッド:** `DELETE`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **cURL の例:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **条件付き書式からセル範囲を削除** – 以前に定義したセル範囲を条件付き書式ルールから削除します。  
  - **メソッド:** `DELETE`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **cURL の例:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **条件付き書式を削除** – ワークシートから条件付き書式ルール全体を削除します。  
  - **メソッド:** `DELETE`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **cURL の例:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

上記の例は、各操作に必要な HTTP メソッド、URL パターン、主要なパラメータ、およびリクエストペイロードのサンプルを示しています。言語固有のコードスニペットが必要な場合は、対応する SDK（C#、Java、Python など）をご利用ください。