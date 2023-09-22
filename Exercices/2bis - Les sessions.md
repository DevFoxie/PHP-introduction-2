**Exercice 3 : Création d'une Session de Connexion**

1. Créez un fichier HTML nommé **`connexion.html`** avec un formulaire de connexion contenant un champ pour le nom d'utilisateur et un champ pour le mot de passe.
2. Dans **`traitement.php`**, créez une session si les identifiants de connexion sont corrects. Pour simplifier, utilisez des identifiants en dur dans le code (par exemple, "utilisateur123" et "motdepasse123").
3. Stockez le nom d'utilisateur dans une variable de session (**`$_SESSION["username"]`**) si la connexion est réussie.

**Exercice 4 : Affichage du Nom d'Utilisateur Stocké dans la Session**

1. Créez une nouvelle page PHP nommée **`accueil.php`**.
2. Dans **`accueil.php`**, utilisez **`session_start();`** pour démarrer la session.
3. Affichez un message de bienvenue en utilisant le nom d'utilisateur stocké dans **`$_SESSION["username"]`**.