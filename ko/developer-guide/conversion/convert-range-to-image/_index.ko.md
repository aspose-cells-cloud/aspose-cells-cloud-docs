---
title: "엑셀 범위를 이미지로 변환 – Aspose.Cells Cloud API"
description: "로컬 엑셀 파일에서 특정 범위를 PNG, JPEG, SVG, TIFF 또는 BMP로 변환 – 전체 워크북 업로드 없이 Aspose.Cells Cloud REST API를 통해 수행합니다."
keywords: "Aspose.Cells Cloud, 범위를 이미지로 변환, 엑셀 API, 이미지 형식, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

이 호출은 로컬 스프레드시트 파일을 읽어 지정된 범위를 변환한 뒤, 이미지를 바이너리 스트림으로 반환합니다.

## 범위를 이미지로 변환 메서드

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **보안 및 인증**

Aspose.Cells Cloud API는 <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

## 요청 매개변수

| 이름                 | 위치                              | 유형    | 필수 여부 | 설명                                                                 |
| -------------------- | --------------------------------- | ------- | --------- | -------------------------------------------------------------------- |
| **Spreadsheet**      | Form‑Data (`multipart/form-data`) | 파일    | **필수**  | 처리할 엑셀 파일.                                                    |
| **worksheet**        | 쿼리 파라미터                      | 문자열  | **필수**  | 범위가 포함된 워크시트 이름(예: `Sheet1`).                           |
| **range**            | 쿼리 파라미터                      | 문자열  | **필수**  | 변환할 셀 영역(예: `A1:C10`).                                         |
| **format**           | 쿼리 파라미터                      | 문자열  | **필수**  | 출력 이미지 형식(`png`, `jpeg`, `svg`, `tiff`, `bmp`).               |
| **printHeadings**    | 쿼리 파라미터                      | 불리언  | 아니요     | `true`로 설정 시 이미지에 행/열 제목을 포함합니다.                   |
| **outPath**          | 쿼리 파라미터                      | 문자열  | 아니요     | 클라우드 스토리지에 생성된 파일을 저장하려는 경우 폴더 경로.          |
| **outStorageName**   | 쿼리 파라미터                      | 문자열  | 아니요     | 스토리지 서비스 이름(예: `MyStorage`).                               |
| **fontsLocation**    | 쿼리 파라미터                      | 문자열  | 아니요     | 변환 중 사용되는 사용자 정의 글꼴의 URL 또는 경로.                    |
| **region**           | 쿼리 파라미터                      | 문자열  | 아니요     | 로케일 식별자(예: `en-US`, `fr-FR`). 숫자 및 날짜 서식에 영향을 줍니다. |
| **password**         | 쿼리 파라미터                      | 문자열  | 아니요     | 암호화된 워크북의 비밀번호.                                           |
| **AutoRowsFit**      | 쿼리 파라미터                      | 불리언  | 아니요     | 렌더링 전에 행 높이 자동 조정.                                         |
| **AutoColumnsFit**   | 쿼리 파라미터                      | 불리언  | 아니요     | 렌더링 전에 열 너비 자동 조정.                                         |

## 응답

API는 변환된 이미지 파일을 **바이너리 스트림**(`application/octet-stream`)으로 반환합니다.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### 성공 응답 예시(HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

응답 본문을 파일(예: `report.png`)로 저장하여 브라우저에서 렌더링된 이미지를 확인합니다.

---

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                              |
| ---- | -------------------- | ----------------------------------------------------------------- |
| 200  | OK                   | 필터가 성공적으로 적용됨; 응답에 작업 세부 정보가 포함됨.          |
| 400  | Bad Request          | 누락되거나 잘못된 매개변수(예: 지원되지 않는 파일 형식).           |
| 401  | Unauthorized         | 잘못되거나 누락된 JWT 토큰.                                        |
| 413  | Payload Too Large    | 업로드된 파일이 크기 제한을 초과함.                                |
| 500  | Internal Server Error | 예기치 않은 서버 오류.                                             |

## SDK를 사용하여 범위를 이미지로 변환 API를 어떻게 사용하나요?

### OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage)은 공개적으로 접근 가능한 API를 정의하며, 웹 브라우저에서 직접 REST 요청을 보낼 수 있도록 합니다.

cURL 명령줄 도구를 사용하면 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예시는 cURL을 사용하여 Cloud API를 호출하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 저수준 세부 사항을 추상화하여 최소한의 코드로 범위를 이미지 파일로 빠르게 변환할 수 있습니다.  
Aspose.Cells Cloud SDK 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)에서 확인하세요.

다음 코드 예시는 다양한 SDK를 사용하여 Aspose.Cells 웹 서비스를 호출하는 방법을 보여줍니다. Gist에서 로드가 차단된 경우, 저장소에서 직접 예제를 다운로드할 수 있습니다.

---