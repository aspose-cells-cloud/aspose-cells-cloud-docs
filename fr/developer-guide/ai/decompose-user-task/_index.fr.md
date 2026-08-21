---
title: "Aspose.Cells Cloud AI – API de décomposition des tâches utilisateur (v4.0) | Planification SMART des tâches"
second_title: "Document"
articleTitle: "Comment convertir les objectifs utilisateurs en plans d’actions séquentiels à l’aide de l’API de décomposition des tâches Aspose.Cells Cloud"
linktype: "Décomposer la tâche utilisateur"
type: docs
url: /fr/decompose-user-task/
keywords: "Aspose.Cells AI, API de décomposition des tâches, planification SMART des tâches, import Redmine, automatisation de projet"
description: "Transformez des objectifs libres en listes de tâches SMART dotées d’estimations temporelles à l’aide d’Aspose.Cells Cloud AI. Obtenez une sortie CSV/XLSX pour Redmine, Jira ou Azure DevOps en une seule requête PUT."
weight: 100
---

L’endpoint **DecomposeUserTask** fournit une interface REST permettant de transformer une description de tâche libre en un plan d’action détaillé et séquentiel conforme aux critères SMART. Il attribue automatiquement des estimations de temps exprimées en heures, formate la sortie pour une importation compatible Redmine et génère des nœuds de jalons de projet. En fournissant uniquement la liste brute des tâches et des estimations de temps optionnelles, l’API renvoie un fichier prêt à l’emploi (CSV, XLSX, etc.) pouvant être directement importé dans des outils de gestion de projet, automatisant ainsi la décomposition des tâches et réduisant l’effort manuel.

## **API de décomposition des tâches utilisateur**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête :**

| Nom du paramètre | Type   | Emplacement | Obligatoire/Optionnel | Description                                                                                                                                                                                                                                                                              |
| :---------------- | :----- | :---------- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription  | string | Corps       | Obligatoire          | Une description en texte brut de l’objectif global de l’utilisateur. Le service analyse cette description et génère des tâches individuelles. Exemple : « Lancer une campagne marketing pour le T3, incluant la création de contenu, l’envoi d’e-mails et la publicité sur les réseaux sociaux. » |

### **Réponse**

Réponse réussie (200 OK)  
Type de contenu : `application/octet-stream` (flux binaire)

En‑têtes :

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <taille en octets>`

La même structure est utilisée pour les formats XLSX/ODS, avec les colonnes placées dans la première feuille de calcul.

**Codes d’état HTTP**

| Code | Signification              | Description                                                       |
| ---- | -------------------------- | ----------------------------------------------------------------- |
| 200  | OK                         | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête           | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé               | Jeton JWT invalide ou manquant.                                   |
| 413  | Charge utile trop grande    | Le fichier uploadé dépasse la taille limite.                     |
| 500  | Erreur interne du serveur   | Erreur inattendue du serveur.                                     |

**Exemple de réponse d’erreur (400 Mauvaise requête)**

```json
{
  "code": "InvalidParameter",
  "message": "Le champ « TaskDescription » est obligatoire et ne peut pas être vide."
}
```

**Exemple de corps de requête (JSON)**

```json
{
  "TaskDescription": "Développer une API web pour une fonctionnalité de scission de tâches sur le système existant."
}
```

**Exemple de réponse**  
L’API renvoie un flux binaire contenant le fichier généré. Pour prévisualiser les quelques premières lignes d’une réponse au format CSV, décodez le flux et affichez la ligne d’en‑tête, par exemple :

```
ID,Sujet,Responsable,Duration estimée,Description
1	Collecte des besoins pour l’API de scission de tâches	Analyste métier	8	Collecter les exigences fonctionnelles et non fonctionnelles, les user stories et les critères d’acceptation pour le nouvel endpoint de scission de tâches.
2	Spécification de l’API (OpenAPI)	Analyste métier	6	Définir le contrat OpenAPI pour POST /tasks/split, incluant le schéma des requêtes, les formats de réponse, les codes d’erreur et les exigences de sécurité.
3	Algorithme de scission et conception du modèle de données	Architecte solution	5	Concevoir l’algorithme central qui divise une tâche parente en sous-tâches, et étendre le modèle de données (tables/bases de données / entités) afin de stocker la hiérarchie et les métadonnées.
4	Avis d’intégration architecturale	Architecte solution	4	Analyser l’impact sur les services existants, les flux d’événements et les migrations de base de données ; produire le plan d’intégration.
...
```

## Où utiliser l’API de décomposition des tâches utilisateur ?

- **Lancement de projet** : Convertir un cahier des charges de haut niveau en une liste de tâches compatible Redmine dotée d’estimations temporelles, permettant une planification immédiate des sprints.
- **Automatisation marketing** : Décomposer les objectifs de campagne en étapes exécutables, exporter au format CSV, et importer dans des outils de gestion des tâches pour une coordination inter-équipes.
- **Allocation des ressources** : Générer des estimations horaires pour chaque sous-tâche, permettant aux responsables d’équilibrer la charge de travail entre les membres de l’équipe avant le début du projet.
- **Suivi des jalons** : Créer automatiquement des nœuds de jalon pouvant être synchronisés avec des outils de diagrammes de Gantt, garantissant que chaque phase possède un livrable clairement défini.

## Pourquoi utiliser l’API de décomposition des tâches utilisateur ?

- **Résultat conforme aux critères SMART** : chaque tâche générée respecte les critères Spécifique, Mesurable, Atteignable, Réaliste et Temporellement délimité.
- **Estimation temporelle horaire intégrée** : élimine le besoin de calculs manuels et améliore la précision des prévisions.
- **Formats de fichier prêts à l’importation** (CSV, XLSX, etc.) : facilite l’intégration avec Redmine, Jira, Azure DevOps et d’autres plateformes de gestion de projet.
- **Automatisation en une seule requête** : permet la décomposition des tâches via une unique requête, accélérant ainsi la mise en route des projets et minimisant l’effort manuel.

## Comment utiliser l’API de décomposition des tâches utilisateur à l’aide des SDK ?

### Spécification de l’API de décomposition des tâches utilisateur

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">Spécification de l’API de décomposition des tâches utilisateur</a> fournit une interface de programmation accessible publiquement permettant d’exécuter directement des interactions REST depuis un navigateur web.

## SDK pour l’API Excel

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation des SDK constitue la méthode la plus rapide de développement, car elle abstractise les détails de bas niveau et permet d’appeler l’endpoint DecomposeUserTask à l’aide d’un code concis.  
Veuillez consulter le <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">dépôt GitHub</a> pour obtenir la liste complète des SDK Aspose.Cells Cloud.  
Les exemples de code ci‑dessous illustrent comment interagir avec les services web Aspose.Cells à l’aide de divers SDK :

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}