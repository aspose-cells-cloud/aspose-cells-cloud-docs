---
title: "워크북 변환 옵션"
second_title: "문서"
linktitle: "워크북 변환 옵션"
type: docs
url: /convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel 변환, PDF, CSV, API"
description: "워크북 변환 옵션 – Aspose.Cells Cloud API를 사용하여 Excel 워크북을 PDF, CSV, HTML 등으로 변환할 때 설정을 구성합니다."
weight: 79
ArticleTitle: "워크북 변환 옵션 – Aspose.Cells Cloud API"
---

# ConvertWorkbookOptions 속성

**API 버전:** 23.12 (2024‑03)

`ConvertWorkbookOptions`는 Aspose.Cells Cloud 변환 API에서 Excel 워크북을 다른 형식(PDF, CSV, HTML 등)으로 변환하는 방법을 지정하기 위해 사용되는 요청 모델입니다. 이 모델은 소스 파일 정보, 대상 형식, 페이지 설정 설정 및 형식별 저장 옵션을 하나로 묶습니다.

| 이름                                | 유형        | 설명                                                                                                   | 비고 |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | 데이터 파일 소스: `CloudFileSystem`, `RequestFiles`, `HttpUri`.                                            |       |
| **[FileInfo](/cells/file-info/)**   | **Object**  | 파일 이름, 크기, Base64 인코딩 콘텐츠를 설명합니다.                                                   |       |
| **[PageSetup](/cells/page-setup/)** | **Object**  | 여백, 방향, 배율 등 페이지 설정 속성입니다.                                              |       |
| **SaveOptions**                     | **Object**  | 형식별 저장 옵션 객체(`PdfSaveOptions`, `HtmlSaveOptions` 등)를 담은 컨테이너입니다.                |       |
| **ConvertFormat**                   | **string**  | 대상 파일 형식(예: **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF** 등)입니다.                              |       |
| **CheckExcelRestriction**           | **boolean** | Excel 특정 제한(최대 행, 열, 시트 이름 길이 등)을 적용할지 여부를 가져오거나 설정합니다. |       |

**사전 조건**

- Aspose.Cells Cloud에 대한 유효한 OAuth 2.0 액세스 토큰을 획득합니다.  
- 소스 파일이 지원되는 `DataSource` 유형 중 하나를 통해 접근 가능해야 합니다.

**빠른 예시**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64‑인코딩된-콘텐츠>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**API 요청 세부 정보**

변환 작업은 다음 엔드포인트로 **POST** 요청을 수행하여 실행됩니다:

```
https://api.aspose.cloud/v3.0/cells/convert
```

필수 헤더:

| 헤더                  | 값                                 |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

요청 본문은 `ConvertWorkbookOptions`의 JSON 표현이어야 합니다(위 예시 참조). `ConvertFormat`에 따라 특정 속성이 필요하지 않은 경우, 모든 속성은 선택 사항입니다.

**API 응답**

성공적인 변환은 **HTTP 200 OK**(또는 비동기 처리의 경우 **202 Accepted**) 상태 코드와 함께 변환된 파일을 응답 본문에 스트리밍으로 반환합니다. 응답이 스트리밍되는 경우, `Content-Disposition` 헤더에 제안된 파일 이름이 포함됩니다.

비동기 요청에 대한 JSON 응답 예시:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**상태 코드**

| 코드 | 의미                                     |
|------|------------------------------------------|
| 200  | 변환 완료; 파일 반환됨.     |
| 202  | 변환 수락됨; 결과는 나중에 사용 가능. |
| 400  | 잘못된 요청 – 누락 또는 유효하지 않은 매개변수. |
| 401  | 인증되지 않음 – 유효하지 않거나 누락된 토큰. |
| 403  | 접근 거부됨 – 권한 부족.   |
| 500  | 내부 서버 오류.                   |

**참고 / 제한 사항**

