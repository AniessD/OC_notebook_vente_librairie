# Analyse des ventes d'une librairie avec Python

## Objectif du projet
Ce projet a été réalisé dans le cadre de ma formation OpenClassrooms. Il consiste à analyser les ventes d'une librairie en ligne, afin d'aider la direction commerciale à : 
- comprendre les performances globales du site,
- identifier les comportements clients,
- détecter les produits stratégiques (top/flop),
- proposer des axes d'amélioration marketing

L'analyse est réalisée en Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy) dans un Notebook Jupyter.

## Données
Les données couvrent mars 2021 à février 2023 et proviennent de 3 fichiers : 
- customers : Informations clients
- products : Catalogue produits
- transactions : Historique des ventes

## Préparation et nettoyage des données
- conversion des dates,
- fusion des 3 fichiers,
- identification et exclusion des clients BtoB,
- calcul de l'âge réel des clients,
- création d'indicateurs dérivés (panier moyen, fréquence d'achat, ...)

## Analyses réalisées
1. Profil des clients
   - Identification d'un groupe VIP
   - Répartition par genre (52% femmes / 48% hommes)
   - Répartition par âge (sur-représentation des 18 ans => âge mini d'inscription)

2. Evolution dans le temps
   - CA mensuel stable, sans saisonnalité marquée
   - Nombre de transactions stabilisé
   - Arrôt total de recrutement de nouveaux clients à partir de février 2022

3. Produits
   - 24 produits invendus => potentielle suppression
   - Analyse par catégories (0 = entrée de gamme, 1 = milieu de gamme, 2 = premium)

4. Comportement clients
   - Genre - Catégorie : lien significatif (Chi-2)
   - Age - Dépenses : corrélation faible (Spearman)
   - Age - Fréquence d'achat : corrélation faible (Spearman)
   - Age - Panier moyen : corrélation modérée (Spearman)
   - Age - Catégorie : lien significatif (Kruskal-Wallis)

## Recommandations stratégiques
- Cibler les femmes de 35-55 ans avec les produits de catégorie 1
- Développer une offre pour les 20-30 ans avec les produits premium
- Revoir le cataglogue (produits invendus ou très peu vendus)
- Relancer acquisition client

## Compétences
- Analyses statistiques
- Visualisations
- Analyses de séries temporelles (moyennes mobiles)
- Recommandations stratégiques orientées business
