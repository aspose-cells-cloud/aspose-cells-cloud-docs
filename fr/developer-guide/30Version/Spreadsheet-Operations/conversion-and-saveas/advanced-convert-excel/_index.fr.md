---
title: "Conversion avancée de fichier Excel"
second_title: "Document"
linktitle: "Conversion avancée"
type: docs
url: /fr/advanced-convert-excel/
keywords: "Aspose.Cells, conversion Excel, API cloud, SDK"
description: "L'API REST Aspose.Cells Cloud offre des fonctionnalités puissantes pour convertir des classeurs Excel vers de nombreux formats, configurer la mise en page, les options d'enregistrement et les paramètres d'impression. Des SDK sont disponibles pour Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift, permettant une intégration fluide sur plusieurs plateformes."
weight: 50
ArticleTitle: "Conversion avancée de fichier Excel – Guide de l’API Aspose.Cells Cloud"
---

## API cloud avancée pour la conversion Excel

L'opération de conversion avancée vous permet de transformer un classeur Excel en divers formats de sortie (PDF, HTML, CSV, etc.), tout en vous offrant un contrôle précis sur la mise en page, les options d’enregistrement et les paramètres d’impression.

**Prérequis / Authentification**  
Pour utiliser ce point de terminaison, vous devez obtenir un jeton d’accès auprès d’Aspose.Cells Cloud et l’inclure dans l’en-tête `Authorization` sous forme de jeton Bearer.

**Référence de l’API**  
- **Méthode :** `PUT`  
- **Point de terminaison :** `/cells/convert`  
- **Paramètres :**  
  - `format` (chaîne de caractères, obligatoire) – Format de sortie souhaité (par exemple, `pdf`, `html`).  
  - `outPath` (chaîne de caractères, optionnel) – Chemin dans le stockage cloud où le fichier converti sera enregistré.  
  - `options` (objet, optionnel) – Objet JSON contenant des options avancées de conversion telles que `pageSetup`, `saveOptions` et `printSettings`.  
- **Exemple de corps de requête :**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Réponse :**  
  - `200 OK` – La conversion a réussi ; la réponse contient le flux du fichier converti ou une référence vers le fichier enregistré.  
  - `400 Bad Request` – Paramètres invalides ou corps de requête mal formé.  
  - `401 Unauthorized` – Échec de l’authentification ou jeton manquant.  
  - `500 Internal Server Error` – Erreur côté serveur pendant la conversion.  

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT invalide ou manquant. |
| 413  | Payload Too Large           | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Internal Server Error       | Erreur serveur inattendue. |

**Remarques**  
* Certains formats de sortie présentent des limitations spécifiques (par exemple, la conversion HTML ne préserve pas les macros). Consultez la documentation spécifique à chaque format pour plus de détails.

### Possibilité de charger des fichiers de feuille de calcul à partir de multiples sources de données

### Définir la mise en page et les options d’enregistrement

## Famille de SDK cloud

L'utilisation d’un SDK accélère le développement en gérant les détails de bas niveau, ce qui vous permet de vous concentrer sur les tâches de votre projet. Consultez le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Conversion avancée",
  "description":"Convertir un classeur Excel en PDF/HTML/CSV avec des options avancées.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Format de sortie souhaité (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>