- `CheckExcelRestriction` 플래그는 최대 행 수(1,048,576) 및 열 수(16,384) 등 Excel 제한을 적용합니다.  
- 모든 대상 형식이 모든 `SaveOptions` 속성을 지원하지는 않으며, 지원되지 않는 옵션은 무시됩니다.  
- 데이터 소스로 `HttpUri`를 사용하는 경우, URL은 인증 없이 공개적으로 접근 가능해야 합니다.  
- API 메서드 및 엔드포인트 정보가 개발자 명확성 향상과 통합 오류 감소를 위해 추가되었습니다.  

## FileSource 속성

| 속성 이름  | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | 소스 유형(`CloudFileSystem`, `RequestFiles`, `HttpUri`)을 나타냅니다. |
| FilePath       | String        | true     | false    |               | 파일 경로 위치입니다.                                                       |

## DbfSaveOptions 속성

| 속성 이름                 | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | **true**인 경우, 숫자 값을 문자열로 내보냅니다.  |
| SaveFormat                | String        | true     | false    |               | DBF 파일의 형식 식별자입니다.               |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## DifSaveOptions 속성

| 속성 이름                 | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | DIF 파일의 형식 식별자입니다.               |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## DocxSaveOptions 속성

| 속성 이름                     | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | 소스 글꼴을 사용할 수 없을 때 사용할 글꼴입니다.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 워크북 기본 글꼴이 적용되었는지 확인합니다.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 대상 형식에 대한 글꼴 호환성을 검증합니다.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 문자 단위 글꼴 대체를 제어합니다.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 각 시트를 별도의 페이지에 배치합니다.               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 시트의 모든 열을 한 페이지에 맞춥니다.            |
| IgnoreError                       | Boolean       | true     | false    |               | 변환 중 비중대한 오류를 무시합니다.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 렌더링할 내용이 없을 경우 빈 페이지를 생성합니다. |
| PageIndex                         | Integer       | true     | false    |               | 내보낼 첫 번째 페이지의 인덱스입니다.                    |
| PageCount                         | Integer       | true     | false    |               | 내보낼 페이지 수입니다.                            |
| PrintingPageType                  | String        | true     | false    |               | 인쇄를 위한 페이지 유형을 지정합니다.                 |
| GridlineType                      | String        | true     | false    |               | 격자선을 렌더링하는 방식을 결정합니다.                |
| TextCrossType                     | String        | true     | false    |               | 텍스트 렌더링을 위한 크로스 유형을 정의합니다.            |
| DefaultEditLanguage               | String        | true     | false    |               | 텍스트 편집의 기본 언어입니다.                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 렌더링 설정입니다.                           |
| MergeAreas                        | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.       |
| SaveFormat                        | String        | true     | false    |               | DOCX 파일의 형식 식별자입니다.                 |
| CachedFileFolder                  | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.               |
| ClearData                         | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.           |
| RefreshChartCache                 | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.           |
| SortNames                         | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.      |

## HtmlSaveOptions 속성

