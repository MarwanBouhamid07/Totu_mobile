# 2.1. Décomposer la fonctionnalité « Gérer les catégories »

## Décomposition en tâches

| # | Libellé (action concrète) | Dépendance |
|---|---|---|
| T1 | Créer la migration de la table `categories` (id, nom, description, timestamps) et l'exécuter | Aucune |
| T2 | Créer le modèle `Category` (avec `$fillable`) | T1 |
| T3 | Créer le layout Sidebar + Contenu (Tailwind) réutilisable par les vues | Aucune |
| T4 | Créer `CategoryController` (resource) et déclarer les routes | T2 |
| T5 | Créer la vue liste : tableau qui affiche les catégories (`index`) | T3, T4 |
| T6 | Créer le formulaire d'ajout + méthode `store` avec validation | T4, T5 |
| T7 | Créer le formulaire de modification + méthodes `edit` / `update` | T5, T6 |
| T8 | Ajouter la suppression (`destroy`) avec confirmation | T5 |
| T9 | Tester l'ensemble (ajout, modification, suppression, validation) | T6, T7, T8 |
