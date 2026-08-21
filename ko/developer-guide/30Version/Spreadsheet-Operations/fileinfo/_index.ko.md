---
title: "파일 정보"
second_title: "문서"
linktitle: "파일 정보"
type: docs
url: /ko/file-info/
keywords: "파일, 정보, Excel, Aspose.Cells, 클라우드 API, 메타데이터, Base64"
description: "Aspose.Cells 클라우드 API를 사용하여 Excel 파일 이름, 크기 및 Base64 인코딩 콘텐츠를 조회합니다. 요청 구문, 샘플 코드, 오류 처리를 포함합니다."
weight: 79
ArticleTitle: "파일 정보 – Excel 파일 메타데이터 및 Base64 콘텐츠 (Aspose.Cells 클라우드 API)"
---

## FileInfo 속성


| 이름            | 유형   | 설명                                             |
| --------------- | ------ | ------------------------------------------------ |
| **FileName**    | string | 파일 이름(확장자 포함).                          |
| **FileSize**    | long   | 파일 크기(바이트 단위).                          |
| **FileContent** | string | Base64로 인코딩된 원시 Excel 파일 데이터를 포함. |

응답은 위 표에 표시된 세 가지 속성을 포함하는 JSON 형식으로 반환됩니다. 예:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### 오류

| HTTP 코드 | 의미                    | 발생 시점                              |
| --------- | ----------------------- | -------------------------------------- |
| 200       | OK – 요청 성공.         | 일반적인 응답.                         |
| 401       | 인증되지 않음           | 인증 토큰 누락 또는 유효하지 않은 경우. |
| 404       | 찾을 수 없음            | 지정된 파일이 존재하지 않는 경우.      |
| 500       | 내부 서버 오류          | 예상치 못한 서버 측 실패 발생 시.      |

각 오류에 대해 인증 토큰이 유효한지 확인(401), 파일 경로를 확인(404)하거나, 재시도 전략을 위한 일반적인 오류 처리 가이드를 참조(500)하세요.

## 참조

- [워크북 조회](https://docs.aspose.cloud/cells/get-workbook) – 워크북 객체 및 워크시트를 조회합니다.  
- [파일 다운로드](https://docs.aspose.cloud/cells/download-file) – Base64 인코딩 없이 원시 파일 바이트를 다운로드합니다.  
- [인증 개요](https://docs.aspose.cloud/cells/authentication) – 액세스 토큰을 획득하고 사용하는 방법입니다.  
---