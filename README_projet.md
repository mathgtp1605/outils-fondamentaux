# Projet : Solveur hybride Newton + Dichotomie

## Ce que fait le projet

Ce projet implémente et compare deux méthodes classiques pour trouver les racines d'une fonction :

- **La dichotomie** : robuste, toujours convergente si on lui donne un intervalle où la fonction change de signe, mais lente (~33 itérations pour une précision de 1e-10).
- **La méthode de Newton** : très rapide quand elle converge (moins de 10 itérations), mais elle peut diverger ou cycler selon le point de départ et la fonction.

Le cœur du projet est un **solveur hybride** qui tente Newton en premier, détecte si Newton cycle ou sort de l'intervalle, et bascule automatiquement sur la dichotomie si nécessaire.

## Notions du module mobilisées

- Calcul numérique et flottants (TP1) : précision, tolérance, comparaison de flottants
- Polynômes et recherche de racines (TP3) : Newton, dichotomie, évaluation de fonctions

## Comment lancer

Ouvrir `projet.ipynb` dans JupyterLite ou Jupyter, puis exécuter les cellules de haut en bas avec `Maj+Entrée`.

Aucune bibliothèque externe n'est nécessaire (stdlib Python uniquement).

## Ce qu'on observe

- Newton converge en 5 itérations sur x²-2, contre 33 pour la dichotomie.
- Sur x³-2x+2 depuis x=0, Newton alterne indéfiniment entre 0 et 1 : le solveur hybride détecte ce cycle et bascule sur la dichotomie.
- Le solveur hybride est aussi rapide que Newton quand Newton marche, et aussi robuste que la dichotomie quand Newton échoue.

## Limite identifiée

Le critère de bascule (sortie de l'intervalle ou cycle détecté sur 3 points) peut rater des divergences lentes. Une amélioration possible serait de surveiller si |f(x)| augmente entre deux itérations.
