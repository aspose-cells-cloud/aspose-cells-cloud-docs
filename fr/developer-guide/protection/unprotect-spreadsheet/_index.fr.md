---
title: "API Web Aspose.Cells Cloud pour déproteger Excel – Supprimer programmatically les mots de passe d’ouverture et de modification"
second_title: "Document"
ArticleTitle: "Supprimer la protection par mot de passe Excel – Déverrouiller instantanément les mots de passe d’ouverture et de modification"
linktitle: "Déproteger la feuille de calcul"
type: docs
url: /unprotect-spreadsheet/
keywords: "déprotection, feuille de calcul, Aspose.Cells, API, Excel, suppression de mot de passe"
description: "Supprimez les mots de passe d’ouverture et de modification des fichiers Excel de façon programmatique à l’aide de l’API Aspose.Cells Cloud de déprotection des feuilles de calcul. Prend en charge les formats .xlsx/.xls, l’authentification OAuth2 et le traitement par lots."
weight: 100
---

L’API de déprotection des feuilles de calcul supprime la protection par mot de passe d’ouverture et de modification des fichiers Excel en une seule appel. Elle convient parfaitement aux pipelines de données, aux systèmes de gestion de documents et aux flux de travail de migration.

## **API de déprotection des feuilles de calcul**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête**

| Nom du paramètre | Type   | Emplacement | Description                                                                                 |
| ---------------- | ------ | ----------- | ------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData    | Le fichier Excel à déproteger.                                                              |
| password         | Chaîne | Query       | Le mot de passe protégeant le fichier contre l’ouverture.                                  |
| modifyPassword   | Chaîne | Query       | Le mot de passe requis pour modifier le fichier (facultatif si seul un mot de passe d’ouverture est défini). |
| outPath          | Chaîne | Query       | (Facultatif) Chemin du dossier dans lequel le classeur déprotegé sera enregistré.         |
| outStorageName   | Chaîne | Query       | (Facultatif) Nom du stockage dans lequel le fichier de sortie sera écrit.                 |
| region           | Chaîne | Query       | (Facultatif) Paramètres régionaux de la feuille de calcul.                                 |

### **Réponse**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Une réponse réussie renvoie le fichier déprotegé sous forme de flux. Le fichier peut être enregistré à l’emplacement spécifié par `outPath`/`outStorageName`, ou récupéré directement depuis la charge utile de la réponse.

**Codes de statut HTTP**

| Code | Signification         | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte    | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.                     |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                            |

## Dans quel cas utiliser l’API de déprotection des feuilles de calcul ?

- **Restaurer l’accès aux classeurs verrouillés** – Supprimez rapidement les mots de passe d’ouverture ou de modification oubliés, sans intervention manuelle.
- **Automatiser le déverrouillage en masse** – Traitez un grand nombre de fichiers dans le cadre de projets de migration de données ou d’archivage.
- **Intégration aux flux de travail existants** – Combinez avec les API de stockage ou de conversion pour créer des pipelines complets (par exemple : téléchargement → déprotection → conversion en PDF).
- **Maintenir la sécurité des données** – L’opération s’effectue côté serveur, ce qui garantit la sécurité des fichiers d’origine, tandis que la version déprotegée est stockée dans votre stockage cloud.

## Comment utiliser l’API de déprotection des feuilles de calcul à l’aide des SDK

### **Spécification OpenAPI**

La [spécification de l’API de déprotection des feuilles de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) fournit une interface de programmation accessible publiquement pour faciliter les interactions REST directes depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment effectuer des appels à l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

### **Utiliser les SDK Aspose.Cells Cloud**

L’utilisation d’un SDK simplifie l’appel en gérant l’authentification, la construction de la requête et l’analyse de la réponse. Les SDK sont disponibles pour de nombreux langages et incluent des méthodes prêtes à l’emploi pour déproteger les feuilles de calcul.

Les exemples de code ci-dessous illustrent comment appeler l’API de déprotection des feuilles de calcul à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}