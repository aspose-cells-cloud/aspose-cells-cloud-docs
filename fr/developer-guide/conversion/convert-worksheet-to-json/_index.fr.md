---
title: "Aspose.Cells Cloud Web API – Convertir une feuille de calcul en JSON"
second_title: "Document"
ArticleTitle: "Comment convertir une feuille de calcul de classeur en JSON à l'aide de l'API Aspose.Cells Cloud"
linktitle: "Convertir une feuille de calcul en JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, feuille de calcul vers JSON, conversion Excel, API cloud, API v4, export de données"
description: "Guide pas à pas pour convertir une feuille de calcul Excel en JSON à l'aide de l'API Aspose.Cells Cloud, incluant les paramètres de requête, la gestion des réponses, les codes d'erreur et des exemples de SDK."
weight: 100
---

Le point de terminaison **ConvertWorksheetToJson** lit un fichier de classeur à partir du système de fichiers local, extrait la feuille de calcul spécifiée, et renvoie son contenu sous forme de fichier JSON. La conversion est entièrement effectuée sur les serveurs Aspose.Cells Cloud, ce qui élimine la nécessité de télécharger ou stocker préalablement les fichiers. Cette solution prend en charge les classeurs protégés par mot de passe, les emplacements personnalisés de polices de caractères et les paramètres régionaux, offrant ainsi une solution rapide et native cloud pour exporter des données de feuille de calcul au format JSON, en vue d’un traitement ultérieur.

## **API Convertir une feuille de calcul en JSON**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligatoire / Facultatif | Description                                                                                                                                                                                            |
| :--------------- | :----- | :---------- | :----------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | file   | FormData    | Obligatoire              | Le classeur Excel à traiter. Doit être au format pris en charge (xls, xlsx, csv, etc.). Envoyé en tant que multipart/form-data. Exemple : `Spreadsheet=@C:\Docs\Exemple.xlsx`.                       |
| worksheet        | string | Query       | Obligatoire              | Nom exact de la feuille de calcul à convertir (sensible à la casse). Si omis ou introuvable, l’API renvoie une erreur. Exemple : `worksheet=Feuil1`.                                                 |
| outPath          | string | Query       | Facultatif               | Dossier de destination sur le stockage cloud configuré, où le fichier JSON généré sera enregistré. Si non fourni, le JSON est renvoyé directement dans le flux de réponse. Exemple : `outPath=/converted/`. |
| outStorageName   | string | Query       | Facultatif               | Nom du stockage cible (par exemple, « MyStorage ») contenant le chemin `outPath`. Utilise le stockage par défaut si omis.                                                                            |
| fontsLocation    | string | Query       | Facultatif               | Dossier côté serveur contenant les polices personnalisées nécessaires à un rendu précis du texte dans la feuille de calcul. Exemple : `fontsLocation=/fonts/custom/`.                               |
| region           | string | Query       | Facultatif               | Identifiant culturel/régional qui influence le formatage des nombres, des dates et des devises dans le JSON généré (par exemple, `fr-FR`, `en-US`).                                                     |
| password         | string | Query       | Facultatif               | Mot de passe permettant d’ouvrir un classeur chiffré. Si le classeur n’est pas protégé par mot de passe, omettez ce paramètre.                                                                         |

### **Réponse**

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

| Code | Signification         | Description                                                              |
| ---- | --------------------- | ------------------------------------------------------------------------ |
| 200  | OK                    | Le filtre a été appliqué avec succès ; la réponse contient les détails. |
| 400  | Demande incorrecte    | Paramètres manquants ou invalides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé          | Jeton JWT invalide ou manquant.                                          |
| 413  | Payload trop volumineux | Le fichier téléchargé dépasse la limite de taille.                     |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                              |

## À quelles situations faut-il utiliser l’API Convertir une feuille de calcul en JSON ?

- **Tableaux de bord web** – Exporter les données de la feuille de calcul au format JSON pour les bibliothèques de graphiques côté client (par exemple, Chart.js, D3.js).
- **Migration de données** – Transférer des données Excel héritées vers des bases de données NoSQL ou des services REST consommant du JSON.
- **Applications mobiles ou hors ligne** – Convertir le contenu de la feuille de calcul en JSON côté serveur, puis synchroniser la charge utile légère sur les appareils mobiles.
- **Pipelines de production de rapports** – Alimenter directement les moteurs d’analyse avec les données de la feuille de calcul au format JSON, sans étape intermédiaire en CSV.

## Pourquoi utiliser l’API Convertir une feuille de calcul en JSON ?

- **Flux de travail sans téléchargement préalable** – Traiter des fichiers locaux dans le cloud sans les télécharger d’abord vers le stockage, économisant ainsi bande passante et coûts de stockage.
- **Conversion complète** – Prend en charge les classeurs protégés par mot de passe, les polices personnalisées et le formatage régional pour une représentation précise des données.
- **Exécution rapide et évolutif** – Exploite le moteur haute performance d’Aspose.Cells sur une infrastructure cloud, gérant efficacement les grandes feuilles de calcul.
- **Intégration simplifiée** – Un seul appel PUT renvoie un fichier JSON prêt à l’emploi ou l’enregistre directement, réduisant la complexité du code dans les applications clientes.

## Comment utiliser l’API Convertir une feuille de calcul en JSON avec les SDK

### Spécification de l’API Convertir une feuille de calcul en JSON

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">Spécification de l’API Convertir une feuille de calcul en JSON</a> fournit une interface de programmation publiquement accessible pour exécuter des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Feuil1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@monClasseur.xlsx" \
  -o converted.json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (encodé en Base64)",
  "contentType": "type MIME",
  "fileDownloadName": "nom de fichier facultatif"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et vous permet de travailler avec des classeurs à l’aide d’un code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code suivants montrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}