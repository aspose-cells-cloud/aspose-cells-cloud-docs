---
title: "範囲のスタイルを設定 – Aspose.Cells Cloud API"
second_title: "ドキュメント"
linktitle: "範囲のスタイルを設定"
type: docs
url: /ja/ranges/update/style/
aliases: [  /ja/set-the-style-of-the-range/ ]
keywords: "Aspose.Cells, 範囲のスタイル, API, Excel, クラウド"
description: "Aspose.Cells Cloud REST API を使用して、Excelワークシート内のセル範囲のスタイルを設定する方法を学びます。認証手順、リクエスト形式、レスポンスの詳細、および .NET、Java、Python、Go などの SDK サンプルを含みます。"
weight: 70
---  

## **はじめに**  
この例では、Aspose.Cells Cloud API を使用して範囲のスタイルを設定する方法を示します。.NET、Java、PHP、Ruby、Python、JavaScript (jQuery) など、多くのプログラミング言語からこの API を呼び出すことができます。  

## **API 情報**  

| API                                                   | タイプ | 説明                                 | リソースリンク                                                                                                                                |
| ----------------------------------------------------- | ------ | ------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST   | 名前付き範囲のセルスタイルを設定する | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL の例**  

{{< tabs tabTotal="2" tabID="1" tabName1="リクエスト" tabName2="レスポンス" >}}

{{< tab tabNum="1" >}}

**前提条件**  
1. OAuth2 クライアント認証フロー (`POST https://api.aspose.cloud/connect/token`) を使用してアクセストークンを取得します。  
2. すべてのリクエストで `Authorization: Bearer <access_token>` ヘッダーを含めます。  

**リクエスト**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*`Range` オブジェクトは範囲の左上セルとサイズを指定します。`Style` オブジェクトには適用する書式オプションが含まれます。*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**レスポンス**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**エラー処理** – 失敗したリクエストの場合、API は適切な HTTP ステータスコード（例：400、401、500）を返し、`Error` および `Message` フィールドを含む JSON ボディを付与します。`Code` の値を確認し、200 以外の結果はログに記録し、ご自身のエラー処理ポリシーに従って処理してください。  

{{< /tab >}}

{{< /tabs >}}

## **SDK ソース**  
Aspose.Cells Cloud SDK は、以下のページからダウンロードできます： [利用可能な SDK](/cells/available-sdks/)

### **SDK の例**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}