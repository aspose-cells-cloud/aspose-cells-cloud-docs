---
title: "Aspose.Cells Cloud에서 로컬 파일 처리와 클라우드 파일 처리의 차이점은 무엇인가요?"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud에서 로컬 파일 처리와 클라우드 파일 처리의 차이점은 무엇인가요?"
linktitle: "로컬 파일 처리 vs. 클라우드 파일 처리"
type: docs
url: /learn/local-file-processing-vs-cloud-file-processing/
description: "Aspose.Cells Cloud의 로컬 파일 및 클라우드 파일 처리 방식을 비교합니다: 저장소, 비용, 보안 및 일반적인 활용 사례를 살펴보고 어떤 접근 방식이 워크플로우에 적합한지 이해하세요."
keywords: "Aspose.Cells Cloud, 로컬 파일 처리, 클라우드 파일 처리, 스프레드시트 변환, API"
weight: 10
---

로컬 파일 처리와 클라우드 파일 처리는 서로 다른 데이터 관리 패러다임이며, 파일 저장 인프라, 비즈니스 처리, 접근 방식, 비용 구조, 보안 및 적용 시나리오 측면에서顯著한 차이가 있습니다. 두 방식의 주요 차이점은 다음과 같습니다:

**사전 준비 사항:** 예제를 사용하기 전에 유효한 Aspose.Cells Cloud 계정, 최신 SDK 버전 설치, 인증을 위한 클라이언트 ID 및 클라이언트 시크릿을 준비해야 합니다.

## 1. 파일 저장 위치 및 인프라

- 로컬 파일:

  - 파일은 사용자가 소유하거나 관리하는 물리적 장치(예: 개인용 컴퓨터의 하드디스크, 내부 서버, 외장 하드디스크 등)에 저장됩니다. **Cells Cloud 클라이언트를 로컬 저장 장치에 있는 파일에 직접 연결할 수 있습니다.**
  - 고객은 하드웨어에 대한 물리적 제어를 완전히 보유합니다.
  - 인프라의 구매, 유지보수, 업그레이드 및 폐기 책임은 사용자 또는 사용자의 조직에 있습니다.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import ConvertSpreadsheetRequest

# CellsApi 초기화
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# 로컬 Excel 파일을 PDF로 변환
api.convert_spreadsheet(
    ConvertSpreadsheetRequest('D:\\Data\\BookSales.xlsx', "pdf"),
    local_outpath="BookSales.pdf"
)
```

**API 참조 – 스프레드시트 변환**

| 메서드                | HTTP 동사 | 엔드포인트         | 매개변수 (키)                                      | 응답                       |
|-----------------------|-----------|--------------------|--------------------------------------------------|----------------------------|
| `convert_spreadsheet` | POST      | `/cells/convert`   | `inputFile` – 소스 파일 경로<br>`format` – 대상 포맷(예: `pdf`) | `200 OK` – 변환 성공<br>`400 Bad Request` – 잘못된 매개변수<br>`401 Unauthorized` – 인증 실패 |

- 클라우드 파일:

  - 파일은 타사 클라우드 서비스 제공업체(Aspose 클라우드 스토리지, Dropbox, AWS, Google Cloud, Microsoft Azure)가 운영하는 원격 데이터 센터에 저장됩니다. **AWS, Dropbox, Google Cloud 및 Microsoft Azure 모두 Aspose 클라우드 스토리지와 연결할 수 있습니다.**
  - 고객은 인터넷을 통해 해당 파일에 접근하며, 기반 하드웨어의 위치나 유지보수 상태와 무관합니다.
  - 인프라는 클라우드 서비스 제공업체의 책임이며, 사용자는 필요 시 즉시 사용합니다.

```python
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.requests import (
    UploadFileRequest,
    ExportSpreadsheetAsFormatRequest,
    SaveSpreadsheet_asRequest,
)

# CellsApi 초기화
api = CellsApi('YourCellsCloudClientId', 'YourCellsCloudClientSecret')

# 로컬 파일을 클라우드 스토리지에 업로드
api.upload_file(
    UploadFileRequest(
        "D:\\Data\\EmployeeSalesSummary.xlsx",
        "PythonSDK/EmployeeSalesSummary.xlsx"
    )
)

