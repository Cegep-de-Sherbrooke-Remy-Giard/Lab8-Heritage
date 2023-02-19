# Deuxième Partie

Dans cette deuxième partie, on vous demande de créer une classe `BilanComptable`.  Cette classe englobera les actifs (et éventuellement les passifs) d'une personne pour finalement en afficher le bilan.

Les attributs de cette classe:
- string nomDuProprietaire
- Un tableau de pointeurs d'actifs (`Actif** _actifs;`)
- Un attribut qui indique le nombre d'actifs dans le tableau

Les méthodes de cette classe:
- Constructeur
- Une méthode `ajouterActif(Actif* actif)` qui ajoutera un actif dans le tableau
- Une surcharge de l'opérateur << qui affichera par exemple: 
```
Bilan Comptable
===============
Client: Marcel Desjardins

Actifs
------
Compte de banque - 8473890-15 Desjardins                      12345.00$
REER - 8473748-12-ES2 - Desjardins                             6789.00$
REER - 8473750-12-ES1 - Desjardins                            50000.00$
                                                             ----------      
                                                     Total : 69 134.00$
```

Pour générer cette affichage, la classe `BilanComptable` demandera à un `Actif` quelle est sa description `getDescription()`.  Cette méthode doit être définie sur la classe `Actif` et doit forcer les classes enfants de dernier niveau à l'implanter.  Donc, `CompteBanque` et `Reer` devront l'implanter.  

## Questions
- Comment peut-on forcer une méthode à être définie sur les classes enfants ?
- Qu'est ce qu'une classe abstraite et quelle classe pourrait être considérée comme abstraite dans ce laboratoire ? 
