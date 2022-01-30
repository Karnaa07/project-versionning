# project-versionning
## 03_01_2021_Projet_versionning
## QUENTIN GIRARD 3IW1 

#### La première étape consiste à compléter la branche main par défaut avec une branche develop. 

- $ git branch develop
- $ git push -u origin develop

#### l'exécution de git flow init sur un dépôt existant permet de créer la branche de développement (develop) :

- $ git flow init

#### ceci devrait apparaitre

```

Initialized empty Git repository in ~/project/.git/
No branches exist yet. Base branches must be created now.
Branch name for production releases: [main]
Branch name for "next release" development: [develop]


How to name your supporting branch prefixes?
Feature branches? [feature/]
Release branches? [release/]
Hotfix branches? [hotfix/]
Support branches? [support/]
Version tag prefix? [] 

```
#### il suffit d'appuyer sur entrer jusqu'a la version "tag prefix"

- $ git branch

#### la nouvelle branch develop a été crée

#### Création d'une branche de fonctionnalité

- $ git checkout develop

- $ git checkout -b feature_branch

#### Terminer une branche de fonctionnalité

- $ git checkout develop
- $ git merge feature_branch

#### Création des releases

- $ git checkout develop
- $ git checkout -b release/0.1.0

#### Pour terminer une branche release, utilisez les méthodes suivantes :

- $ git checkout main
- $ git merge release/0.1.0

#### Création de branch hotfix

- $ git checkout main
- $ git checkout -b hotfix_branch

#### Comme à la fin d'une branche release, une branche hotfix est mergée à la fois dans main et develop

- $ git checkout main
- $ git merge hotfix_branch
- $ git checkout develop
- $ git merge hotfix_branch
- $ git branch -D hotfix_branch


