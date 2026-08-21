---
title: "Proteggi file Excel"
second_title: "Documenti"
linktype: "Crittografa file Excel"
type: docs
url: /it/protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, API per la protezione Excel, crittografia cartella di lavoro Excel, sicurezza foglio elettronico cloud, API REST"
description: "Utilizza l'API REST Aspose.Cells Cloud per proteggere i file Excel. Questa guida mostra come crittografare le cartelle di lavoro tramite HTTP POST, cURL e SDK per diversi linguaggi di programmazione, aggiornata al 2026."
weight: 40
---

Questa API REST protegge i file Excel.

## API REST

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Sicurezza e autenticazione

Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Parametri della richiesta

| Nome parametro | Tipo   | Posizione                  | Descrizione                             |
| -------------- | ------ | ------------------------- | --------------------------------------- |
| file           | file   | formData (body)           | File da caricare                        |
| password       | string | stringa di query (`password`) | Password utilizzata per proteggere la cartella di lavoro |

### Risposta

```json
{
  "Status": "OK",
  "Code": 200,
  "Files": [
    {
      "Filename": "nome file protetto: smaple1.xlsx",
      "FileSize": dimensione,
      "FileContent": "-----Stringa Base64 di sample1-----"
    },
    {
      "Filename": "nome file protetto: sample2.xlsx",
      "FileSize": dimensione,
      "FileContent": "-----Stringa Base64 di sample2-----"
    }
  ]
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                         |
|--------|-----------------------------|---------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto sul server. |

## Come utilizzare l'API PostProtect con gli SDK

### Specifica dell'API PostProtect

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Stringa Base64 di sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Stringa Base64 di sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Gestione degli errori**

– L'API può restituire i seguenti codici di stato:

| Codice HTTP | Significato                                    | Esempio di payload JSON di errore                    |
|-------------|-----------------------------------------------|------------------------------------------------------|
| 400         | Richiesta non valida (ad esempio, file mancante) | `{"Code":400,"Message":"Il file è obbligatorio."}`   |
| 401         | Non autorizzato (token non valido o mancante)   | `{"Code":401,"Message":"Token di accesso non valido."}` |
| 403         | Accesso negato (permessi insufficienti)         | `{"Code":403,"Message":"Accesso negato."}`           |
| 500         | Errore interno del server                       | `{"Code":500,"Message":"Errore imprevisto del server."}` |

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}