---
title: "Aspose.Cells Cloud을(를) 사용하여 스프레드시트 파일 형식 변환하는 방법"
linktitle: "스프레드시트 파일 형식 변환하는 방법"
type: docs
url: /how-to-convert-file-formats-ko
description: "Aspose.Cells Cloud을(를) 사용하여 파일 형식을 변환하는 방법."
weight: 10
kwords: Excel, Office Cloud, REST API, 스프레드시트, PDF, CSV, Json, Markdown, Aspose.Cells Cloud을(를) 통한 파일 형식 변환 방법
---

## 소개

Aspose.Cells Cloud 스프레드시트 API는 로컬 및 클라우드 기반 스프레드시트 파일 변환을 위한 이중 채널 인터페이스 세트를 제공합니다. Excel(XLS, XLSX), CSV, HTML, PDF 등 다양한 형식을 지원하여 다양한 요구사항에 맞는 변환을 손쉽게 수행할 수 있습니다.

### 세 가지 변환 모드 · 통합 객체 모델 · 전체 형식 지원

![변환 모드](image.png)

## **핵심 변환 매트릭스**

| 변환 유형         | 객체 수준     | 일반적인 API                     | 출력 형식                      |
|------------------|--------------|---------------------------------|-------------------------------|
| **로컬 변환**     | 워크북        | `ConvertSpreadsheet`            | PDF/XLSX/JSON/.... 30개 이상 형식 |
|                  | 워크시트      | `ConvertWorksheetToImage`       | PNG/JPEG/SVG                  |
|                  |              | `ConvertWorksheetToPdf`         | Pdf                           |
|                  | 테이블        | `ConvertTableToImage`           | PNG/JPEG/SVG/....             |
|                  |              | `ConvertTableToPdf`             | Pdf                           |
|                  |              | `ConvertTableToCsv`             | Csv                           |
|                  |              | `ConvertTableToHtml`            | Html                          |
|                  |              | `ConvertTableToJson`            | Html                          |
|                  | 범위          | `ConvertRangeToImage`           | PNG/JPEG/SVG/....             |
|                  |              | `ConvertRangeToPdf`             | Pdf                           |
|                  |              | `ConvertRangeToCsv`             | Csv                           |
|                  |              | `ConvertRangeToHtml`            | Html                          |
|                  |              | `ConvertRangeToJson`            | JSON                          |
|                  | 차트          | `ConvertChartToImage`           | PNG/JPEG/SVG/....             |
|                  |              | `ConvertChartToPdf`             | PDF                           |
| **클라우드 변환** | 워크북        | `ExportSpreadsheetAsFormat`     | PDF/XLSX/JSON/.... 30개 이상 형식 |
|                  | 워크시트      | `ExportWorksheetAsFormat`       | PDF/XLSX/JSON/.... 30개 이상 형식 |
|                  | 테이블        | `ExportTableAsFormat`           | PDF/XLSX/JSON/.... 30개 이상 형식 |
|                  | 범위          | `ExportRangeAsFormat`           | PDF/XLSX/JSON/.... 30개 이상 형식 |
|                  | 차트          | `ExportChartAsFormat`           | PDF/XLSX/JSON/.... 30개 이상 형식 |
| **클라우드 저장** | 워크북        | `SaveSpreadsheetAs`             | PDF/XLSX/JSON/.... 30개 이상 형식 |

### **로컬 파일 변환**

```csharp
// Cells Cloud API 클라이언트 가져오기
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel 파일 변환**

```c#
// 로컬 Excel 파일을 PDF로 변환
cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

- **Excel 차트를 SVG 파일로 변환**

```c#
// 로컬 Excel 차트를 SVG로 변환
cellsApi.ConvertChartToImage(new SDK.Request.ConvertChartToImageRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    chartIndex = 0,
    format = "svg"
}, "EmployeeSalesSummary.svg");

```

- **테이블을 CSV 파일로 변환**

```C#
# Sales 워크시트의 SaleLogs 테이블을 csv로 변환
result = api.ConvertTableToCsv( new SDK.Request.ConvertTableToCsvRequest
{
    Spreadsheet = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    tableName = "SaleLogs",
    format = "csv"
}, "EmployeeSalesLog.csv");

```

### **클라우드 파일 변환**

Aspose Cells Cloud API 클라이언트도 먼저 가져와야 합니다.

```csharp
// Cells Cloud API 클라이언트 가져오기
CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
```

- **Excel을 PDF로 변환**

```csharp
// 클라우드 Excel 파일을 PDF로 변환 후 로컬 파일로 저장
cellsApi.ExportSpreadsheetAsFormat( new SDK.Request.ExportSpreadsheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx" ,
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary.pdf");   
```

- **Excel 워크시트를 PDF로 변환**

```csharp
// 클라우드 Excel 워크시트를 PDF로 변환 후 로컬 파일로 저장
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

```csharp
// 클라우드 Excel 워크시트를 PDF로 변환 후 로컬 파일로 저장
cellsApi.ExportWorksheetAsFormat (new SDK.Request.ExportWorksheetAsFormatRequest 
{ 
    name = "EmployeeSalesSummary.xlsx",
    worksheet = "Sales",
    format = "pdf",
    folder ="NetSDKData" 
} , "EmployeeSalesSummary_Sales.pdf");   
```

## Aspose.Cells Cloud SDK 설치 및 초기화

.NET 프로젝트에서 Aspose.Cells-Cloud NuGet 패키지를 설치합니다. NuGet 패키지 관리자 콘솔 또는 Visual Studio의 NuGet 패키지 관리자를 사용할 수 있습니다.  
패키지 관리자 콘솔을 사용하여 패키지를 설치하는 방법은 다음과 같습니다:

```powershell

Install-Package Aspose.Cells-Cloud

```

CellsApi 클래스의 새 인스턴스를 생성하고 클라이언트 ID 및 클라이언트 비밀번호로 초기화합니다. 위 코드 스니펫의 세부 정보는 다음과 같습니다:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

YOUR_API_KEY, YOUR_APP_SID, YOUR_APP_KEY를 실제 API 키, 애플리케이션 SID 및 애플리케이션 키로 바꿔야 합니다.

## **파일 형식 변환 사용 사례**

Aspose Cells Cloud API는 핵심 비즈니스 시나리오를 위한 엔터프라이즈급 **스프레드시트 변환** 기능을 제공합니다:  

1. **Excel → PDF**  
   서식이 유지된 인쇄용 보고서 생성  
2. **스프레드시트 → HTML**  
   웹 애플리케이션에 대화형 테이블 포함  
3. **CSV → Excel (XLSX)**  
   원시 데이터를 분석 가능한 워크북으로 변환  
4. **사용자 정의 형식 트랜스코딩**  
   20개 이상의 형식(XLS, XLSB, ODS, FODS, TSV) 간 변환  
![입력 형식에서 출력 형식으로의 변환](image-1.png)

## **결론: 한 번의 API 호출로 변환 간소화**  

---