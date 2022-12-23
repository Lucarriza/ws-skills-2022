# Tester son application

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les tests unitaires ✔️
- les mocks ✔️
- les tests d'integration ✔️
- les tests de bout en bout (end to end) ✔️
- le TDD ❌
- les tests par snapshot ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️
//import de playwright
import { test, expect } from "@playwright/test";

//on accède à la page de l'editeur
test("Code editor is functionnal", async ({ page }) => {
  await page.goto("http://localhost:3000/editor");

  //on vérifie que certains champs soient bien affichés et d'autres non
  await expect(page).toHaveTitle(/Codeless4/);
  await expect(page.getByAltText("save file")).toBeVisible();
  await expect(page.getByAltText("download file")).toBeVisible();
  await expect(page.getByAltText("share file")).toBeVisible();
  await expect(page.getByTestId("code_editor")).toBeVisible();
  await expect(page.getByAltText("arrow left")).toBeVisible();
  await expect(page.getByAltText("arrow right")).toBeHidden();
  await expect(page.getByTestId("code_result")).toBeHidden();

  //on attribue élément de la page à la variable run
  const run = page.getByRole("button", { name: "Run" });
  //on click sur run
  await run.click();
  //on vérifie que l'affichage corresponde à la situation
  await expect(page.getByAltText("save file")).toBeVisible();
  await expect(page.getByAltText("download file")).toBeVisible();
  await expect(page.getByAltText("share file")).toBeVisible();
  await expect(page.getByTestId("code_editor")).toBeVisible();
  await expect(page.getByAltText("arrow left")).toBeHidden();
  await expect(page.getByAltText("arrow right")).toBeVisible();
  await expect(page.getByTestId("code_result")).toBeVisible();

  //on attribue élément de la page à la variable arrowRight
  const arrowRight = page.getByAltText("arrow right");
  await arrowRight.click();
  await expect(page.getByAltText("save file")).toBeVisible();
  await expect(page.getByAltText("download file")).toBeVisible();
  await expect(page.getByAltText("share file")).toBeVisible();
  await expect(page.getByAltText("arrow left")).toBeVisible();
  await expect(page.getByAltText("arrow right")).toBeHidden();
  await expect(page.getByTestId("code_editor")).toBeVisible();
  await expect(page.getByTestId("code_result")).toBeHidden();

  //on attribue élément de la page à la variable arrowLeft
  const arrowLeft = page.getByAltText("arrow left");
  await arrowLeft.click();
  await expect(page.getByAltText("save file")).toBeVisible();
  await expect(page.getByAltText("download file")).toBeVisible();
  await expect(page.getByAltText("share file")).toBeVisible();
  await expect(page.getByTestId("code_editor")).toBeVisible();
  await expect(page.getByAltText("arrow left")).toBeHidden();
  await expect(page.getByAltText("arrow right")).toBeVisible();
  await expect(page.getByTestId("code_result")).toBeVisible();
});


### Utilisation dans un projet  ✔️

https://github.com/WildCodeSchool/2209-wns-rivest-groupe4-front/

Description :

### Utilisation en production si applicable❌

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ✔️

Description: Il faut que je me familiarise davantage avec les tests.

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
