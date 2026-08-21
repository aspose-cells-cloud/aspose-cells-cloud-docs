---
title: "Aspose.Cells Cloud SDK for C#: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
second_title: "문서"
ArticleTitle: "Aspose.Cells Cloud SDK for C#: 변환, 병합, 분할, 보호, 검색, 바꾸기 등"
linktype: "Aspose.Cells Cloud SDK for .NET"
type: docs
url: /available-sdks/aspose-cells-cloud-net/
description: "Aspose.Cells Cloud .NET SDK는 Office 설치 없이 Excel 파일을 생성, 변환, 병합, 분할, 보호, 검색 및 바꾸기 위한 크로스플랫폼 API를 제공합니다."
keywords: "Aspose.Cells, 클라우드 SDK, .NET, Excel, 변환, 병합, 분할, 보호, 검색, 바꾸기, API"
weight: 30
---

이 SDK는 오픈소스이며 MIT 라이선스하에 배포됩니다. Aspose.Cells Cloud의 .NET 라이브러리 소스 코드는 [여기](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet)에서 확인할 수 있습니다.

# **.NET용 Aspose.Cells Cloud 라이브러리 사용 방법**

Aspose.Cells Cloud SDK for .NET은 .NET 프로그래밍 언어를 사용해 마이크로소프트 Excel 파일을 조작하고 처리할 수 있는 강력한 라이브러리입니다. 이 SDK를 사용하면 로컬 머신에 추가 소프트웨어나 종속성을 설치하지 않고도 클라우드에서 Excel 문서를 생성, 편집 및 변환할 수 있습니다.

이 문서에서는 Aspose.Cells Cloud SDK for .NET을 사용하여 새로운 Excel 워크북 생성, 셀에 데이터 삽입, 수정된 워크북을 클라우드에 저장 등 일반적인 작업을 수행하는 방법을 알아보겠습니다.

## 시작하기 전에

Aspose.Cells Cloud SDK for .NET 사용을 시작하려면 개발 환경을 설정하고 필요한 종속성을 설치해야 합니다. 클라이언트 ID와 클라이언트 시크릿을 얻으려면 Aspose 웹사이트의 [해당 문서](https://docs.aspose.cloud/cells/quickstart/)를 참조하세요.

**사전 요구사항**  
- .NET 6.0 이상 설치됨  
- 클라이언트 ID 및 클라이언트 시크릿이 있는 Aspose Cloud 계정  
- 스토리지 위치(Aspose Cloud 스토리지 또는 호환되는 서비스) 접근 권한

## Aspose.Cells Cloud용 .NET 패키지 설치 방법

NuGet을 사용해 Aspose.Cells Cloud SDK for .NET을 설치할 수 있습니다. 아래는 NuGet을 사용한 설치 단계입니다:

```nuget
Install-Package Aspose.Cells-Cloud
```

dotnet CLI를 사용해도 설치가 가능합니다. 아래는 dotnet을 사용한 설치 단계입니다:

```powershell
dotnet add package Aspose.Cells-Cloud
```

## .NET 패키지를 사용해 Xlsx를 PDF로 변환하는 방법

- Aspose.Cells Cloud 라이브러리 가져오기  
  프로젝트에 Aspose.Cells Cloud .NET SDK에서 필요한 패키지를 먼저 가져옵니다.  
- 자격 증명으로 API 클라이언트 구성  
  고유한 클라이언트 ID와 클라이언트 시크릿으로 API 클라이언트를 인증합니다.  
- 변환 매개변수 준비  
  변환 작업의 매개변수를 정의합니다. 여기에는 소스 파일 이름, 원하는 출력 형식, 스토리지 폴더 경로가 포함됩니다.  
- 워크북 변환 실행  
  `PostConvertWorkbook` 메서드를 호출해 변환 작업을 실행하고 응답을 처리합니다.

### **샘플 코드**

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_AvailableSDKs.cs" >}}