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