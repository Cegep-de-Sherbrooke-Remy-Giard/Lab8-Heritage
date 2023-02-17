# Deuxième Partie

Dans cette deuxième partie, on vous demande de créer une classe `BilanComptable`.  Cette classe englobera les actifs (et éventuellement les passifs) d'une personne pour finalement en afficher le bilan.

Les attributs de cette classe:
- string nomDuProprietaire
- Un tableau de pointeurs d'actifs (classe `Actif`)

Les méthodes de cette classe:
- Constructeur
- Le constructeur doit initialiser des `Actif` dans le tableau d'actifs.  Par exemple: `actifs[0] = new CompteBanque(......)`.
- Destructeur qui détruira les actifs créés
- Une méthode `afficher()` qui affichera par exemple: 
```
Bilan de Marcel Desjardins 
==========================

Actifs
------
Compte de banque - 8473890-15 Desjardins                      12345.00$
REER - 8473748-12-ES2 - Desjardins                             6789.00$
REER - 8473750-12-ES1 - Desjardins                            50000.00$
                                                             ----------      
                                                     Total : 69 134.00$
```



## Étape 2
Maintenant, on veut pouvoir faire une copie d'un `BilanComptable`.  Puisque la classe utilise les pointeurs à l'interne comme attribut, quelles méthodes faut-il pour pouvoir bien gérer les copies ?  
Veuillez implanter ces méthodes !
