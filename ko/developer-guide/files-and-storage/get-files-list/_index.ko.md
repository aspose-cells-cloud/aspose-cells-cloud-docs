---
title: "Aspose.Cells Cloud API – 파일 목록 가져오기(폴더 내용)"
description: "Aspose.Cells Cloud 저장소의 특정 폴더에서 파일 및 하위 폴더 목록을 가져옵니다."
keywords:
  - Aspose.Cells
  - API
  - Get Files List
  - Cloud Storage
  - Excel
  - REST
type: docs
weight: 100
---

**파일 목록 가져오기**(Get Files List) 작업은 Aspose.Cells Cloud 저장소의 지정된 폴더에 저장된 파일 및 하위 폴더의 컬렉션을 반환합니다.  
이 작업은 클라우드 기반 Excel 워크북, 아카이브 및 기타 지원되는 파일 유형을 탐색하기 위한 기본 진입점입니다.

## Aspose.Cells Cloud API – 파일 목록 가져오기(폴더 내용)

```
GET https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안을 위해 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>을 요구합니다.

### 요청 매개변수

| 이름              | 위치   | 유형      | 필수 여부 | 설명                                                              |
| ----------------- | ------ | --------- | --------- | ----------------------------------------------------------------- |
| **path**          | 경로   | 문자열    | 예        | 클라우드 저장소 내 폴더의 경로.                                   |
| **storageName**   | 쿼리   | 문자열    | 아니요    | 사용할 저장소 이름. 생략 시 기본 저장소가 사용됩니다.            |
| **pageSize**      | 쿼리   | 정수      | 아니요    | 페이지당 반환할 항목의 최대 개수(기본값: 100).                    |
| **pageNumber**    | 쿼리   | 정수      | 아니요    | 가져올 페이지 번호(1부터 시작, 기본값: 1).                        |

- **Value** – `StorageFile` 객체 배열. 각 객체는 다음을 포함합니다:
  - `Name` – 파일 또는 폴더 이름.
  - `IsFolder` – 항목이 폴더인 경우 `true`.
  - `Size` – 바이트 단위 크기(폴더는 `0` 보고).
  - `ModifiedDate` – 최종 수정 타임스탬프(ISO 8601).

### **응답**

**HTTP 상태 코드**

| HTTP 코드 | HTTP 상태             | 설명                                                       |
| --------- | --------------------- | ---------------------------------------------------------- |
| 200       | OK (성공)             | 웹 API가 성공적으로 호출됨; 응답에 작업 세부정보 포함.     |
| 400       | Bad Request (잘못된 요청) | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 유형).  |
| 401       | Unauthorized (인증 없음) | 잘못되거나 누락된 JWT 토큰.                                |
| 413       | Payload Too Large (ペイロードが大きすぎます) | 업로드된 파일이 크기 제한을 초과함.                    |
| 500       | Internal Server Error (내부 서버 오류) | 예기치 않은 서버 오류.                                   |
|           |                       |                                                            |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Folder/GetFilesList)은 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 액세스할 수 있습니다. 다음 예시는 cURL을 사용해 Cloud API에 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/folder/{path}?storageName=MyStorage&pageSize=100&pageNumber=1" \
     -H "Authorization: Bearer <your_access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "Size": 124578,
      "ModifiedDate": "2024-03-10T12:34:56Z"
    },
    {
      "Name": "Archives",
      "IsFolder": true,
      "Size": 0,
      "ModifiedDate": "2024-02-01T08:00:00Z"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로 프로젝트 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub 저장소</a>를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스에 요청을 보내는 방법을 보여줍니다: