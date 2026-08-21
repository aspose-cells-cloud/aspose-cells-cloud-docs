---
title: "Aspose.Cells Cloud API로 시작하기 – 3단계로 엑셀 파일 처리하기"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud 시작하기"
linktype: "시작하기"
type: docs
url: /getting-started/
description: "Aspose.Cells Cloud REST API를 사용하여 엑셀 파일을 3단계로 업로드, 변환 및 다운로드하는 방법을 알아보세요. cURL 코드 샘플 포함."
weight: 10
keywords: "Aspose.Cells Cloud, 엑셀 API, 스프레드시트 변환, 엑셀을 PDF로, 클라우드 스프레드시트, Aspose.Cells Cloud API"
---

- [개요](/cells/overview/)
- [빠른 시작](/cells/quickstart/)
- [사용 가능한 SDK](/cells/available-sdks/)
- [지원되는 플랫폼](/cells/supported-platforms/)
- [지원되는 파일 형식](/cells/supported-file-formats/)
- [Aspose.Cells Cloud 평가판](/cells/evaluate-aspose-cells/)
- [요금제](/cells/pricing-plan/)
- [기술 지원](/cells/technical-support/)
- [Docker 컨테이너 실행 방법](/cells/how-to-run-docker-container/)

**시작 가이드**

시작하기 전에 유효한 **Aspose Cloud API 키**와 **스토리지 이름**이 있는지 확인하세요. 이러한 자격 증명은 이후 모든 API 호출에 필요합니다.

**단계 1: 엑셀 파일 업로드**  
소스 워크북을 Aspose Cloud 스토리지에 업로드합니다.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*요청 본문*: 파일은 이진 스트림(`application/octet‑stream`)으로 전송됩니다.  
*필수 매개변수*:

- `path` – 파일이 저장될 스토리지 경로 (예: `folder/sample.xlsx`).

**단계 2: 워크북을 PDF로 변환**  
파일이 저장된 후 변환 요청을 보냅니다.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*필수 매개변수*:

- `name` – 업로드된 워크북 이름 (예: `sample.xlsx`).
- `format` – 대상 형식 (`pdf`).
- `outputPath` – 변환된 파일이 저장될 스토리지 경로 (예: `folder/result.pdf`).

*샘플 응답 페이로드* (JSON):

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**단계 3: 변환된 PDF 다운로드**  
스토리지에서 생성된 PDF를 가져옵니다.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*필수 매개변수*:

- `outputPath` – 이전 단계에서 생성된 PDF의 경로.

**샘플 요청 / 응답 요약**

| 작업 | HTTP 메서드 | 엔드포인트 (예시) | 매개변수 | 성공 상태 |
|------|-------------|-------------------|----------|-----------|
| 업로드 | PUT | /cells/storage/file/{path} | `path` (스토리지 위치) | 200 OK |
| 변환 | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| 다운로드 | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**일반적인 오류 코드**

- **400 잘못된 요청** – 누락되거나 잘못된 매개변수.  
- **401 인증되지 않음** – 잘못되거나 누락된 액세스 토큰.  
- **404 찾을 수 없음** – 지정된 파일 또는 경로가 존재하지 않음.  
- **500 내부 서버 오류** – 예기치 않은 서버 오류; 재시도 또는 지원팀에 문의.  
---