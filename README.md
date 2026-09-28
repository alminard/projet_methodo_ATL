# Scénario 1 - Utiliser `git` pour un travail individuel

Pour toute cette première activité, vous jouerez le rôle d'une developpeuse ou d'un développeur qui code un projet dans son coin.
Vous utiliserez `git` dans le but de garder trace des différentes versions de votre travail et le service en ligne GitHub vous servira pour stocker des sauvegardes.

```{admonition} À noter
:class: tip

`git` permet de gérer les versions de vos fichiers, quel que soit le langage considéré.
Dans cette partie, le code à sauvegarder sera du code Python, mais les commandes `git` utilisées seront les mêmes que pour du code R, HTML, _etc_.
```

## Gestion d'un projet Python local avec `git`

```{admonition} Résumé du scénario

Vous allez initialiser un nouveau projet `git` et créer des points de sauvegarde au fur et à mesure que vous avancerez dans votre projet.
```

* Créez un dossier `tutoriel_git`.
* Dans ce repertoire, créez un sous-dossier vide nommé `projet_ATL`.

````{admonition} Configuration de git pour la première utilisation
:class: tip

Il est nécessaire avant de commencer de réaliser quelques configurations par défaut, au minimum spécifier ses identifiants.
Pour cela, lancez un terminal et entrez les commandes suivantes : 
    
```bash
git config --global user.name "Your Name"
git config --global user.email you@example.com
```

Rajouter la commande :     

```bash 
git config --global pull.rebase false
```

qui permet de dire que par défaut chaque opération de _pull_ tente de faire aussi un _merge_ en même temps (si besoin).
````

* En utilisant le terminal, initialisez un nouveau dépôt `git` (`git init`) dans le dossier courant.
* Créez dans ce dossier un fichier `bibliographie.txt` qui contiendra une référence bibliographique pour votre projet.

Une fois votre fichier enregistré, vous allez créer un premier point de sauvegarde.
Pour cela :

* Vérifiez l'état actuel de votre dépôt `git` (`git status`) et assurez vous que le fichier `bibliographie.txt` est bien listé dans la section "Modifications qui ne seront pas validées".
* Ajoutez ce fichier à la liste des fichiers suivis par `git` (`git add`).
* Affichez de nouveau l'état du dépôt `git`. Qu'est-ce qui a changé ?
* Créez un _commit_ dont le message sera "création du fichier biblio".
* Vérifiez maintenant que le fichier  `bibliographie.txt` n'apparaît plus du tout lorsque vous affichez l'état du dépôt `git`.
* Regardez l'historique `git` (`git log`) : quelles informations sont stockées à chaque _commit_ ?

* Modifiez votre fichier et ajouter quelques mots clés liés à la référence.
* Créez un nouveau _commit_ avec un message adapté pour cette modification.
* Ajoutez les mots clés en anglais. 
* Finalement, vous vous rendez compte que cette dernière modification n'a pas sa place dans votre dépôt. Utilisez `git` pour revenir en arrière au dernier _commit_ (`git restore`), c'est-à-dire avant la modification en question.

Vous souhaitez maintenant vous prémunir d'une défaillance de votre machine et donc stocker une sauvegarde de votre dépôt `git` en ligne.
Pour cela, vous allez utiliser le service en ligne GitHub.

* Créez un nouveau dépôt (_repository_) sur votre compte GitHub dont le nom sera `projet_methodo`.
* Sur votre machine, ajoutez ce dépôt GitHub distant (`git remote add`) en le nommant `origin` (nom communément utilisé pour un dépôt distant stockant la version de "référence" d'un projet `git`). (`git remote add origin ` URL du projet)
* Envoyez vos travaux locaux vers le dépôt distant (`git push origin main`).
* Rajoutez vos nom et prénom dans votre fichier, et validez cette modification par un _commit_.
* Vérifiez l'état actuel de votre dépôt `git` : que remarquez-vous ?
* Vérifiez maintenant l'état du dépôt sur GitHub : votre dernier _commit_ y est-il visible ? Pourquoi ?
* Synchronisez les versions locale et distante de votre projet.
* Vérifiez que tous vos _commits_ locaux sont maintenant visibles sur GitHub.
