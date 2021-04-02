<p align="center">
  <h1 align="center">workshop-symfony_discovery</h3>

  <p align="center">
    Un Workshop pour découvrir les bases du framework Symfony
  </p>
</p>

## Description

Ce Workshop est réalisé dans le but que vous découvriez le framework Symfony pas à pas. Nous allons voir comment créer des Entités, des Controllers ainsi que des Templates.

## Installation

Tout d'abord, vérifions si vous avez bien PHP d'installer sur votre machine ainsi que toutes les extensions nécessaires à Symfony :

**Fedora**
```sh
sudo dnf install php php-cli php-intl php-ctype php-iconv php-json php-simplexml php-tokenizer
```

**Ubuntu**
```sh
sudo apt install php php-cli php-intl php-ctype php-iconv php-json php-simplexml php-tokenizer
```

Maintenant, nous allons installer Composer qui est un package manager pour PHP :

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"

php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"

php composer-setup.php

php -r "unlink('composer-setup.php');"
```

Grâce à composer, nous allons pouvoir créer notre application Symfony :

```sh
php composer.phar create-project symfony/website-skeleton workshop-symfony_discovery
```
