---
title: "Excel vers PNG"
second_title: "Document"
linktitle: "Excel vers PNG"
type: docs
url: /fr/frconvert-excel-file-to-png-file/
keywords: "Excel vers PNG, Aspose.Cells Cloud, API REST, conversion de feuilles de calcul, format PNG"
description: "Convertissez des feuilles de calcul Excel en images PNG à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge plusieurs SDK et fournit des exemples détaillés pour divers langages de programmation."
weight: 90
---

Cette API REST convertit un fichier de feuille de calcul au format PNG.

## Spécification de l’API REST

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètre de requête**

| Nom du paramètre      | Type   | Description                                                                                  |
| --------------------- | ------ | -------------------------------------------------------------------------------------------- |
| password              | string | Le mot de passe requis pour ouvrir le fichier Excel.                                        |
| storageName           | string | Le nom du stockage où le fichier est situé.                                                 |
| checkExcelRestriction | bool   | Détermine s’il faut vérifier les restrictions des fichiers Excel lors de la modification des cellules ou des objets associés. |

### **Paramètre du corps de la demande**

| Nom du paramètre | Type      | Description                                                               |
| ---------------- | --------- | ------------------------------------------------------------------------- |
| datafile         | fichier de données | Le fichier de feuille de calcul inclus dans la première partie de la demande multipart. |

### **Réponse**

L’API renvoie un objet **FileInfo** contenant le fichier PNG généré.

| Champ           | Type   | Description                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Nom du fichier PNG (par ex., `exemple.png`). |
| **FileSize**    | int    | Taille du fichier en octets.                  |
| **FileContent** | string | Contenu du fichier PNG encodé en Base64.      |

[FileInfo](/cells/file-info/)

**Codes de statut HTTP**

| Code | Signification               | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT non valide ou manquant. |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur. |

## Comment utiliser l’API PostConvertWorkbookToPNG avec les SDK

### Spécification de l’API PostConvertWorkbookToPNG

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "Contenu du fichier : chaîne_encodée_en_base64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau afin que vous puissiez vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Autres API implémentant des fonctions similaires

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Enregistre un fichier Excel en tant que CSV (ou autres formats) avec des paramètres supplémentaires et stocke le résultat.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Convertit un fichier Excel en CSV (ou autres formats) avec des paramètres optionnels et renvoie le résultat dans la réponse.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Récupère un fichier Excel et peut le convertir en CSV (ou autres formats) à la volée.

---