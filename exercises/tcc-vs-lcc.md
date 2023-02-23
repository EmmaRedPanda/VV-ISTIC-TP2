# TCC *vs* LCC

Explain under which circumstances *Tight Class Cohesion* (TCC) and *Loose Class Cohesion* (LCC) metrics produce the same value for a given Java class. Build an example of such as class and include the code below or find one example in an open-source project from Github and include the link to the class below. Could LCC be lower than TCC for any given class? Explain.

## Answer

On a : 
NP = nombre maximum de connexions possibles = N * (N − 1)/2 où N est le nombre de méthodes,
NDC = nombre de connexions directes (nombre d'arêtes dans le graphe de connexion),
NID = nombre de connexions indirectes.

Sachant que TCC = NDC/NP et LCC = (NDC + NIC)/NP, pour avoir TCC = LCC on veut NIC = 0.

