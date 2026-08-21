---
title: "Aspose.Cells Cloud Web API – Convertir une feuille de calcul en PDF"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul locale en PDF à l’aide de l’API Aspose.Cells Cloud"
linktitle: "Convertir une feuille de calcul en PDF"
type: docs
url: /convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, feuille de calcul en PDF, conversion Excel, API cloud, génération PDF, API REST, v4.0"
description: "Guide étape par étape pour convertir une feuille de calcul locale en PDF à l’aide de l’API Aspose.Cells Cloud. Inclut la syntaxe de la requête, les paramètres, les détails de la réponse, la gestion des erreurs et des cas d’utilisation pratiques."
weight: 100
---

Le point de terminaison **ConvertSpreadsheetToPdf** lit un fichier de feuille de calcul téléchargé depuis un lecteur local, le traite sur le serveur Aspose.Cells Cloud, puis renvoie le document PDF résultant sous forme de flux binaire. Cette conversion native cloud élimine la nécessité de télécharger le fichier source vers le stockage, réduit la consommation des ressources et simplifie les flux de travail en restituant directement le PDF au client. Les formats pris en charge dépendent des bibliothèques sous-jacentes ; l’API valide l’existence du fichier, les permissions et l’intégrité de la conversion, lançant les erreurs HTTP appropriées en cas d’entrée invalide ou d’échec du traitement.

## **API Convert Spreadsheet To Pdf**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligatoire/Optionnel | Description                                                                                                                                                                                    |
| :--------------- | :----- | :---------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData    | Obligatoire          | Le fichier source de la feuille de calcul (XLS, XLSX, CSV, etc.) à convertir. Doit être un fichier valide et lisible ; la taille maximale est de 100 Mo. Exemple : `monClasseur.xlsx`.        |
| outPath          | Chaîne  | Query       | Optionnel            | Chemin du dossier de destination où le PDF converti sera stocké sur le serveur (si vous souhaitez le conserver). Si omis, le fichier est renvoyé directement dans la réponse. Exemple : `/output/reports/`. |
| outStorageName   | Chaîne  | Query       | Optionnel            | Nom du service de stockage cible (par exemple, `MonStockageCloud`). Obligatoire uniquement si `outPath` est utilisé et que le stockage n’est pas celui par défaut.                           |
| fontsLocation    | Chaîne  | Query       | Optionnel            | Chemin vers un dossier personnalisé de polices sur le serveur afin d’assurer un rendu correct du texte dans le PDF. Exemple : `/polices/personnalisees/`.                                      |
| region           | Chaîne  | Query       | Optionnel            | Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et les comportements spécifiques à la localisation. |
| password         | Chaîne  | Query       | Optionnel            | Mot de passe requis pour ouvrir une feuille de calcul protégée. À omettre si le fichier n’est pas chiffré.                                                                                    |

### **Réponse**

Réponse réussie (200 OK)  
Content-Type : application/pdf  
Content-Disposition : attachment; filename="converti.pdf"  
Content-Length : `<taille en octets>`

Corps : flux binaire du fichier PDF généré

**Codes de statut HTTP**

| Code | Signification           | Description                                                      |
| ---- | ----------------------- | ---------------------------------------------------------------- |
| 200  | OK                      | Conversion effectuée avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                    |

## Où utiliser l’API Convert Spreadsheet To Pdf ?

- **Canal automatisé de production de rapports** – Convertir des rapports Excel générés quotidiennement en PDF pour archivage ou distribution par courriel, sans intervention manuelle.
- **Systèmes de gestion documentaire (DMS)** – Stocker directement les PDF dans un DMS après conversion, en ne conservant la feuille de calcul d’origine que côté client.
- **Applications web avec export dynamique** – Permettre aux utilisateurs finaux de télécharger une version PDF d’une feuille de calcul qu’ils modifient dans leur navigateur, en exploitant la conversion cloud pour préserver la mise en page.
- **Conformité réglementaire** – Générer des instantanés PDF immuables de feuilles de calcul financières pour les traces d’audit, en garantissant que le fichier source ne quitte jamais l’environnement client.
- **Flux de travail de conversion multi-format** – Combiner avec d’autres points de terminaison de conversion, tels que l’API [Convert Spreadsheet to CSV](/convert-spreadsheet-to-csv/) pour créer des archives multi-format.

## Pourquoi utiliser l’API Convert Spreadsheet To Pdf ?

- **Flux de travail sans téléchargement vers le cloud** – Aucune nécessité de télécharger le fichier source vers un stockage cloud ; la conversion a lieu directement depuis le flux téléchargé, économisant bande passante et coûts de stockage.
- **Rendu haute fidélité** – Aspose.Cells préserve les formules complexes, les graphiques et la mise en forme lors de la conversion en PDF, correspondant à la sortie d’Excel sur ordinateur.
- **Exécution cloud évolutif** – Exploite l’infrastructure cloud d’Aspose pour une conversion rapide et fiable, indépendamment du matériel client.
- **Interface REST simple** – Une seule requête `PUT` avec des paramètres de requête optionnels ; renvoie un flux PDF prêt au téléchargement, facilitant l’intégration dans n’importe quel langage.

## Comment utiliser l’API Convert Spreadsheet To Pdf avec les SDK ?

### Spécification de l’API Convert Spreadsheet To Pdf

La [Spécification de l’API Convert Spreadsheet To Pdf](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf) fournit une interface de programmation accessible publiquement pour exécuter directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converti.pdf
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de fusionner une feuille de calcul dans une autre via un code concis. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Aspose.Cells Cloud. Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}