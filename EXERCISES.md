# Tips

Dans chacun de votre projet Symfony, vous avez a disposition une console intégré avec une multitude de commande.

Pour accéder à la console, avec la CLI de Symfony :
```sh
  symfony console
```

Sans la CLI, à la racine de votre projet :
```sh
  php bin/console
```

# Exercice 0

Vous allez tout d'abord setup votre base de donnée, en modifiant les informations du .env de votre application Symfony. Puis, grâce à la console vous allez pouvoir créer votre base de donnée.

```sh
symfony console doctrine:database:create
```

# Exercice 1

**1.** Vous allez devoir créer un Controller Symfony. Grâce à la console Symfony, vous allez pouvoir créer facilement votre Controller, lui définir une route ainsi qu'afficher son template avec des paramètres ou non.

### Controller
Nom : *HomeController*
<br />
Paramètre pour la vue : *[website_name] -> "Workshop Symfony Discovery"*

### Route
Path : */*
<br />
Nom : *app.home*

### Template
Titre de la page : *Accueil*
<br />
Body : un H1 avec inscrit *Bienvenue sur le site [website_name] !"

**2.** Maintenant, que ce passe-t-il si [website_name] n'existe pas ou est null ? Il faudrait peut-être voir comment intégrer des conditions directement dans notre template Twig.

# Exercice 2
