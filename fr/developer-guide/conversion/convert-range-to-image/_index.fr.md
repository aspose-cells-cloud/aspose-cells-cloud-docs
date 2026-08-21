---
title: "Convertir une plage Excel en image – Aspose.Cells Cloud API"
description: "Convertissez une plage spécifique d’un fichier Excel local en PNG, JPEG, SVG, TIFF ou BMP via l’API REST Aspose.Cells Cloud – aucune upload du classeur complet n’est requise."
keywords: "Aspose.Cells Cloud, convertir une plage en image, API Excel, formats d’image, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

L’appel lit un fichier de feuille de calcul local, convertit la plage spécifiée et renvoie l’image sous forme de flux binaire.

## Méthode de conversion d’une plage en image

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## Paramètres de la requête

| Nom                 | Emplacement                          | Type    | Obligatoire | Description                                                                     |
| ------------------- | ------------------------------------ | ------- | ----------- | ------------------------------------------------------------------------------- |
| **Spreadsheet**     | Données de formulaire (`multipart/form-data`) | Fichier | **Oui**     | Le fichier Excel à traiter.                                                     |
| **worksheet**       | Requête (query)                      | Chaîne  | **Oui**     | Nom de la feuille contenant la plage (par exemple, `Feuil1`).                  |
| **range**           | Requête (query)                      | Chaîne  | **Oui**     | Zone de cellules à convertir, par exemple `A1:C10`.                            |
| **format**          | Requête (query)                      | Chaîne  | **Oui**     | Format d’image de sortie (`png`, `jpeg`, `svg`, `tiff`, `bmp`).               |
| **printHeadings**   | Requête (query)                      | Booléen | Non         | `true` pour inclure les titres de lignes/colonnes dans l’image.               |
| **outPath**         | Requête (query)                      | Chaîne  | Non         | Chemin du dossier pour le fichier généré si vous souhaitez le stocker dans le stockage cloud. |
| **outStorageName**  | Requête (query)                      | Chaîne  | Non         | Nom du service de stockage (par exemple, `MyStorage`).                         |
| **fontsLocation**   | Requête (query)                      | Chaîne  | Non         | URL ou chemin vers les polices personnalisées utilisées lors de la conversion.|
| **region**          | Requête (query)                      | Chaîne  | Non         | Identifiant de paramètres régionaux (par exemple, `en-US`, `fr-FR`). Affecte le format des nombres et des dates. |
| **password**        | Requête (query)                      | Chaîne  | Non         | Mot de passe pour les classeurs chiffrés.                                      |
| **AutoRowsFit**     | Requête (query)                      | Booléen | Non         | Ajustement automatique des lignes avant le rendu.                              |
| **AutoColumnsFit**  | Requête (query)                      | Booléen | Non         | Ajustement automatique des colonnes avant le rendu.                            |

## Réponse

L’API renvoie le fichier HTML converti sous forme de **flux binaire** (`application/octet-stream`).

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

### Exemple de réponse réussie (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Enregistrez le corps de la réponse dans un fichier (par exemple, `report.png`) pour visualiser l’image rendue dans un navigateur.

---

**Codes de statut HTTP**

| Code | Signification        | Description                                                       |
| ---- | -------------------- | ----------------------------------------------------------------- |
| 200  | OK                   | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête     | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé         | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop grande | Le fichier téléchargé dépasse la limite de taille.             |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur.                                   |

## Comment utiliser l’API de conversion d’une plage en image avec les SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) décrit une API publiquement accessible, permettant des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Feuil1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant de convertir une plage de données en fichier image avec un code minimal.  
Consultez la liste complète des SDK Aspose.Cells Cloud sur notre [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK. Si le chargement à partir de Gist est bloqué, vous pouvez télécharger directement les exemples depuis le dépôt.