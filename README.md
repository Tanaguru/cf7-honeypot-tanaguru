# CF7 Honeypot Tanaguru

A fork of the “Honeypot for Contact Form 7” WordPress plugin to make it works with our [CF7 Tanaguru](https://github.com/Tanaguru/contact-form-7) plugin.

## Introduction

This repository is the Tanaguru team's version of the WordPress Plugin [Honeypot for Contact Form 7](https://wordpress.org/plugins/contact-form-7-honeypot/) by Nocean and modified by Tanaguru team.

## Why this plugin?

We have created a customise version of the Contact Form 7 plugin, [CF7 Tanaguru](https://github.com/Tanaguru/contact-form-7), in order to fix its accessibility problems.

Honeypot for Contact Form 7 is detecting the activation of Contact Form 7 so as to install itself. So, we need to customise this plugin to make it compatible with our CF7 Tanaguru plugin.

## How to contribute?

We try to stay close to the evolving changes of the original plugin. Therefore we have to manually update this repository.

### One branch = one fix

Create a Git branch by fix you want to do. Name this branch following this model: `[version]_name-of-the-fix`.

Example : `1-14-1_path-name-to-cf7-tanaguru`

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

For example, this could look like this (this example is not taken from the original plugin by the way):

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

## How to update CF7 Honeypot Tanaguru plugin from Honeypot for Contact Form 7

Follow these instructions to update the CF7 Honeypot Tanaguru plugin from the official Honeypot for Contact Form 7:

1. Check that the `master` branch is up to date on your computer;
1. Create a new branch, from the `master` branch, naming `update_[version]` replacing “version” by the new version number of Honeypot for Contact Form 7. Example : `update_1-14-1`;
1. Put the new version from the official Honeypot for Contact Form 7 on this branch;
1. Before committing this, compare what you are about to commit and report all CF7 Honeypot Tanaguru modifications on the new version of Honeypot for Contact Form 7;
1. When everything seems to be OK, commit and push your modifications on your branch `update_[version]`;
1. Go on Github and make a Pull Request to merge your branch `update_[version]` on `master`. Read your Pull Request carefully. If you can, request a review from a colleague to benefit from a fresh eyes looking;
1. Approve the Pull Request;
1. Make a Github Release.
