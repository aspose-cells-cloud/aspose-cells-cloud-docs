---
title: "Aspose.Cells Cloud API – 파일 및 폴더 관리 (업로드, 다운로드, 복사, 이동)"
second_title: "문서"
ArticleTitle: "Excel용 클라우드 파일 관리 – 효율적이고 안전한 Excel 파일 저장 및 지능형 조직 솔루션"
linktype: "files-and-storage"
type: docs
url: /ko/files-and-storage/
aliases: [  /ko/working-with-files-and-storage-using-aspose-cells-cloud/ ]
keywords: "Aspose.Cells Cloud, 파일 저장소 API, Excel 파일 업로드, Excel 파일 다운로드, 파일 복사, 파일 이동, 파일 삭제, 폴더 관리, REST API, cURL 예제"
description: "Aspose.Cells Cloud 저장소에서 Excel 파일 및 폴더를 관리하는 종합 가이드입니다. cURL 예제, 필수 매개변수, 인증 참고 사항을 포함한 업로드, 다운로드, 복사, 이동, 삭제 및 폴더 작업을 제공합니다."
weight: 100
---

Aspose.Cells Cloud는 Aspose.Cells Cloud 저장소 또는 선택한 타사 클라우드 저장소에 저장된 파일을 작업하기 위한 종합적인 도우미 기능 세트를 제공합니다. 타사 저장소 설정에 대한 도움이 필요하시면 [Aspose Cloud UI 도움말 주제](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics)를 참조하십시오.

**Aspose.Cells Cloud는 파일, 폴더 및 저장소 작업 API의 다양한 기능을 제공합니다.**

> **참고:** 모든 API 호출은 **HTTPS**를 사용해야 합니다. JWT 토큰 획득 방법은 [인증 가이드](/cells/authentication/)를 참조하십시오.

**사전 요구 사항:** 이 API를 사용하려면 유효한 Aspose Cloud 계정이 필요하며, JWT 액세스 토큰을 획득하고 저장소 위치를 구성해야 합니다(Aspose Cloud 저장소 또는 연결된 타사 저장소 중 하나).

**최종 업데이트:** 2024-12-01

## **파일 업로드 방법**

### 파일 업로드 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 파일을 업로드할 경로로, 파일 이름과 확장자 포함 (예: `/folder1/Report.xlsx`). |
| file           | file   | formData | 업로드할 파일입니다. |
| storageName    | string | query | 사용할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일이 성공적으로 업로드되었습니다. |
| 400  | 잘못된 요청 – 매개변수 누락 또는 유효하지 않음. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 저장소를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/File/UploadFile)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 업로드 예제

cURL 명령줄 도구를 사용하여 Aspose.Cells 웹 서비스에 쉽게 접근할 수 있습니다. 다음 예제는 cURL을 사용하여 파일을 업로드하는 방법을 보여줍니다.