| 속성 이름                   | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | HTML 출력에 페이지 헤더를 포함합니다.            |
| ExportPageFooters               | Boolean       | true     | false    |               | HTML 출력에 페이지 푸터를 포함합니다.            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | 행 및 열 제목을 내보냅니다.                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | 하나의 HTML 파일에 모든 워크시트를 표시합니다.          |
| ImageOptions                    | Class         | true     | false    |               | 이미지 렌더링을 제어하는 설정입니다.               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | 전체 워크북을 하나의 HTML 파일로 저장합니다.          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | 숨겨진 워크시트를 내보내기에 포함합니다.            |
| ExportGridLines                 | Boolean       | true     | false    |               | HTML 출력에 격자선을 렌더링합니다.               |
| PresentationPreference          | Boolean       | true     | false    |               | 프레젠테이션 모드에 최적화된 HTML을 생성합니다.                |
| CellCssPrefix                   | String        | true     | false    |               | 셀의 생성된 CSS 클래스 이름에 추가되는 접두사입니다. |
| TableCssId                      | String        | true     | false    |               | 생성된 HTML 테이블의 ID 속성입니다.           |
| IsFullPathLink                  | Boolean       | true     | false    |               | 리소스에 대한 전체 경로 하이퍼링크를 생성합니다.        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | 각 워크시트의 CSS를 별도의 파일에 배치합니다.      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | 유사한 테두리 스타일을 병합하여 CSS 크기를 줄입니다.     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | 빈 `<td>` 요소를 강제로 병합합니다.             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | HTML에 셀 좌표(예: A1)를 포함합니다.    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | 필요한 경우 추가 제목 행/열을 추가합니다.       |
| ExportHeadings                  | Boolean       | true     | false    |               | 행 및 열 제목을 내보냅니다.                     |
| ExportFormula                   | Boolean       | true     | false    |               | 계산된 값 대신 수식을 표시합니다.         |
| AddTooltipText                  | Boolean       | true     | false    |               | 셀 주석을 포함한 도구 설명을 추가합니다.                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | 빈 데이터에 대한 플레이스홀더 행을 포함합니다.            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | 사용되지 않는 CSS 스타일을 제거합니다.                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | 문서 수준 속성을 HTML 메타 태그에 기록합니다.  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | 워크시트 수준 속성을 HTML에 기록합니다.           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | 워크북 수준 속성을 HTML에 기록합니다.            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | 프레임의 스크립트 및 속성을 포함합니다.          |
| AttachedFilesDirectory          | String        | true     | false    |               | 첨부 파일의 디렉터리 경로입니다.                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | 첨부 파일의 URL 접두사입니다.                       |
| Encoding                        | String        | true     | false    |               | HTML 파일의 문자 인코딩입니다.                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | 활성 워크시트만 내보냅니다.                   |
| ExportChartImageFormat          | String        | true     | false    |               | 포함된 차트에 사용되는 이미지 형식입니다.               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | 이미지를 Base64 문자열로 인코딩합니다.                    |
| HiddenColDisplayType            | String        | true     | false    |               | 숨겨진 열을 표시하는 방식입니다.                    |
| HiddenRowDisplayType            | String        | true     | false    |               | 숨겨진 행을 표시하는 방식입니다.                       |
| HtmlCrossStringType             | String        | true     | false    |               | 크로스 스트링 데이터를 렌더링하는 방식을 결정합니다.        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | 이미지를 임시 디렉터리로 내보냅니다.             |
| PageTitle                       | String        | true     | false    |               | 생성된 HTML 페이지에 사용되는 제목입니다.              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | 셀 값에 포함된 HTML 태그를 구문 분석합니다.             |
| CellNameAttribute               | String        | true     | false    |               | 셀 참조를 보유하는 속성 이름입니다.        |
| SaveFormat                      | String        | true     | false    |               | HTML 파일의 형식 식별자입니다.                |
| CachedFileFolder                | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.              |
| ClearData                       | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                  |
| CreateDirectory                 | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.   |
| EnableHttpCompression           | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.           |
| RefreshChartCache               | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.           |
| SortNames                       | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.              |
| MergeAreas                      | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                 |
| SortExternalNames               | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.     |

## ImageSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | 차트 렌더링에 사용되는 이미지 형식입니다.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG 출력에 포함된 이미지에 할당된 이름입니다.    |
| HorizontalResolution      | Integer       | true     | false    |               | 내보낸 이미지의 수평 DPI입니다.              |
| ImageFormat               | String        | true     | false    |               | 대상 이미지 형식(PNG, JPG 등)입니다.              |
| IsCellAutoFit             | Boolean       | true     | false    |               | 셀 내용을 이미지 크기에 맞게 자동 조정합니다.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 각 워크시트를 별도의 페이지에 렌더링합니다.         |
| OnlyArea                  | Boolean       | true     | false    |               | 워크시트의 정의된 영역만 내보냅니다.    |
| PrintingPage              | String        | true     | false    |               | 인쇄에 사용되는 페이지 레이아웃입니다.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 인쇄 중 상태 대화 상자를 표시합니다.             |
| Quality                   | Integer       | true     | false    |               | JPEG 이미지 압축 품질(0-100)입니다.       |
| TiffCompression           | String        | true     | false    |               | TIFF 이미지의 압축 유형입니다.                  |
| VerticalResolution        | Integer       | true     | false    |               | 내보낸 이미지의 수직 DPI입니다.                |
| SaveFormat                | String        | true     | false    |               | 이미지 파일의 형식 식별자입니다.             |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## JsonSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | 내보낼 워크시트 영역을 정의합니다.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 첫 번째 행에 열 제목이 포함되어 있는지 여부를 나타냅니다. |
| ExportAsString            | Boolean       | true     | false    |               | 모든 값을 문자열로 내보냅니다.                           |
| Indent                    | String        | true     | false    |               | 들여쓰기에 사용되는 문자열(예: 두 개의 공백)입니다.          |
| SaveFormat                | String        | true     | false    |               | JSON 파일의 형식 식별자입니다.                    |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                  |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                      |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.               |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.               |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                  |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                     |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.         |

## MarkdownSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | 마크다운 파일의 문자 인코딩입니다.                    |
| FormatStrategy            | String        | true     | false    |               | 마크다운을 서식화하는 데 사용되는 전략(예: GitHub, CommonMark)입니다. |
| LineSeparator             | String        | true     | false    |               | 사용할 줄 바꿈 문자입니다.                              |
| SaveFormat                | String        | true     | false    |               | 마크다운 파일의 형식 식별자입니다.                    |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                      |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                          |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.           |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.                   |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.                   |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                      |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                         |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.            |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.             |

## OoxmlSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | 내보낸 파일에 셀 이름을 포함합니다.            |
| UpdateZoom                | Boolean       | true     | false    |               | 출력 문서의 줌 수준을 업데이트합니다.       |
| EnableZip64               | Boolean       | true     | false    |               | 대용량 파일에 대한 ZIP64 확장 기능을 활성화합니다.            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | OOXML을 OLE 개체로 포함합니다.                       |
| CompressionType           | String        | true     | false    |               | 적용되는 압축 유형(예: Normal, Maximum)입니다. |
| SaveFormat                | String        | true     | false    |               | OOXML 파일의 형식 식별자입니다.               |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.              |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                  |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.           |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.           |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.              |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                 |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.     |

## PclSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | 사용할 글꼴의 전체 이름입니다.                      |
| fontPclName               | String        | true     | false    |               | PCL 전용 글꼴 이름입니다.                            |
| SaveFormat                | String        | true     | false    |               | PCL 파일의 형식 식별자입니다.               |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## PDFSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | 문서 제목을 PDF 제목으로 사용합니다.            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | 문서의 논리적 구조를 보존합니다.     |
| EmfRenderSetting          | String        | true     | false    |               | EMF 이미지 렌더링 설정입니다.                   |
| CustomPropertiesExport    | String        | true     | false    |               | 사용자 정의 문서 속성 내보내기를 제어합니다.       |
| OptimizationType          | String        | true     | false    |               | PDF 최적화 유형(예: Size, Speed)입니다.        |
| Producer                  | String        | true     | false    |               | PDF 생성 애플리케이션의 이름입니다.                |
| PDFCompression            | String        | true     | false    |               | PDF 스트림에 사용되는 압축 알고리즘입니다.               |
| FontEncoding              | String        | true     | false    |               | 포함된 글꼴에 사용되는 인코딩입니다.                    |
| Watermark                 | Class         | true     | false    |               | PDF에 적용되는 워터마크 설정입니다.               |
| CalculateFormula          | Boolean       | true     | false    |               | 내보내기 전 수식을 계산합니다.                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | PDF 렌더링을 위한 글꼴 호환성을 검증합니다.      |
| Compliance                | String        | true     | false    |               | PDF/A 또는 PDF/X 준수 수준입니다.                     |
| DefaultFont               | String        | true     | false    |               | 소스 글꼴을 사용할 수 없을 때 사용할 글꼴입니다.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | 각 워크시트를 별도의 PDF 페이지에 배치합니다.        |
| PrintingPageType          | String        | true     | false    |               | 인쇄를 위한 페이지 유형을 지정합니다.                |
| SecurityOptions           | Class         | true     | false    |               | 암호 및 권한 등 보안 설정입니다.               |
| desiredPPI                | Integer       | true     | false    |               | 원하는 픽셀당 인치 해상도입니다.                  |
| jpegQuality               | Integer       | true     | false    |               | JPEG 이미지 품질(0-100)입니다.                          |
| ImageType                 | String        | true     | false    |               | 래스터화에 사용되는 이미지 유형입니다.                   |
| SaveFormat                | String        | true     | false    |               | PDF 파일의 형식 식별자입니다.                 |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.              |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                  |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.           |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.           |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.              |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                 |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.     |

