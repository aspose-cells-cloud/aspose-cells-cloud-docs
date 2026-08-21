---
title: "Crittografare un libro Excel con l'API Aspose.Cells Cloud – Esempi rapidi cURL e SDK"
second_title: "Documento"
linktype: "Crittografare un file Excel"
type: docs
url: /excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Aspose Cells crittografa libro, API di crittografia Excel, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Scopri come crittografare un libro Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include comando cURL, esempi di codice SDK (C#, Java, Python, …), parametri richiesti e gestione degli errori."
weight: 20
ArticleTitle: "Crittografare un libro Excel con l'API Aspose.Cells Cloud – Esempi cURL e SDK"
---

Questa REST API crittografa un **libro** Excel.

**Prerequisiti:** È necessario disporre di un token JWT valido e del libro caricato in una posizione di archiviazione prima di chiamare questo endpoint.

## API PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della query**

| Nome Parametro | Tipo   | Obbligatorio | Descrizione                                      |
| -------------- | ------ | ------------ | ------------------------------------------------ |
| folder         | string | ✗            | Percorso della cartella del libro originale.    |
| storageName    | string | ✗            | Nome dell'archiviazione da utilizzare.          |

### **Parametro del corpo della richiesta**

| Nome Parametro | Tipo                      | Obbligatorio | Descrizione                            |
| -------------- | ------------------------- | ------------ | -------------------------------------- |
| encryption     | WorkbookEncryptionRequest | ✓            | Impostazioni di crittografia del libro. |

#### **WorkbookEncryptionRequest**

| Nome Parametro | Tipo    | Obbligatorio | Descrizione                                                                           |
| -------------- | ------- | ------------ | ------------------------------------------------------------------------------------- |
| EncryptionType | string  | ✓            | Algoritmo di crittografia. Vedere la tabella sottostante per i valori supportati.    |
| KeyLength      | integer | ✗            | Lunghezza della chiave di crittografia in bit (ignorata per `XOR` e `Compatible`).   |
| Password       | string  | ✓            | Password utilizzata per la crittografia.                                              |

#### **Valori di EncryptionType**

| Valore                            | Descrizione                                          |
| --------------------------------- | ---------------------------------------------------- |
| `XOR`                             | Algoritmo XOR semplice (obsoleto, bassa sicurezza). |
| `Compatible`                      | Crittografia compatibile con Excel 97‑2003 (40‑bit).|
| `EnhancedCryptographicProviderV1` | AES‑128 con hash SHA‑1.                              |
| `StrongCryptographicProvider`     | AES‑256 con hash SHA‑512 (più sicura).              |

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato              | Descrizione                                                           |
|--------|--------------------------|-----------------------------------------------------------------------|
| 200    | OK                       | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida     | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato          | Token JWT non valido o mancante.                                      |
| 413    | Payload troppo grande    | Il file caricato supera il limite di dimensione.                     |
| 500    | Errore interno del server| Errore imprevisto del server.                                         |

## Come utilizzare l'API PostEncryptDocument con gli SDK

### Specifica dell'API PostEncryptDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando **cURL** per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare una chiamata all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
# Crittografa il libro "test.xlsx" usando l'algoritmo XOR (chiave 128‑bit) e la password "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Possibili risposte di errore**

| Stato HTTP | Codice                | Messaggio                                             |
| ---------- | --------------------- | ----------------------------------------------------- |
| 400        | BadRequest            | Parametri mancanti o non validi.                      |
| 401        | Unauthorized          | Token di autenticazione assente o non valido.         |
| 403        | Forbidden             | Autorizzazioni insufficienti per accedere all'archiviazione. |
| 500        | InternalServerError   | Errore imprevisto del server.                         |

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}