{{< tabs tabTotal="2" tabID="11" tabName11="요청" tabName12="응답" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 업로드 가능한 최대 파일 크기는 100MB입니다. 요금제에 따라 속도 제한이 적용될 수 있습니다.*

## **파일 다운로드 방법**

### 파일 다운로드 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 파일 경로 (예: `/folder/Report.xlsx`). |
| storageName    | string | query | 사용할 저장소 이름입니다. |
| versionId      | string | query | 다운로드할 파일 버전 식별자 (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일 다운로드 완료; 바이너리 스트림 반환. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 파일을 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/File/DownloadFile)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 다운로드 예제

{{< tabs tabTotal="2" tabID="13" tabName13="요청" tabName14="응답" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<바이너리 데이터>"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 응답에는 파일의 바이너리 스트림이 포함됩니다. cURL을 사용할 때는 (`-o filename.xlsx`)를 사용하여 결과를 파일로 저장하십시오.*

## **파일 삭제 방법**

### 파일 삭제 API 정보

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 파일 경로 (예: `/folder/Report.xlsx`). |
| storageName    | string | query | 사용할 저장소 이름입니다. |
| versionId      | string | query | 삭제할 파일 버전 식별자 (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일이 성공적으로 삭제되었습니다. |
| 400  | 잘못된 요청 – 매개변수 누락 또는 유효하지 않음. |
| 401  | 인증되지 않음 – 잘못된 JWT 토큰. |
| 404  | 파일을 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/File/DeleteFile)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 삭제 예제

{{< tabs tabTotal="2" tabID="15" tabName15="요청" tabName16="응답" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 파일을 삭제하면 영구적으로 삭제되며, 필요 시 백업이 필수입니다.*

## **파일 복사 방법**

### 파일 복사 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 위치  | 설명 |
|------------------|--------|-------|-------------|
| srcPath          | string | path  | 원본 파일 경로 (예: `/folder/Source.xlsx`). |
| destPath         | string | query | 대상 파일 경로 (예: `/folder/Destination.xlsx`). |
| srcStorageName   | string | query | 원본 저장소 이름 (선택 사항). |
| destStorageName  | string | query | 대상 저장소 이름 (선택 사항). |
| versionId        | string | query | 복사할 파일 버전 ID (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일이 성공적으로 복사되었습니다. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 원본 파일을 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/File/CopyFile)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 복사 예제

{{< tabs tabTotal="2" tabID="17" tabName17="요청" tabName18="응답" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 복사 작업은 원본 파일을 제거하지 않습니다.*

## **파일 이동 방법**

### 파일 이동 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 위치  | 설명 |
|------------------|--------|-------|-------------|
| srcPath          | string | path  | 원본 파일 경로 (예: `/folder/Source.xlsx`). |
| destPath         | string | query | 대상 파일 경로 (예: `/folder/Destination.xlsx`). |
| srcStorageName   | string | query | 원본 저장소 이름 (선택 사항). |
| destStorageName  | string | query | 대상 저장소 이름 (선택 사항). |
| versionId        | string | query | 이동할 파일 버전 ID (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일이 성공적으로 이동되었습니다. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 원본 파일을 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/File/MoveFile)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 이동 예제

{{< tabs tabTotal="2" tabID="1" tabName1="요청" tabName2="응답" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 파일을 이동하면 파일의 버전 기록이 유지됩니다.*

## **폴더 생성 방법**

### 폴더 생성 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 생성할 폴더 경로 (예: `folder1/folder2/`). |
| storageName    | string | query | 사용할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 폴더가 성공적으로 생성되었습니다. |
| 400  | 잘못된 요청 – 경로 또는 매개변수가 잘못되었습니다. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 폴더 생성 예제

{{< tabs tabTotal="2" tabID="3" tabName3="요청" tabName4="응답" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 폴더 경로는 대소문자를 구분합니다.*

## **폴더 내 파일 목록 조회 방법**

### 파일 목록 조회 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 폴더 경로 (예: `/folder`). |
| storageName    | string | query | 사용할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일 및 하위 폴더 목록 반환. |
| 400  | 잘못된 요청 – 경로가 잘못되었습니다. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 폴더를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 목록 조회 예제

{{< tabs tabTotal="2" tabID="5" tabName5="요청" tabName6="응답" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 응답은 지정된 경로 내의 파일과 하위 폴더를 모두 나열합니다.*

## **폴더 삭제 방법**

### 폴더 삭제 API 정보

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형    | 위치  | 설명 |
|----------------|---------|-------|-------------|
| path           | string  | path  | 폴더 경로 (예: `/folder`). |
| storageName    | string  | query | 사용할 저장소 이름입니다. |
| recursive      | boolean | query | `true`로 설정하면 폴더를 재귀적으로 삭제합니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 폴더가 성공적으로 삭제되었습니다. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 폴더를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 폴더 삭제 예제

{{< tabs tabTotal="2" tabID="7" tabName7="요청" tabName8="응답" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: `recursive=true`로 폴더를 삭제하면 내용물이 모두 영구적으로 삭제됩니다.*

## **폴더 복사 방법**

### 폴더 복사 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 위치  | 설명 |
|------------------|--------|-------|-------------|
| srcPath          | string | path  | 원본 폴더 경로 (예: `/src`). |
| destPath         | string | query | 대상 폴더 경로 (예: `/dst`). |
| srcStorageName   | string | query | 원본 저장소 이름 (선택 사항). |
| destStorageName  | string | query | 대상 저장소 이름 (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 폴더가 성공적으로 복사되었습니다. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 원본 폴더를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 폴더 복사 예제

{{< tabs tabTotal="2" tabID="21" tabName21="요청" tabName22="응답" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 복사 작업은 원본과 동일한 내용을 가진 새 폴더를 생성합니다.*

## **폴더 이동 방법**

### 폴더 이동 API 정보

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름     | 유형   | 위치  | 설명 |
|------------------|--------|-------|-------------|
| srcPath          | string | path  | 원본 폴더 경로 (예: `/folder`). |
| destPath         | string | query | 대상 폴더 경로 (예: `/dst`). |
| srcStorageName   | string | query | 원본 저장소 이름 (선택 사항). |
| destStorageName  | string | query | 대상 저장소 이름 (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 폴더가 성공적으로 이동되었습니다. |
| 400  | 잘못된 요청 – 매개변수 오류. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 원본 폴더를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 폴더 이동 예제

{{< tabs tabTotal="2" tabID="23" tabName23="요청" tabName24="응답" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*참고: 폴더를 이동하면 내부 구조와 파일 버전이 유지됩니다.*

## **저장소 존재 여부 확인 방법**

### 저장소 존재 여부 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| storageName    | string | path  | 확인할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 저장소 존재 여부(`true` 또는 `false`) 반환. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 저장소를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Storage/StorageExists)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 저장소 존재 여부 예제

{{< tabs tabTotal="2" tabID="33" tabName33="요청" tabName34="응답" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **파일 또는 폴더 존재 여부 확인 방법**

### 객체 존재 여부 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 파일 또는 폴더 경로 (예: `/file.xlsx` 또는 `/folder`). |
| storageName    | string | query | 확인할 저장소 이름입니다. |
| versionId      | string | query | 파일 버전 식별자 (선택 사항). |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 존재 여부 정보 반환. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 파일 또는 폴더를 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 객체 존재 여부 예제

{{< tabs tabTotal="2" tabID="37" tabName37="요청" tabName38="응답" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **디스크 사용량 확인 방법**

### 디스크 사용량 조회 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| storageName    | string | query | 쿼리할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 디스크 사용량 정보 반환. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 디스크 사용량 조회 예제

{{< tabs tabTotal="2" tabID="40" tabName40="요청" tabName41="응답" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **파일 버전 목록 조회 방법**

### 파일 버전 조회 API 정보

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

요청 매개변수는 다음과 같습니다:

| 매개변수 이름   | 유형   | 위치  | 설명 |
|----------------|--------|-------|-------------|
| path           | string | path  | 파일 경로 (예: `/file.xlsx`). |
| storageName    | string | query | 쿼리할 저장소 이름입니다. |

**HTTP 응답 코드**

| 코드 | 설명 |
|------|------------------------------------------|
| 200  | 파일 버전 목록 반환. |
| 401  | 인증되지 않음 – 잘못되거나 누락된 JWT 토큰. |
| 404  | 파일을 찾을 수 없습니다. |
| 500  | 내부 서버 오류입니다. |

[OpenAPI 사양](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions)은 웹 브라우저에서 직접 REST 상호 작용을 가능하게 하는 공개적으로 액세스 가능한 프로그래밍 인터페이스를 정의합니다.

### 파일 버전 조회 예제

{{< tabs tabTotal="2" tabID="46" tabName46="요청" tabName47="응답" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}