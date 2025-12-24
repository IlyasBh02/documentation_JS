Carnet du Développeur
PHASE 1 : L'EXPLORATION
Fiche Méthode #1 : .filter()
// ==============================
// MÉTHODE : .filter()
// ==============================
// 1. MA DÉFINITION PERSONNELLE
C'est une méthode qui passe chaque élément d'un tableau dans un test. Elle garde seulement les éléments qui réussissent le test.

// 2. PARAMÈTRES ACCEPTÉS
Une fonction de test qui reçoit chaque élément et retourne vrai ou faux.

// 3. CE QU'ELLE RETOURNE
Un nouveau tableau avec seulement les éléments qui ont passé le test.

// 4. QUAND L'UTILISER ?
Quand tu veux sélectionner certains éléments d'un tableau selon une condition.

// 5. CE QU'ELLE NE FAIT PAS

Elle ne modifie pas le tableau original

Elle ne change pas les éléments, elle les garde tels quels

Fiche Méthode #2 : .map()
// ==============================
// MÉTHODE : .map()
// ==============================
// 1. MA DÉFINITION PERSONNELLE
C'est une méthode qui transforme chaque élément d'un tableau. Elle applique une fonction à chaque élément.

// 2. PARAMÈTRES ACCEPTÉS
Une fonction qui reçoit chaque élément et retourne sa nouvelle version.

// 3. CE QU'ELLE RETOURNE
Un nouveau tableau avec les éléments transformés.

// 4. QUAND L'UTILISER ?
Quand tu veux transformer tous les éléments d'un tableau (ex: mettre en majuscule, doubler les valeurs).

// 5. CE QU'ELLE NE FAIT PAS
Elle ne filtre pas - elle transforme TOUS les éléments.

Fiche Méthode #3 : .reduce()
// ==============================
// MÉTHODE : .reduce()
// ==============================
// 1. MA DÉFINITION PERSONNELLE
C'est une méthode qui combine tous les éléments d'un tableau pour produire une seule valeur.

// 2. PARAMÈTRES ACCEPTÉS
Une fonction d'accumulation et une valeur de départ.

// 3. CE QU'ELLE RETOURNE
Une valeur unique (nombre, chaîne, objet, tableau).

// 4. QUAND L'UTILISER ?
Quand tu veux calculer un total, concaténer des chaînes, ou combiner des données.

// 5. CE QU'ELLE NE FAIT PAS
Elle ne retourne pas un tableau (sauf si tu le construis).

--------------------------------------------------------------------------------------------------------------------------
CHALLENGE 1 :
--------------
--------------

.filter() :
-------------
const étudiants = [
  { nom: "Alice", note: 15, présent: true },
  { nom: "Bob", note: 8, présent: false },
  { nom: "Charlie", note: 18, présent: true }
];

// 1. Filtrer presents
const présents = étudiants.filter(étudiant => étudiant.présent);
// Résultat : [{Alice}, {Charlie}]

// 2. Filtrer bonne note
const bonsÉlèves = étudiants.filter(étudiant => étudiant.note >= 10);
// Résultat : [{Alice}, {Charlie}]

// 3. Filtrer par nom
const trouveAlice = étudiants.filter(étudiant => étudiant.nom.includes("Ali"));
// Résultat : [{Alice}]


.map() :
---------
// 1. Transformer tableau of nombres
const nombres = [1, 2, 3];
const nombresDoublés = nombres.map(n => n * 2);
// Résultat : [2, 4, 6]

// 2. Extraire une propriété d'objets
const prix = produits.map(produit => produit.prix);
// Résultat : [999, 25, 35]

// 3. Formater des données
const descriptions = produits.map(p => `${p.nom}: ${p.prix}€`);
// Résultat : ["Ordinateur: 999€", "T-shirt: 25€", "Livre JS: 35€"]


.reduce() :
---------
// 1. Calculer une somme
const notes = [15, 8, 18];
const totalNotes = notes.reduce((acc, note) => acc + note, 0);
// Résultat : 41

// 2. Trouver le maximum
const maxNote = notes.reduce((max, note) => note > max ? note : max, 0);
// Résultat : 18

// 3. Compter des éléments
const présences = [true, false, true];
const nombrePrésents = présences.reduce((count, présent) => présent ? count + 1 : count, 0);
// Résultat : 2


<!-- PHASE 2 : Le Laboratoire -->

.push() / .pop() - L'Ajouteur et L'Enleveur:
---------------------------------------------

#C'est comme une pile d'assiettes :

.push() ajoute une assiette sur le dessus

.pop() enleve l'assiette du dessus


const courses = ["lait", oeufs"];

// AJOUTER a la fin avec .push()
courses.push("pain");
console.log(courses); // ["lait", "œufs", "pain"]

courses.push("fromage", "yaourt");
console.log(courses); // ["lait", "œufs", "pain", "fromage", "yaourt"]

// ENLEVER le dernier avec .pop()
const dernier = courses.pop();
console.log(dernier); // "yaourt"
console.log(courses); // ["lait", "œufs", "pain", "fromage"]

// .pop() retourne ce qu'il a enlevé
const encoreUn = courses.pop();
console.log(encoreUn); // "fromage"


.sort() - Le Trieur
--------------------
C'est comme ranger tes affaires dans l'ordre.

// ATTENTION : .sort() modifie le tableau original !
const nombres = [5, 1, 8, 3, 2];

// Sans paramètre, il trie comme du texte (mauvais pour les nombres !)
const mauvaisTri = nombres.slice().sort(); // .slice() fait une copie
console.log(mauvaisTri); // [1, 2, 3, 5, 8] (ça a l'air bon mais c'est par hasard)

// Pour trier des NOMBRES, il faut une fonction
const triCroissant = nombres.slice().sort((a, b) => a - b);
console.log(triCroissant); // [1, 2, 3, 5, 8]

const triDécroissant = nombres.slice().sort((a, b) => b - a);
console.log(triDécroissant); // [8, 5, 3, 2, 1]

// Pour trier du texte
const mots = ["banane", "pomme", "abricot"];
mots.sort();
console.log(mots); // ["abricot", "banane", "pomme"] (ordre alphabétique)

// Pour trier des objets
const personnes = [
  { nom: "Alice", âge: 25 },
  { nom: "Bob", âge: 30 },
  { nom: "Charlie", âge: 20 }
];

personnes.sort((a, b) => a.âge - b.âge);
console.log(personnes);
// [
//   { nom: "Charlie", âge: 20 },
//   { nom: "Alice", âge: 25 },
//   { nom: "Bob", âge: 30 }
// ]





Resum en une phrase pour chaque :
-----------------------------------
.find() → "Donne-moi le premier qui correspond"

.push() → "Ajoute à la fin" / .pop() → "Enlève le dernier"

.some() → "Est-ce qu'au moins un... ?" / .every() → "Est-ce que tous... ?"

.sort() → "Range dans l'ordre" (attention, ça modifie !)