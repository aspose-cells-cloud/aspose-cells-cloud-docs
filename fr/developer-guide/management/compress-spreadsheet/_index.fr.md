---
title: "API Web Aspose.Cells Cloud pour la compression Excel – Réduire la taille des fichiers de feuilles de calcul de manière programmée"
second_title: "Document"
ArticleTitle: "Comment compresser des fichiers Excel – Réduire la taille des feuilles de calcul et optimiser les performances"
linktype: "Compresser la feuille de calcul"
type: docs
url: /fr/compress-spreadsheet/
keywords: "compression Excel, Aspose.Cells Cloud, réduction de la taille des feuilles de calcul, API, optimisation du classeur"
description: "Découvrez comment compresser des classeurs Excel à l’aide de l’API Aspose.Cells Cloud. Obtenez des exemples détaillés pas à pas, les paramètres, l’authentification et les meilleures pratiques."
weight: 100
---

Comprimez de manière programmée des feuilles de calcul Excel et réduisez la taille des fichiers à l’aide de l’API Aspose.Cells Cloud. Optimisez les performances des classeurs en supprimant les données inutilisées, en compressant les objets intégrés et en nettoyant les formats. Cette API REST permet d’automatiser les workflows de compression et d’optimisation des fichiers Excel.

## **API de compression de feuille de calcul**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / requête / chaîne / corps HTTP) | Description                                                                                                                           |
| ---------------- | ------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                              | **Obligatoire.** Le fichier de classeur Excel source (`.xlsx`, `.xls`, etc.) à compresser.                                          |
| level            | Entier  | Requête                                               | **Facultatif.** Intensité de la compression (0 = plus rapide / plus faible, 9 = plus lent / plus forte). Si omis, une valeur par défaut équilibrée (5) est appliquée. |
| outPath          | Chaîne  | Requête                                               | **Facultatif.** Chemin du dossier de destination dans votre stockage cloud. Si omis, le fichier est enregistré dans le même dossier que le classeur source. |
| outStorageName   | Chaîne  | Requête                                               | **Obligatoire.** Identifiant du service de stockage cloud configuré (par exemple, `CorporateDrive`).                               |
| region           | Chaîne  | Requête                                               | **Facultatif.** Paramètre régional (par exemple, `de-DE`) pouvant influencer le traitement des données spécifiques à la région.     |
| password         | Chaîne  | Requête                                               | **Facultatif.** Mot de passe pour décrypter une feuille de calcul protégée. Laissez vide si le fichier n’est pas chiffré.          |

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

**Codes de statut HTTP**

| Code | Signification           | Description                                                         |
| ---- | ----------------------- | ------------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                     |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.                |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                         |

## Où utiliser l’API de compression de feuille de calcul ?

- **Distribution automatisée des rapports** – Comprimez les états financiers mensuels avant de les envoyer par e-mail afin de garantir la réussite de la livraison et d’améliorer l’expérience du destinataire.
- **Optimisation des fichiers téléchargés par les utilisateurs** – Compressez en arrière-plan les fichiers Excel téléchargés afin d’économiser de l’espace de stockage cloud et réduire les coûts de stockage.
- **Traitement et migration dans les pipelines de données** – Compressez les fichiers Excel intermédiaires générés lors des processus ETL pour accélérer les transferts réseau et diminuer la pression sur le stockage temporaire.

## Pourquoi utiliser l’API de compression de feuille de calcul ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide avec une documentation complète.
- **Réduction des coûts en main-d’œuvre** – Élimine la nécessité de personnel dédié pour consolider manuellement les documents.
- **Tarification à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels d’API effectués.
- **Aucune maintenance de serveur requise** – Aucun serveur à maintenir, aucune mise à jour logicielle à effectuer et aucune préoccupation liée à la compatibilité.

## Comment utiliser l’API de compression de feuille de calcul avec les SDK

### Spécification de l’API de compression de feuille de calcul

La [spécification de l’API de compression de feuille de calcul](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) fournit une interface accessible publiquement pour les interactions REST, permettant ainsi des appels directs à l’API depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de compresser une feuille de calcul en quelques lignes de code seulement. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}