---
title: "Aspose.Cells Cloud Excel Text Search Web API – Recherche de texte dans une feuille de calcul distante"
second_title: "Document"
articleTitle: "Rechercher du texte dans une feuille de calcul Excel distante – Trouver des données spécifiques"
linktitle: "Rechercher du contenu dans une feuille de calcul distante"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, API Excel, recherche de texte, feuille de calcul distante"
description: "Recherchez du texte, des nombres ou des formules dans une feuille de calcul Excel distante à l’aide de l’API Aspose.Cells Cloud. Prend en charge la recherche insensible à la casse et les fichiers protégés par mot de passe."
weight: 100
---

## **Rechercher du contenu dans une feuille de calcul distante**

Recherchez de manière programmatique un texte spécifique dans n’importe quelle feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud. Ce service permet de localiser du texte, des nombres ou des formules dans des fichiers distants stockés dans un stockage cloud, facilitant ainsi les workflows automatisés de découverte de données, d’analyse de contenu et d’audit de feuilles de calcul.

### **API Web**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de requête**

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                       |
| ---------------- | ------- | ------------------------------------------------------ | ------------------------------------------------------------------------------------------------- |
| name             | Chaîne  | Chemin                                                 | **Obligatoire.** Nom du classeur cible (par exemple, `rapport_annuel.xlsx`).                     |
| worksheet        | Chaîne  | Chemin                                                 | **Obligatoire.** Nom de la feuille de calcul dans laquelle la recherche est effectuée.           |
| searchText       | Chaîne  | Chaîne de requête                                      | **Obligatoire.** Chaîne de texte ou nombre exact à localiser.                                    |
| ignoreCase       | Booléen | Chaîne de requête                                      | **Facultatif.** Si `true`, la recherche est insensible à la casse. Valeur par défaut : `false`. |
| folder           | Chaîne  | Chaîne de requête                                      | **Facultatif.** Chemin du dossier contenant le classeur. Si omis, le dossier racine est utilisé. |
| storageName      | Chaîne  | Chaîne de requête                                      | **Facultatif.** Nom d’un stockage cloud personnalisé. Si omis, le stockage par défaut est utilisé. |
| region           | Chaîne  | Chaîne de requête                                      | **Facultatif.** Paramètre de localisation (par exemple, `fr-FR`) qui peut influencer la comparaison des textes. |
| password         | Chaîne  | Chaîne de requête                                      | **Facultatif.** Mot de passe pour un classeur protégé. À omettre si le fichier n’est pas chiffré. |

### **Réponse**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Tableau des correspondances. Chaque élément contient l’adresse de la cellule (`cellName`), la chaîne trouvée (`text`) et le nombre d’occurrences dans cette cellule (`occurrences`).
- **code** – Code d’état HTTP renvoyé par le service.
- **status** – Description textuelle du résultat.

### **Codes d’erreur**

- **400 Bad Request** – URI API invalide ou paramètres mal formés.
- **401 Unauthorized** – Jeton OAuth 2.0 manquant ou invalide.
- **404 Not Found** – Le classeur ou la feuille de calcul est introuvable.
- **500 Server Error** – Une condition inattendue s’est produite lors du traitement de la requête.

## Où utiliser la recherche de contenu dans une feuille de calcul via l’API Spreadsheet ?

- **Audit de conformité du classeur :** Localisez rapidement des termes sensibles (par exemple, « Confidentiel ») dans l’ensemble du fichier.
- **Association de données inter-feuilles :** Trouvez un numéro de projet ou un nom de client apparaissant sur plusieurs feuilles.
- **Vérification des modèles :** Après génération de rapports, confirmez que les espaces réservés comme `{{Date}}` ont bien été remplacés.
- **Data mining historique :** Recherchez des codes d’événement spécifiques dans des feuilles de calcul héritées afin de comprendre la logique métier passée.

## Pourquoi utiliser la recherche de contenu dans une feuille de calcul via l’API Spreadsheet ?

- **Développeur-friendly :** Les SDK disponibles pour de nombreux langages accélèrent le développement et sont entièrement documentés.
- **Réduction des coûts de main-d’œuvre :** Diminue le besoin de personnel dédié à la consolidation manuelle des données.
- **Paiement à l’usage :** Vous ne payez que pour les appels API effectivement réalisés.
- **Maintenance nulle :** Aucun serveur à gérer, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.
- **Préservation du formatage complexe d’Excel** lors de l’export des résultats en PDF ou dans d’autres formats.

## Comment utiliser la recherche de liens brisés dans une feuille de calcul via l’API Spreadsheet à l’aide des SDK ?

### Spécification OpenAPI

La [Spécification OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) définit une interface de programmation accessible publiquement et permet des interactions REST directement depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK constitue la meilleure méthode pour accélérer le développement. Le SDK gère les détails sous-jacents, vous permettant ainsi d’implémenter simplement la recherche de contenu dans les feuilles de calcul avec un minimum de code. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.