# 클라우드 파일을 지정된 형식으로 변환하여 로컬 스토리지로 내보내기
api.export_spreadsheet_as_format(
    ExportSpreadsheetAsFormatRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder="PythonSDK"
    ),
    local_outpath="D:\\DataOutput\\EmployeeSalesSummary.pdf"
)

# 원격 폴더 정의 (다른 폴더명 사용 시 실제 폴더명으로 변경)
RemoteFolder = "PythonSDK"

# Cells Cloud의 Excel 파일을 Cells Cloud의 다른 포맷 파일로 저장
api.save_spreadsheet_as(
    SaveSpreadsheet_asRequest(
        "EmployeeSalesSummary.xlsx",
        "pdf",
        folder=RemoteFolder
    )
)
```

**API 참조 – 클라우드 파일 작업**

| 메서드                     | HTTP 동사 | 엔드포인트                     | 매개변수 (키)                                                                                  | 응답                                           |
|----------------------------|-----------|--------------------------------|------------------------------------------------------------------------------------------------|------------------------------------------------|
| `upload_file`              | PUT       | `/cells/storage/file`          | `localPath` – 로컬 파일 경로<br>`remotePath` – 클라우드 스토리지 내 대상 경로                   | `200 OK` – 업로드 성공<br>`401 Unauthorized` |
| `export_spreadsheet_as_format` | POST      | `/cells/{name}/export`         | `name` – 클라우드 파일 이름<br>`format` – 대상 포맷(예: `pdf`)<br>`folder` – 선택적 폴더       | `200 OK` – 내보내기 성공<br>`400 Bad Request` |
| `save_spreadsheet_as`      | POST      | `/cells/{name}/saveas`         | `name` – 클라우드 파일 이름<br>`format` – 대상 포맷<br>`folder` – 대상 폴더                   | `200 OK` – 저장 성공<br>`401 Unauthorized` |

## 2. 비즈니스 처리

로컬 파일 처리 또는 클라우드 파일 처리 여부와 관계없이, 모든 비즈니스 처리는 Cells Cloud 서버에서 완료되므로 **인터넷 연결이 필요합니다**.

## 3. 데이터 접근

- 로컬 파일 처리:

  - 접근은 일반적으로 해당 장치 내에서만 가능합니다.
  - 다중 사용자 협업이 어렵습니다.
  - 장치나 위치 변경 시 불편함이 있습니다.

- 클라우드 파일 처리:

  - 인터넷 연결이 가능한 경우, 언제 어디서나(컴퓨터, 휴대폰, 태블릿 등) 파일에 접근할 수 있습니다.
  - 다중 사용자 실시간 협업을 기본적으로 지원하며, 여러 사용자가 동일 문서를 동시에 편집할 수 있으며, 시스템이 자동으로 버전 관리를 수행합니다.
  - 이동성이 강력하고, 유연한 오피스 지원 및 원격 근무가 가능합니다.

## 4. 비용 구조 및 보안

- 로컬 파일:

  - 초기 단계에서 높은 자본 지출이 필요하며, 이는 이후 운영 지원 비용을 증가시킵니다.
  - 물리적 보안 및 네트워크 보안은 모두 사용자 자신이 관리합니다.

- 클라우드 파일:

  - 초기 투자 비용이 낮고, 주로 운영 비용으로 구성되며, 사용량에 따라 요금이 부과됩니다.
  - 보안 및 무결성은 클라우드 서비스 제공업체의 책임입니다.

## 5. 적용 시나리오

- 로컬 파일: 파일 작업은 로컬에서만 수행됩니다.  
- 클라우드 파일: 파일 작업은 로컬 또는 클라우드에서 모두 수행 가능합니다.  

**참고/제한사항:** API는 클라우드 처리 시 최대 200 MB까지의 파일을 지원하며, 문서에 명시된 포맷만 변환이 가능합니다. 네트워크 지연은 대규모 스프레드시트 처리 시간에 영향을 줄 수 있습니다.

_최종 업데이트: 2026년 7월 30일_