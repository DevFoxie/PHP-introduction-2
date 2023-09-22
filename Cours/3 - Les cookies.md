### **3. Les Cookies en PHP**

Les cookies qui ne sont à pas confondre avec vos gâteaux favoris 🍪 sont de petits fichiers texte stockés sur l'ordinateur de l'utilisateur. Ils sont souvent utilisés pour suivre les préférences de l'utilisateur ou garder une session active.

### a. Définir un Cookie

Pour définir un cookie en PHP, vous pouvez utiliser la fonction **`setcookie()`** :

```php
<?php
setcookie("nom_cookie", "valeur_cookie", time() + 3600, "/");
?>
```

### b. Lire un Cookie

Pour lire un cookie, vous pouvez utiliser la superglobale **`$_COOKIE`** :

```php
<?php
$cookie_value = $_COOKIE["nom_cookie"];
echo "Valeur du cookie : " . $cookie_value;
?>
```

Voilà ! Vous avez maintenant une introduction aux formulaires, aux sessions et aux cookies en PHP natif. Ces concepts sont fondamentaux pour créer des sites web interactifs et personnalisés, à la différence des pages web statiques. N'hésitez pas à explorer davantage et à pratiquer pour devenir un développeur web PHP compétent. Bonne chance dans votre apprentissage !