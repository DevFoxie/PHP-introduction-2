### **2. Les Sessions en PHP**

Les sessions sont utilisées pour stocker des informations sur l'utilisateur tout au long de sa visite sur le site. Elles sont très utiles pour garder l'utilisateur connecté et stocker des données temporaires.

### a. Démarrer une Session

Pour commencer une session en PHP, vous devez ajouter **`session_start();`** en haut de chaque page où vous souhaitez utiliser des sessions.

### b. Stocker des Données dans une Session

Vous pouvez stocker des données dans une session comme ceci :

```php
<?php
session_start();
$_SESSION["username"] = "utilisateur123";
?>
```

### c. Accéder aux Données de Session

Pour accéder aux données de session ultérieurement, vous pouvez les récupérer de cette manière :

```php
<?php
session_start();
echo "Bienvenue, " . $_SESSION["username"];
?>