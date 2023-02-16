# Lab8 - Héritage

Théorie visé par ce lab:
- Concept de l'héritage en programmation orienté objet
- Visibilité *protected*
- Utilisation de pointeurs dans les classes

## Description
Pour ce laboratoire, nous allons réutiliser la classe `CompteBanque` du laboratoire 6.  Tout de même, nous allons créer un nouveau projet dans lequel nous copierons ces classes plus loin.  Pour l'instant, veuillez suivre les prochaines étapes.

# Étape 1 - Création de la classe `Actif`
1. Créez une nouvelle classe `Actif`.  Cette classe représentera un actif dans le monde de la comptabilité.
2. Cette classe devrait contenir un attribut `float _solde` en visibilité *protected*.  
3. L'attribut `_solde` doit avoir un getter en mode *public*.  

## Questions:
- Que représente la visibilité *protected* ? 
- Pourquoi le visibilité du getter du solde n'est pas *protected* lui aussi ? 

# Étape 2 - Création de la classe `Placement`
1. Créez une nouvelle classe `Placement` qui hérite de la classe `Actif`.  
2. Cette classe devrait contenir un attribut "string _institution" en visibilité *protected*
3. L'attribut `_institution` doit avoir un getter *public*

# Étape 3 - Création de la classe `Reer` 
1. Créez une nouvelle classe `Reer` qui hérite de la classe `Placement`.  
2. Cette classe devrait contenir un attribut "string _numeroCompte" en visibilité *protected*
3. L'attribut `_numeroCompte` doit avoir un getter *public*
4. Ajouter un constructeur qui reçoit en paramètre le solde, l'institution et le numéro de compte. 

# Étape 4 - Modification de la classe `CompteBanque`
1. Copiez la classe `CompteBanque` du lab6 dans votre projet
2. Modifiez la classe `CompteBanque` pour qu'elle hérite de la classe `Actif`.  
3. Puisque la classe est maintenant un actif, elle n'a pas besoin d'avoir son propre `solde` puisque cet attribut provient maintenant de la classe `Actif`.  On peut donc supprimer l'attribut `solde` et son getter de la classe `CompteBanque`.
4. Ajouter l'attribut `string _noCompte` et son getter
5. Ajouter l'attribut `string _institution` et son getter

## Questions: 
- Quelle visibilité devrait avoir les nouveaux attributs de la classe `CompteBanque` et pourquoi ? 
- Quelle visibilité devrait avoir les getters des nouveaux attributs et pourquoi ? 