## PptxSaveOptions 속성

| 속성 이름                     | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | 내보내기 중 숨겨진 행을 건너뜁니다.                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | 행 유형에 따라 글꼴 크기 조정을 제어합니다.       |
| ExportViewType                    | String        | true     | false    |               | 내보낼 뷰(슬라이드, 메모)를 결정합니다.        |
| DefaultFont                       | String        | true     | false    |               | 소스 글꼴을 사용할 수 없을 때 사용할 글꼴입니다.           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 워크북 기본 글꼴이 적용되었는지 확인합니다.   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 대상 형식에 대한 글꼴 호환성을 검증합니다.    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 문자 단위 글꼴 대체를 제어합니다.            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 각 워크시트를 별도의 슬라이드에 배치합니다.             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 시트의 모든 열을 한 슬라이드에 맞춥니다.            |
| IgnoreError                       | Boolean       | true     | false    |               | 변환 중 비중대한 오류를 무시합니다.         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 렌더링할 내용이 없을 경우 빈 슬라이드를 생성합니다. |
| PageIndex                         | Integer       | true     | false    |               | 내보낼 첫 번째 슬라이드의 인덱스입니다.                    |
| PageCount                         | Integer       | true     | false    |               | 내보낼 슬라이드 수입니다.                            |
| PrintingPageType                  | String        | true     | false    |               | 인쇄를 위한 페이지 유형을 지정합니다.                  |
| GridlineType                      | String        | true     | false    |               | 격자선을 렌더링하는 방식을 결정합니다.                 |
| TextCrossType                     | String        | true     | false    |               | 텍스트 렌더링을 위한 크로스 유형을 정의합니다.             |
| DefaultEditLanguage               | String        | true     | false    |               | 텍스트 편집의 기본 언어입니다.                     |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 렌더링 설정입니다.                            |
| MergeAreas                        | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                   |
| SortExternalNames                 | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.        |
| SaveFormat                        | String        | true     | false    |               | PPTX 파일의 형식 식별자입니다.                  |
| CachedFileFolder                  | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                |
| ClearData                         | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                    |
| CreateDirectory                   | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.     |
| EnableHttpCompression             | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.             |
| RefreshChartCache                 | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.             |
| SortNames                         | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.       |

## SqlScriptSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | 대상 테이블이 이미 존재하는지 확인합니다.          |
| ColumnTypeMap             | String        | true     | false    |               | 열 이름을 SQL 데이터 유형에 매핑합니다.               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | 모든 행을 스캔하여 열 유형을 추론합니다.                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | 생성된 행 사이에 빈 줄을 삽입합니다.             |
| Separator                 | String        | true     | false    |               | 열을 구분하는 데 사용되는 문자열(예: 쉼표, 탭)입니다.      |
| OperatorType              | String        | true     | false    |               | 사용되는 SQL 연산자(INSERT, UPDATE 등)입니다.                |
| PrimaryKey                | Integer       | true     | false    |               | 기본 키 역할을 하는 열 인덱스입니다.               |
| CreateTable               | Boolean       | true     | false    |               | CREATE TABLE 문을 생성합니다.                      |
| IdName                    | String        | true     | false    |               | 식별자 열의 이름입니다.                           |
| StartId                   | Integer       | true     | false    |               | 자동 증가 ID의 시작 값입니다.                 |
| TableName                 | String        | true     | false    |               | 대상 데이터베이스 테이블의 이름입니다.                       |
| ExportAsString            | Boolean       | true     | false    |               | 모든 값을 문자열로 내보냅니다.                           |
| ExportArea                | Class         | true     | false    |               | 내보낼 워크시트 영역을 정의합니다.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 첫 번째 행에 열 제목이 포함되어 있는지 여부를 나타냅니다. |
| SaveFormat                | String        | true     | false    |               | SQL 스크립트 파일의 형식 식별자입니다.              |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                  |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                      |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.               |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.               |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                  |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                     |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.         |

## SvgSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | 내보낼 워크시트의 인덱스입니다.                  |
| ChartImageType            | String        | true     | false    |               | 차트 렌더링에 사용되는 이미지 형식입니다.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | SVG 출력에 포함된 이미지에 할당된 이름입니다.    |
| HorizontalResolution      | Integer       | true     | false    |               | 내보낸 SVG의 수평 DPI입니다.                |
| ImageFormat               | String        | true     | false    |               | 래스터 요소의 대상 이미지 형식입니다.           |
| IsCellAutoFit             | Boolean       | true     | false    |               | 셀 내용을 SVG 크기에 맞게 자동 조정합니다.           |
| OnePagePerSheet           | Boolean       | true     | false    |               | 각 워크시트를 별도의 SVG 페이지에 렌더링합니다.     |
| OnlyArea                  | Boolean       | true     | false    |               | 워크시트의 정의된 영역만 내보냅니다.    |
| PrintingPage              | String        | true     | false    |               | 인쇄에 사용되는 페이지 레이아웃입니다.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | 인쇄 중 상태 대화 상자를 표시합니다.             |
| Quality                   | Integer       | true     | false    |               | 래스터 이미지의 압축 품질입니다.             |
| TiffCompression           | String        | true     | false    |               | SVG에 포함된 TIFF 이미지의 압축 유형입니다.  |
| VerticalResolution        | Integer       | true     | false    |               | 내보낸 SVG의 수직 DPI입니다.                  |
| SaveFormat                | String        | true     | false    |               | SVG 파일의 형식 식별자입니다.               |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## TxtSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | 사용되는 인용 유형(예: 쌍따옴표, 홀따옴표)입니다.                            |
| Separator                 | String        | true     | false    |               | 열 구분 기호 문자입니다(예: 쉼표, 탭).                          |
| SeparatorString           | String        | true     | false    |               | 두 개 이상의 문자가 필요한 경우 구분자로 사용되는 전체 문자열입니다. |
| AlwaysQuoted              | Boolean       | true     | false    |               | 모든 필드를 인용하도록 강제합니다.                                         |
| SaveFormat                | String        | true     | false    |               | TXT 파일의 형식 식별자입니다.                                    |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                                 |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                                     |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.                              |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.                              |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                                 |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                                    |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.                        |

## XlsSaveOptions & XlsbSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | 내보내기 중 정확한 셀 색상을 보존합니다.         |
| WpsCompatibility          | Boolean       | true     | false    |               | WPS Office와의 호환성을 활성화합니다.             |
| SaveFormat                | String        | true     | false    |               | XLS/XLSB 파일의 형식 식별자입니다.          |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.            |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                |
| CreateDirectory           | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다. |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.         |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.         |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.            |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.               |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.   |

