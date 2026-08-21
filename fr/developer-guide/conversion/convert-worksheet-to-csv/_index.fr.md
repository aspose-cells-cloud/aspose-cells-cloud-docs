---
title: "Convertir une feuille de calcul en CSV – Documentation de l'API Aspose.Cells Cloud"
second_title: "Document"
articleTitle: "Comment convertir une feuille de calcul de classeur en CSV à l’aide de l’API Aspose.Cells Cloud"
linktitle: "Convertir une feuille de calcul en CSV"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, conversion CSV, feuille de calcul vers CSV, API REST, classeur cloud, Excel vers CSV"
description: "Découvrez comment convertir une feuille de calcul spécifique d’un fichier Excel en CSV à l’aide de l’API Aspose.Cells Cloud (v4.0). Inclut l’endpoint, les paramètres, un exemple cURL, du code SDK et la gestion des erreurs."
weight: 100
---

L’endpoint **ConvertWorksheetToCsv** transforme une seule feuille de calcul d’un fichier de classeur local en document CSV entièrement sur le serveur Aspose.Cells Cloud. En téléchargeant le fichier source et en spécifiant la feuille cible, les développeurs reçoivent un flux binaire CSV sans avoir à stocker le fichier dans le stockage cloud. Cette API est idéale pour automatiser l’extraction de données, intégrer des données de classeurs dans des systèmes en aval et réduire la surcharge de stockage.

## API Convertir une feuille de calcul en CSV

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement | Obligatoire / Facultatif | Description                                                                                                                                 |
| :--------------- | :----- | :---------- | :----------------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData    | **Obligatoire**          | Fichier binaire du classeur source (par ex. `.xlsx`, `.xls`). Exemple : `myWorkbook.xlsx`.                                                  |
| worksheet        | Chaîne  | Query       | **Obligatoire**          | Nom de la feuille à convertir (sensible à la casse). Si omis, la première feuille est utilisée. Exemple : `Sheet1`.                        |
| outPath          | Chaîne  | Query       | Facultatif               | Chemin du dossier cible dans le stockage cloud où le CSV généré sera enregistré. Si omis, le CSV est renvoyé directement dans le flux de réponse. |
| outStorageName   | Chaîne  | Query       | Facultatif               | Nom du service de stockage (par ex. Azure, AWS S3) dans lequel le fichier de sortie doit être placé. Obligatoire uniquement si `outPath` est utilisé. |
| fontsLocation    | Chaîne  | Query       | Facultatif               | Chemin vers un dossier de polices personnalisé sur le serveur, permettant au moteur de conversion d’utiliser des polices non standards.      |
| region           | Chaîne  | Query       | Facultatif               | Identifiant de paramètres régionaux influençant le formatage des nombres et des dates dans le CSV (par ex. `en-US`, `fr-FR`).               |
| password         | Chaîne  | Query       | Facultatif               | Mot de passe pour ouvrir un classeur protégé. Doit correspondre au mot de passe de chiffrement du fichier source.                          |

### Réponse

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codes d’état HTTP**

| Code | Signification         | Description                                                     |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite.                      |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                     |

## Quand utiliser l’API Convertir une feuille de calcul en CSV ?

- **Extraction de données pour les pipelines BI** – Extraire une feuille spécifique d’un rapport Excel et alimenter directement le CSV résultant dans Power BI ou Tableau, sans traitement intermédiaire des fichiers.
- **Traitement automatisé des factures** – Convertir la feuille contenant les lignes de facture en CSV pour une importation rapide dans les systèmes comptables.
- **Intégration avec des systèmes hérités** – Exporter les données de la feuille en CSV pour une consommation par des applications plus anciennes qui n’acceptent que des fichiers texte délimités.
- **Génération de rapports à la demande** – Générer des instantanés CSV des données de classeurs en direct dans un service web, en renvoyant immédiatement le fichier au navigateur client.

## Pourquoi utiliser l’API Convertir une feuille de calcul en CSV ?

- **Aucun stockage cloud permanent requis** – Le fichier est transmis directement au moteur de conversion et supprimé après conversion, ce qui économise la bande passante et les coûts de stockage.
- **Exécution cloud à haute performance** – La conversion s’effectue sur les serveurs optimisés d’Aspose, généralement en moins de 2 secondes pour des fichiers allant jusqu’à 100 Mo.
- **Contrôle précis** – Sélectionner une seule feuille, appliquer des polices personnalisées, un formatage régional et une protection par mot de passe en une seule requête.
- **Sortie CSV cohérente multiplateforme** – Garantit une sortie CSV identique sur .NET, Java, Python et d’autres SDK utilisant le même endpoint REST.

## Comment utiliser l’API Convertir une feuille de calcul en CSV avec les SDK

### Spécification de l’API Convertir une feuille de calcul en CSV

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">spécification de l’API Convertir une feuille de calcul en CSV</a> fournit une interface de programmation publiquement accessible permettant d’exécuter des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier optionnel"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation du SDK simplifie le développement en masquant les détails de bas niveau, vous permettant d’intégrer un classeur dans un autre à l’aide d’un code concis. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}