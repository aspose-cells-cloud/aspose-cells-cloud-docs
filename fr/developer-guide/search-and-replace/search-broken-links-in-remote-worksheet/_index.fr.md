---
title: "Aspose.Cells Cloud – API de détection de liens brisés dans Excel – Analyser et valider les liens de feuilles de calcul distantes"
second_title: "Document"
ArticleTitle: "Trouver et corriger les liens brisés dans une feuille de calcul Excel distante – Vérificateur de liens de feuilles de calcul en ligne"
linktype: "Search broken links in remote worksheet"
type: docs
url: /fr/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, liens brisés, API Excel, feuille de calcul cloud, validation des liens"
description: "Détecter et corriger les liens externes brisés dans des feuilles de calcul Excel stockées dans un stockage cloud. Utilisez l'API Aspose.Cells Cloud pour analyser des plages, renvoyer les détails des liens et automatiser les contrôles qualité."
weight: 100
---

## **Rechercher les liens brisés dans une feuille de calcul distante via l’API**

Détectez automatiquement les liens brisés dans une feuille de calcul Excel stockée dans un stockage cloud. Notre API analyse les plages spécifiées afin de localiser les références externes brisées, les formules invalides et les sources de données manquantes. Prend en charge l'audit à distance des feuilles de calcul, les contrôles qualité automatisés et l'intégration avec les fournisseurs de stockage cloud. API RESTful pour l’automatisation des workflows d’entreprise.

### **API Web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                                                                                                                |
| :--------------- | :----- | :------------------------------------------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | String | Chemin                                                  | **Obligatoire.** Le nom du fichier (avec extension) du classeur Excel dans lequel rechercher les liens brisés (par exemple, `Rapport_annuel.xlsx`).                                                                                       |
| worksheet        | String | Chemin                                                  | **Obligatoire.** Le nom exact de la feuille de calcul dans laquelle effectuer l'analyse des liens (par exemple, `FeuilDonnees1`).                                                                                                        |
| folder           | String | Chaîne de requête                                       | **Facultatif.** Le chemin du répertoire dans votre stockage cloud où se trouve le classeur cible. Si omis, le dossier racine est utilisé.                                                                                                 |
| storageName      | String | Chaîne de requête                                       | **Facultatif.** L'identifiant de votre stockage cloud personnalisé. Si non fourni, l'API utilise le stockage par défaut du compte.                                                                                                       |
| region           | String | Chaîne de requête                                       | **Facultatif.** Le paramètre de localisation à appliquer lors de la recherche (par exemple, `fr-FR`). Ce paramètre peut influencer l'interprétation de certaines formules ou formats régionaux. _Les codes de localisation pris en charge incluent `en-US`, `fr-FR`, `de-DE`, `es-ES`, etc._ |
| password         | String | Chaîne de requête                                       | **Facultatif.** Le mot de passe de déchiffrement pour une feuille de calcul protégée par mot de passe. À omettre si le fichier n’est pas chiffré.                                                                                         |

**Exemple de requête cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Rapport_annuel.xlsx/worksheets/FeuilDonnees1/search/broken-links?folder=Rapports&storageName=MonStockage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Réponse**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Fichier source introuvable"
    }
  ]
}
```

L’objet réponse est de type **BrokenLinksResponse** et contient :

- **BrokenLinks** – une collection d’objets `BrokenLink`, chacun décrivant la référence problématique (adresse, code d’erreur et message).
- **Code** – code d’état numérique renvoyé par le service.
- **Status** – description textuelle du résultat.

**Remarques** : L’API ne pagine pas les résultats. Jusqu’à 10 000 liens brisés peuvent être retournés par requête. La limite de débit est de 100 requêtes par minute et par compte.

### Codes d’erreur

- **400 Bad Request** – URI invalide de l’API Aspose.Cells Cloud.
- **401 Unauthorized** – Jeton d’accès invalide ou manquant.
- **404 Not Found** – Le fichier de feuille de calcul n’est pas accessible.
- **500 Server Error** – Une erreur s’est produite lors de l’obtention des données de calcul.

## Où utiliser la recherche de liens brisés dans la feuille de calcul via l’API ?

- **Audit régulier des grands modèles financiers** : Avant la diffusion des rapports mensuels ou trimestriels, analyser automatiquement les zones clés de calcul (par exemple, `TableauDeBord!B5:K50`) contenant de nombreuses références externes afin de garantir que tous les liens pointent vers des fichiers sources valides.
- **Intégration de données lors de fusions et acquisitions** : Après la fusion de plusieurs fichiers Excel représentant différentes unités commerciales, analyser la feuille « Aperçu » pour identifier les liens devenus invalides suite à des modifications des chemins des fichiers sources ou à des problèmes de permissions.
- **Préparation des dossiers investisseurs** : Avant la finalisation des supports de présentation comportant des graphiques et tableaux liés à des bases de données externes ou des sources de données marchandes, vérifier la validité de tous les liens.

## Pourquoi utiliser la recherche de liens brisés dans la feuille de calcul via l’API ?

- **Adapté aux développeurs** : Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, ce qui permet un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Réduction des coûts en main-d’œuvre** : Élimine le besoin de personnel dédié à la consolidation manuelle des documents et à la vérification des liens.
- **Paiement à l’usage** : Aucun investissement initial requis ; vous ne payez que pour les appels API effectivement réalisés.
- **Zéro coût de maintenance** : Aucun serveur à maintenir, aucune mise à jour logicielle, aucun problème de compatibilité à gérer.
- **Préservation du formatage Excel complexe** dans un format PDF universellement accessible.

## Comment utiliser la recherche de liens brisés dans la feuille de calcul via l’API avec les SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le moyen optimal d’accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi de simplement implémenter la recherche de liens brisés dans les feuilles de calcul avec un minimum de code. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}