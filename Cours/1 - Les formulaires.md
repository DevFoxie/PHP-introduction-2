### **1. Les Formulaires en PHP**

Les formulaires sont des éléments clés de l'interaction utilisateur sur les sites web. Ils permettent aux utilisateurs de saisir des données, de les envoyer au serveur, et de recevoir une réponse.

### a. Créer un Formulaire HTML

Pour commencer, nous devons créer un formulaire HTML. Voici un exemple simple de formulaire de connexion :

```php
<form action="traitement.php" method="post">
    <label for="username">Nom d'utilisateur :</label>
    <input type="text" id="username" name="username" required>
    
    <label for="password">Mot de passe :</label>
    <input type="password" id="password" name="password" required>
    
    <input type="submit" value="Se connecter">
</form>
```

### b. Traitement des Données du Formulaire en PHP

Une fois que l'utilisateur remplit le formulaire et appuie sur "Se connecter", nous devons traiter les données en PHP. Voici comment récupérer les données :

```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $username = $_POST["username"];
    $password = $_POST["password"];
    
    // Ici, vous pouvez vérifier l'authenticité de l'utilisateur, par exemple, en comparant les informations avec une base de données.
}
?>
