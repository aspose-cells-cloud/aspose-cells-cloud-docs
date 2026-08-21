---
title: "사용 가능한 Aspose.Cells Cloud SDK"
second_title: "문서"
ArticleTitle: "사용 가능한 Aspose.Cells Cloud SDK: C#, Java, PHP, Python, Ruby, Node.js, Go, Perl"
LinkTitle: "사용 가능한 SDK"
type: docs
url: /available-sdks/
description: "C#, Java, PHP, Python, Ruby, Node.js, Go 및 Perl용 Aspose.Cells Cloud SDK를 살펴보세요. 저렴한 비용의 크로스플랫폼 API를 사용하여 클라우드에서 Excel 파일을 빌드, 변환 및 분석하세요."
weight: 30
keywords: "Aspose.Cells Cloud SDK, C#, Java, PHP, Python, Ruby, Node.js, Go, Perl, Excel, 클라우드 API"
---

# **Aspose.Cells Cloud SDK를 사용하는 이유**

## **크로스플랫폼 호환성**

Aspose.Cells Cloud SDK는 여러 개발 언어에 대해 신뢰할 수 있고 안정적인 라이브러리를 제공합니다. 이 SDK는 Windows, Linux, macOS 등 다양한 플랫폼에서 쉽게 통합할 수 있도록 강력한 크로스플랫폼 지원을 제공합니다.

## **효율적인 Excel 처리 및 풍부한 기능 세트**

Aspose.Cells Cloud SDK를 사용하면 개발자는 로컬 Office 소프트웨어를 설치하지 않고도 클라우드에서 Excel 파일을 효율적으로 읽기, 쓰기, 수정 및 변환할 수 있습니다. 이 SDK는 수식 계산, 차트 생성, 조건부 서식 등 복잡한 Excel 작업을 지원하는 풍부한 API와 기능을 제공하여 개발자의 다양한 요구를 충족시킵니다.

## **쉬운 통합**

SDK는 간결하고 명확한 API를 제공하여 개발자가 기존 프로젝트에 빠르게 통합할 수 있도록 도와주며, 개발 시간과 비용을 절감합니다.

## **비용 절감**

Aspose.Cells Cloud SDK를 사용하면 비싼 온프레미스 Office 소프트웨어 또는 서버를 구매하고 유지보수할 필요가 없어 비즈니스 운영 비용을 절감할 수 있습니다.

### SDK 개요

<table>
<thead>
<tr>
<th>언어</th>
<th>최신 버전</th>
<th>설치 방법</th>
<th>빠른 시작 예제</th>
</tr>
</thead>
<tbody>
<tr>
<td>C#</td>
<td>23.12</td>
<td><code>dotnet add package Aspose.Cells-Cloud</code></td>
<td>
<pre><code class="language-csharp">var api = new CellsApi("clientId", "clientSecret");
var result = api.ConvertSpreadsheet(new ConvertSpreadsheetRequest("sample.xlsx", "pdf"));</code></pre>
</td>
</tr>
<tr>
<td>Java</td>
<td>23.12</td>
<td><code>mvn dependency:copy -Dartifact=aspose:aspose-cells-cloud:23.12</code></td>
<td>
<pre><code class="language-java">CellsApi api = new CellsApi("clientId", "clientSecret");
ConvertSpreadsheetRequest request = new ConvertSpreadsheetRequest();
request.setSpreadsheet("Book1.xlsx");
request.setFormat("pdf");
File result = api.ConvertSpreadsheetRequest(request);</code></pre>
</td>
</tr>
<tr>
<td>PHP</td>
<td>23.12</td>
<td><code>composer require aspose/cells-cloud-sdk</code></td>
<td>
<pre><code class="language-php">$instance = new CellsApi(getenv("CellsCloudClientId"), getenv("CellsCloudClientSecret"));
$convertSpreadsheetRequest = new ConvertSpreadsheetRequest();
$convertSpreadsheetRequest->setSpreadsheet($EmployeeSalesSummaryXlsx);
$convertSpreadsheetRequest->setFormat("pdf");
$instance->convertSpreadsheet($convertSpreadsheetRequest, "export-out1.pdf");</code></pre>
</td>
</tr>
<tr>
<td>Python</td>
<td>23.12</td>
<td><code>pip install aspose-cells-cloud</code></td>
<td>
<pre><code class="language-python">instance = CellsApi(os.getenv('CellsCloudClientId'), os.getenv('CellsCloudClientSecret'))
instance.convert_spreadsheet(ConvertSpreadsheetRequest('EmployeeSalesSummary.xlsx', 'pdf'), local_outpath="EmployeeSalesSummary.pdf")</code></pre>
</td>
</tr>
<tr>
<td>Ruby</td>
<td>23.12</td>
<td><code>gem install aspose_cells_cloud</code></td>
<td>
<pre><code class="language-ruby">@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'])
request = AsposeCellsCloud::ConvertSpreadsheetRequest.new(:Spreadsheet=>'EmployeeSalesSummary.xlsx', :format=>'pdf')
response = @instance.convert_spreadsheet(request)</code></pre>
</td>
</tr>
<tr>
<td>Node.js</td>
<td>23.12</td>
<td><code>npm install asposecellscloud</code></td>
<td>
<pre><code class="language-javascript">const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret, "v4.0", process.env.CellsCloudApiBaseUrl);
var request = new model.ConvertSpreadsheetRequest();
request.spreadsheet = "Book1.xlsx";
request.format = "pdf";
return cellsApi.convertSpreadsheet(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});</code></pre>
</td>
</tr>
<tr>
<td>Go</td>
<td>23.12</td>
<td><code>go get github.com/aspose/cells-cloud-go/v2</code></td>
<td>
<pre><code class="language-go">instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
convertedData, httpResponse, err := instance.ConvertSpreadsheet(&amp;ConvertSpreadsheetRequest{Spreadsheet: employeeSalesSummaryXlsx, Format: "pdf"})</code></pre>
</td>
</tr>
</tbody>
</table>

