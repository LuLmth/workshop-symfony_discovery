# Tips

***1.*** Dans chacun de votre projet Symfony, vous avez a disposition une console intégré avec une multitude de commande.

Pour accéder à la console, avec la CLI de Symfony :
```sh
  symfony console
```

Sans la CLI, à la racine de votre projet :
```sh
  php bin/console
```

***2.*** La <a href="https://symfony.com/doc/current/index.html">documentation de Symfony</a> est bien fourni et vous pourrez y trouver toutes les informations nécessaires au bon déroulement de ce workshop.

***3.*** Pour les vues, Symfony utilise le template engine PHP **Twig**, voici la <a href="https://twig.symfony.com/">documentation</a>.

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
<br />
Type : *String [255]* | *Not null*

<br />

Name : *description*
<br />
Type : *Text* | *Can be null*

<br />

Name : *releaseDate*
<br />
Type : *Date* | *Not null*

<br />

Name : *duration*
<br />
Type : *Dateinterval* | *Not null*

***2.*** Maintenant, vous allez faire en sorte de créer une "version" de votre entité et de migrer cette version en base de donnée.

# Exercice 3

Vous allez devoir comprendre comment utiliser les Fixtures. Les Fixtures sont utilisés pour charger de fausses données en base. Libre à vous de mettre les fausses données que vous souhaitez, mais faites au minimum 5 faux films. Une fois que vous avez fait votre fixture, vous allez pouvoir la load et voir les données qu'y ont été flush en base.

# Exercise 4

Dans cet exercice, vous allez maintenant récupérer, depuis votre controller, les films que vous avez sauvegardés en base de données et les afficher dans votre vue. Pour cela, vous allez apprendre à utiliser les Repository. Il y a déjà des méthodes de disponible de base mais vous pouvez toujours créer vos propres méthodes en utilisant le QueryBuilder (ce sont vos requêtes SQL en base).

# Exercise 5

***1.*** Vous allez voir comment créer facilement un formulaire. Celui-ci va nous permettre d'ajouter de nouveaux films à notre applications.

### Formulaire
Nom : *MovieType*
Entité lié : *Movie*

***2.*** Le formulaire que vous venez de créer doit être visible sur une autre page que la *app.home*. Vous allez donc en créer une nouvelle (le mieux reste de créer un nouveau Controller et une Vue destinés aux films).
Il va falloir que vous fassiez des recherches dans la documentation sur les formulaires. Comment les créer dans notre Controller ? Comment les envoyés et les afficher dans notre Vue ? Ainsi que comment récupérer les informations du formulaires et les envoyés sauvegarder en base ?

# Exercise 6

Dans cet exercice, vous allez apprendre à utiliser le système de traduction de Symfony. Le but va être de créer une nouvelle page, qui contiendra un titre, qui aura deux versions, une en Anglais et une en Français.

### Route
Path : */en/international*
<br />
Name : *app.international*
<br />
Body : un H1 avec inscrit *Welcome to the international section of this website"

### Route
Path : */fr/international*
<br />
Name : *app.international*
<br />
Body : un H1 avec inscrit *Bienvenue sur la section internationale de notre site"
