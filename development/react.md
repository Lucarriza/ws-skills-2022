# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

import React, {useState} from "react";

const counter = () => {
  const [counter, setCounter]=useState(0);
  
  return(
    <div>
    <h1>{counter}</h1>
    <button onClick={()=>setCounter(counter+=1)} value={counter}>Click me</button>
    </div>
  )
}

### Utilisation dans un projet ✔️
https://github.com/Lucarriza/OhMyQuote

Description : Générateur de citations en react.

### Utilisation en production si applicable ✔️
https://github.com/Lucarriza/OhMyQuote

Description : Générateur de citations en react.

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ✔️

Description: Je ne connais tous les hooks.

Plan d'action : (à valider par le formateur)

- action 1: Me renseigner sur la doc de react ❌ / ✔️
- action 2: Faire + de projets react ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
