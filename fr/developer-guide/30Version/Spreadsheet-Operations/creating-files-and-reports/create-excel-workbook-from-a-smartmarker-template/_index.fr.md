---
title: "Créer des rapports Excel avec des modèles Smart Marker"
second_title: "Document"
linktitle: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Classeur, SDK, API, Génération de rapports"
description: "Découvrez comment générer des classeurs Excel à partir de modèles Smart Marker à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête/réponse, un exemple cURL, les conditions préalables, des notes et des exemples de code SDK."
weight: 40
ArticleTitle: "Créer des rapports Excel avec des modèles Smart Marker – Guide de l’API Aspose.Cells Cloud"
---

Cette API REST permet de créer un classeur à partir d’un modèle Smart Marker.

## API SmartMarker pour les classeurs

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification par jeton JWT</a>.

### **Qu’est-ce qu’un Smart Marker ?**

Un Smart Marker est une syntaxe de placeholder qui fait correspondre des champs de données d’un fichier XML (ou JSON) à des cellules d’un modèle Excel. À l’exécution, Aspose.Cells remplace les marqueurs par les données correspondantes, ce qui permet de générer des rapports entièrement remplis de manière programmatique.

### **Paramètres de requête**

| Nom du paramètre | Type   | Description                                                  |
| ---------------- | ------ | ------------------------------------------------------------ |
| outPath          | string | Chemin de destination où le classeur généré sera enregistré. |
| folder           | string | Dossier contenant le classeur original.                      |
| storageName      | string | Nom du service de stockage à utiliser.                       |

### **Paramètre du corps de la requête**

| Nom du paramètre | Type | Description                                           |
| ---------------- | ---- | ----------------------------------------------------- |
| xmlFile          | file | Fichier de données XML Smart Marker envoyé avec la requête. |

### **Réponse**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Notes / Limites :**  
- L’API prend en charge les fichiers Excel d’une taille maximale de **50 Mo**.  
- Les formats acceptés sont uniquement **.xlsx**, **.xlsm** et **.xlsb**.  
- Une limite de débit de **20 requêtes par seconde** par compte est appliquée.

**Codes de statut HTTP**

| Code | Signification               | Description                                                    |
| ---- | --------------------------- | -------------------------------------------------------------- |
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                     |

## Comment utiliser l’API SmartMarker pour les classeurs

### Spécification de l’API SmartMarker pour les classeurs

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

**Exemple rapide en une seule ligne**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Gestion des erreurs**

| Code d’état HTTP | Description           | Cause typique                                              |
| ---------------- | --------------------- | ---------------------------------------------------------- |
| 400              | Mauvaise requête      | Modèle manquant, XML mal formé ou paramètres invalides.   |
| 401              | Non autorisé          | Jeton d’authentification invalide ou manquant.             |
| 404              | Non trouvé            | Le classeur ou l’emplacement de stockage spécifié n’existe pas. |
| 500              | Erreur interne du serveur | Échec serveur inattendu.                                  |

**Exemple de réponse d’erreur (400)**

```json
{
  "Code": 400,
  "Message": "Le fichier de données XML est manquant ou mal formé."
}
```

## Famille de SDK Cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}