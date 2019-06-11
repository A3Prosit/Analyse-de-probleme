
# Mots-clés :
-	Complexité : cb de calcul ou mémoire il faut
-	NP Complet : classe spécifique de problème qui peuvent être résolu par un algo de brute force. Tous les pb np-complet peuvent être résolus avec le même algo
-	Algorithme heuristique :  aka un métaheuristique, algo d'opti  où il n'y a pas de méthode classique. En général se sont des algo sotchastiques (guess) ils progressent vers l'extremum global d'une fonction
-	Réduction polynomiale : transfo un algo en un autre
-	Algorithme de complexité exponentielle : exp(n)
-	P et NP : polynomial, non-deterministic polynomial
-	Cycle hamiltonien et eulérien : respectivement tt les somets 1 fois et tt les arêtes 1 fois
-	Complexité spatiale / temporelle : cb de calcul cb de mémoire
-	Algorithme de certificat : un certificat est une info permettant de certifier que l'entrée est correcte = façon de montrer que la réponse est "oui"
-	Codage en binaire
-	Graphe orienté / non orienté
-	Machine de Turing
-	Problème du voyageur de commerce : TSP, cycle hamiltonien de poids minimum
-	Plus court chemin
-	Problème de décision / optimisation : uestion qui est oui ou non. On veut savoir si il existe un algo qui réponds à la question
-	Complexité asymptotique : c'est pas une des complexité mais la façon de trouver la complexité (et c'est le 5)
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

Un voyageur de commerce doit visiter un certain nombre de villes, et chaque ville une et une seule fois. Etant donné des distances entre chaque paire de villes, il doit minimiser la distance totale parcourue

On peut représenter ce problème par un graphe : chaque ville correspond à un sommet et chaque arête à une paire de villes pouvant être visitées l’une à la suite de l’autre. 
Le problème correspond à trouver un tour complet (circuit Hamiltonien) dans ce graphe qui minimise la somme des distances (f). 
L’ensemble X correspond à un chemin dans le graphe, soit une liste de villes, et l’ensemble Ω ⊂ X est l’ensemble des circuit Hamiltoniens.
Le nombre de solutions pour n villes est de (n − 1)!/2.
on cherche le cycle hamiltonien de poids minimum



##	Graphe (non) orienté avec / sans poids

##	Problème de décision (# classe de résolution de pb)
le halting problem ?

Problème de décision / optimisation : gestion qui est oui ou non. On veut savoir si il existe un algo qui réponds à la question

existe: 3-sat


##	P et NP, Complexité (spatiale, temporelle) ⇒ Ordonnancement

Un grand nombre de problèmes sont difficiles. Des solutions exactes sont envisageables, mais dans un d´elai acceptable, on se contentera de solutions approchées obtenues par des m´ethodes heuristiques.

instance vs problème 
min x∈X {f_a(x) : x ∈ Ω_a}
où X est un ensemble discret et fini et Ω ⊆ X est l’ensemble des solutions réalisables.

Une instance du problème est une formulation du modèle dans laquelle a est déterminé

compléxité:
Borne supérieure (“au plus, de l’ordre de”) :
 O( f(n) ) = { t : N → R + : il existe c > 0 et n0 ∈ N tels que t(n) ≤ cf(n) pour tout n ≥ n0 o . }
 On note t ∈ O( f(n)) ou t(n) ∈ O( f(n) ) et on dit que t(n) est de l’ordre de f(n)

Borne inférieure (“au moins, de l’ordre de”) :
 Ω( f(n) ) = { t : N → R + : il existe c > 0 et n_0 ∈ N tels que t(n) ≥ cf(n) pour tout n ≥ n_0 } .
 
Équivalence (“de l’ordre de”) : 
Θ( f(n) ) = { t : N → R + : il existe c1, c2 > 0 et n_0 ∈ N tels que c1f(n) ≤ t(n) ≤ c2f(n) ∀n ≥ n_0 o = O f(n)  ∩ Ω f(n) }

Borne supérieure stricte (“est négligeable par rapport à”) :
 t(n) ∈ o (f(n) <=> pour tout c > 0, il existe n_0 ∈ N tel que t(n) ≤ cf(n) pour tout n ≥ n_0 
 ⇔ lim n→∞ t(n)/f(n) = 0.
 
Borne inférieure stricte (“est prépondérant par rapport à”) :
 t(n) ∈ ω( f(n) ) ⇔ pour tout c > 0, il existe n_0 ∈ N tel que t(n) ≥ cf(n) pour tout n ≥ n_0 ⇔ limn→∞ t(n)/f(n) = ∞



##	Réduction polynomiale

transfo un pb en un autre, exemple: mario en 3-sqt

##	Prouver que c’est NP-COMPLET

on peut le convert en 3 optimal matching


## Corbeille
