# Lab8 - Héritage

Théorie visé par ce lab:
- Concept de l'héritage en programmation orienté objet
- Visibilité *protected*
- Masquage et démasquage de méthodes

## Description
Pour ce laboratoire, nous allons réutiliser la classe `CompteBanque` du laboratoire 6.  Tout de même, nous allons créer un nouveau projet dans lequel nous copierons la classe plus loin.  Pour l'instant, veuillez suivre les prochaines étapes.

# Étape 1 - Création de la classe `Actif`
1. Créez une nouvelle classe `Actif`.  Cette classe représentera un actif dans le monde de la comptabilité.
2. Cette classe devrait contenir un attribut `float _solde` en visibilité *protected*.  
3. L'attribut `_solde` doit avoir un getter en mode *public*.  

## Questions:
- Que représente la visibilité *protected* ? 
- Pourquoi le visibilité du getter du solde n'est pas *protected* elle aussi ? 

# Étape 2 - Création de la classe `Placement`
1. Créez une nouvelle classe `Placement` qui hérite de la classe `Actif`.  
2. Cette classe devrait contenir un attribut `string _institution` en visibilité *protected*
3. L'attribut `_institution` doit avoir un getter *public*

# Étape 3 - Création de la classe `Reer` 
1. Créez une nouvelle classe `Reer` qui hérite de la classe `Placement`.  
2. Ajoutez un attribut `string _numeroCompte` et son getter
3. Ajouter un attribut `string _echeance` et son getter
4. Ajouter un constructeur qui reçoit en paramètre le solde, l'institution, le numéro de compte et l'échéance. 

## Questions: 
- Quelle visibilité devraient avoir les nouveaux attributs de la classe `Reer` et pourquoi ? 
- Quelle visibilité devraient avoir les getters des nouveaux attributs et pourquoi ? 

# Étape 4 - Modification de la classe `CompteBanque`
Nous allons modifier le `CompteBanque` pour qu'il devienne un `Actif`.
1. Copiez la classe `CompteBanque` du lab6 dans votre projet
2. Modifiez la classe `CompteBanque` pour qu'elle hérite de la classe `Actif`.  
3. Puisque la classe est maintenant un actif, elle n'a pas besoin d'avoir son propre `solde` puisque cet attribut provient maintenant de la classe `Actif`.  On peut donc supprimer l'attribut `solde` et son getter de la classe `CompteBanque`.
4. Ajouter l'attribut `string _noCompte` et son getter
5. Ajouter l'attribut `string _institution` et son getter
6. Ajouter un constructeur qui reçoit en paramètre le solde, l'institution et le numéro de compte.

## Questions: 
- Quelle visibilité devraient avoir les nouveaux attributs de la classe `CompteBanque` et pourquoi ? 
- Quelle visibilité devraient avoir les getters des nouveaux attributs et pourquoi ? 

# Étape 5 - Ajout des méthodes `afficherDetails()`
On désire pouvoir afficher les détails des instances de chacune des classes de la hiérarchie `Actif`. Nous allons donc créer des méthodes `afficherDetails(ostream& flux)`.  
1. Créez la méthode `afficherDetails(ostream& flux)` pour la classe `Actif`.  Cette méthode doit afficher par exemple: 
```
Solde: 1234.00$
```
2. Créez la méthode `afficherDetails(ostream& flux)` pour la classe `Placement`.  Il est nécessaire d'utiliser la méthode `afficherDetails` de la classe parent.  Par exemple, cette méthode pourrait afficher:
```
Institution: Desjardins
Solde: 1234.00$
```
3. Créez la méthode `afficherDetails(ostream& flux)` pour la classe `Reer`.  Il est nécessaire d'utiliser la méthode `afficherDetails` de la classe parent.  Par exemple, cette méthode pourrait afficher:
```
REER
====
No compte: 8473748-12-ES2
Échéance: 2 mars 2025
Institution: Desjardins
Solde: 1234.00$
```
4. Créez la méthode `afficherDetails(ostream& flux)` pour la classe `CompteBanque`.  Il est nécessaire d'utiliser la méthode `afficherDetails` de la classe parent.  Par exemple, cette méthode pourrait afficher:
```
Compte de Banque
================
No compte: 8473890-15
Institution: Desjardins
Solde: 4567.00$
```
