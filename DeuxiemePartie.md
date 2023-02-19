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
Propriétaire: Joseph Léveillée

Actifs
------
Compte de Banque - Desjardins - 852126-ES2                       1 000,25 $
REER - Desjardins - 6745894-RR1                                 10 232,12 $
                                                             --------------
                                                Total:          11 232,37 $
```

Pour générer cette affichage, la classe `BilanComptable` demandera à un `Actif` quelle est sa description `getDescription()`.  Cette méthode doit être définie sur la classe `Actif` et doit forcer les classes enfants de dernier niveau à l'implanter.  Donc, `CompteBanque` et `Reer` devront l'implanter.  

## Questions
- Comment peut-on forcer une méthode à être définie sur les classes enfants ?
- Qu'est ce qu'une classe abstraite et quelle classe pourrait être considérée comme abstraite dans ce laboratoire ? 
