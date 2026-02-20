# Treasures & Monsters - Projet UNamur

**Note de confidentialité :** Ce projet a été réalisé dans le cadre du cours d'Algorithmique 2 (Bachelier en Sciences Informatiques) à l'Université de Namur. Pour respecter les règles académiques anti-plagiat, le code source complet est maintenu dans un dépôt privé de l'université. Cependant, je serais ravi d'effectuer une démonstration du jeu et un parcours du code source lors d'un entretien technique.

## Contexte du Projet
"Treasures & Monsters" est un jeu rogue-lite en interface terminal où un héros parcourt un donjon généré de manière procédurale. Le héros doit descendre d'étage en étage pour récolter des trésors tout en survivant aux monstres, avec des contraintes de déplacement strictes (impossible de remonter ou de faire demi-tour horizontalement).

L'objectif de ce projet n'était pas seulement de créer un jeu, mais d'implémenter **quatre grands paradigmes algorithmiques** pour régir la logique du jeu, tout en spécifiant formellement le code avec **OpenJML**.

## L'Architecture Globale
Le moteur du jeu repose sur 4 algorithmes implémentés "from scratch" par notre équipe :

1. **Générer et Tester :** Génération procédurale équilibrée des donjons.
2. **Diviser pour Régner (QuickSort) :** Algorithme de tri optimisé en $O(n \log n)$ pour réarranger les lignes du donjon en fonction de leur dangerosité (les plus difficiles en haut, les plus lucratives en bas).
3. **Recherche Gloutonne (Greedy) :** Calcul algorithmique d'un "score à battre" pour le joueur, en explorant les chemins sous-optimaux avec une profondeur maximale de 5 coups ($O(3^n)$).
4. **Programmation Dynamique (Top-Down Memoization) :** Implémentation du système "d'indice" du jeu, calculant le chemin absolument parfait (Santé restante + Trésors) depuis n'importe quelle case en $O(n \times m)$ grâce à la mémorisation des états.

## Le résultat
Au-delà des exigences algorithmiques, nous avons poussé le projet jusqu'à développer une interface jouable complète en console (en Java pur), permettant de naviguer dans les niveaux, d'utiliser les indices générés par la programmation dynamique, et de suivre les statistiques en temps réel.

## Stack Technique
* **Langage :** Java 17
* **Spécification formelle :** OpenJML
* **Outils :** Git, Scanner (I/O Terminal)
* **Concepts maîtrisés :** Invariants de boucles, Récursivité, Mémoïsation, Tri en-place, Complexité (Temps/Espace).
