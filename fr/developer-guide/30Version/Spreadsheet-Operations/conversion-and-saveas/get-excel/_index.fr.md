---
title: "Aspose.Cells Cloud – Convertir un classeur Excel en PDF, CSV, HTML et plus (GET /cells/{name})"
second_title: "Document"
linktitle: "Convertir Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, conversion Excel, convertir Excel, PDF, CSV, HTML, ODS, JSON, formats d’image, exportation de feuilles de calcul, API, REST"
description: "Découvrez comment récupérer un classeur Excel dans n’importe quel format (PDF, CSV, HTML, PNG, etc.) à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL, des SDK, l’authentification et les détails de la réponse."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Convertir un classeur Excel en PDF, CSV, HTML et plus (GET /cells/{name})"
---

Cette API REST permet de récupérer un classeur Excel dans un format différent.

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de requête**

| Nom du paramètre      | Type   | Description                                                                                                                                                          | Valeur par défaut |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| format                | string | Format cible du fichier (par ex., CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.). | –                 |
| password              | string | Mot de passe requis pour ouvrir le fichier Excel.                                                                                                                   | –                 |
| isAutoFit             | bool   | Ajuste automatiquement la largeur des lignes et des colonnes.                                                                                                        | false             |
| onlySaveTable         | bool   | Si **true**, seules les données du tableau sont enregistrées. Accepte `true` ou `false`.                                                                            | false             |
| outPath               | string | Chemin d’enregistrement du résultat. Pour un fichier unique, inclure le nom du fichier et son extension ; pour plusieurs fichiers, spécifier uniquement le dossier.    | –                 |
| outStorageName        | string | Nom du stockage dans lequel le fichier de sortie sera enregistré.                                                                                                   | –                 |
| checkExcelRestriction | bool   | Vérifie les restrictions Excel lors de la modification des cellules ou des objets associés.                                                                        | false             |
| region                | string | Paramètres régionaux appliqués au classeur.                                                                                                                         | –                 |
| pageWideFitOnPerSheet | bool   | Ajuste la largeur de page à chaque feuille de calcul lors de la conversion en PDF.                                                                                 | false             |
| pageTallFitOnPerSheet | bool   | Ajuste la hauteur de page à chaque feuille de calcul lors de la conversion en PDF.                                                                                 | false             |
| onePagePerSheet       | bool   | Génère une page PDF par feuille de calcul.                                                                                                                          | false             |
| folder                | string | Chemin du dossier contenant le classeur original.                                                                                                                   | –                 |
| storageName           | string | Nom du stockage où se trouve le fichier source.                                                                                                                     | –                 |

### Réponse

**Succès (200)**

- L’API renvoie un objet **[Workbook](/cells/workbook/)** contenant des informations sur la structure du classeur si le paramètre de requête `format` est omis.

- L’API renvoie le fichier converti dans le format demandé si le paramètre de requête `format` spécifie un type de fichier.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(données binaires PDF)
```

**Codes de statut HTTP**

| Code | Signification               | Description                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou invalides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                             |
| 413  | Charge utile trop grande     | Le fichier envoyé dépasse la limite de taille.                             |
| 500  | Erreur interne du serveur    | Erreur serveur inattendue.                                                  |

> **Notes :**  
> - Les grands classeurs peuvent nécessiter plus de temps pour être convertis ; envisagez d’augmenter le délai d’expiration de la requête.  
> - Certains formats (par ex., `ODS`) ne sont pas pris en charge pour certaines fonctionnalités Excel, telles que les macros.

## Comment utiliser l’API GetWorkBook avec les SDK

> **Prérequis :**  
> - Un **jeton d’accès JWT** valide obtenu via le flux d’authentification Aspose.Cells.  
> - Le classeur source doit être stocké dans un stockage pris en charge par Aspose ou être fourni directement dans la requête.  
> - Assurez-vous que la version de l’API (`v3.0`) correspond à la version la plus récente publiée.

### Spécification de l’API GetWorkBook

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

### Exemple de requête

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder aux services web Aspose.Cells. L’exemple ci-dessous illustre une requête GET correcte avec l’en-tête d’autorisation requis.

{{< tabs tabTotal="1" tabID="11" tabName11="Requête" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK constitue la méthode la plus rapide pour développer. Un SDK masque les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Voir aussi**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Convertir un classeur (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Enregistrer sous (GET)</a>

---

_Dernière mise à jour : 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Convertir un classeur Excel en PDF, CSV, HTML et plus (GET /cells/{name})",
  "description": "Documentation relative à l’endpoint GET /cells/{name} d’Aspose.Cells Cloud, permettant de convertir des classeurs Excel en divers formats tels que PDF, CSV, HTML, etc.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, conversion Excel, PDF, CSV, HTML, API, REST, cloud",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>