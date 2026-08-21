---
title: "API Web Aspose.Cells Cloud pour la protection par mot de passe des fichiers Excel – Automatisez le chiffrement des mots de passe d'ouverture et de modification"
second_title: "Guide du développeur pour la protection Excel"
ArticleTitle: "Outil de protection par mot de passe Excel – Définir les mots de passe d’ouverture et de modification – Sécurisez vos feuilles de calcul"
linktype: "docs"
url: /fr/protect-spreadsheet/
keywords: "Aspose.Cells, protection Excel par mot de passe, API, mot de passe d’ouverture, mot de passe de modification, stockage cloud, sécurité des feuilles de calcul"
description: "Sécurisez vos fichiers Excel par programmation avec Aspose.Cells Cloud. Définissez à la fois les mots de passe d’ouverture et de modification via un seul appel API. Prend en charge les formats .xlsx, .xls et le stockage cloud. Essayez gratuitement."
weight: 100
---

Automatisez à grande échelle la protection par mot de passe des fichiers Excel grâce à notre API dédiée aux développeurs : appliquez à la fois les mots de passe d’ouverture et de modification par programmation. Idéal pour les flux de travail d’entreprise et compatible avec les formats .xlsx ainsi que les anciens formats. Consultez la documentation et lancez dès aujourd’hui votre intégration gratuite.

## **API de protection de feuille de calcul**

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de requête :**

| Nom du paramètre | Type   | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                    |
| :--------------- | :----- | :------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fichier | FormData                                                | Le fichier de feuille de calcul Excel à télécharger et protéger à l’aide d’un chiffrement par mot de passe.                                   |
| openPassword     | Chaîne  | Chaîne de requête                                        | Le mot de passe requis pour ouvrir (décrypter) la feuille de calcul protégée.                                                                 |
| modifyPassword   | Chaîne  | Chaîne de requête                                        | Le mot de passe requis pour autoriser la modification ou l’édition du contenu de la feuille de calcul.                                        |
| outPath          | Chaîne  | Chaîne de requête                                        | (Facultatif) Spécifie le chemin du dossier de sortie où le classeur protégé sera enregistré. Si non fourni, le fichier est renvoyé dans la réponse. |
| outStorageName   | Chaîne  | Chaîne de requête                                        | Le nom du stockage cloud utilisé pour stocker le fichier protégé en sortie.                                                                    |
| region           | Chaîne  | Chaîne de requête                                        | Spécifie les paramètres régionaux/culturels (par exemple, format de date, format des nombres) appliqués à la feuille de calcul lors du traitement. |

**Authentification**  
Tous les appels à l’API de protection de feuille de calcul nécessitent un jeton d’accès OAuth 2.0 valide. Incluez ce jeton dans l’en-tête `Authorization` :

```http
Authorization: Bearer {access_token}
```

Le jeton doit être obtenu à partir du point d’entrée d’authentification d’Aspose Cloud et doit inclure la portée **Cells**.

## **Réponse**

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

| Code | Signification           | Description                                                     |
| ---- | ----------------------- | --------------------------------------------------------------- |
| 200  | OK                      | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte      | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé            | Jeton JWT invalide ou manquant.                                 |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                     |

## Où utiliser l’API de protection de feuille de calcul ?

- **Protéger des données financières sensibles** – Protégez les fichiers Excel contenant des budgets, des factures ou des informations de paie à l’aide de mots de passe d’ouverture et de modification afin d’empêcher tout accès ou modification non autorisé.
- **Partager en toute sécurité des rapports confidentiels** – Assurez que seuls les destinataires autorisés peuvent consulter ou modifier des rapports métier, d’audit ou de conformité, qu’ils soient diffusés en interne ou en externe.
- **Automatiser la sécurité des documents dans les flux de travail** – Intégrez l’API dans des systèmes d’entreprise (par exemple, ERP, CRM) pour protéger automatiquement par mot de passe les feuilles de calcul générées avant leur stockage ou leur envoi par e-mail.
- **Appliquer un accès en lecture seule** – Permettez aux utilisateurs d’ouvrir les rapports en vue de les consulter tout en limitant les modifications à l’aide d’un mot de passe de modification distinct — idéal pour les modèles ou les jeux de données finalisés.
- **Respecter les exigences réglementaires** – Aidez à satisfaire aux exigences du RGPD, de la HIPAA ou de la SOX en chiffrant les données sensibles des feuilles de calcul, tant au repos qu’en transit, via une protection automatisée.

## Pourquoi utiliser l’API de protection de feuille de calcul ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, facilitant un développement rapide, accompagné d’une documentation complète. Comparé à la création de solutions personnalisées, cela réduit considérablement la charge de développement.
- **Réduit les besoins en personnel** – Automatise la consolidation et la sécurité des documents, réduisant ainsi le besoin de personnel dédié.
- **Paiement à l’usage** – Aucun investissement initial ; vous ne payez que pour les appels API réellement utilisés.
- **Zéro coût de maintenance** – Aucun serveur à gérer, aucune mise à jour logicielle à effectuer, aucune préoccupation liée à la compatibilité.
- **Préservation de tous les formats Excel d’origine** lors de l’application de la protection par mot de passe, garantissant que le classeur protégé ait exactement la même apparence que le fichier source.

## Comment utiliser l’API de protection de feuille de calcul avec les SDK ?

### Spécification OpenAPI

La [spécification de l’API de protection de feuille de calcul](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet) fournit une interface de programmation publiquement accessible afin de faciliter les interactions REST directes depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/protection/spreadsheet?openPassword=MonMotDePasseOuverture&modifyPassword=MonMotDePasseModification" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/chemin/vers/classeur.xlsx"
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

L’utilisation des SDK est le moyen le plus efficace d’accélérer le développement. Les SDK prennent en charge les détails sous-jacents, vous permettant ainsi d’implémenter simplement la fonctionnalité de protection de feuille de calcul avec un minimum de code. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}