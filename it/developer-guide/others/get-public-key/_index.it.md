---
title: Aspose.Cells Cloud WEb API - Ottieni Public Ke
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Ottieni Ke pubblico
type: docs
url: /it/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Recupera una chiave pubblica asimmetrica per la crittografia sicura dei dati
weight: 100
kwords: crittografia asimmetrica, chiave pubblica, REST API, Excel API, sicurezza, crittografia dei dati, integrazione API, JSON, documentazione API
---
Recupera la chiave pubblica da un algoritmo di crittografia asimmetrica.

## **Ottieni la chiave pubblica API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|||||

### **Risposta**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## Come utilizzare la chiave pubblica Get API con gli SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente dal browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice l'acquisizione della chiave pubblica per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:
