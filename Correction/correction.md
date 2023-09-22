# **Place à la correction … !** ✍️

**Exercice 1 : Création d'un Formulaire d'Inscription**

**Le HTML** :

```php
<form action="traitement.php" method="post">
    <label for="nom">Nom :</label>
    <input type="text" id="nom" name="nom" required>
    
    <label for="prenom">Prénom :</label>
    <input type="text" id="prenom" name="prenom" required>
    
    <label for="email">Adresse e-mail :</label>
    <input type="email" id="email" name="email" required>
    
    <label for="motdepasse">Mot de passe :</label>
    <input type="password" id="motdepasse" name="motdepasse" required>
    
    <input type="submit" value="S'inscrire">
</form>
```

**Le traitement en PHP** :

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nom = $_POST["nom"];
    $prenom = $_POST["prenom"];
    $email = $_POST["email"];
    $motdepasse = $_POST["motdepasse"];
    
    echo "Bienvenue, $prenom $nom ! Votre adresse e-mail est $email.";
}
?>
```

**Exercice 2 : Validation des Données**

Dans le fichier **`traitement.php`**, avant d'afficher le message de bienvenue, ajoutez des vérifications pour vous assurer que l'adresse e-mail a un format valide (vous pouvez utiliser la fonction **`filter_var`**) et que le mot de passe a une longueur minimale de 8 caractères.

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nom = $_POST["nom"];
    $prenom = $_POST["prenom"];
    $email = $_POST["email"];
    $motdepasse = $_POST["motdepasse"];
    
    // Validation de l'adresse e-mail
    if (!filter_var($email, FILTER_VALIDATE_EMAIL)) {
        echo "Adresse e-mail invalide.";
    } elseif (strlen($motdepasse) < 8) {
        echo "Le mot de passe doit contenir au moins 8 caractères.";
    } else {
        echo "Bienvenue, $prenom $nom ! Votre adresse e-mail est $email.";
    }
}
?>
```

**Exercice 3 : Création d'une Session de Connexion**

**Le HTML** : 

```php
<form action="traitement.php" method="post">
    <label for="username">Nom d'utilisateur :</label>
    <input type="text" id="username" name="username" required>
    
    <label for="password">Mot de passe :</label>
    <input type="password" id="password" name="password" required>
    
    <input type="submit" value="Se connecter">
</form>
```

**Le traitement en PHP** : 

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $username = $_POST["username"];
    $password = $_POST["password"];
    
    // Vérification des identifiants (utilisation d'identifiants en dur pour cet exemple)
    if ($username === "utilisateur123" && $password === "motdepasse123") {
        session_start();
        $_SESSION["username"] = $username;
        echo "Vous êtes connecté en tant que $username.";
    } else {
        echo "Identifiants incorrects.";
    }
}
?>
```

**Exercice 4 : Affichage du Nom d'Utilisateur Stocké dans la Session**

Pour bien démarrer une session et évitez les bugs, pensez à la démarrer **tout en haut de votre page** !

```php
<?php
session_start();
?>
```

Pensez à accueillir les utilisateurs de votre futur site web ! 👋

```php
<?php
if (isset($_SESSION["username"])) {
    echo "Bienvenue, " . $_SESSION["username"] . "!";
} else {
    echo "Vous n'êtes pas connecté.";
}
?>
```

**Exercice 5 : Création d'un Cookie de Préférence**

**Le HTML** :

```php
<form action="traitement_cookie.php" method="post">
    <label for="theme">Choisissez un thème :</label>
    <select id="theme" name="theme">
        <option value="clair">Thème Clair</option>
        <option value="sombre">Thème Sombre</option>
    </select>
    
    <input type="submit" value="Enregistrer">
</form>
```

**Le traitement en PHP** :

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $theme = $_POST["theme"];
    setcookie("theme_preference", $theme, time() + 3600, "/");
    echo "Préférence de thème enregistrée avec succès !";
}
?>
```

**Exercice 6 : Lecture et Modification du Cookie de Préférence**

**theme.php** :

```php
<?php
if (isset($_COOKIE["theme_preference"])) {
    $theme = $_COOKIE["theme_preference"];
} else {
    $theme = "clair"; // Valeur par défaut si le cookie n'existe pas
}
?>
```

Et pour afficher le theme, ça se passe dans le html … :

```php
<body style="background-color: <?php echo $theme === '
```