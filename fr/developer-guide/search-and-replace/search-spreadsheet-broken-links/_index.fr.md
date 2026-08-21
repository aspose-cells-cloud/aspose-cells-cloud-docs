---
title: "Rechercher les liens rompus dans un classeur – API Aspose.Cells Cloud"
second_title: "Document"
articleTitle: "Trouver et corriger les liens rompus dans Excel – Vérificateur de liens de feuilles de calcul cloud"
linktype: "Search Spreadsheet Broken Links"
type: docs
url: /fr/search-spreadsheet-broken-links/
keywords: "Aspose Cells, liens rompus, audit de feuille de calcul, API Excel, feuille de calcul cloud, vérificateur de liens"
description: "Détectez et corrigez les liens rompus dans les classeurs Excel via l’API Aspose.Cells Cloud. Analysez des plages, obtenez des résultats détaillés au format JSON et intégrez avec n’importe quel SDK de langage."
weight: 100
---

## **API de recherche des liens rompus dans les classeurs**

Détectez automatiquement les liens rompus dans les fichiers Excel. Notre API analyse les plages spécifiées à la recherche de références externes rompues, de formules invalides et de sources de données manquantes. Prend en charge l’audit à distance des feuilles de calcul, les contrôles automatisés de qualité et l’intégration avec les fournisseurs de stockage cloud. API RESTful pour l’automatisation des flux de travail d’entreprise.

**Résumé :** Utilisez ce point de terminaison pour identifier et corriger rapidement les liens invalides dans les classeurs, garantissant ainsi l’intégrité des données dans les modèles financiers, les jeux de données liés à des fusions-acquisitions et les documents préparés pour les investisseurs.

### **API Web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Paramètres de la requête

| Nom du paramètre | Type   | Emplacement                  | Description                                                                                                                                              |
|------------------|--------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier| FormData (multipart)         | **Obligatoire.** Le fichier de classeur Excel (`.xlsx`, `.xls`, etc.) à analyser.                                                                      |
| worksheet        | Chaîne | Requête                      | **Facultatif.** Le nom de la feuille de calcul à analyser. Si omis, la première feuille de calcul est utilisée.                                       |
| cellArea         | Chaîne | Requête                      | **Facultatif.** Plage cible de cellules en notation A1 (par exemple, `B2:D10`). Si non spécifié, toute la plage utilisée est analysée.               |
| region           | Chaîne | Requête                      | **Facultatif.** Paramètre régional (par exemple, `fr-FR`) pouvant affecter l’interprétation des dates, des nombres ou des devises.                   |
| password         | Chaîne | Requête                      | **Facultatif.** Mot de passe des classeurs chiffrés. Laissez vide si le fichier n’est pas protégé.                                                    |

### Réponse

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "Fichier introuvable",
      "Status": "Rompu"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Introuvable",
      "Status": "Rompu"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Codes d’erreur

| Code | Description |
|------|-------------|
| **400 Bad Request** | URI invalide pour l’API Aspose.Cells Cloud. |
| **401 Unauthorized** | Jeton d’accès, ID client ou secret client invalide. |
| **404 Not Found** | Le fichier de feuille de calcul n’est pas accessible. |
| **429 Too Many Requests** | Limite de taux dépassée (60 appels / minute). |
| **500 Server Error** | Une anomaly est survenue dans la feuille de calcul lors de l’obtention des données de calcul. |


## Où utiliser l’API de recherche des liens rompus dans les classeurs ?

- **Audit régulier des grands modèles financiers** : Avant la diffusion des rapports mensuels ou trimestriels, scannez automatiquement les zones de calcul clés (par exemple, `Dashboard!B5:K50`) contenant de nombreuses références à des données externes, afin de vérifier que tous les liens pointent vers des fichiers sources valides.  
- **Intégration de données dans le cadre de fusions-acquisitions** : Lors de la fusion de plusieurs fichiers de feuilles de calcul représentant des unités commerciales, analysez la feuille de calcul « Vue d’ensemble » après l’intégration afin d’identifier les liens devenus invalides suite à des modifications de chemins de fichiers ou à des problèmes de permissions.  
- **Préparation des dossiers pour les investisseurs** : Avant la finalisation des supports de présentation contenant des graphiques et des tableaux liés à des bases de données externes ou des sources de données de marché, vérifiez la validité de tous les liens.

## Pourquoi utiliser l’API de recherche des liens rompus dans les classeurs ?

- **Conçu pour les développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant le développement rapide et accompagné d’une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement la charge de travail de développement.  
- **Réduction des coûts de main-d’œuvre** – Élimine le besoin de personnel dédié pour vérifier manuellement les liens dans les documents.  
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels à l’API que vous utilisez réellement.  
- **Zéro coût de maintenance** – Aucun serveur à maintenir, aucune mise à jour logicielle, aucune incompatibilité.  
- **Préservation du formatage complexe d’Excel** – Les résultats sont renvoyés sous un format JSON universellement accessible tout en conservant la mise en page d’origine du classeur.

## Comment utiliser l’API de recherche des liens rompus dans les classeurs à l’aide des SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} définit une interface de programmation publiquement accessible, vous permettant d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant simplement d’implémenter la fonctionnalité de recherche des liens rompus avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}