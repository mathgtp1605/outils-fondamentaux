# Outils fondamentaux — Python

Travaux pratiques du module "Outils fondamentaux" — IUT Nord Franche-Comté.

## Contenu du dépôt

```
tp/
    tp1.ipynb   — Calcul numérique
    tp2.ipynb   — Arithmétique et nombres premiers
    tp3.ipynb   — Polynômes et fonctions
    tp4.ipynb   — Matrices et systèmes linéaires
    tp5.ipynb   — Synthèse : chiffrer, déchiffrer, casser
    tp6.ipynb   — Géométrie du plan

projet/
    projet.ipynb  — Solveur hybride Newton + Dichotomie
    README_projet.md
```

## TP

Chaque notebook contient les exercices du TP et les réponses dans les cellules de code. Pour exécuter : ouvrir dans JupyterLite (https://cours.gclab.fr) ou dans Jupyter localement, puis `Maj+Entrée` cellule par cellule.

## Projet

Le projet compare la méthode de Newton et la dichotomie pour trouver des racines de fonctions. Il implémente un solveur hybride qui détecte automatiquement quand Newton diverge ou cycle, et bascule sur la dichotomie. Voir `projet/README_projet.md` pour les détails.

## Comment lancer

Les notebooks fonctionnent directement dans JupyterLite sans installation. Pour un usage local :

```bash
pip install notebook
jupyter notebook
```

Puis ouvrir le fichier `.ipynb` voulu.

## Note sur l'usage de l'IA

Les solutions des TPs et le projet ont été réalisés avec l'aide d'un assistant IA (Claude). Les résultats ont été vérifiés par exécution.
