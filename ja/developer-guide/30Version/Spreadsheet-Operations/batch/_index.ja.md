---
title: "Excelファイルのバッチ処理：変換、ロック、保護、分割、アンロック"
second_title: "Document"
linktitle: "Excelファイルのバッチ処理"
type: docs
url: /batch/
keywords: "バッチ処理、Excel、変換、ロック、保護、分割、アンロック、Aspose.Cells Cloud API、APIリファレンス、バッチ操作"
description: "Aspose.Cells Cloud APIでは、複数のExcelファイルを一度のリクエストで変換、ロック、保護、分割、アンロックするバッチ処理が可能です。詳細なAPI仕様と、Android、C#、Go、Java、NodeJS、Perl、PHP、Python、Ruby、Swift向けのSDKサポートを提供します。"
weight: 35
ArticleTitle: "Excelファイルのバッチ処理 – Aspose.Cells Cloud APIで変換、ロック、保護、分割、アンロック"
---

Aspose.Cells Cloud API は、複数のExcelファイルに対して一度のリクエストで共通の操作を実行できるバッチエンドポイントを提供します。以下に、利用可能なバッチ操作の概要と、各操作の簡潔なAPI仕様を示します。

- **["Excelファイルをバッチで変換"](https://docs.aspose.cloud/cells/batch/convert "Excelファイルをバッチで変換")**  
  *1回のリクエストで複数のExcelファイルを選択した出力形式に変換します。*  

  **API 詳細**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **パラメータ**  

  | 名前           | タイプ    | 説明                                      |
  |---------------|----------|-------------------------------------------|
  | files         | file[]   | 変換する1つ以上のExcelファイル。          |
  | outputFormat  | string   | 出力形式（例：pdf、csv、html）。         |
  | storage       | string   | （オプション）クラウドストレージ名。       |

  **レスポンス**  

  | コード | 説明                              |
  |-------|-----------------------------------|
  | 200   | 変換成功；ファイルを返します。     |
  | 400   | 無効なパラメータが指定されました。 |
  | 401   | 認証エラー：トークンが不足または無効です。 |
  | 500   | サーバー内部エラー。              |

- **["Excelファイルをバッチでロック"](https://docs.aspose.cloud/cells/batch/lock "Excelファイルをバッチでロック")**  
  *複数のExcelファイルに同時にパスワードによるロックを適用します。*  

  **API 詳細**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **パラメータ**  

  | 名前       | タイプ   | 説明                                |
  |-----------|---------|-------------------------------------|
  | files     | array   | ファイル識別子またはURLのリスト。   |
  | password  | string  | ワークブックに適用するパスワード。  |
  | storage   | string  | （オプション）クラウドストレージ名。 |

  **レスポンス**  

  | コード | 説明                          |
  |-------|-------------------------------|
  | 200   | ロック成功。                  |
  | 400   | パラメータが不足または無効です。 |
  | 401   | 認証されていないアクセス。    |
  | 500   | サーバーエラー。              |

- **["Excelファイルをバッチで保護"](https://docs.aspose.cloud/cells/batch/protect "Excelファイルをバッチで保護")**  
  *複数のワークブックに保護設定（例：読み取り専用、構造）を追加します。*  

  **API 詳細**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **パラメータ**  

  | 名前          | タイプ   | 説明                                      |
  |--------------|---------|-------------------------------------------|
  | files        | array   | ファイル識別子またはURLのリスト。        |
  | protection   | object  | 保護オプション（例：readOnly、structure）。 |
  | storage      | string  | （オプション）クラウドストレージ名。      |

  **レスポンス**  

  | コード | 説明                              |
  |-------|-----------------------------------|
  | 200   | 保護の適用に成功しました。         |
  | 400   | リクエストデータが無効です。       |
  | 401   | 認証に失敗しました。               |
  | 500   | 予期しないサーバーエラーです。     |

- **["バッチで分割"](https://docs.aspose.cloud/cells/batch/split "バッチで分割")**  
  *ワークシートまたは行範囲に基づいて、大型のExcelワークブックを複数の小さなファイルに分割します。*  

  **API 詳細**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **パラメータ**  

  | 名前        | タイプ   | 説明                                  |
  |------------|---------|---------------------------------------|
  | files      | array   | 分割するファイル。                     |
  | splitBy    | string  | 基準： "worksheet" または "rowRange"。 |
  | criteria   | object  | 選択した分割方法の詳細。              |
  | storage    | string  | （オプション）クラウドストレージ名。   |

  **レスポンス**  

  | コード | 説明                                  |
  |-------|---------------------------------------|
  | 200   | 分割操作完了；分割されたファイルを返します。 |
  | 400   | 分割パラメータが不正確です。           |
  | 401   | 認証されていないリクエストです。       |
  | 500   | 処理エラーです。                       |

- **["バッチでアンロック"](https://docs.aspose.cloud/cells/batch/unlock "バッチでアンロック")**  
  *1回の呼び出しで複数のExcelファイルのパスワード保護を解除します。*  

  **API 詳細**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **パラメータ**  

  | 名前       | タイプ   | 説明                              |
  |-----------|---------|-----------------------------------|
  | files     | array   | ロックされたファイルの識別子またはURLのリスト。 |
  | password  | string  | ファイルの現在のパスワード。       |
  | storage   | string  | （オプション）クラウドストレージ名。 |

  **レスポンス**  

  | コード | 説明                              |
  |-------|-----------------------------------|
  | 200   | アンロック成功。                  |
  | 400   | パスワードが誤っている、またはファイルが不足しています。 |
  | 401   | 認証されていないアクセスです。     |
  | 500   | サーバーサイドのエラーです。       |
---