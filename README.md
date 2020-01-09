# Weblate helper repository for Cockpit

Repository for syncing Weblate translations. If you are not a bot, please ignore this repository.

## I want to translate Cockpit
Great! Please do so in https://translate.stg.fedoraproject.org/projects/cockpit

## I found wrong translation
You can fix it in [Weblate](https://translate.stg.fedoraproject.org/projects/cockpit) directly, but if you don't want to register and become translator, please [open an issue](https://github.com/cockpit-project/cockpit) and maintainers will fix it in Weblate in your stead.

## Then what is this repository good for?
Weblate introduced a "push" workflow - meaning that the project repository keeps the source document (`.pot` file) upstream and Weblate has hooks that run when it updates.  When strings are translated, Weblate pushes these changes into upstream (or sends pull request).

The Cockpit team does not want to keep the `.pot` file upstream, also we don't want to get loads of commits and pull requests from Weblate. We prefer "pull" workflow - meaning that we regularly update `.pot` file and also download current translated strings, and gate their landing through our tests.

This repository acts as a buffer between the two - here we update the `.pot` file and Weblate directly pushes translations. We then take translation files from this repository, test them and land into the project itself.  All is done by our and Weblate bots, so there should be no manual interaction.
