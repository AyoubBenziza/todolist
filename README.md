# ToDoList

## Consigne

Vous reprenez l'exercice fait en formation de la Todo List dans lequel nous avons utilisé les verbes des requêtes http suivants : GET, POST et DELETE et PATCH.

### Première tâche (12pts) :

Vous commentez toutes les méthodes de manière à ce que l'on sache :
à quoi elles servent
ce qu'elles attendent en paramètre
ce qu'elles renvoient

### Deuxième tâche (6pts) :

Vous utilisez du TypeScript en lieu et place du JavaScript. Vous ajoutez un fichier README.txt ou README.md pour expliquer comment il faut s'y prendre pour que le TypeScript soit transpilé en JavaScript.

### Troisième tâche (2pts) :

Gérer les erreurs éventuelles lors des appels à json-server : par exemple si l'url n'est pas correcte lors de l'ajout d'une tâche, vous devrez faire en sorte que l'interface affiche une erreur (pas seulement dans la console donc) et que la tâche ajoutée soit automatiquement supprimée via un appel à la méthode loadTask.

Vous utilisez l'interface des devoirs de Teams pour attacher votre travail sous forme d'une archive (zip, tar.gz, ...)

## Instructions

### Initier la configuration TypeScript

TypeScript installé globalement

```shell
tsc --init
```

or

TypeScript installé localement

```shell
npx tsc --init
```

### Transpiler le code TypeScript en JavaScript

TypeScript installé globalement

```shell
tsc
```

or

TypeScript installé localement

```shell
npx tsc
```

### Exécuter notre serveur de base de données

```shell
npx json-server ./jsonserver/db.json
```

## Troisième tâche

Dans ToDoList.ts

```ts
FetchData.addTask(new_task).then(() => {
  window.location.reload();
});
```

J'empêche la création de notre tâche dans la page HTML en effectuant un rechargement de la page dès la requête addTask se termine, ce qui va rappeller la méthode loadTasks().
