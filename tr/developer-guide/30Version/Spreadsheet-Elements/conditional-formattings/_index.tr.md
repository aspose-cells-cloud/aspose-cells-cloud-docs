---
title: "Excel Koşullu Biçimlendirme ile Çalışma"
second_title: "Belge"
linktitle: "Koşullu Biçimlendirme"
type: docs
url: /conditional-formattings/
aliases: [/working-with-conditional-formatting/]
keywords: "Excel, Koşullu Biçimlendirme, Aspose.Cells Cloud, API"
description: "Aspose.Cells Cloud API’si, Excel için koşullu biçimlendirme kurallarını almak, eklemek, değiştirmek ve temizlemek için uç noktalar sağlar; bu sayede çalışma sayfası verilerinin dinamik görsel analizini mümkün kılar."
weight: 100
ArticleTitle: "Excel Koşullu Biçimlendirme ile Çalışma – API Kılavuzu"
---

Excel’de koşullu biçimlendirme, hücre değerine göre hücreleri belirli bir renkle vurgulamanızı sağlar.

Koşullu biçimlendirmeyi, verilerinizi görsel olarak keşfetmek ve analiz etmek, kritik sorunları tespit etmek ve desenleri ile trendleri belirlemek için kullanabilirsiniz.

Koşullu biçimlendirme, ilgi çekici hücreleri veya hücre aralıklarını vurgulamayı, olağandışı değerleri vurgulamayı ve verilerdeki belirli değişikliklere karşılık gelen veri çubukları, renk ölçekleri ve simge setleri kullanarak verileri görselleştirmeyi kolaylaştırır.

Koşullu biçimlendirme, belirttiğiniz koşullara göre hücrelerin görünümünü değiştirir. Koşullar doğruysa hücre aralığı biçimlendirilir; koşullar yanlışsa hücre aralığı değişmeden kalır. Birçok yerleşik koşul mevcuttur ve ayrıca kendi koşullarınızı da (formül kullanarak **TRUE** veya **FALSE** değerlendiren) oluşturabilirsiniz.

Aspose.Cells Cloud API’si, koşullu biçimlendirme kurallarını programlı olarak yönetmek için bir dizi uç nokta sağlar. Aşağıdaki işlemler mevcuttur:

- **Çalışma Sayfasının Koşullu Biçimlendirmelerini Al** – Bir çalışma sayfasına uygulanan tüm koşullu biçimlendirme kurallarını alır.  
  - **Yöntem:** `GET`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Parametreler:** `fileName` (dize, gerekli), `sheetName` (dize, gerekli), `folder`, `storageName` gibi isteğe bağlı sorgu parametreleri  
  - **Örnek cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Koşullu Biçimlendirmeyi Al** – Tanımlayıcısına göre belirli bir koşullu biçimlendirme kuralını döndürür.  
  - **Yöntem:** `GET`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Parametreler:** `index` (tamsayı, gerekli) kuralın konumunu belirtir.  
  - **Örnek cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Biçim Koşulu İçin Hücre Alanı Ekle** – Belirtilen koşullu biçimi etkileyecek bir hücre aralığı ekler.  
  - **Yöntem:** `POST`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **İstek Gövdesi (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Örnek cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Biçim Koşulu İçin Koşul Ekle** – Mevcut bir biçim kuralı için yeni bir koşul (örneğin değer, formül) tanımlar.  
  - **Yöntem:** `POST`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **İstek Gövdesi (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Örnek cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Biçim Koşulu Ekle** – Türü ve stili dahil olmak üzere tam bir koşullu biçimlendirme kuralı oluşturur.  
  - **Yöntem:** `POST`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **İstek Gövdesi (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Örnek cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Tüm Koşul Biçimlendirmelerini Temizle** – Hedef çalışma sayfasından tüm koşullu biçimlendirme kurallarını kaldırır.  
  - **Yöntem:** `DELETE`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Örnek cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Koşullu Biçimlendirmeden Hücre Alanını Kaldır** – Bir koşullu biçimlendirme kuralından önceden tanımlanmış bir hücre alanını siler.  
  - **Yöntem:** `DELETE`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Örnek cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Koşullu Biçimlendirmeyi Kaldır** – Çalışma sayfasından tüm bir koşullu biçimlendirme kuralını siler.  
  - **Yöntem:** `DELETE`  
  - **Uç nokta:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Örnek cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Bu örnekler, her işlem için gerekli HTTP yöntemi, URL kalıbı, temel parametreler ve örnek istek yüklerini göstermektedir. Daha tercih ederseniz diline özel kod parçacıkları için uygun SDK’yı (C#, Java, Python vb.) kullanabilirsiniz.