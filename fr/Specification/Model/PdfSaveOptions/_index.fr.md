---
title: PdfSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/pdfsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : PdfSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **pdfEnregistrerOptions**

 Représente les options d’enregistrement du fichier pdf.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| AfficherTitreDoc| Booléen| Vrai| FAUX|| Indique si la barre de titre de la fenêtre doit afficher le titre du document.|
| ExporterDocumentStructure| Booléen| Vrai| FAUX|| Indique s’il faut exporter la structure du document.|
| EmfRenderSetting| Chaîne| Vrai| FAUX|| Paramètre de rendu du métafichier Emf.|
| Exportation de propriétés personnalisées| Chaîne| Vrai| FAUX|| Spécifie la manière dont CustomDocumentPropertyCollection est exporté vers le fichier PDF.|
| Type d'optimisation| Chaîne| Vrai| FAUX|| Obtient et définit le type d'optimisation PDF.|
| Producteur| Chaîne| Vrai| FAUX|| Obtient et définit le producteur du document PDF généré.|
| CompressionPDF| Chaîne| Vrai| FAUX||Indiquez l'algorithme de compression.|
| FontEncoding| Chaîne| Vrai| FAUX|| Obtient ou définit l’encodage des polices intégrées au format PDF.|
| Filigrane| Classe : RenduFiligrane| Vrai| FAUX|| Obtient ou définit le filigrane à afficher.|
| CalculerFormule| Booléen| Vrai| FAUX|| Indique si calculer les formules avant d'enregistrer le fichier pdf. La valeur par défaut est fausse.|
| Vérifier la compatibilité des polices| Booléen| Vrai| FAUX|| Indique si la compatibilité des polices est vérifiée pour chaque caractère du texte. La valeur par défaut est vraie. Désactiver cette propriété peut donner de meilleures performances. Mais lorsque la police de texte/caractère par défaut ou spécifiée ne peut pas être utilisée pour le restituer, des caractères illisibles (tels qu'un bloc) peuvent apparaître dans le fichier PDF généré. Dans une telle situation, l'utilisateur doit conserver cette propriété comme vraie afin qu'une police alternative puisse être recherchée et utilisée pour restituer le texte à la place ;|
| Conformité| Chaîne| Vrai| FAUX|| Le classeur est converti en PDF conformément à PdfCompliance dans cette propriété.|
| Police par défaut| Chaîne| Vrai| FAUX||Lorsque les caractères du Excel sont Unicode et ne sont pas définis avec la police correcte dans le style de cellule, ils peuvent apparaître sous forme de bloc dans l'image PDF. Définissez DefaultFont tel que MingLiu ou MS Gothic pour afficher ces caractères. Si cette propriété n'est pas définie, Aspose.Cells utilisera la police par défaut du système pour afficher ces caractères Unicode.|
| Une page par feuille| Booléen| Vrai| FAUX|| Si OnePagePerSheet est true , tout le contenu d’une feuille sera affiché sur une seule page. Le format de papier de la configuration de la page ne sera pas valide et les autres paramètres de la configuration de la page prendront toujours effet.|
| Type de page d'impression| Chaîne| Vrai| FAUX|| Indique quelles pages ne seront pas imprimées.|
| Options de sécurité| Classe : PdfSecurityOptions| Vrai| FAUX|| Définissez ces options lorsque la sécurité est nécessaire dans le résultat xls2pdf.|
| souhaitéPPI| Entier| Vrai| FAUX||Définissez le PPI (pixels par pouce) souhaité pour les images de rééchantillonnage et la qualité jpeg. Toutes les images seront converties en JPEG avec le paramètre de qualité spécifié, et les images supérieures au PPI (pixels par pouce) spécifié seront rééchantillonnées. Pixels par pouce souhaités. 220 de haute qualité. Qualité d'écran 150. Qualité de courrier électronique de 96.|
| jpegQualité| Entier| Vrai| FAUX|| Définissez le PPI (pixels par pouce) souhaité pour les images de rééchantillonnage et la qualité jpeg. Toutes les images seront converties en JPEG avec le paramètre de qualité spécifié, et les images supérieures au PPI (pixels par pouce) spécifié seront rééchantillonnées. 0 - 100 % qualité JPEG.|
| Type d'image| Chaîne| Vrai| FAUX|| Représente le type d'image lors de la conversion du graphique et de la forme.|
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
|Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : (EnregistrerOptions)[Enregistreroptions]