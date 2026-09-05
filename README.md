## Rétro-ingénierie de l'Algorithme Yuka : Modélisation Économétrique 

Projet réalisé lors de mon master 1 en Économie de l'entreprise et des marchés (spécialité Big Data, Analyse et Business Intelligence) à l'Université Sorbonne Paris Nord

### Contexte de ce projet : 
Ce projet académique a pour objectif de rétro-concevoir l'algorithme de notation de l'application Yuka, utilisée par plus de 40 millions d'utilisateurs. À partir d'un échantillon de 1000 produits alimentaires, l'enjeu est d'identifier et d'estimer un modèle économétrique capable d'expliquer la distribution des notes (de "Mauvais" à "Excellent") en fonction des caractéristiques nutritionnelles brutes des aliments.  

### Compétences analytiques et techniques mises en oeuvre :
 Ce dépôt démontre ma capacité à mener un projet d'analyse de données de bout en bout, de l'exploration statistique à la modélisation avancée 
 
  - Statistiques Descriptives & Tests d'Hypothèses : Réalisation de tests ANOVA pour évaluer la variance des nutriments selon le score, tests du Chi-deux pour l'impact des variables catégorielles (Bio, Ultra-transformé), et analyse des matrices de corrélation pour écarter les risques de colinéarité.  
  - Économétrie (Modélisation Qualitative) : Implémentation d'un modèle Logit Ordonné (Ordered Logit) adapté à une variable dépendante qualitative ordonnée à 4 modalités.  
  - Validation Statistique : Vérification de l'hypothèse des pentes parallèles via le test de Brant, évaluation de l'ajustement via les critères d'information (AIC, BIC) et le Pseudo R² de McFadden.  
  - Interprétation : Traduction des coefficients en Odds Ratios (rapport des chances) et calcul des effets marginaux moyens (AME) pour formuler des recommandations claires (ex: impact exact d'un gramme de sucre supplémentaire).  
  - Évaluation de la Performance : Construction de matrices de confusion et tracé de courbes ROC, atteignant un AUC de 0.998 pour la détection de la classe "Excellent".  
  - Outils & Langages : Scripting en R (utilisation de dplyr, ggplot2, MASS, caret, pROC, margins).  📂 

### Structure du RéférentielLes éléments constitutifs du livrable sont les suivants :

- Econometrie qualitative-R-Yuka.Rmd : Le script R Markdown commenté contenant le nettoyage, l'analyse exploratoire visuelle, et l'estimation des différents modèles économétriques (complet et simplifié).  
  
- jeu_donnees_yuka.csv : Le dataset comprenant les 1000 observations et les 10 variables étudiées (calories, sucres, sel, graisses saturées, additifs, fibres, protéines, statut bio, indicateur de transformation et score Yuka).  

- Presentation-Modelisation des notations.pdf : Le support visuel de la présentation finale résumant la méthodologie, les tests de validation statistiques et les conclusions d'affaires. 

### Résultats Clés : 
Notre modèle économétrique offre un excellent pouvoir prédictif avec une "Accuracy" de 93% et un Pseudo-R2 de 0.875. L'analyse des Odds Ratios révèle la hiérarchie de l'algorithme :  
- Les leviers majeurs (Bonification) : La certification Bio est le facteur le plus déterminant (multiplie massivement les chances d'une classe supérieure), suivie par l'apport en fibres.  
- Les pénalités critiques : Le sel, la présence d'additifs et l'indicateur "ultra-transformé" (NOVA 4) agissent comme de puissants déclasseurs immédiats vers les scores "Médiocre" ou "Mauvais".  
  
Travail réalisé en groupe de 3.