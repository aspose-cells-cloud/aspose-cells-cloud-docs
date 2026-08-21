---
title: "Excel 워크시트에서 행 삭제하기"
second_title: "문서"
linktitle: "행"
type: docs
url: /ko/rows/delete/row/
aliases: [  /ko/delete-row-from-a-worksheet/ ]
description: "Aspose.Cells Cloud REST API를 통해 Excel 워크시트에서 특정 행을 제거하려면 DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} 엔드포인트를 사용하세요. cURL 명령어, SDK 샘플 및 전체 매개변수 참조가 포함됩니다."
keywords: "Aspose.Cells, 행 삭제, Excel, API, REST, 클라우드, SDK"
weight: 80
ArticleTitle: "Excel 워크시트에서 행 삭제하기 – Aspose.Cells Cloud API 가이드"
---

이 REST API는 Excel 워크시트에서 행을 삭제합니다.

**사전 요구 사항**  
- 유효한 JWT **Authorization**(인증) 토큰.  
- 워크북은 지원되는 Aspose Cloud 스토리지(기본 또는 사용자 정의)에 저장되어 있어야 합니다.  
- 대상 폴더(지정된 경우)는 선택한 스토리지에 존재해야 합니다.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **요청 매개변수**

| 매개변수 이름       | 유형    | 경로 / 쿼리 | 필수 여부 | 설명                                                                                       |
| ------------------- | ------- | ------------ | -------- | ------------------------------------------------------------------------------------------ |
| **name**            | string  | path         | Yes      | 워크북 이름.                                                                               |
| **sheetName**       | string  | path         | Yes      | 워크시트 이름.                                                                             |
| **rowIndex**        | integer | path         | Yes      | 삭제할 행의 0부터 시작하는 인덱스입니다.                                                  |
| **startrow**        | integer | query        | No       | 삭제할 첫 번째 행의 인덱스(보통 `rowIndex`와 동일함).                                    |
| **totalRows**       | integer | query        | No       | 연속적으로 삭제할 행의 수.                                                                 |
| **updateReference** | boolean | query        | No       | `true`(기본값)일 경우, 삭제 후 수식, 이름 범위 및 기타 참조가 업데이트됩니다.             |
| **folder**          | string  | query        | No       | 워크북이 저장된 폴더.                                                                      |
| **storageName**     | string  | query        | No       | 스토리지 서비스의 이름.                                                                    |

[OpenAPI 스펙](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예제는 실행 가능한 전체 호출을 보여줍니다.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**가능한 HTTP 응답 코드**

| 코드 | 의미                               | 설명                                                                             |
|------|------------------------------------|----------------------------------------------------------------------------------|
| 200  | OK (성공)                          | 행이 성공적으로 삭제되었습니다.                                                   |
| 400  | Bad Request (잘못된 요청)          | 누락되거나 잘못된 매개변수(예: 숫자가 아닌 `rowIndex`).                           |
| 401  | Unauthorized (인증되지 않음)       | 잘못되거나 누락된 JWT 토큰.                                                       |
| 404  | Not Found (찾을 수 없음)           | 지정된 워크북, 워크시트 또는 행이 존재하지 않습니다.                               |
| 500  | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류; 자세한 내용은 오류 응답을 참조하세요.                      |

**오류 응답 예시**

```json
{
  "Code": 400,
  "Message": "Invalid row index supplied." // 유효하지 않은 행 인덱스가 제공되었습니다.
}
```

## 클라우드 SDK 패밀리

SDK를 사용하면 개발 속도를 높이는 데 가장 효과적입니다. SDK는 저수준 세부 사항을 추상화하여 프로젝트 작업에 집중할 수 있도록 도와줍니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예제는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스에 호출을 수행하는 방법을 보여줍니다:

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**관련 작업**  
- [행 추가](/cells/rows/add/row/)  
- [여러 행 삭제](/cells/rows/delete/rows/)  
- [행 세부 정보 조회](/cells/rows/get/row/)  
---