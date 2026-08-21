---
title: "Convertir une plage en CSV"
ArticleTitle: "Convertir une plage en CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Convertir une plage en CSV"
type: docs
url: /fr/cells/convert/range/csv
aliases: []
keywords: "convertir, csv, plage, Aspose.Cells"
description: "Convertit une plage de feuille de calcul située sur un disque local en fichier CSV."
weight: 1
---

## Convertir une plage en CSV via les services web Aspose.Cells Cloud

Cette opération lit un fichier de feuille de calcul à partir du système de fichiers local, convertit une plage spécifiée au format CSV, puis renvoie directement le résultat converti. Elle s'exécute entièrement sur le serveur cloud, ce qui élimine la nécessité d'un téléversement intermédiaire vers le stockage cloud. L'API prend en charge des paramètres optionnels tels que les polices personnalisées, l'ajustement automatique des lignes et des colonnes, les paramètres régionaux, ainsi que les classeurs protégés par mot de passe.

### Point de terminaison de l'API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Description                                                                                                                                              |
|------------------|---------|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fichier | FormData                                               | Télécharger le fichier de feuille de calcul.                                                                                                             |
| worksheet        | Chaîne  | Chaîne de requête                                      | Nom de la feuille de calcul. **Obligatoire**.                                                                                                            |
| range            | Chaîne  | Chaîne de requête                                      | Zone de cellules, par exemple `A1:C10`. **Obligatoire**.                                                                                                 |
| outPath          | Chaîne  | Chaîne de requête                                      | (Optionnel) Chemin du dossier où le classeur est stocké. La valeur par défaut est null.                                                                |
| outStorageName   | Chaîne  | Chaîne de requête                                      | Nom du stockage de sortie.                                                                                                                               |
| fontsLocation    | Chaîne  | Chaîne de requête                                      | Utiliser des polices personnalisées.                                                                                                                     |
| AutoRowsFit      | Booléen | Chaîne de requête                                      | (Optionnel) Ajuste automatiquement toutes les lignes dans les feuilles de calcul.                                                                       |
| AutoColumnsFit   | Booléen | Chaîne de requête                                      | (Optionnel) Ajuste automatiquement toutes les colonnes dans les feuilles de calcul.                                                                     |
| region           | Chaîne  | Chaîne de requête                                      | Paramètre régional/langue de la feuille de calcul (par exemple, `fr-FR`, `en-US`). Affecte le formatage des nombres, l'analyse des dates et le comportement spécifique à la locale. |
| password         | Chaîne  | Chaîne de requête                                      | Mot de passe permettant d’ouvrir le fichier de feuille de calcul.                                                                                        |

### Paramètre du corps de la requête

| Nom du paramètre | Type | Description |
| ---------------- | ---- | ----------- |
| Aucun            | N/A  | Aucun paramètre dans le corps de la requête. |

### **Réponse**

```json
{
  "ResponseFile": "flux binaire (contenu CSV)"
}
```

**Codes de statut de la réponse**

| Code | Signification | Description |
|------|---------------|-------------|
| 200  | OK            | La plage a été convertie avec succès, et le fichier CSV est renvoyé dans le corps de la réponse. |
| 400  | Mauvaise requête | URL invalide ou paramètres obligatoires manquants. |
| 401  | Non autorisé  | Échec de l'authentification ou absence de justificatifs d'identification. |
| 413  | Charge utile trop volumineuse | La charge utile de la requête dépasse la limite de taille autorisée. |
| 500  | Erreur interne du serveur | Une anomalies s'est produite lors de la récupération des données de conversion de la feuille de calcul. |

## Comment utiliser la fonction Convertir une plage en CSV avec les SDK

### Spécification de la fonction Convertir une plage en CSV

La [spécification de l'API Convertir une plage en CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) définit une interface de programmation accessible publiquement et permet d'effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l'outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L'exemple suivant montre comment effectuer des appels à l'API cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
# Utiliser HTTPS pour une connexion sécurisée
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sheet1&range=A1:C10&outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/custom/fonts&AutoRowsFit=true&AutoColumnsFit=true&region=fr-FR&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jeton jwt>" \
  -F 'Spreadsheet=@exemple.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "ContenuCsvEncodéEnBase64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose Cells Cloud

L'utilisation d'un SDK constitue la méthode la plus rapide pour accélérer le développement. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells Cloud à l’aide de divers SDK :
`[À compléter]`