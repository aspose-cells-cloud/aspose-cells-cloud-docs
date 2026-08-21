---
title: "Aspose.Cells Cloud – Échanger des colonnes, lignes et plages (v4.0)"
second_title: "Document"
ArticleTitle: "Échanger des données entre colonnes, lignes et cellules dans Excel"
linktype: "docs"
url: /fr/swap-range/
keywords: "Aspose Cells, API Excel, Échanger une plage, classeur cloud"
description: "Échangez des colonnes, des lignes ou des plages dans des fichiers Excel à l’aide de l’API Aspose.Cells Cloud. Préservez le formatage, les formules et les références de cellules en une seule requête."
weight: 100
---

Échangez automatiquement des données entre deux colonnes, lignes, plages ou cellules quelconques dans des fichiers Excel à l’aide de l’API Aspose.Cells Cloud. L’API d’échange de plages permet d’échanger précisément des données tout en préservant tout le formatage, les formules et les références de cellules. Elle prend en charge la réorganisation complexe des données, le traitement par lots et l’intégration transparente dans le cloud pour les flux de travail professionnels.

## **API d’échange de plages**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Paramètres de la requête**

| Nom du paramètre   | Type   | Emplacement | Description                                                                                                                                   |
| ------------------ | ------ | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fichier | FormData    | **Obligatoire.** Le fichier de classeur Excel source (`.xlsx`, `.xls`).                                                                       |
| **worksheet1**     | Chaîne | Query       | **Obligatoire.** Nom de la feuille de calcul contenant la première zone de données.                                                          |
| **range1**         | Chaîne | Query       | **Obligatoire.** Plage de cellules (par ex. `A1:D10`) dans `worksheet1` à échanger.                                                           |
| **worksheet2**     | Chaîne | Query       | **Obligatoire.** Nom de la feuille de calcul contenant la deuxième zone de données (peut être identique à `worksheet1`).                    |
| **range2**         | Chaîne | Query       | **Obligatoire.** Plage de cellules (par ex. `F1:I10`) dans `worksheet2` à échanger. **Important :** `range1` et `range2` doivent avoir des dimensions identiques. |
| **outPath**        | Chaîne | Query       | **Facultatif.** Dossier dans le stockage cloud où le classeur modifié sera enregistré.                                                       |
| **outStorageName** | Chaîne | Query       | **Obligatoire.** Nom du service de stockage cloud configuré (par ex. `MyCompanyStorage`).                                                    |
| **region**         | Chaîne | Query       | **Facultatif.** Paramètre régional (par ex. `fr-FR`, `ja-JP`) pouvant influencer le formatage.                                               |
| **password**       | Chaîne | Query       | **Facultatif.** Mot de passe permettant de déchiffrer un classeur protégé. Omettre s’il n’est pas chiffré.                                    |

**Exemple de requête (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

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

**Remarques :**  
- L’API renvoie le classeur modifié sous forme de flux de fichier. Si `outPath` est spécifié, le fichier est également enregistré à l’emplacement donné dans le stockage cloud.  
- Des dimensions de plages non correspondantes entraîneront une erreur **400 Bad Request**.

### Codes d’erreur

| Code                 | Description                                                        |
| -------------------- | ------------------------------------------------------------------ |
| **400 Bad Request**  | URI de requête invalide ou dimensions de plages non correspondantes. |
| **401 Unauthorized** | Jeton d’accès invalide ou expiré ; le client-id ou le secret est incorrect. |
| **404 Not Found**    | Le fichier de classeur spécifié ne peut pas être accédé.         |
| **500 Server Error** | Une erreur interne s’est produite lors du traitement du classeur. |

## Où faut-il utiliser l’API d’échange de plages ?

- **Restructuration de modèles financiers** – Réorganisez des blocs de données (par ex. déplacez la prévision du T3 vers le T4) tout en préservant les formules et le formatage conditionnel.
- **Canalisation de données et processus ETL** – Échangez des plages de données brutes avec des plages nettoyées dans une feuille intermédiaire avant la production finale.
- **Correction d’erreurs et récupération de données** – Corrigez rapidement des données déplacées sans avoir à copier-coller manuellement.

## Pourquoi utiliser l’API d’échange de plages ?

- **Adaptée aux développeurs** – Des SDK sont disponibles pour plusieurs langages, réduisant l’effort de développement par rapport à la création de solutions personnalisées.
- **Réduction des coûts de main-d’œuvre** – Automatise le réarrangement des données, diminuant ainsi le besoin de consolidation manuelle.
- **Paiement à l’usage** – Vous ne payez que pour les appels à l’API que vous effectuez réellement.
- **Zéro maintenance** – Aucun serveur à gérer, aucune mise à jour logicielle à effectuer, aucune préoccupation de compatibilité.

## Comment utiliser l’API d’échange de plages avec les SDK ?

### Spécification de l’API d’échange de plages

La [spécification de l’API d’échange de plages](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer, car elle masque les détails de bas niveau et permet d’échanger des plages à l’aide d’un code concis. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---