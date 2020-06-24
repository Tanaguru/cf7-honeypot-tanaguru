# CF7 Honeypot Tanaguru

* [Accéder à la version française](#cf7-honeypot-tng-fr)
* [Go to English version](#cf7-honeypot-tng-en)

# <h1 id="cf7-honeypot-tng-fr">CF7 Honeypot Tanaguru ReadMe - Version française</h1>

## Introduction

Ce répertoire Github héberge l'extension WordPress [Honeypot for Contact Form 7](https://wordpress.org/plugins/contact-form-7-honeypot/), crée par DaoByDesign et modifié par l'équipe Tanaguru.

## Pourquoi ce plugin ?

Nous avons créé une version personnalisée de l'extension Contact Form 7, [CF7 Tanaguru](https://github.com/Tanaguru/Cf7-tanaguru), afin de corriger ses problèmes d'accessibilité.

Honeypot for Contact Form 7 détecte la présence de Contact Form 7 pour pouvoir s'installer. Par conséquent, nous devons également personnaliser cette extension afin qu'elle soit fonctionnelle avec notre extension CF7 Tanaguru.

## Comment contribuer ?

Nous essayons de rester au plus près des évolutions du plugin original, c'est pourquoi nous devons tenir à jour ce répertoire manuellement.

### Une branche par correctif

Créez une branche par correctif nommée selon le modèle suivant :
`[version]_intitule-du-correctif`.

Par exemple : `5-1-1_error-role-alert`

### Utiliser des commentaires spécifiques

Pour faciliter la fusion des modifications avec les mises à jour du plugin, nous documentons nos changements dans le code. Assuez-vous d'encadrer les portions de code que vous avez changé avec les blocs de commentaires suivants :

```php
/**
 * #cf7-honeypot-tng-start
 * Décrivez brièvement en anglais les changements effectués
 */

// code

/* #cf7-honeypot-tng-end */
```

### Commenter le code original

Si jamais vous souhaitez retirer tout un morceau de code (par exemple, un bloc conditionnel (if/else), une fonction entière etc.), commentez le code original et dans le bloc de commentaire `#cf7-honeypot-tng-start`, expliquez brièvement *pourquoi* ceci a été retiré, surtout si cela a un lien avec l'accessibilité.

Par exemple, ceci pourrait ressembler à ce qui suit (cet exemple n'a pas été pris du plugin original) :

```php
/**
 * #cf7-honeypot-tng-start
 * Remove role="button" : if button is needed
 * use <button> tags instead of <a> tags.
 */

// if (link) {
//    link.setAttribute('role', 'button')
// }

/* #cf7-honeypot-tng-end */
```

## Comment mettre à jour le plugin CF7 Honeypot Tanaguru

Suivez les instructions suivantes pour mettre à jour le plugin CF7 Honeypot Tanaguru :

* Vérifiez que la branche `master` est bien à jour
* Créez une nouvelle branche, à partir de la branche master, appelée `update_[version]` en remplaçant "version" par le numéro de la nouvelle version.
    * Par exemple : `update_5-1-2`
* Mettre sur cette branche la nouvelle version du plugin original Contact Form 7
* Régler les conflits et reporter les modifications de Honeypot for Contact Form 7 dans la nouvelle version de CF7 Honeypot Tanaguru
* Poussez sur la branche `update_[version]` vos modifications
* Fusionner la branche `update_[version]` (avec pull request) avec la branche `master` pour que celle-ci soit à jour.

***

# <h1 id="cf7-honeypot-tng-en">CF7 Tanaguru ReadMe - English version</h1>

## Introduction

This repository is the Tanaguru team's version of the WordPress Plugin [Honeypot for Contact Form 7](https://wordpress.org/plugins/contact-form-7-honeypot/) by DaoByDesign and modified by Tanaguru's team.

## Why this plugin?

We have created a customise version of the Contact Form 7 plugin, [CF7 Tanaguru](https://github.com/Tanaguru/Cf7-tanaguru), in order to fix its accessibility problems.

Honeypot for Contact Form 7 is detecting the activation of Contact Form 7 so as to install itself. So, we need to customise this plugin to make it compatible with our CF7 Tanaguru plugin.

## How to make changes?

We try to stay close to the evolving changes of the original plugin. Therefore we have to manually update this repository.

### Using specific comment tags

To make it easier to merge changes with new updates, we document our changes in the code. Make sure to wrap the section of code you've changed with the following comment tags :

```php
/**
 * #cf7-honeypot-tng-start
 * Describe quickly in English the changes made
 */

// code

/* #cf7-honeypot-tng-end */
```

### Commenting original code

If you ever want to remove a whole chunk of code (ie. if statement, a whole function, etc.), comment the original code and in the `#cf7-honeypot-tng-start` comment tag, quickly explain *why* this has been removed, especially if it has to do with web accessibility.

For example, this could look like this (this example is not taken from the original plugin by the way) :

```php
/**
 * #cf7-honeypot-tng-start
 * Remove role="button" : if button is needed
 * use <button> tags instead of <a> tags.
 */

// if (link) {
//    link.setAttribute('role', 'button')
// }

/* #cf7-honeypot-tng-end */
```
