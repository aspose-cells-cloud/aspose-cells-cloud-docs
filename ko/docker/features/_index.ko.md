---
title: "Aspose.Cells Cloud Docker 핵심 기능: 스프레드시트 변환, 병합, 분할, 보호, 데이터 처리 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud Docker 핵심 기능"
linktype: "기능"
type: docs
url: /ko/docker-container-features/
description: "Aspose.Cells Cloud Docker 컨테이너를 사용하여 로컬에서 Aspose.Cells Cloud API를 실행하세요. 이 Docker 기반 컨테이너화된 서비스는 Aspose의 퍼블릭 클라우드를 사용하지 않고도 전체 스프레드시트 처리, 개인정보 보호, 오프라인 기능을 제공합니다."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - 스프레드시트 변환
  - Excel 처리
  - PDF 내보내기
  - CSV 처리
  - REST API
  - 컨테이너화된 서비스
  - 프라이빗 클라우드
  - 오프라인 처리
---

## Aspose.Cells Cloud Docker 컨테이너란 무엇인가요?

Aspose.Cells Cloud Docker 컨테이너는 Aspose에서 제공하는 Docker 기반 컨테이너화된 서비스로, Aspose의 퍼블릭 클라우드 서비스에 의존하지 않고 로컬 또는 프라이빗 클라우드 환경에서 Aspose.Cells Cloud API의 기능을 배포할 수 있도록 해줍니다.

## 왜 Aspose.Cells Cloud Docker 컨테이너를 사용해야 하나요?

Aspose.Cells Cloud Docker 컨테이너는 다음과 같은 기능을 지원하는 강력한 스프레드시트 처리 서비스 컨테이너입니다.

### 핵심 기능

- Excel 파일 읽기 및 쓰기(XLS, XLSX, CSV, ODS 등)
- 수식 계산, 차트, 조건부 서식, 피벗 테이블 등
- 형식 변환(예: Excel을 PDF, HTML, 이미지 등으로 변환)
- 셀 조작, 스타일 설정, 워크시트 관리 등

Aspose.Cells Cloud Docker 컨테이너는 이러한 기능을 RESTful API로 캡슐화하여 Docker 이미지로 패키징하고, 사용자의 인프라에서 실행할 수 있도록 지원합니다.

### 주요 장점

| 장점                     | 설명                                                                 |
| ------------------------ | -------------------------------------------------------------------- |
| 데이터 개인정보 보호 및 보안 | 모든 파일 처리가 사용자의 프라이빗 네트워크 내에서 수행되며, 제3자 클라우드에 업로드할 필요가 없습니다. |
| 오프라인 사용 가능        | Aspose 퍼블릭 클라우드에 의존하지 않아, 사내 인트라넷 또는 격리 환경에 적합합니다. |
| 확장성                  | Docker/Kubernetes를 통해 쉽게 확장할 수 있습니다.                   |
| 통일된 API              | Aspose.Cells Cloud 퍼블릭 API와 완전히 호환되며, 코드 변경이 필요 없습니다. |
| 라이선스 제어            | 두 가지 인증 방식을 지원하며, 상황에 맞는 방식을 선택할 수 있습니다. |

## Aspose.Cells Cloud Docker 컨테이너 사용 방법

사용자 매뉴얼 참조 — [Aspose.Cells Cloud Docker 컨테이너 사용 방법](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**사전 요구 사항**

- 호스트 머신에 Docker Engine 20.10 이상이 설치되어 있어야 합니다.  
- 일반적인 워크로드를 처리하기 위해 컨테이너에 최소 2GB RAM과 2개 CPU 코어를 할당해야 합니다.  
- 유효한 Aspose.Cells Cloud 라이선스 파일(또는 접근 토큰)을 컨테이너에 마운트할 디렉터리에 준비해야 합니다.

**빠른 시작**

1. Docker 이미지 풀: `docker pull aspose/cells-cloud`.  
2. 라이선스 및 데이터 디렉터리를 마운트하여 컨테이너 실행 예시:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. REST API에 `http://localhost:8080/v3.0/`으로 접근합니다. 자세한 API 사용법은 [Aspose.Cells Cloud API 참조](https://docs.aspose.cloud/cells/api-reference/)를 참고하세요.

## 참고 문서

- [Aspose.Cells Cloud Docker 컨테이너 스토리지 설정 방법.](https://docs.aspose.cloud/cells/docker/storage/)