**필수 조건** – .NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+. 또한 유효한 Aspose Cloud 클라이언트 ID와 클라이언트 비밀 키가 필요합니다.

**샘플 API 요청 및 응답** – Excel 워크북을 PDF로 변환:

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

SDK는 오픈소스이며 GitHub에 호스팅되어 있습니다. GitHub에서 포크하거나 기여할 수 있습니다:

- C#: https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

요약하자면, Aspose.Cells Cloud SDK를 사용하면 크로스플랫폼 호환성, Excel 파일 처리 효율성, 풍부한 기능 세트, 보안 및 개인정보 보호, 높은 확장성, 쉬운 통합, 커뮤니티 지원 및 문서화, 비용 절감 등 많은 이점을 제공합니다. 이러한 장점들로 인해 이 SDK는 Excel 파일을 다루는 개발자에게 이상적인 선택이 됩니다.

# **적용 사례**

## **스프레드시트 처리 자동화**

- Aspose.Cells Cloud SDK를 사용하여 개발자는 Excel과 같은 스프레드시트 파일의 일괄 처리를 위한 자동화 스크립트를 작성할 수 있습니다.  
- 자동화 작업에는 데이터 가져오기/내보내기, 서식 지정, 수식 계산, 차트 생성 등이 포함될 수 있습니다.

## **클라우드 데이터 처리 및 분석**

- 클라우드의 Aspose.Cells 서비스를 활용하면 로컬 컴퓨팅 리소스를 사용하지 않고도 대규모 스프레드시트 데이터를 처리할 수 있습니다.  
- 복잡한 데이터 분석, 데이터 마이닝 또는 보고서 생성이 필요한 시나리오에 적합합니다.

## **크로스플랫폼 호환성**

- SDK의 크로스플랫폼 특성으로 인해 Aspose.Cells Cloud SDK는 다양한 운영 체제 및 아키텍처에서 스프레드시트 처리를 쉽게 구현할 수 있습니다.  
- 웹 애플리케이션 백엔드, 데스크톱 애플리케이션, 모바일 애플리케이션 백엔드 등 여러 운영 환경을 지원해야 하는 시나리오에 특히 적합합니다.

## **API 통합 및 확장**

- Aspose.Cells Cloud SDK는 기존 API에 통합되어 서비스의 일부로 스프레드시트 처리 기능을 제공할 수 있습니다.  
- 엔터프라이즈 수준의 애플리케이션, SaaS 플랫폼 구축 또는 API 서비스 제공에 적합합니다.

## **문서 협업 및 공유**

- Aspose.Cells Cloud SDK를 사용하면 여러 사람이 동시에 온라인으로 스프레드시트를 공동 편집할 수 있습니다.  
- 사용자는 클라우드에서 실시간으로 스프레드시트 파일을 편집하고, 코멘트를 달고, 공유할 수 있어 팀 협업을 향상시킬 수 있습니다.

## **데이터 마이그레이션 및 변환**

- 다른 형식 또는 시스템에서 데이터를 마이그레이션해야 할 경우, Aspose.Cells Cloud SDK는 데이터 변환을 위한 다리 역할을 할 수 있습니다.  
- 다른 형식의 데이터를 Excel 형식으로 변환하여 후속 분석 및 처리를 수행할 수 있습니다.

## **자동 보고서 생성**

- 주기적으로 스크립트를 실행하면 Aspose.Cells Cloud SDK를 사용하여 정기적인 보고서 또는 대시보드를 자동으로 생성할 수 있습니다.  
- 비즈니스 지표, 판매 데이터 또는 재무 데이터를 정기적으로 모니터링해야 하는 조직에 유용합니다.

## **CI/CD 프로세스 통합**

- Aspose.Cells Cloud SDK를 지속적 통합/지속적 배포(CI/CD) 프로세스에 통합하여 스프레드시트 데이터의 정확성을 자동으로 테스트할 수 있습니다.  
- 코드 변경으로 인해 스프레드시트 데이터의 무결성이나 서식이 손상되지 않도록 보장하는 데 도움이 됩니다.

## **맞춤형 스프레드시트 애플리케이션**

- Aspose.Cells Cloud SDK를 사용하여 특정 비즈니스 요구에 맞는 맞춤형 스프레드시트 애플리케이션을 구축할 수 있습니다.  
- 예를 들어, 맞춤형 양식 처리 애플리케이션, 재무 데이터 관리 도구 등을 개발할 수 있습니다.

# **SDK 장점**

SDK는 100% 테스트되었으며 바로 실행할 수 있습니다. MIT 라이선스의 오픈소스로, 완전히 무료로 사용하고 자유롭게 커스터마이징할 수 있습니다.