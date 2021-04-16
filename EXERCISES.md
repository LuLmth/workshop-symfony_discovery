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

Pour les vues, Symfony utilise le template engine PHP **Twig**, voici la documentation :
```url
https://twig.symfony.com/
```

# Exercice 0

Vous allez tout d'abord setup votre base de donnée, en modifiant les informations du .env de votre application Symfony. Puis, grâce à la console vous allez pouvoir créer votre base de donnée.

```sh
symfony console doctrine:database:create
```

# Exercice 1

***1.*** Vous allez devoir créer un Controller Symfony. Grâce à la console Symfony, vous allez pouvoir créer facilement votre Controller, lui définir une route ainsi qu'afficher son template avec des paramètres ou non.

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

***2.*** Maintenant, que ce passe-t-il si [website_name] n'existe pas ou est null ? Il faudrait peut-être voir comment intégrer des conditions directement dans notre template Twig.

# Exercice 2

***1.*** Vous allez devoir créer une Entité Symfony. Grâce à la console Symfony, vous allez pouvoir créer facilement Entité que vous pourrez sauvegarder facilement en base de données et pouvoir les intégrer à vos vues.
Cette entité aura pour but de représenter un film et ses caractéristiques qui le définisse.

### Entité
Nom : *Movie*

### Propriétés
Name : *title*
Type : *String [255]* | *Not null*

Name : *description*
Type : *Text* | *Can be null*

Name : *duration*
Type : *Dateinterval* | *Not null*

***2.*** Maintenant, vous allez faire en sorte de créer une "version" de votre entité et de migrer cette version en base de donnée.

# Exercice 3

Vous allez devoir comprendre comment utiliser les Fixtures. Les Fixtures sont utilisés pour charger de fausses données en base. Libre à vous de mettre les fausses données que vous souhaitez, mais faites au minimum 5 faux films. Une fois que vous avez fait votre fixture, vous allez pouvoir la load et voir les données qu'y ont été flush en base.

# Exercise 4

Dans cet exercise, vous allez maintenant récupérer, depuis votre controller, les films que vous avez sauvegardés en base de données et les afficher dans votre vue.
