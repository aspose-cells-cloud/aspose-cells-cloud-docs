---
title: "Mettre à jour l’axe des valeurs secondaire d’un graphique"
ArticleTitle: "Mettre à jour l’axe des valeurs secondaire d’un graphique – Aspose.Cells Cloud REST API"
type: docs
url: /charts/second-value-axis/update/
weight: 160
keywords: "Aspose.Cells, API graphique, Axe des valeurs secondaire, Excel, REST, SDK cloud"
description: "Met à jour l’axe des valeurs secondaire d’un graphique dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples de requêtes, des codes de réponse et les conditions préalables."
---

Cet API REST met à jour l’axe des valeurs secondaire d’un graphique.

**Conditions préalables :**  
- Un jeton d’accès JWT valide (voir le [guide d’authentification](https://docs.aspose.cloud/cells/authentication/)).  
- Le fichier Excel cible doit être stocké dans le stockage Aspose Cloud (fournir `folder` et éventuellement `storageName`).  
- La version API v3.0 est utilisée ; assurez-vous que l’URL de base est `https://api.aspose.cloud/v3.0`.

## API PostChartSecondValueAxis

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                         |
| ---------------- | ------- | ----------- | --------------------------------------------------- |
| name             | string  | path        | Nom du fichier Excel.                               |
| sheetName        | string  | path        | Nom de la feuille de calcul contenant le graphique. |
| chartIndex       | integer | path        | Index de base zéro du graphique à modifier.         |
| axis             | object  | body        | Paramètres de l’axe des valeurs secondaire.         |
| folder           | string  | query       | Chemin du dossier dans le stockage où le fichier se trouve. |
| storageName      | string  | query       | Nom du service de stockage.                         |

**Exemple de corps de requête (JSON) :**

```json
{
  "IsAutomaticMajorUnit": true,
  "Maximum": 100,
  "Minimum": 0,
  "MajorUnit": 10,
  "MinorUnit": 2,
  "Title": {
    "Text": "Axe secondaire"
  }
}
```

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostChartSecondValueAxis) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/secondvalueaxis" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codes de statut HTTP**

| Code | Signification              | Description                                               |
|------|----------------------------|-----------------------------------------------------------|
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT non valide ou manquant.                         |
| 413  | Charge utile trop grande   | Le fichier téléchargé dépasse la limite de taille.       |
| 500  | Erreur interne du serveur  | Erreur inattendue sur le serveur.                         |

**Voir également :**  
- [Obtenir l’axe des valeurs secondaire d’un graphique](https://docs.aspose.cloud/cells/charts/second-value-axis/get/)  
- [Mettre à jour l’axe des valeurs d’un graphique](https://docs.aspose.cloud/cells/charts/value-axis/update/)

## Famille de SDK cloud

Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

```csharp
// Exemple en C# pour mettre à jour l’axe des valeurs secondaire
var api = new CellsApi("clientId", "clientSecret");
var axis = new Axis { IsAutomaticMajorUnit = true, Maximum = 100 };
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java
// Exemple en Java pour mettre à jour l’axe des valeurs secondaire
CellsApi api = new CellsApi("clientId", "clientSecret");
Axis axis = new Axis();
axis.setIsAutomaticMajorUnit(true);
axis.setMaximum(100.0);
api.postChartSecondValueAxis(name, sheetName, chartIndex, axis);
```

{{< /tab >}}

{{< tab tabNum="3" >}}

```php
// Exemple en PHP pour mettre à jour l’axe des valeurs secondaire
$api = new CellsApi($clientId, $clientSecret);
$axis = new Axis();
$axis->setIsAutomaticMajorUnit(true);
$axis->setMaximum(100);
$api->postChartSecondValueAxis($name, $sheetName, $chartIndex, $axis);
```

{{< /tab >}}

{{< tab tabNum="4" >}}

```ruby
# Exemple en Ruby pour mettre à jour l’axe des valeurs secondaire
api = AsposeCellsCloud::ApiClient.new(client_id, client_secret)
axis = Axis.new(is_automatic_major_unit: true, maximum: 100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="5" >}}

```python
# Exemple en Python pour mettre à jour l’axe des valeurs secondaire
api = asposecellscloud.ApiClient(client_id, client_secret)
axis = Axis(is_automatic_major_unit=True, maximum=100)
api.post_chart_second_value_axis(name, sheet_name, chart_index, axis)
```

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartSecondValueAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

```java
// Exemple Android (Java) – identique au fragment de code Java ci-dessus
```

{{< /tab >}}

{{< tab tabNum="8" >}}

```swift
// Exemple en Swift pour mettre à jour l’axe des valeurs secondaire
let api = CellsApi(clientId: "clientId", clientSecret: "clientSecret")
var axis = Axis()
axis.isAutomaticMajorUnit = true
axis.maximum = 100
api.postChartSecondValueAxis(name: name, sheetName: sheetName, chartIndex: chartIndex, axis: axis)
```

{{< /tab >}}

{{< tab tabNum="9" >}}

```perl
# Exemple en Perl pour mettre à jour l’axe des valeurs secondaire
my $api = AsposeCellsCloud::ApiClient->new(client_id => $client_id, client_secret => $client_secret);
my $axis = AsposeCellsCloud::Object::Axis->new(isAutomaticMajorUnit => 1, maximum => 100);
$api->post_chart_second_value_axis(name => $name, sheet_name => $sheet_name, chart_index => $chart_index, axis => $axis);
```

{{< /tab >}}

{{< tab tabNum="10" >}}

```go
// Exemple en Go pour mettre à jour l’axe des valeurs secondaire
api := cells.NewApiClient("clientId", "clientSecret")
axis := cells.Axis{IsAutomaticMajorUnit: true, Maximum: 100}
api.PostChartSecondValueAxis(name, sheetName, chartIndex, axis)
```

{{< /tab >}}

{{< /tabs >}}