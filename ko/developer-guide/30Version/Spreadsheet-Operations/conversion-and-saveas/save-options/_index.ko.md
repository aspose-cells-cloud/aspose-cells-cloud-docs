---
title: "저장 옵션"
second_title: "문서"
linktitle: "저장 옵션"
type: docs
url: /ko/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, 워크북, REST API, 파일 형식, PDF, CSV, JSON, HTTP 압축, 차트 캐시, 이름 범위, 디렉터리 생성"
description: "Aspose.Cells Cloud REST API의 SaveOptions 속성을 설명하며, 개발자가 HTTP 압축, 차트 캐시 갱신, 자동 디렉터리 생성 등 다양한 파일 형식 및 옵션을 통해 워크북 저장 동작을 구성할 수 있도록 지원합니다."
weight: 79
ArticleTitle: "Save Options – Aspose.Cells Cloud REST API 문서"
---

# SaveOptions 속성

SaveOptions를 사용하면 Aspose.Cells Cloud REST API를 통해 워크북을 저장할 때 동작을 제어할 수 있습니다. 이러한 옵션을 구성하면 HTTP 압축 활성화, 출력 형식 지정, 임시 저장소 관리, 차트 캐시 갱신 및 자동 디렉터리 생성 등의 추가 동작을 제어할 수 있습니다.

**사전 요구 사항**  
- 인증된 Aspose.Cells Cloud 세션(OAuth 2.0 또는 JWT).  
- 저장 전에 대상 워크북이 API를 통해 로드되었거나 생성되어 있어야 합니다.

| 이름                      | 유형       | 설명                                                                                      | 비고         |
| ------------------------- | ---------- | ----------------------------------------------------------------------------------------- | ------------ |
| **EnableHTTPCompression** | **bool?**  | 응답에 대해 HTTP 압축을 활성화합니다.                                                    | [선택 사항] |
| **SaveFormat**            | **string** | 워크북을 저장할 대상 파일 형식을 지정합니다.                                             | [선택 사항] |
| **ClearData**             | **bool?**  | 파일을 저장한 후 워크북을 비웁니다.                                                      | [선택 사항] |
| **CachedFileFolder**      | **string** | 대용량 데이터를 임시로 저장하는 데 사용되는 캐시된 파일 폴더입니다.                     | [선택 사항] |
| **ValidateMergedAreas**   | **bool?**  | 파일 저장 전에 병합 영역을 유효성 검사할지 여부를 나타냅니다. 기본값은 false입니다.      | [선택 사항] |
| **RefreshChartCache**     | **bool?**  | 저장 전에 차트 캐시 데이터를 갱신합니다.                                                 | [선택 사항] |
| **CreateDirectory**       | **bool?**  | true인 경우 디렉터리가 존재하지 않으면 파일 저장 전에 자동으로 생성됩니다.              | [선택 사항] |
| **SortNames**             | **bool?**  | 저장 시 이름 범위를 알파벳순으로 정렬합니다.                                             | [선택 사항] |

**요청**  
- **메서드:** `POST` (또는 작업에 따라 `PUT`)  
- **엔드포인트:** `/cells/workbook/save`  
- **헤더:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **본문:** `SaveOptions` 모델(위 표 참조)의 JSON 표현과 워크북 데이터 또는 참조가 결합된 JSON.

**응답 예시**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "워크북이 성공적으로 저장되었습니다."
}
```

**HTTP 상태 코드**

| 코드 | 의미                        | 설명                                          |
|------|-----------------------------|-----------------------------------------------|
| 200  | OK                          | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | 잘못된 요청                 | 누락되었거나 유효하지 않은 매개변수(예: 지원되지 않는 파일 형식). |
| 401  | 인증되지 않음               | 유효하지 않거나 누락된 JWT 토큰. |
| 413  | 페이로드가 너무 큼          | 업로드된 파일이 크기 제한을 초과했습니다. |
| 500  | 내부 서버 오류              | 예기치 않은 서버 오류. |

**참고 / 주의 사항**  
- **CreateDirectory**가 `true`로 설정된 경우, API는 대상 폴더가 존재하지 않을 경우 자동으로 생성합니다.  
- **EnableHTTPCompression**을 활성화하면 대용량 워크북에 대한 페이로드 크기를 줄일 수 있으나, 클라이언트가 gzip/deflate 디코딩을 지원해야 합니다.  
- 워크북 생성 후 차트가 사용하는 동적 데이터가 변경되었을 수 있는 경우 **RefreshChartCache**를 사용해야 합니다.