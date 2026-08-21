---
title: "Aspose.Cells Cloud API – Excel 파일 변환, 병합, 분할 및 보호"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud API – Excel 파일 변환, 병합, 분할 및 보호"
linktitle: "개발자 센터"
type: docs
url: /ko/
description: "Aspose.Cells Cloud REST API를 사용하면 Excel 스프레드시트를 변환, 병합, 분할, 보호 및 종합적으로 처리할 수 있습니다. 월 150회 무료 호출, 8개 언어용 SDK 제공."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, 스프레드시트 변환, Excel 병합, Excel 분할, Excel 보호, 클라우드 스프레드시트 SDK, REST API, Excel 처리"
---

## Aspose.Cells Cloud API란 무엇인가요?

Aspose.Cells Cloud API는 클라우드 기반 스프레드시트/Excel 서비스 모음입니다. Office 설치나 서버 설정이 필요 없으며, 단순히 HTTP 요청을 보내기만 하면 어떤 언어로도 스프레드시트를 생성, 편집, 변환, 데이터 정리, 차트 생성, 피벗 테이블 구성, 암호화, 분할, 병합, 워터마크 추가, 디지털 서명 적용 등 다양한 작업을 수행할 수 있습니다.

## 왜 Aspose.Cells Cloud API를 사용해야 하나요?

- Aspose.Cells Cloud 웹 API 서비스를 기반으로 클라우드 스토리지에서 스프레드시트를 생성, 편집, 변환 및 분석합니다.  
- Aspose.Cells Cloud 웹 API 서비스를 기반으로 로컬 스프레드시트 파일을 생성, 편집, 변환 및 분석합니다.  
- 지원되는 파일 형식은 **xlsx**, **csv**, **ods**, **xlsb** 등 총 30개입니다.  
- Microsoft Excel 의존성 없이 Aspose.Cells Cloud 웹 API를 통해 스프레드시트를 직접 조작합니다.  
- 무료 플랜은 월 최대 150회 API 호출을 포함합니다.  
- 사용량 기반 유연한 요금제입니다.  
- **단문 설명**: 한 문장으로 수행 가능한 작업들  
  - **XLSX를 PDF로 변환** → ConvertSpreadsheetToPdf  
  - **파일 전체의 불필요한 공백 제거** → TrimSpreadsheetContent  
  - **10개 이상의 파일을 하나의 보고서로 병합** → MergeSpreadsheets  

## **Aspose.Cells Cloud API를 어떻게 사용하나요?**

### 1단계: **API 자격 증명 획득**  

- **[Aspose Cloud 계정 등록](https://dashboard.aspose.cloud/signup)**  
- **[클라이언트 자격 증명 받기](https://dashboard.aspose.cloud/#/applications)**  

### 2단계: **SDK를 사용하여 스프레드시트 웹 API 호출 (권장)**  

인증 및 요청 처리를 간소화하기 위해 공식 SDK 사용을 권장합니다. SDK는 액세스 토큰을 자동으로 획득하고 갱신합니다.

#### **[.NET SDK 설치 (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### 예제: **SDK를 사용하여 Excel을 PDF로 변환**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### 설명

- **Spreadsheet**: 로컬 저장소에 위치한 Excel 파일 이름입니다.  
- **Format**: 변환할 대상 형식 (예: pdf, png, csv, json 등).  
- **Output file**: 결과 파일은 지정된 이름으로 로컬에 저장됩니다.  

## **핵심 기능**

Aspose.Cells Cloud는 엔터프라이즈 수준의 스프레드시트 자동화 요구사항을 충족하기 위해 다음 주요 기능을 제공합니다:

### **스프레드시트 변환**

- **[스프레드시트를 PDF 파일로 변환](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[스프레드시트 차트를 이미지로 변환](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[스프레드시트를 다른 형식으로 저장](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **데이터 처리**

- **[스프레드시트 병합](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[스프레드시트 분할](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[스프레드시트의 빈 행 삭제](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[스프레드시트의 빈 열 삭제](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[스프레드시트 콘텐츠 바꾸기](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **참고:** 각 엔드포인트에 대한 자세한 요청/응답 스키마, HTTP 메서드, 쿼리 매개변수 및 샘플 응답은 아래 링크된 **Aspose.Cells Cloud 스프레드시트 웹 API 참조**에서 확인할 수 있습니다.

**빠른 엔드포인트 참조**

| 작업 | HTTP 메서드 | 경로 | 필수 매개변수 | 샘플 응답 |
|------|-------------|------|---------------------|-----------------|
| 스프레드시트 변환 | POST | `/cells/convert` | `Spreadsheet` (파일), `format` (문자열) | 바이너리 파일 (예: PDF) |
| 스프레드시트 병합 | POST | `/cells/worksheets/merge` | `files` (파일 목록) | 병합된 워크북 |
| 스프레드시트 분할 | POST | `/cells/worksheets/split` | `Spreadsheet` (파일), `format` (문자열) | 분할된 파일 아카이브 |
| 빈 행 삭제 | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (파일) | 업데이트된 워크북 |
| 콘텐츠 바꾸기 | POST | `/cells/replace` | `Spreadsheet` (파일), `oldValue`, `newValue` | 업데이트된 워크북 |

## 지원 SDK (**사용 가능한 SDK**)

- Aspose.Cells Cloud는 주요 언어별로 즉시 사용 가능한 [SDK](https://github.com/aspose-cells-cloud)를 제공합니다. 끌어와서 코드를 작성하고 배포하세요:

| 언어 | 설치 방법 | GitHub 저장소 |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Java SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [.NET SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Python SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Node.js SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [PHP SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [GoLang SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Ruby SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Perl SDK GitHub 저장소](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **API 엔드포인트** | [Aspose.Cells Cloud 스프레드시트 웹 API 참조](https://reference.aspose.cloud/cells/) |  |

## **코드 예제 및 오픈소스 프로젝트**

모든 SDK는 오픈소스이며 풍부한 예제를 포함합니다:

- [Github의 Java SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [Github의 .NET SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Github의 Python SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Github의 Node.js SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [Github의 PHP SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Github의 Go SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Github의 Ruby SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Github의 Perl SDK 예제.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---