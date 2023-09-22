# On file à **l’entraînement …** 💪

**Exercice 1 : Création d'un Formulaire d'Inscription**

1. Créez un fichier HTML nommé **`inscription.html`**.
2. Dans ce fichier, créez un formulaire d'inscription avec les champs suivants : nom, prénom, adresse e-mail et mot de passe. Utilisez l'attribut **`required`** pour rendre les champs obligatoires.
3. Ajoutez un bouton "S'inscrire" pour soumettre le formulaire.
4. Créez un fichier PHP nommé **`traitement.php`** pour traiter les données du formulaire.
5. Dans **`traitement.php`**, récupérez les données du formulaire à l'aide de **`$_POST`** et affichez un message de bienvenue à l'utilisateur

**Exercice 2 : Validation des Données**

1. Dans le fichier **`traitement.php`**, avant d'afficher le message de bienvenue, ajoutez des vérifications pour vous assurer que l'adresse e-mail a un format valide (vous pouvez utiliser la fonction **`filter_var`**) et que le mot de passe a une longueur minimale de 8 caractères.