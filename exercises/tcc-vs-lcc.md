# TCC *vs* LCC

Explain under which circumstances *Tight Class Cohesion* (TCC) and *Loose Class Cohesion* (LCC) metrics produce the same value for a given Java class. Build an example of such as class and include the code below or find one example in an open-source project from Github and include the link to the class below. Could LCC be lower than TCC for any given class? Explain.

## Answer

On a : 
NP = nombre maximum de connexions possibles = N * (N − 1)/2 où N est le nombre de méthodes,
NDC = nombre de connexions directes (nombre d'arêtes dans le graphe de connexion),
NIC = nombre de connexions indirectes.

Sachant que TCC = NDC/NP et LCC = (NDC + NIC)/NP, pour avoir TCC = LCC on veut NIC = 0.

exemple avec la classe Group:

    class Group {

        private int A;

        public Group(int A) {
            this.A = A;
        }

        public int compareTo(Other other) {
            return A - other.A;
        }

    }

    class Other {

        private int A;

        public Other(int A) {
            this.A = A;
        }

    }

Mathématiquement, il serait possible que LCC<TCC si NIC<0 mais dans les faits ce n'est pas possible car NIC représente un nombre de connexions indirectes et donc ne pourra pas passer en dessous de 0.
