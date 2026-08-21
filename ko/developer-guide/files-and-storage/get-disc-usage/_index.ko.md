---
title: "Aspose.Cells Cloud API – 디스크 사용량 조회 | 실시간 스토리지 메트릭"
second_title: "문서"
ArticleTitle: "클라우드 기반 엑셀 파일 관리 솔루션 – 클라우드에서 디스크 사용량을 빠르게 조회할 수 있는 인터페이스"
linktype: "Get Disk Usage"
type: docs
url: /ko/get-disk-usage/
keywords: "Aspose Cells, 클라우드 API, 디스크 사용량, 스토리지 메트릭, 엑셀, REST"
description: "Aspose.Cells Cloud의 실시간 디스크 사용량을 조회하세요. GET /v4.0/cells/storage/disk 엔드포인트, 필요한 인증 및 샘플 응답에 대해 알아보세요."
weight: 100
---

**Get Disk Usage**(디스크 사용량 조회) 작업은 Aspose.Cells Cloud 계정의 실시간 스토리지 메트릭을 반환합니다. 이 엔드포인트를 사용하여 소비된 디스크 공간과 전체 디스크 공간을 모니터링할 수 있습니다.

- Aspose Cloud 환경에서 Excel API의 현재 디스크 사용량을 조회합니다.
- 개발자가 애플리케이션에서 소비한 스토리지 용량을 모니터링할 수 있도록 합니다.
- 스토리지 한도 및 비용 관리를 사전에 계획하고 실행할 수 있도록 지원합니다.

## Excel API: GetDiskUsage

### 웹 API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **보안 및 인증**

Aspose.Cells Cloud API는 보안이 보장되며, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT 토큰 기반 인증</a>이 필요합니다.

### 요청 매개변수

| 매개변수 이름 | 유형   | 위치   | 설명                                                  | 필수 여부 |
| -------------- | ------ | ------ | ----------------------------------------------------- | --------- |
| storageName    | String | Query  | 사용량을 조회할 스토리지의 이름입니다.               | 선택 사항 |

### **응답**

```json
{
  "Name": "DiskUsage",
  "Description": ["디스크 공간 정보를 위한 클래스입니다."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["애플리케이션에서 사용 중인 디스크 공간의 양입니다."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["사용 가능한 전체 디스크 공간입니다."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP 상태 코드**

| 코드 | 의미                 | 설명                                                            |
| ---- | -------------------- | --------------------------------------------------------------- |
| 200  | OK(성공)             | 필터가 성공적으로 적용되었으며, 응답에 작업 세부 정보가 포함됩니다. |
| 400  | Bad Request(잘못된 요청) | 매개변수 누락 또는 유효하지 않음(예: 지원되지 않는 파일 유형)     |
| 401  | Unauthorized(인증되지 않음) | 유효하지 않거나 누락된 JWT 토큰                                 |
| 413  | Payload Too Large(페이로드가 너무 큼) | 업로드한 파일이 크기 제한을 초과함                              |
| 500  | Internal Server Error(내부 서버 오류) | 예기치 않은 서버 오류                                            |

## OpenAPI 사양

[OpenAPI 사양](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage)은 공개적으로 접근 가능한 프로그래밍 인터페이스를 정의하며, 웹 브라우저에서 직접 REST 상호 작용을 수행할 수 있도록 합니다.

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 아래 예시는 cURL을 사용해 Cloud API로 요청을 보내는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK 사용하기

SDK를 사용하면 개발 속도를 높일 수 있습니다. SDK는 저수준 세부 사항을 처리하므로, 프로젝트의 핵심 작업에 집중할 수 있습니다. Aspose.Cells Cloud SDK의 전체 목록은 [GitHub 저장소](https://github.com/aspose-cells-cloud)를 확인하세요.

다음 코드 예시는 다양한 SDK를 사용해 Aspose.Cells 웹 서비스로 요청을 보내는 방법을 보여줍니다.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}