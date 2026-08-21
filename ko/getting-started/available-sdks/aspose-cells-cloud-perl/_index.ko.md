---
title: "Aspose.Cells Cloud SDK for Perl – 변환, 병합, 분할, 보호 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – 변환, 병합, 분할, 보호 등"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /ko/available-sdks/aspose-cells-cloud-perl/
description: "Aspose.Cells Cloud Perl SDK 살펴보기 – Office가 설치되지 않은 상태에서 Excel 파일을 생성, 변환, 병합, 분할, 보호, 검색 및 바꾸기할 수 있는 크로스플랫폼 라이브러리. 설치 가이드, 코드 예제, API 참조 포함."
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, 변환, PDF, API, Excel 조작, Perl SDK, 클라우드 Excel 처리"
---

_최종 업데이트: 2026년 7월 30일_

이 SDK는 오픈소스이며 MIT 라이선스하에 제공됩니다. Aspose.Cells Cloud용 Perl 라이브러리 소스 코드는 [여기](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl)에서 확인하실 수 있습니다.

# **Perl용 Aspose.Cells Cloud 라이브러리 사용 방법**

Aspose.Cells Cloud SDK for Perl은 Perl 프로그래밍 언어를 사용해 마이크로소프트 Excel 파일을 조작하고 처리할 수 있는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 종속성을 설치하지 않고도 클라우드에서 Excel 문서를 생성, 편집 및 변환할 수 있습니다.

이 문서에서는 Aspose.Cells Cloud SDK for Perl을 사용하여 새 Excel 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장하는 등의 일반적인 작업을 수행하는 방법을 살펴보겠습니다.

## 시작하기

**Perl**용 Aspose.Cells Cloud SDK 사용을 시작하려면 개발 환경을 설정하고 필요한 종속성을 설치해야 합니다. Aspose 웹사이트의 **[Aspose.Cells Cloud 빠른 시작 가이드](https://docs.aspose.cloud/cells/quickstart/)**를 참고하여 클라이언트 ID 및 클라이언트 시크릿을 발급받으세요.

## Aspose.Cells Cloud용 Perl 패키지 설치 방법

**필수 조건**  
- Perl 5.10 이상  
- CPAN(Comprehensive Perl Archive Network) 설치됨  
- 유효한 Aspose.Cells Cloud 클라이언트 ID 및 클라이언트 시크릿  

다음 명령을 사용해 Aspose.Cells Cloud SDK for Perl을 설치할 수 있습니다:

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## Perl 패키지를 사용해 Xlsx를 다른 형식으로 변환하는 방법

- **Aspose.Cells Cloud 라이브러리 가져오기**  
  프로젝트에 Aspose.Cells Cloud Perl SDK에서 필요한 패키지를 먼저 가져옵니다.

- **자격 증명으로 API 클라이언트 구성**  
  고유한 클라이언트 ID 및 클라이언트 시크릿을 사용해 API 클라이언트를 인증합니다.

- **변환 매개변수 준비**  
  변환 작업의 매개변수를 정의합니다. 여기에는 소스 파일 이름, 원하는 출력 형식 및 저장 폴더 경로가 포함됩니다.

- **워크북 변환 실행**  
  `PostConvertWorkbook` 메서드를 사용해 변환 작업을 실행하고 응답을 처리합니다.

아래는 `PostConvertWorkbook` 작업에 대한 간략한 참고 정보입니다:

| HTTP 메서드 | 엔드포인트                               | 필수 매개변수                                       | 샘플 요청(Perl)                                                                                              | 샘플 응답(JSON)                                        | 가능한 상태 코드                |
|-------------|------------------------------------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|-------------------------------|
| POST        | `/cells/convert`                         | `file`(소스 워크북), `outputFormat`, `storage`     | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK, 400 Bad Request, 401 Unauthorized, 500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}