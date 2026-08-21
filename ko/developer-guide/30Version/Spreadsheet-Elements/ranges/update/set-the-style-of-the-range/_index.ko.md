---
title: "범위 스타일 설정 – Aspose.Cells Cloud API"
second_title: "문서"
linktitle: "범위 스타일 설정"
type: docs
url: /ko/ranges/update/style/
aliases: [  /ko/set-the-style-of-the-range/ ]
keywords: "Aspose.Cells, 범위 스타일, API, Excel, 클라우드"
description: "Aspose.Cells Cloud REST API를 사용하여 Excel 워크시트의 셀 범위 스타일을 설정하는 방법을 알아보세요. 인증 단계, 요청 형식, 응답 세부 정보, .NET, Java, Python, Go 등 여러 언어에 대한 SDK 예제가 포함됩니다."
weight: 70
---

## **소개**
이 예제는 Aspose.Cells Cloud API를 사용하여 범위의 스타일을 설정하는 방법을 보여줍니다. .NET, Java, PHP, Ruby, Python, JavaScript(jQuery) 등 다양한 프로그래밍 언어에서 API를 호출할 수 있습니다.

## **API 정보**

| API                                                   | 유형 | 설명                                 | 리소스 링크                                                                                                                                   |
| ----------------------------------------------------- | ---- | ------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | 명명된 범위의 셀 스타일을 설정합니다 | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL 예제**

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}

{{< tab tabNum="1" >}}

**사전 조건**  
1. OAuth2 클라이언트 자격 증명 흐름(`POST https://api.aspose.cloud/connect/token`)을 통해 액세스 토큰을 획득합니다.  
2. 모든 요청에 `Authorization: Bearer <access_token>` 헤더를 포함합니다.  

**요청**  

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

*`Range` 객체는 범위의 좌상단 셀과 크기를 지정합니다. `Style` 객체는 적용할 서식 옵션을 포함합니다.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**응답**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**오류 처리** – 요청이 실패할 경우 API는 적절한 HTTP 상태 코드(예: 400, 401, 500)와 함께 `Error` 및 `Message` 필드를 포함하는 JSON 본문을 반환합니다. `Code` 값을 확인하고, 200이 아닌 결과는 로그에 기록하고 오류 처리 정책에 따라 처리해야 합니다.  

{{< /tab >}}

{{< /tabs >}}

## **SDK 소스**
Aspose.Cells Cloud SDK는 다음 페이지에서 다운로드할 수 있습니다: [사용 가능한 SDK](/cells/available-sdks/)

### **SDK 예제**
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