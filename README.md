

# Mots-clés :
-	Complexité * : Etude formelle de la quantité de ressources nécessaire à l'exécution de cet algorithme
-	NP Complet * : Problème de décision qui vérifie deux propriétés : trouver un temps polynoial + pas de réduction polynomiale
-	Algorithme heuristique * : Méthode de calcul qui fournit rapidement une solution réalisable, pas nécessairement optimale ou exacte
-	Réduction polynomiale * : Si on réduit une fonction polynomiale et qu'on trouve une autre fonction, alors l'autre fonction est une réduction polynomiale.
-	Algorithme de complexité exponentielle * : 
-	P et NP * : Cf def
-	Cycle hamiltonien et eulérien * : Cf prosit précèdent (Sommets / arrêtes)
-	Complexité spatiale / temporelle * :
	- On les calcules séparéments
	-	Spaciale : Nombre maximum de cases mémoire utilisés simultanément pendant un calcul
	-	Temporelle : Nombre d'étapes de calculs avant d'arriver  à un réusltat
-	Algorithme de certificat * : Pour NP
-	Codage en binaire
-	Graphe orienté / non orienté
-	Machine de Turing
-	Problème du voyageur de commerce * : cf prosit
-	Plus court chemin
-	Problème de décision / optimisation * : décision = V/F -- Optimisation = minimiser ou maximiser une fonction sur un ensemble
-	Complexité asymptotique * :
(* = à définir)

# Contexte :

Quoi ?
-	Trouver le chemin le plus court entre les feux tricolores

Comment ?
-	En utilisant les algorithme / méthodes scientifiques

Pourquoi ?
-	Optimiser

# Contraintes :
-	Utiliser une solution théorique
-	Une après-midi
Problématique :
-	Quel algorithme permettrait de trouver le chemin le plus optimisé ?
-	Comment maîtriser la complexité algorithmique ?

# Généralisation :
-	Modélisation
-	Optimisation

# Hypothèses : 
-	P est != de NP
-	Un algo heuristique permet de trouver le chemin le plus court entre deux sommets d’un graphe
-	Un algo heuristique est une approximation d’un résultat (pas le meilleur, mais il marche).
-	Pas d’algo avec une complexité > asymptotique
-	Voyageur de commerce = hamiltonien avec des poids


# Plan d'action :

##	Problème de la tournée du voyageur de commerce

- Un voyageur de commerce doit visiter un certain nombre de villes et chaque ville, une et une seule fois. 
- Pondéré (poids)
- Il doit minister la distance totale parcourue. 
- On représente le problème par un graphe, chaque ville un sommet, et une arrête entre chaque fille
- On doit chercher un Hamiltonien minimum

- Personne n'a de solution EXACTE

Pour trouver : 
- **Algorithmes exacts** : solution optimale, globale, mais très llongs si le problème est difficile
	- Séparation et évaluation
	- Programmation linéaire pour l'optimisation continue
	- Programmation dynamique
- **Algorithmes locaux :** Garantissent une situation locale
	- Méthodes descente
	- Gradient / Newton pour l'optimisation continue
- **Métaheuristiques :** Très peu de garanties sur la qualité de la solution, mais très rapide
	- Algorithme glouton
	- Recherche tabou
	- Recherche à voisinages variables (VNS)
	- Algorithmes génétiques
	- Algorithme d'aproximation : on fais l'arbre couvrant minimum, puis on passe toujours par la gauche (sauf si on bloque), mais si un sommet a déjà été visité, on ne le marque pas

##	Graphe (non) orienté avec | sans poids

? On met une flèche


##	Problème de décision (# classe de résolution de pb)

- Décision : Oui ou Non
- 

##	P et NP, Complexité (spatiale, temporelle) ⇒ Ordonnancement

*Rappel :* 
- Un polynôme c'est une fonction avec des ***puissances*** (fonction polynomiale).
- La complexité est nomée O([complexité])
- Le nombre de complexité à calculer est en fonction du nombre de paramètres; une complexité par paramètre
- P et NP sont des problèmes de décisions (vrai ou faux)
 - Une complexité peut-être Spatiale / mémoire / temporelle

**P et NP** permettent de trouver la **complexité polynomiale** *

- **P** : Utilisé pour des algorithmes très simple à faire, très facile à vérifier. 
	- Ex : Listes / Eulérien / Nombres primaires / Rubiscube...
	- On peut résoudre en linéaire avec O(n^m)
- **NP** : Utilisé pour des algorithmes difficile à faire, facile à véirifier.
	- Ex : TSP / N-Coloriage / Factorisation...
	- Il s'appui sur un pattern lors du calcul de la complexité pour **vérifier une polynomiale**
	- Si le polynôme comporte plusieurs monômes, la complexité est basée sur le plus impactant (on fais des estimations)

Certains algorithmes se ressemblent, on dits qu'ils sont dans le **CORE NP**.
- Si on arrive à trouver la complexité d'un, on peut trouver la complexité d'un autre
- On dit alors que l'algorithme A se **réduit** dans B
-  Le princie pour savoir si deux algorithmes sont **CORE NP** : *Turing-Reduction*
- Si on utilise une seule fois un solveur dans un autre solveur (pour une traduction d'un vers l'autre),on utilise la *Karp-réduction*.
- Si ça marche dans les deux sens, on peut  dire qu'ils sont *NP-Complet*
- Ex : Graph-coloring ⇒ SAT

**Nb :** La turing réduction permet de comparer la complexité entre les différents problèmes de décision.

Il existe plusieurs types de NP :
- NP-Difficile : Si il passe par une turing reduction
- NP-Facile : Simple NP sans turing (pas dans le CORE)
- NP Equivalent : Les deux à la fois

La première personne qui répond à P = NP ⇒ 1M de $


##	Réduction polynomiale
Outil d'information théorique
- Si on réduit une fonction polynomiale et qu'on trouve une autre fonction, alors l'autre fonction est une réduction polynomiale.


##	Prouver que c’est NP-COMPLET
Prouver que B est NP-Complet revient à dire:
- qu'il existe un certificat polynômial pour B
- Tous les problèmes de la classe NP se ramène à celui-ci via une réduction polynomiale. CAD que le pb est moins difficile que les autres pb de la classe NP.



## Diverses types de complexités  :
On regarde le **comportement asymtotique** du nombre d'instructions 

**Technique :** Incrémenter et compter

On compare C(n+1) avec C(n), il existe 5 solutions

- SI C(n+1) = C(n) == **Constante**
- Si C(n+1) = C(n) + 1 ==.**Linéaire**
- complexité **logarithmique** == (Ex : Autant de pompes qu'on peut diviser n/2) (au bout d'un moment elle s'arrête)
- **Polynomiale** == Deux boucles imbriqués (n²) entre nombre jours et pompes
 - **exponentielle** == Quand on fait un x2 dans un algo
 - 
## Corbeille




