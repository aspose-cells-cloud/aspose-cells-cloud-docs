---
---
title: "Exporter une plage Excel vers PDF, PNG, CSV – API Aspose.Cells Cloud"
second_title: "Document"
ArticleTitle: "Comment exporter une plage de feuille de calcul distante vers d'autres formats : guide étape par étape"
linktitle: "Exporter une plage au format"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells, exporter une plage Excel, PDF, PNG, CSV, API cloud, conversion de feuille de calcul"
description: "Découvrez comment convertir une plage Excel spécifique stockée dans Aspose.Cells Cloud en PDF, PNG, CSV ou d'autres formats. Inclut les détails des points de terminaison, les paramètres, les exemples de requêtes, la gestion des réponses et les informations d'erreur."
weight: 100
---

Exporter une plage de feuille de calcul ou Excel dans le cloud vers un fichier d’un format donné. Ce fichier peut être enregistré dans le cloud ou exporté vers un stockage local.

## API d’exportation de plage au format

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre   | Type   | Emplacement | Description                                                                                                                                        |
| :----------------- | :----- | :---------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path        | (Obligatoire) Le nom du fichier classeur à récupérer.                                                                                             |
| **worksheet**      | String | Path        | Le nom de la feuille de calcul.                                                                                                                   |
| **range**          | String | Path        | La plage à convertir (par exemple, `A1:C12`).                                                                                                      |
| **format**         | String | Query       | (Obligatoire) Format de sortie souhaité (par exemple, `pdf`, `png`, `svg`).                                                                        |
| **folder**         | String | Query       | (Facultatif) Chemin du dossier dans lequel le classeur est stocké.                                                                                |
| **storageName**    | String | Query       | (Facultatif) Nom du stockage si vous utilisez un stockage cloud personnalisé.                                                                     |
| **outPath**        | String | Query       | (Facultatif) Chemin du fichier de sortie dans le stockage cloud.                                                                                  |
| **outStorageName** | String | Query       | (Facultatif) Nom du stockage pour le fichier de sortie.                                                                                           |
| **fontsLocation**  | String | Query       | (Facultatif) Emplacement personnalisé des polices.                                                                                                 |
| **region**         | String | Query       | (Facultatif) Paramètre de région/langue de la feuille de calcul (par exemple, `en-US`, `fr-FR`). Affecte le formatage des nombres, l’analyse des dates et le comportement spécifique à la locale. |
| **password**       | String | Query       | (Facultatif) Mot de passe requis pour ouvrir le fichier de feuille de calcul.                                                                     |

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

**Codes d’état HTTP**

| Code | Signification             | Description                                                          |
| ---- | ------------------------- | -------------------------------------------------------------------- |
| 200  | OK                        | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé              | Jeton JWT non valide ou manquant.                                    |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la limite de taille.                  |
| 500  | Erreur interne du serveur | Erreur serveur inattendue.                                           |

## Où utiliser l’API d’exportation de plage vers un autre format ?

### Scénarios d’exportation et de migration de données

- **Intégration avec base de données** – Exporter des plages Excel spécifiques directement vers des systèmes de base de données.
- **Intégration d’applications** – Alimenter des applications SaaS avec des données de feuille de calcul sélectionnées.
- **Migration de systèmes** – Transférer des plages de données spécifiques entre systèmes hérités et modernes.
- **Partage interplateforme** – Partager des sous-ensembles de données ciblés entre différentes plateformes.

### Rapports et analyse

- **Rapports ciblés** – Exporter des sections spécifiques de rapports vers d’autres formats pour une analyse ciblée.
- **Flux de données vers tableaux de bord** – Fournir des plages de données spécifiques à des outils de tableaux de bord BI.
- **Indicateurs de performance** – Extraire des plages de clés indicateurs (KPI) pour les systèmes de suivi des performances.
- **Rapports financiers** – Exporter des sections d’états financiers pour audit externe.

### Développement et tests

- **Gestion des données de test** – Exporter des plages de données spécifiques à des fins de test.
- **Environnements de développement** – Partager des plages de données d’exemple avec les équipes de développement.
- **Tests d’API** – Générer des données de test au format CSV à partir de sections spécifiques de la feuille de calcul.
- **Développement de prototypes** – Fournir des jeux de données ciblés pour des prototypes d’applications.

### Opérations métier

- **Partage sélectif de données** – Partager des plages de données spécifiques avec des partenaires externes.
- **Sauvegarde partielle des données** – Sauvegarder des plages critiques dans un format choisi.
- **Transfert interdépartemental** – Partager des données spécifiques entre départements.
- **Rapports de conformité** – Exporter des plages de données réglementaires pour soumission à des exigences de conformité.

### Flux de travail automatisés

- **Exportations planifiées de plages** – Exporter automatiquement des plages spécifiques selon un calendrier.
- **Extraction déclenchée** – Exporter des plages en fonction d’événements métier ou de déclencheurs.
- **Intégration dans les flux de travail** – Intégrer les exports de plages dans les flux de travail de processus métier.
- **Traitement par lots de plages** – Traiter plusieurs plages spécifiques en opérations par lots.

## Pourquoi utiliser l’API d’exportation de plage vers un autre format ?

- **Adaptée aux développeurs** – Aspose.Cells Cloud propose des bibliothèques SDK dans plusieurs langages, permettant un développement rapide grâce à une documentation complète. Comparé à la mise en place de solutions personnalisées de rendu de graphiques, cela réduit considérablement la charge de développement.
- **Réduction des coûts en personnel** – Moins de personnel nécessaire pour la consolidation de documents.
- **Paiement à l’utilisation** – Aucun investissement initial ; vous ne payez que pour les appels d’API que vous utilisez réellement.
- **Aucune maintenance serveur** – Aucun serveur à maintenir, aucune mise à jour logicielle, aucune incompatibilité.
- **Préservation du formatage Excel complexe** – Les fichiers de sortie conservent le formatage d’origine de la feuille de calcul.

## Comment utiliser l’API d’exportation de plage de feuille de calcul au format via les SDK ?

### Spécification de l’API d’exportation de plage au format

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Spécification de l’API d’exportation de plage au format</a> fournit une interface de programmation accessible publiquement, permettant des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud via cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Requête" tabName12="Réponse" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau, vous permettant d’exporter une plage de feuille de calcul vers un fichier d’un format donné à l’aide d’un code concis. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour une liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}