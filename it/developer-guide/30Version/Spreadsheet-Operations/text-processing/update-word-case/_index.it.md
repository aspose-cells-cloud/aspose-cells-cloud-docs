---
title: "Aspose.Cells – API Aggiorna Maiuscole/Minuscole Parole"
second_title: "Documentazione"
linktype: "Maiuscole/Minuscole Parole"
type: docs
url: /it/post-update-word-case/
keywords: "Aspose.Cells, API Aggiorna Maiuscole/Minuscole Parole, conversione maiuscole/minuscole testo, Excel, CSV, Google Fogli, API REST"
description: "Converti la maiuscola/minuscola del testo nei file Excel, CSV o Google Fogli con l'API Aggiorna Maiuscole/Minuscole Parole di Aspose.Cells Cloud. Supporta maiuscolo/minuscolo, maiuscole iniziali parole e capitalizzazione prima lettera."
weight: 100
ArticleTitle: "Aspose.Cells – Documentazione API Aggiorna Maiuscole/Minuscole Parole"
---

**Versione API:** 3.0

Gestire la mancanza di coerenza nella maiuscola/minuscola del testo nei fogli di calcolo (Excel, Google Fogli, CSV) può essere frustrante, soprattutto con grandi set di dati. L'**API web PostUpdateWordCase** automatizza le conversioni della maiuscola/minuscola, garantendo dati puliti e standardizzati con il minimo sforzo.


## **API Web Excel – API Aggiorna Maiuscole/Minuscole Parole**

```http
POST https://api.aspose.cloud/v3.0/cells/updatewordcase
```
### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Descrizione della funzione**

L'API web PostUpdateWordCase affronta il comune problema della mancanza di coerenza nella maiuscola/minuscola nei fogli di calcolo, che può influenzare significativamente l'analisi e la elaborazione dei dati. Questa API automatizza la conversione della maiuscola/minuscola, garantendo che i tuoi dati siano puliti, standardizzati e pronti per ulteriori manipolazioni o analisi.

- **Conversione automatica della maiuscola/minuscola**
  - **Maiuscolo in Minuscolo** – Converte tutte le lettere maiuscole in minuscole.
  - **Minuscolo in Maiuscolo** – Converte tutte le lettere minuscole in maiuscole.
  - **Prima lettera maiuscola** – Capitalizza la prima lettera di ogni parola.
  - **Maiuscole Iniziali Parole (Title Case)** – Converte il testo in maiuscole iniziali parole, dove la prima lettera di ogni parola principale viene capitalizzata.

- **Supporto per più formati** – L'API funziona con una vasta gamma di formati di fogli di calcolo, inclusi Excel, OpenOffice, JSON, CSV e altri. Questa versatilità la rende adatta a diverse esigenze di elaborazione dati.

### **Parametri della richiesta**

| Nome Parametro    | Tipo   | Posizione     | Descrizione                                                                                                               |
| ----------------- | ------ | ------------- | ------------------------------------------------------------------------------------------------------------------------- |
| `wordCaseOptions` | oggetto | Corpo richiesta | Opzioni che definiscono la trasformazione della maiuscola/minuscola desiderata, come l'intervallo di origine, il tipo di maiuscola/minuscola target e impostazioni aggiuntive. |

**Schema `wordCaseOptions`**

```json
{
  "Range": "A1:B10", // Intervallo in stile Excel da elaborare (obbligatorio)
  "CaseType": "Upper", // Enumerazione: Upper, Lower, Capitalize, Title (obbligatorio)
  "IgnoreBlank": true // Booleano, opzionale – quando true, le celle vuote rimangono invariate
}
```

**Esempio di corpo della richiesta**

```json
{
  "Range": "A1:B10",
  "CaseType": "Upper",
  "IgnoreBlank": true
}
```

- **Range** – L'intervallo di celle a cui verrà applicata la conversione della maiuscola/minuscola (es. `A1:C5`).
- **CaseType** – Il tipo di conversione della maiuscola/minuscola. I valori ammessi sono `Upper`, `Lower`, `Capitalize` e `Title`.
- **IgnoreBlank** – Se `true`, le celle vuote vengono ignorate; il valore predefinito è `false`.

### **Risposta**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[nome file unito]",
    "Filesize" : [dimensione file],
    "FileContent" : "[Base64String]"
}
```

- **Filename** – Nome del file elaborato.
- **FileSize** – Dimensione del file in byte.
- **FileContent** – Contenuto del file trasformato, codificato in Base64.

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | File caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto del server. |

## Come utilizzare l'API PostUpdateWordCase con gli SDK

### Specifica dell'API PostUpdateWordCase

La <a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostUpdateWordCase" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_PostUpdateWordCase.cs" >}}
{{</ tab>}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_PostUpdateWordCase.java" >}}
{{</ tab>}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_PostUpdateWordCase.php" >}}
{{</ tab>}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_PostUpdateWordCase.rb" >}}
{{</ tab>}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_PostUpdateWordCase.ts" >}}
{{</ tab>}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_PostUpdateWordCase.py" >}}
{{</ tab>}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_PostUpdateWordCase.pl" >}}
{{</ tab>}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_PostUpdateWordCase.go" >}}
{{</ tab>}}
{{</ tabs >}}
---