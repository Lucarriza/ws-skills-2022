# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️
- les besoins auxquels répond GraphQL ✔️
- la définition d'un schéma
- Query ✔️
- Mutation ✔️
- Subscription ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

//La Query va retourner un tableau de wilder dans lequel on lie les champs de wilder et le champ skill de grade.
@Query(() => [Wilder])
  async getAllWilders(): Promise<Wilder[]> {
    return await dataSource.manager.find(Wilder, {
      relations: {
        grades: {
          skill: true,
        },
      },
    });
  }


### Utilisation dans un projet ❌

[lien github](...)

Description :

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

https://graphql.org/ => site officiel de graphql.
https://typegraphql.com/ => version typé de graphql.
https://www.apollographql.com/docs/ => doc de apollo server.

## 🚧 Je franchis les obstacles

### Point de blocage ✔️

Description:
Méconnaissance de toutes les fonctionnalités avancées de graphql.

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
