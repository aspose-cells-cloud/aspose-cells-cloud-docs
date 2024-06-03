---
title: Paramètre du classeur
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/workbooksettings/
description: "Aspose.Cells Spécification du modèle cloud : WorkbookSettings. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, paramètres du classeur
weight: 50
---
## **Paramètres du classeur**

 Représente tous les paramètres du classeur.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Compresser automatiquement les images| Booléen| Vrai| FAUX||Spécifie une valeur booléenne qui indique que l'application compresse automatiquement les images dans le classeur.|
| Récupération automatique| Booléen| Vrai| FAUX|| Indique si le fichier est marqué pour la récupération automatique.|
| Version de construction| Chaîne| Vrai| FAUX|| Spécifie la version publique incrémentielle de l'application.|
| Mode Calc| Chaîne| Vrai| FAUX|| Il précise s'il faut calculer les formules manuellement, automatiquement ou automatiquement, sauf pour les opérations sur plusieurs tables.|
| ID de calcul| Chaîne| Vrai| FAUX|| Spécifie la version du moteur de calcul utilisé pour calculer les valeurs dans le classeur.|
| Vérifier la compatibilité| Booléen| Vrai| FAUX|| Indique si la compatibilité est vérifiée lors de l'enregistrement du classeur. Remarques : La valeur par défaut est true.|
| CheckExcelRestriction| Booléen| Vrai| FAUX||Vérifier ou non la restriction du fichier Excel lorsque l'utilisateur modifie les objets liés aux cellules. Par exemple, Excel ne permet pas de saisir une valeur de chaîne supérieure à 32 Ko. Lorsque vous saisissez une valeur supérieure à 32 Ko, par exemple par Cell.PutValue(string), si cette propriété est vraie, vous obtiendrez une exception. Si cette propriété est fausse, nous accepterons votre valeur de chaîne d'entrée comme valeur de la cellule afin que vous puissiez ultérieurement générer la valeur de chaîne complète pour d'autres formats de fichiers tels que CSV. Toutefois, si vous avez défini un type de valeur non valide pour le format de fichier Excel, vous ne devez pas enregistrer le classeur au format de fichier Excel ultérieurement. Sinon, une erreur inattendue pourrait se produire pour le fichier Excel généré.|
| CrashSave| Booléen| Vrai| FAUX|| indique si l'application a enregistré le fichier de classeur pour la dernière fois après un crash.|
| CréerCalcChain| Booléen| Vrai| FAUX|| Si cela crée une chaîne de formules calculées. La valeur par défaut est fausse.|
| DataExtractLoad| Booléen| Vrai| FAUX||indique si l'application a ouvert le classeur pour la dernière fois pour la récupération de données.|
| Date1904| Booléen| Vrai| FAUX|| Obtient ou définit une valeur qui indique si le classeur utilise le système de date 1904.|
| AfficherDrawingObjects| Chaîne| Vrai| FAUX|| Indique si et comment afficher les objets dans le classeur.|
| Activer les macros| Booléen| Vrai| FAUX|| Activer les macros ;|
| PremierongletVisible| Entier| Vrai| FAUX|| Obtient ou définit le premier onglet de feuille de calcul visible.|
| MasquerPivotFieldList| Booléen| Vrai| FAUX|| Obtient et définit si la liste des champs du tableau croisé dynamique est masquée.|
| IsDefaultEncrypted| Booléen| Vrai| FAUX|| Indique si le chiffrement du classeur avec le mot de passe par défaut si Structure et Windows du classeur sont verrouillés.|
| Est caché| Booléen| Vrai| FAUX|| Indique si ce classeur est masqué.|
| EstHScrollBarVisible| Booléen| Vrai| FAUX|| Obtient ou définit une valeur indiquant si la feuille de calcul générée contiendra une barre de défilement horizontale.|
| Estminimisé| Booléen| Vrai| FAUX|| Représente si la feuille de calcul générée sera ouverte en taille réduite.|
| EstVScrollBarVisible| Booléen| Vrai| FAUX||Obtient ou définit une valeur indiquant si la feuille de calcul générée contiendra une barre de défilement verticale.|
| Itération| Booléen| Vrai| FAUX|| Indique si le calcul itératif est activé pour résoudre les références circulaires.|
| Code de langue| Chaîne| Vrai| FAUX|| Obtient ou définit la langue de l'interface utilisateur de la version du Workbook en fonction du CountryCode qui a enregistré le fichier.|
| ChangementMax| Flottant| Vrai| FAUX|| Renvoie ou définit le nombre maximum de modifications pour résoudre une référence circulaire.|
| MaxItération| Entier| Vrai| FAUX|| Renvoie ou définit le nombre maximum d'itérations pour résoudre une référence circulaire.|
| Paramètres de mémoire| Chaîne| Vrai| FAUX|| Obtient ou définit les options d'utilisation de la mémoire. La nouvelle option sera considérée comme option par défaut pour les feuilles de calcul nouvellement créées mais ne prendra pas effet pour les feuilles de calcul existantes.|
| NombreDécimalSéparateur| Chaîne| Vrai| FAUX|| Obtient ou définit le séparateur décimal pour le formatage/analyse des valeurs numériques. La valeur par défaut est le séparateur décimal de la région actuelle.|
| Séparateur de groupe de nombres| Chaîne| Vrai| FAUX|| Obtient ou définit le caractère qui sépare les groupes de chiffres à gauche de la virgule dans les valeurs numériques. La valeur par défaut est le séparateur de groupe de la région actuelle.|
| AnalyseFormulaOnOpen| Booléen| Vrai| FAUX||Indique si l'analyse de la formule lors de la lecture du fichier.|
| Précision telle qu'affichée| Booléen| Vrai| FAUX|| Vrai si les calculs dans ce classeur seront effectués en utilisant uniquement la précision des nombres tels qu'ils sont affichés|
| RecalculerAvantEnregistrer| Booléen| Vrai| FAUX|| Indique s'il faut recalculer avant d'enregistrer le document.|
| ReCalculerOnOuvert| Booléen| Vrai| FAUX|| Indique s'il faut recalculer toutes les formules à l'ouverture du fichier.|
| RecommanderLecture seule| Booléen| Vrai| FAUX|| Indique si l’option Lecture seule recommandée est sélectionnée.|
| Région| Chaîne| Vrai| FAUX|| Obtient ou définit les paramètres régionaux du classeur.|
| Supprimer les informations personnelles| Booléen| Vrai| FAUX|| True si les informations personnelles peuvent être supprimées du classeur spécifié.|
| RéparationCharge| Booléen| Vrai| FAUX|| Indique si l’application a ouvert le classeur pour la dernière fois en mode sans échec ou en mode réparation.|
| partagé| Booléen| Vrai| FAUX|| Obtient ou définit une valeur qui indique si le classeur est partagé.|
| FeuilleTabBarLargeur| Entier| Vrai| FAUX|| Largeur de la barre d'onglets de la feuille de calcul (en 1/1000 de la largeur de la fenêtre).|
| Afficher les onglets| Booléen| Vrai| FAUX||Obtient ou définit une valeur si les onglets du classeur sont affichés.|
| Mettre à jour la bordure de cellules adjacentes| Booléen| Vrai| FAUX|| Indique si la bordure des cellules adjacentes est mise à jour.|
| Type de liens de mise à jour| Chaîne| Vrai| FAUX|| Obtient et définit la manière dont les liens externes sont mis à jour lorsque le classeur est ouvert.|
| Hauteur de la fenêtre| Flottant| Vrai| FAUX|| La hauteur de la fenêtre, en unité de point.|
| FenêtreGauche| Flottant| Vrai| FAUX|| La distance entre le bord gauche de la zone client et le bord gauche de la fenêtre, en unité de point.|
| FenêtreHaut| Flottant| Vrai| FAUX|| Distance entre le bord supérieur de la zone client et le bord supérieur de la fenêtre, en unité de point.|
| Largeur de la fenêtre| Flottant| Vrai| FAUX|| La largeur de la fenêtre, en unité de point.|
| Auteur| Chaîne| Vrai| FAUX|| Obtient et définit l'auteur du fichier.|
| Vérifier le format de numéro personnalisé| Booléen| Vrai| FAUX|| Indique si la vérification du format de numéro personnalisé lors de la définition de Style.Custom.|
| Type de protection| Chaîne| Vrai| FAUX|| Obtient le type de protection du classeur.|
| Paramètres de mondialisation| Classe : Paramètres de mondialisation| Vrai| FAUX|| Obtient et définit les paramètres de globalisation.|
| Mot de passe| Chaîne| Vrai| FAUX||Représente le mot de passe de chiffrement du fichier Workbook.|
| Protection en écriture| Classe : Protection en écriture| Vrai| FAUX|| Fournit l’accès aux options de protection en écriture du classeur.|
| EstChiffré| Booléen| Vrai| FAUX|| Obtient une valeur qui indique si un mot de passe est requis pour ouvrir ce classeur.|
| EstProtégé| Booléen| Vrai| FAUX|| Obtient une valeur qui indique si la structure ou la fenêtre du Workbook est protégée.|
| MaxRow| Entier| Vrai| FAUX|| Obtient l'index de ligne maximum, en base zéro.|
| ColonneMax| Entier| Vrai| FAUX|| Obtient l'index de colonne maximum, en base zéro.|
| Chiffres significatifs| Entier| Vrai| FAUX|| Obtient et définit le nombre de chiffres significatifs. La valeur par défaut est .|
| Vérifier la compatibilité| Booléen| Vrai| FAUX|| Indique si vous vérifiez la compatibilité avec les versions antérieures lors de l'enregistrement du classeur.|
| Taille de papier| Chaîne| Vrai| FAUX|| Obtient et définit le format de papier d'impression par défaut.|
| MaxRowsOfSharedFormula| Entier| Vrai| FAUX|| Obtient et définit le nombre maximal de lignes de la formule partagée.|
| Conformité| Chaîne| Vrai| FAUX|| Spécifie la version OOXML du document de sortie. La valeur par défaut est Ecma376_2006.|
| CitationPréfixeVersStyle| Booléen| Vrai| FAUX||Indique si la propriété est définie lors de la saisie de la valeur de chaîne (qui commence par un guillemet simple) dans la cellule|
| Paramètres de formule| Classe : Paramètres de formule| Vrai| FAUX|| Obtient les paramètres des fonctionnalités liées aux formules.|
| ForcerCompletCalculer| Booléen| Vrai| FAUX|| Calcule entièrement à chaque fois qu'un calcul est déclenché.|

