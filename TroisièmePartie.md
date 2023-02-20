# Troisième Partie

## Description
Finalement, je vous propose quelques dernières étapes à ce lab.

# Étape 1 - Pointeurs
Premièrement, je vous demande de convertir tous les attributs de la hiérarchie des classes `Actifs` en pointeurs au lieu de variable.  L'impact sera que les constructeurs seront modifiés et que les destructeurs devront gérer la destruction des pointeurs.

De plus, quelles autres méthodes doivent être implantés puisque la classe contient des pointeurs en attribut ? 
Veuillez implanter ces méthodes pour chacune des classes.

# Étape 2 - Hiérarchie de Passifs
Dernièrement, je vous propose de créer une hiérarchie de classe semblable au actifs que nous avons déjà, mais cette fois plutôt en `Passif`.  Cette hérarchie devrait contenir les classes et attributs suivants:

- `Passif`, similaire à `Actif` : contient un solde et une méthode qui permet d'afficher le résumé et le details
- `Hypotheque` qui représente une dette en hypothèque, donc est un Passif.  Il devrait contenir un numéro de compte et une institution en attribut.
- `CarteCredit` qui est aussi un `Passif` et contient les attributs `quatreDerniersCharateres`, `expiration` et `marque` (VISA, MASTERCARD', ...)

Pour avoir une image complète d'un profil de bilan comptable, il faudrait ajouter un `Actif` qui représente un immeuble pour contre-balancer l'hypothèque.  Je vous propose d'ajouter la classe `Immobilier` qui est un `Actif` et contient une adresse comme attribut.


# Étape 3 - Affichage du bilan complet
```
Bilan Comptable
===============
Propriétaire: Joseph Léveillée

Actifs
------
Compte de Banque - Desjardins - 852126-ES2                       1 000,25 $
REER - Desjardins - 6745894-RR1                                 10 232,12 $
Immobilier - 234 Blvd Portland, Sherbrooke                     510 000,00 $
                                                             --------------
                                                Total:         521 232,37 $

Passifs
-------
Hypohèque - Desjardins - 852126-HP2                            225 000,25 $
Carte de crédit - Fini avec 4453 - 02/24 - VISA                    232,56 $
                                                             --------------
                                                Total:         252 232,81 $


                                                            ===============
                                          GRAND TOTAL:         268 999,56 $
```