## XmlSaveOptions 속성

| 속성 이름             | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | 내보내기에 포함할 워크시트 인덱스 목록입니다.      |
| ExportArea                | Class         | true     | false    |               | 내보낼 워크시트 영역을 정의합니다.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | 첫 번째 행에 열 제목이 포함되어 있는지 여부를 나타냅니다. |
| XmlMapName                | String        | true     | false    |               | 워크시트에 적용된 XML 맵의 이름입니다.            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | 시트 이름을 XML 요소 이름으로 사용합니다.             |
| DataAsAttribute           | Boolean       | true     | false    |               | 셀 데이터를 요소 대신 XML 속성으로 내보냅니다. |
| SaveFormat                | String        | true     | false    |               | XML 파일의 형식 식별자입니다.                     |
| CachedFileFolder          | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.                  |
| ClearData                 | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                      |
| CreateDirectory           | String        | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.               |
| RefreshChartCache         | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.               |
| SortNames                 | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.                  |
| MergeAreas                | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                     |
| SortExternalNames         | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.         |

## XpsSaveOptions 속성

| 속성 이름                     | 속성 유형 | Nullable | ReadOnly | 기본값 | 설명                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | 소스 글꼴을 사용할 수 없을 때 사용할 글꼴입니다.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | 워크북 기본 글꼴이 적용되었는지 확인합니다.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | 대상 형식에 대한 글꼴 호환성을 검증합니다.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | 문자 단위 글꼴 대체를 제어합니다.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | 각 워크시트를 별도의 XPS 페이지에 배치합니다.         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | 시트의 모든 열을 한 페이지에 맞춥니다.            |
| IgnoreError                       | Boolean       | true     | false    |               | 변환 중 비중대한 오류를 무시합니다.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | 렌더링할 내용이 없을 경우 빈 페이지를 생성합니다. |
| PageIndex                         | Integer       | true     | false    |               | 내보낼 첫 번째 페이지의 인덱스입니다.                    |
| PageCount                         | Integer       | true     | false    |               | 내보낼 페이지 수입니다.                            |
| PrintingPageType                  | String        | true     | false    |               | 인쇄를 위한 페이지 유형을 지정합니다.                 |
| GridlineType                      | String        | true     | false    |               | 격자선을 렌더링하는 방식을 결정합니다.                |
| TextCrossType                     | String        | true     | false    |               | 텍스트 렌더링을 위한 크로스 유형을 정의합니다.            |
| DefaultEditLanguage               | String        | true     | false    |               | 텍스트 편집의 기본 언어입니다.                    |
| EmfRenderSetting                  | String        | true     | false    |               | EMF 렌더링 설정입니다.                           |
| MergeAreas                        | Boolean       | true     | false    |               | 가능할 때 인접 셀을 병합합니다.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | 외부 이름이 지정된 참조를 정렬합니다.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | SmartArt 개체를 최신 버전으로 업데이트합니다.       |
| SaveFormat                        | String        | true     | false    |               | XPS 파일의 형식 식별자입니다.                  |
| CachedFileFolder                  | String        | true     | false    |               | 임시 캐시 파일을 저장하는 폴더입니다.               |
| ClearData                         | Boolean       | true     | false    |               | 저장 전 기존 데이터를 삭제합니다.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | 대상 디렉터리가 없을 경우 생성합니다.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | 응답에 대해 HTTP 압축을 활성화합니다.            |
| RefreshChartCache                 | Boolean       | true     | false    |               | 저장 전 캐시된 차트 데이터를 새로 고칩니다.            |
| SortNames                         | Boolean       | true     | false    |               | 이름이 지정된 범위를 알파벳순으로 정렬합니다.                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | 병합 셀의 일관성을 검증합니다.               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | 변환 중 Excel 특정 제한을 적용합니다.     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | 출력 파일에서 문서 속성을 암호화합니다.      |
---