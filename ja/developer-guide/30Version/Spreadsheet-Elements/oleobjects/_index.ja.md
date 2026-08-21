---
title: "Excel OLE オブジェクトの操作"
second_title: "ドキュメント"
linktitle: "OleObjects"
type: docs
url: /ja/oleobjects/
aliases: [  /ja/working-with-oleobjects/ ]
keywords: "OLE, Excel, Aspose.Cells, API, クラウド"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内の OLE オブジェクトを取得、追加、更新、削除、および変換します。SDK は Java、.NET、Python、PHP、Ruby、Go、Node.js、Perl、Swift、および Android 用に提供されています。"
weight: 100
ArticleTitle: "Excel OLE オブジェクトの操作 – 取得・追加・更新・削除・変換のガイド"
---

**Excelワークシート内の OLE オブジェクトを操作する方法**

Aspose.Cells Cloud REST API は、OLE オブジェクトをプログラムで管理するための完全な操作セットを提供します。以下は、各操作の簡潔なリファレンスであり、HTTP メソッド、エンドポイントパターン、必要なパラメータ、および簡易なレスポンス例を含みます。

- [Excelワークシートから OLE オブジェクトを取得する方法](/cells/oleobjects/get/)
  - **メソッド:** `GET`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **パラメータ:** `fileName` (文字列)、`sheetName` (文字列)、`oleObjectIndex` (整数)  
  - **サンプルレスポンス:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Excelワークシートに OLE オブジェクトを追加する方法](/cells/oleobjects/add/)
  - **メソッド:** `POST`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **パラメータ:** `fileName`、`sheetName`、`oleObject` (バイナリまたは base64)、`imageFormat` (オプション)  
  - **サンプルリクエスト本文:** ファイルストリームを含む multipart/form-data  
  - **サンプルレスポンス:** `201 Created`、新規 OLE オブジェクトのロケーションヘッダーを含む。

- [Excelワークシート内の特定の OLE オブジェクトを更新する方法](/cells/oleobjects/update/)
  - **メソッド:** `PUT`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **パラメータ:** `fileName`、`sheetName`、`oleObjectIndex`、`oleObject` (更新されたコンテンツ)  
  - **サンプルレスポンス:** `200 OK`、更新されたオブジェクトメタデータを含む。

- [Excelワークシート内の OLE オブジェクトを画像に変換する方法](/cells/oleobjects/convert/)
  - **メソッド:** `GET`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **パラメータ:** `fileName`、`sheetName`、`oleObjectIndex`、`format` (例: `png`、`jpeg`)  
  - **サンプルレスポンス:** 変換された OLE オブジェクトのバイナリ画像ストリーム。

- [Excelワークシート内のすべての OLE オブジェクトを削除する方法](/cells/oleobjects/clear/)
  - **メソッド:** `DELETE`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **パラメータ:** `fileName`、`sheetName`  
  - **サンプルレスポンス:** `204 No Content`、すべての OLE オブジェクトが削除されたことを示す。

- [Excelワークシート内の特定の OLE オブジェクトを削除する方法](/cells/oleobjects/delete/)
  - **メソッド:** `DELETE`  
  - **エンドポイント:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **パラメータ:** `fileName`、`sheetName`、`oleObjectIndex`  
  - **サンプルレスポンス:** `204 No Content`、オブジェクトが削除されたことを確認する。
---