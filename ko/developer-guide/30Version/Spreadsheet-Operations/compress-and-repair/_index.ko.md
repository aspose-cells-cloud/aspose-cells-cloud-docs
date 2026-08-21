---
title: "Excel 파일 압축 및 복구"
second_title: "문서"
type: docs
url: /ko/compress-and-repair-excel-files/
linktitle: "압축 및 복구"
keywords: "Aspose.Cells, Excel 압축, Excel 복구, 클라우드 API, Excel 파일 크기 감소, 손상된 워크북 복구, Excel 파일 압축, Excel 워크북 복구"
description: "Aspose.Cells Cloud API를 사용하여 대용량 Excel 워크북을 압축하고 손상된 파일을 복구하는 방법을 알아보세요. 단계별 예제, 지원 언어, 모범 사례 제공."
weight: 100
ArticleTitle: "Excel 파일 압축 및 복구 – Aspose.Cells Cloud API"
---

Excel 워크북을 압축하면 사용하지 않는 스타일, 이미지, 공유 문자열을 제거하여 파일 크기를 줄이며, 복구는 손상된 워크북의 무결성을 회복합니다. Aspose.Cells Cloud API는 이러한 두 작업을 위한 전용 엔드포인트를 제공합니다.

- **[Excel 파일의 데이터 압축](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Excel 파일 복구](https://docs.aspose.cloud/cells/repair-excel-files/).**

**워크북 압축 API**  
**압축**(Compress) 작업은 간단한 POST 요청을 사용합니다. 아래는 전체 요청/응답 사양입니다:

| 메서드 | 엔드포인트 | 필수 파라미터 | 요청 본문 | 예시 응답 | 일반적인 상태 코드 |
|--------|------------|---------------|------------|-------------|-------------------|
| POST   | `/cells/compress` | `file` (바이너리) – 압축할 워크북; 선택적 `outPath` (문자열) – 저장할 경로 | *없음* (파일은 multipart/form‑data로 전송됨) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**워크북 복구 API**  
**복구**(Repair) 작업 역시 POST 요청을 사용합니다. 해당 사양은 다음과 같습니다:

| 메서드 | 엔드포인트 | 필수 파라미터 | 요청 본문 | 예시 응답 | 일반적인 상태 코드 |
|--------|------------|---------------|------------|-------------|-------------------|
| POST   | `/cells/repair` | `file` (바이너리) – 손상된 워크북; 선택적 `outPath` (문자열) – 복구된 파일을 저장할 위치 | *없음* (파일은 multipart/form‑data로 전송됨) | `{ "isRepaired": true, "message": "워크북이 성공적으로 복구되었습니다." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

이 표는 개발자가 추가 탐색 없이 직접 API를 호출하는 데 필요한 핵심 정보를 제공합니다.

**추가 자료**  
- 사용하지 않는 행 및 열 제거와 같은 고급 옵션을 포함한 전체 **[Excel 파일 압축](/ko/compress-excel-files/)** 가이드를 참조하세요.  
- 문제 해결 팁 및 오류 코드 설명을 포함한 **[Excel 파일 복구](/ko/repair-excel-files/)** 문서를 검토하세요.  
- Aspose.Cells Cloud API의 더 넓은 이해를 위해 **[파일 정보 조회](/ko/file-info/)** 및 **[스프레드시트 작업](/ko/spreadsheet-operations/)** 과 같은 관련 작업을 탐색하세요.