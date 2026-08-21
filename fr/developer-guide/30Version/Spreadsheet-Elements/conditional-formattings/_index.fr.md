---
title: "Travail avec le formatage conditionnel Excel"
second_title: "Document"
linktype: "Formatage conditionnel"
type: docs
url: /fr/conditional-formattings/
aliases: [  /fr/working-with-conditional-formatting/ ]
keywords: "Excel, Formatage conditionnel, Aspose.Cells Cloud, API"
description: "L’API Aspose.Cells Cloud pour Excel fournit des points de terminaison permettant de récupérer, d’ajouter, de modifier et de supprimer des règles de formatage conditionnel, permettant ainsi une analyse visuelle dynamique des données de la feuille de calcul."
weight: 100
ArticleTitle: "Travail avec le formatage conditionnel Excel – Guide API"
---

Le formatage conditionnel dans Excel vous permet de mettre en surbrillance des cellules avec une couleur spécifique, en fonction de la valeur de la cellule.

Utilisez le formatage conditionnel pour vous aider à explorer visuellement et analyser vos données, détecter des problèmes critiques, et identifier des modèles et tendances.

Le formatage conditionnel facilite la mise en surbrillance des cellules ou plages de cellules intéressantes, la mise en évidence des valeurs inhabituelles, et la visualisation des données à l’aide de barres de données, d’échelles de couleurs et de jeux d’icônes correspondant à des variations spécifiques dans les données.

Un formatage conditionnel modifie l’apparence des cellules en fonction des conditions que vous spécifiez. Si les conditions sont vraies, la plage de cellules est formatée ; si les conditions sont fausses, la plage de cellules reste inchangée. De nombreuses conditions intégrées sont disponibles, et vous pouvez également créer vos propres conditions (y compris en utilisant une formule qui renvoie **VRAI** ou **FAUX**).

L’API Aspose.Cells Cloud fournit un ensemble de points de terminaison pour gérer les règles de formatage conditionnel de manière programmatique. Les opérations suivantes sont disponibles :

- **Obtenir les formatages conditionnels d’une feuille de calcul** – Récupère toutes les règles de formatage conditionnel appliquées à une feuille de calcul.  
  - **Méthode :** `GET`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Paramètres :** `fileName` (chaîne, obligatoire), `sheetName` (chaîne, obligatoire), paramètres de requête facultatifs tels que `folder`, `storageName`  
  - **Exemple cURL :**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **Obtenir un formatage conditionnel** – Renvoie une règle spécifique de formatage conditionnel via son identifiant.  
  - **Méthode :** `GET`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Paramètres :** `index` (entier, obligatoire) identifie la position de la règle.  
  - **Exemple cURL :**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **Ajouter une zone de cellules pour une condition de formatage** – Ajoute une plage de cellules qui sera affectée par le formatage conditionnel spécifié.  
  - **Méthode :** `POST`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Corps de la requête (JSON) :** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **Exemple cURL :**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **Ajouter une condition à un formatage conditionnel** – Définit une nouvelle condition (par exemple, valeur, formule) pour une règle de formatage existante.  
  - **Méthode :** `POST`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **Corps de la requête (JSON) :** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **Exemple cURL :**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **Ajouter un formatage conditionnel** – Crée une règle complète de formatage conditionnel, incluant le type et le style.  
  - **Méthode :** `POST`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Corps de la requête (JSON) :**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **Exemple cURL :**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **Effacer tous les formatages conditionnels** – Supprime toutes les règles de formatage conditionnel de la feuille de calcul cible.  
  - **Méthode :** `DELETE`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **Exemple cURL :**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **Supprimer une zone de cellules d’un formatage conditionnel** – Supprime une zone de cellules précédemment définie d’une règle de formatage conditionnel.  
  - **Méthode :** `DELETE`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **Exemple cURL :**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **Supprimer un formatage conditionnel** – Supprime une règle complète de formatage conditionnel de la feuille de calcul.  
  - **Méthode :** `DELETE`  
  - **Point de terminaison :** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **Exemple cURL :**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

Ces exemples illustrent la méthode HTTP requise, le modèle d’URL, les paramètres clés et les charges utiles de requête pour chaque opération. Utilisez le SDK approprié (C#, Java, Python, etc.) pour obtenir des extraits de code spécifiques à votre langage, si souhaité.