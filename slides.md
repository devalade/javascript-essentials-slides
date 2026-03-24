---
theme: seriph
background: https://images.unsplash.com/photo-1579468118864-1b9ea3c0db4a?w=1920&q=80
title: JavaScript Essentials - Révision Complète
info: |
  ## JavaScript Essentials
  Révision complète de JavaScript - 20h
  
  Modules :
  1. Fondamentaux (4h)
  2. Fonctions et Portée (4h)
  3. Objets et Tableaux (4h)
  4. Asynchrone et API (4h)
  5. DOM et Projet Final (4h)
class: text-center
drawings:
  persist: false
transition: slide-left
duration: 20h
---

# JavaScript Essentials

## Révision Complète - 20h

De débutant à avancé

<div class="mt-12">
  <span class="text-2xl">🚀 Modules 1-5</span>
</div>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/devalade/javascript-essentials-slides" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

---
transition: fade-out
---

# Programme de la Formation

<div class="grid grid-cols-2 gap-8 mt-8">

<div>

### Module 1 - Fondamentaux (4h)
- Variables et types
- Opérateurs
- Structures de contrôle
- **Mini-projet** : Jeu "Plus ou Moins"

### Module 2 - Fonctions (4h)
- Déclarations et expressions
- Fonctions fléchées
- Scope et closures
- **Mini-projet** : Convertisseur de devises

</div>

<div>

### Module 3 - Objets & Tableaux (4h)
- Méthodes modernes (map, filter, reduce)
- Manipulation d'objets
- Destructuring ES6
- **Mini-projet** : Gestionnaire de contacts

### Module 4 - Asynchrone (4h)
- Promises
- Async/await
- Consommation d'API
- **Mini-projet** : Application météo

### Module 5 - DOM & Événements (4h)
- Manipulation du DOM
- Gestion des événements
- **Projet final** : Todo List complète

</div>

</div>

---
layout: center
class: text-center
---

# Module 1
## Fondamentaux JavaScript

Durée : 4 heures

---

# Module 1 - Objectifs

<v-clicks>

- ✅ Comprendre la syntaxe de base de JavaScript
- ✅ Maîtriser les différents types de données
- ✅ Savoir utiliser les structures conditionnelles
- ✅ Maîtriser les boucles (for, while)
- ✅ Créer son premier programme interactif

</v-clicks>

---

# Qu'est-ce que JavaScript ?

<v-clicks>

- **Langage de programmation** créé en 1995 par Brendan Eich
- S'exécute dans le **navigateur** (côté client) et sur **Node.js** (côté serveur)
- **Dynamique** et **interprété**
- Standardisé sous le nom **ECMAScript** (ES6, ES7, etc.)

</v-clicks>

<div v-click class="mt-8 p-4 bg-blue-50 rounded-lg">

### 🎯 Où écrit-on du JavaScript ?

```html
<!-- Dans le HTML -->
<script>
  console.log("Hello World!");
</script>

<!-- Ou dans un fichier externe -->
<script src="script.js"></script>
```

</div>

---

# Variables : let, const, var

## Déclaration de variables

```js {monaco}
// ❌ var - Ancienne méthode (à éviter)
var nom = "Alice";

// ✅ let - Variable réassignable
let age = 25;
age = 26; // OK

// ✅ const - Constante (non réassignable)
const PI = 3.14159;
// PI = 3.14; // ❌ Erreur !
```

<div class="mt-4 p-4 bg-yellow-50 rounded-lg">

💡 **Règle d'or** : Utilisez toujours `const` par défaut, et `let` uniquement si la variable doit changer.

</div>

---

# Types de données

## Les 7 types primitifs

<div class="grid grid-cols-2 gap-6">

<div>

```js
// String (chaîne de caractères)
let nom = "Alice";
let message = 'Bonjour';
let template = `Salut ${nom}`;

// Number (nombres)
let entier = 42;
let decimal = 3.14;
let infini = Infinity;

// Boolean (booléen)
let estVrai = true;
let estFaux = false;

// Undefined (non défini)
let variable; // undefined

// Null (valeur nulle)
let vide = null;

// Symbol (symbole unique)
let symbole = Symbol('id');

// BigInt (grands nombres)
let grandNombre = 9007199254740991n;
```

</div>

<div>

### Vérifier le type

```js
typeof "Hello";     // "string"
typeof 42;          // "number"
typeof true;        // "boolean"
typeof undefined;   // "undefined"
typeof null;        // "object" (bug historique !)
typeof {};          // "object"
typeof [];          // "object"
typeof function(){}; // "function"
```

</div>

</div>

---

# Opérateurs

## Opérateurs arithmétiques

```js
let a = 10;
let b = 3;

a + b;   // 13 (addition)
a - b;   // 7  (soustraction)
a * b;   // 30 (multiplication)
a / b;   // 3.333... (division)
a % b;   // 1  (modulo - reste)
a ** b;  // 1000 (puissance)

// Incrémentation / Décrémentation
a++;     // a = 11 (post-incrément)
++a;     // a = 12 (pré-incrément)
a--;     // a = 11 (décrémentation)
```

---

# Opérateurs de comparaison

```js
let x = 5;
let y = "5";

// Égalité
x == y;   // true  (égalité lâche - conversion de type)
x === y;  // false (égalité stricte - type ET valeur)

// Inégalité
x != y;   // false
x !== y;  // true

// Comparaisons
x > 3;    // true
x < 10;   // true
x >= 5;   // true
x <= 4;   // false
```

<div class="mt-4 p-4 bg-red-50 rounded-lg">

⚠️ **Important** : Utilisez toujours `===` et `!==` pour éviter les conversions de type inattendues !

</div>

---

# Opérateurs logiques

```js
let a = true;
let b = false;

// ET logique
a && b;   // false (les deux doivent être true)

// OU logique
a || b;   // true (au moins un true)

// NON logique
!a;       // false
!b;       // true

// Combinaisons
(a || b) && !b;  // true

// Court-circuit
let nom = null;
nom || "Anonyme";  // "Anonyme" (valeur par défaut)
```

---

# 📝 EXERCICE 1

## Calculatrice simple

**Objectif** : Créer une calculatrice basique

```js
let nombre1 = 10;
let nombre2 = 3;

// TODO: Effectuer les 5 opérations de base
// et afficher les résultats avec console.log()

// Résultat attendu :
// Addition: 13
// Soustraction: 7
// Multiplication: 30
// Division: 3.333...
// Modulo: 1
```

<div class="mt-4 p-4 bg-green-50 rounded-lg">

✍️ **À vous de jouer !** Ouvrez votre éditeur et complétez le code.

</div>

---

# Solution Exercice 1

```js
let nombre1 = 10;
let nombre2 = 3;

console.log("Addition: " + (nombre1 + nombre2));
console.log("Soustraction: " + (nombre1 - nombre2));
console.log("Multiplication: " + (nombre1 * nombre2));
console.log("Division: " + (nombre1 / nombre2));
console.log("Modulo: " + (nombre1 % nombre2));

// Ou avec template literals (ES6)
console.log(`Addition: ${nombre1 + nombre2}`);
console.log(`Soustraction: ${nombre1 - nombre2}`);
console.log(`Multiplication: ${nombre1 * nombre2}`);
console.log(`Division: ${nombre1 / nombre2}`);
console.log(`Modulo: ${nombre1 % nombre2}`);
```

---

# Conditions : if/else

```js
let age = 18;

// Condition simple
if (age >= 18) {
  console.log("Majeur");
}

// if/else
if (age >= 18) {
  console.log("Majeur");
} else {
  console.log("Mineur");
}

// if/else if/else
if (age < 13) {
  console.log("Enfant");
} else if (age < 20) {
  console.log("Adolescent");
} else {
  console.log("Adulte");
}
```

---

# Conditions : switch

```js
let jour = "lundi";

switch (jour) {
  case "lundi":
    console.log("Début de semaine");
    break;
  case "vendredi":
    console.log("Bientôt le week-end !");
    break;
  case "samedi":
  case "dimanche":
    console.log("Week-end !");
    break;
  default:
    console.log("Milieu de semaine");
}
```

---

# Opérateur ternaire

## Syntaxe courte pour les conditions simples

```js
let age = 20;

// Au lieu de :
let statut;
if (age >= 18) {
  statut = "Majeur";
} else {
  statut = "Mineur";
}

// On écrit :
let statut = age >= 18 ? "Majeur" : "Mineur";

// Plus complexe :
let message = age < 13 ? "Enfant" 
             : age < 20 ? "Ado" 
             : "Adulte";
```

---

# 📝 EXERCICE 2

## Vérificateur de nombre

**Objectif** : Créer un programme qui vérifie si un nombre est pair ou impair

```js
let nombre = 7;

// TODO: Vérifier si le nombre est pair ou impair
// Utiliser l'opérateur modulo (%)
// Afficher "pair" ou "impair"

// BONUS: Vérifier aussi si le nombre est positif, négatif ou zéro
```

<div class="mt-4 p-4 bg-green-50 rounded-lg">

💡 **Indice** : Un nombre est pair si `nombre % 2 === 0`

</div>

---

# Solution Exercice 2

```js
let nombre = 7;

// Vérification pair/impair
if (nombre % 2 === 0) {
  console.log(`${nombre} est pair`);
} else {
  console.log(`${nombre} est impair`);
}

// Version ternaire
console.log(nombre % 2 === 0 ? "pair" : "impair");

// BONUS: Vérification positif/négatif/zéro
if (nombre > 0) {
  console.log("Positif");
} else if (nombre < 0) {
  console.log("Négatif");
} else {
  console.log("Zéro");
}
```

---

# Boucles : for

```js
// Boucle for classique
for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}

// Parcourir un tableau
let fruits = ["pomme", "banane", "orange"];
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

// Boucle à rebours
for (let i = 10; i >= 0; i--) {
  console.log(i);
}

// Boucle avec pas différent
for (let i = 0; i <= 20; i += 2) {
  console.log(i); // Nombres pairs jusqu'à 20
}
```

---

# Boucles : while et do...while

```js
// While (vérification avant)
let compteur = 0;
while (compteur < 5) {
  console.log(compteur);
  compteur++;
}

// Do...while (vérification après - s'exécute au moins une fois)
let nombre;
do {
  nombre = prompt("Entrez un nombre > 10:");
} while (nombre <= 10);

// Attention aux boucles infinies !
// while (true) { ... } // ❌ Ne jamais faire ça sans condition de sortie
```

---

# Contrôle de boucle : break et continue

```js
// Break : sortir de la boucle
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    break; // Sort à i = 5
  }
  console.log(i); // 0, 1, 2, 3, 4
}

// Continue : sauter l'itération actuelle
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    continue; // Passe les nombres pairs
  }
  console.log(i); // 1, 3, 5, 7, 9
}
```

---

# 📝 EXERCICE 3

## Table de multiplication

**Objectif** : Créer la table de multiplication d'un nombre

```js
let nombre = 7;

// TODO: Afficher la table de multiplication de 1 à 10
// Format attendu :
// 7 x 1 = 7
// 7 x 2 = 14
// ...
// 7 x 10 = 70
```

<div class="mt-4 p-4 bg-green-50 rounded-lg">

💡 **Indice** : Utilisez une boucle `for` de 1 à 10

</div>

---

# Solution Exercice 3

```js
let nombre = 7;

// Version avec for
for (let i = 1; i <= 10; i++) {
  console.log(`${nombre} x ${i} = ${nombre * i}`);
}

// Version avec while
let i = 1;
while (i <= 10) {
  console.log(`${nombre} x ${i} = ${nombre * i}`);
  i++;
}

// BONUS: Tables de 1 à 10
for (let table = 1; table <= 10; table++) {
  console.log(`\nTable de ${table}:`);
  for (let i = 1; i <= 10; i++) {
    console.log(`${table} x ${i} = ${table * i}`);
  }
}
```

---

# 📝 EXERCICE 4

## FizzBuzz (Classique)

**Objectif** : Programme célèbre pour tester les bases

```js
// TODO: Afficher les nombres de 1 à 100
// Règles :
// - Si divisible par 3 → "Fizz"
// - Si divisible par 5 → "Buzz"
// - Si divisible par les deux → "FizzBuzz"
// - Sinon → le nombre
```

<div class="mt-4 p-4 bg-green-50 rounded-lg">

💡 **Indice** : L'ordre des conditions est important ! Testez d'abord le cas "FizzBuzz"

</div>

---

# Solution Exercice 4

```js
for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0 && i % 5 === 0) {
    console.log("FizzBuzz");
  } else if (i % 3 === 0) {
    console.log("Fizz");
  } else if (i % 5 === 0) {
    console.log("Buzz");
  } else {
    console.log(i);
  }
}

// Version optimisée
for (let i = 1; i <= 100; i++) {
  let output = "";
  if (i % 3 === 0) output += "Fizz";
  if (i % 5 === 0) output += "Buzz";
  console.log(output || i);
}
```

---

# 🎮 MINI-PROJET Module 1

## Jeu "Plus ou Moins"

**Objectif** : Créer un jeu où l'utilisateur doit deviner un nombre

```js
// Générer un nombre aléatoire entre 1 et 100
let nombreSecret = Math.floor(Math.random() * 100) + 1;
let tentatives = 0;
let trouve = false;

console.log("🎮 Jeu du Plus ou Moins !");
console.log("Devinez le nombre entre 1 et 100");

// TODO:
// 1. Demander à l'utilisateur de deviner (utiliser prompt() en navigateur)
// 2. Comparer avec nombreSecret
// 3. Dire si c'est "plus" ou "moins"
// 4. Compter les tentatives
// 5. Féliciter quand trouvé !
```

---

# Solution Mini-Projet Module 1

```js
// Générer un nombre aléatoire entre 1 et 100
let nombreSecret = Math.floor(Math.random() * 100) + 1;
let tentatives = 0;
let trouve = false;

console.log("🎮 Jeu du Plus ou Moins !");
console.log("Devinez le nombre entre 1 et 100");

while (!trouve) {
  // En Node.js, utiliser readline ou une valeur fixe pour tester
  let guess = parseInt(prompt("Votre proposition :"));
  tentatives++;
  
  if (isNaN(guess)) {
    console.log("❌ Veuillez entrer un nombre valide");
  } else if (guess < nombreSecret) {
    console.log("📈 C'est plus !");
  } else if (guess > nombreSecret) {
    console.log("📉 C'est moins !");
  } else {
    console.log(`🎉 Bravo ! Vous avez trouvé ${nombreSecret} en ${tentatives} tentatives !`);
    trouve = true;
  }
}
```

---
layout: center
class: text-center
---

# Module 1 - Terminé !

## ✅ Ce que vous avez appris :

- Variables (let, const)
- Types de données
- Opérateurs
- Conditions (if, switch, ternaire)
- Boucles (for, while)

## 🎯 Prochain module : Fonctions

---
layout: center
class: text-center
---

# Module 2
## Fonctions et Portée

Durée : 4 heures

---

# Module 2 - Objectifs

<v-clicks>

- ✅ Différentes façons de déclarer des fonctions
- ✅ Maîtriser les paramètres et valeurs de retour
- ✅ Comprendre la portée (scope) des variables
- ✅ Utiliser les fonctions fléchées (ES6)
- ✅ Introduction aux closures

</v-clicks>

---

# Déclaration de fonction

```js
// Déclaration de fonction (function declaration)
function saluer() {
  console.log("Bonjour !");
}

// Appel de la fonction
saluer(); // "Bonjour !"

// Fonction avec paramètres
function saluerPersonne(nom) {
  console.log(`Bonjour, ${nom} !`);
}

saluerPersonne("Alice"); // "Bonjour, Alice !"

// Fonction avec valeur de retour
function addition(a, b) {
  return a + b;
}

let resultat = addition(5, 3); // 8
```

---

# Expression de fonction

```js
// Expression de fonction (function expression)
const multiplier = function(a, b) {
  return a * b;
};

let resultat = multiplier(4, 5); // 20

// Fonction anonyme
setTimeout(function() {
  console.log("Exécuté après 1 seconde");
}, 1000);

// Fonction nommée dans une expression
const factorial = function calcFactorial(n) {
  if (n <= 1) return 1;
  return n * calcFactorial(n - 1);
};
```

---

# Fonctions fléchées (Arrow functions) - ES6

```js
// Syntaxe classique
function carre(x) {
  return x * x;
}

// Fonction fléchée équivalente
const carre = (x) => {
  return x * x;
};

// Version courte (un seul paramètre, une seule expression)
const carre = x => x * x;

// Autres exemples
const addition = (a, b) => a + b;
const saluer = () => console.log("Hello !");
const creerObjet = (nom, age) => ({ nom, age }); // Note: parenthèses nécessaires

// Différence avec this (voir plus tard)
```

---

# Paramètres et arguments

```js
// Paramètres par défaut (ES6)
function saluer(nom = "Invité") {
  console.log(`Bonjour, ${nom} !`);
}

saluer();        // "Bonjour, Invité !"
saluer("Alice"); // "Bonjour, Alice !"

// Rest parameters (ES6)
function somme(...nombres) {
  return nombres.reduce((total, n) => total + n, 0);
}

somme(1, 2, 3, 4); // 10

// Arguments implicites (ancienne méthode)
function ancienne() {
  console.log(arguments); // objet similaire à un tableau
}
```

---

# 📝 EXERCICE 5

## Conversion Celsius/Fahrenheit

**Objectif** : Créer une fonction de conversion de température

```js
// TODO: Créer deux fonctions
// 1. celsiusToFahrenheit(celsius) → retourne la température en Fahrenheit
// 2. fahrenheitToCelsius(fahrenheit) → retourne la température en Celsius

// Formules :
// F = (C × 9/5) + 32
// C = (F - 32) × 5/9

// Testez avec :
console.log(celsiusToFahrenheit(0));    // 32
console.log(celsiusToFahrenheit(100));  // 212
console.log(fahrenheitToCelsius(32));   // 0
console.log(fahrenheitToCelsius(212));  // 100
```

---

# Solution Exercice 5

```js
// Version classique
function celsiusToFahrenheit(celsius) {
  return (celsius * 9/5) + 32;
}

function fahrenheitToCelsius(fahrenheit) {
  return (fahrenheit - 32) * 5/9;
}

// Version fléchée
const celsiusToFahrenheit = celsius => (celsius * 9/5) + 32;
const fahrenheitToCelsius = fahrenheit => (fahrenheit - 32) * 5/9;

// Tests
console.log(`${celsiusToFahrenheit(0)}°F`);     // 32°F
console.log(`${celsiusToFahrenheit(100)}°F`);   // 212°F
console.log(`${fahrenheitToCelsius(32)}°C`);    // 0°C
console.log(`${fahrenheitToCelsius(212)}°C`);   // 100°C
```

---

# 📝 EXERCICE 6

## Vérification de palindrome

**Objectif** : Créer une fonction qui vérifie si un mot est un palindrome

```js
// TODO: Créer la fonction estPalindrome(mot)
// Un palindrome se lit identiquement dans les deux sens
// Exemples : "radar", "kayak", "ressasser"

// Indice :
// 1. Mettre en minuscules
// 2. Retirer les espaces et ponctuation
// 3. Comparer avec la version inversée

// Testez avec :
console.log(estPalindrome("radar"));      // true
console.log(estPalindrome("Bonjour"));    // false
console.log(estPalindrome("A man a plan a canal Panama")); // true
```

---

# Solution Exercice 6

```js
function estPalindrome(mot) {
  // Nettoyer le texte (minuscules, sans espaces ni ponctuation)
  const nettoye = mot
    .toLowerCase()
    .replace(/[^a-z0-9]/g, ''); // Retire tout sauf lettres et chiffres
  
  // Inverser le texte
  const inverse = nettoye
    .split('')
    .reverse()
    .join('');
  
  // Comparer
  return nettoye === inverse;
}

// Version fléchée compacte
const estPalindrome = mot => {
  const m = mot.toLowerCase().replace(/[^a-z0-9]/g, '');
  return m === m.split('').reverse().join('');
};

// Tests
console.log(estPalindrome("radar"));                    // true
console.log(estPalindrome("Bonjour"));                  // false
console.log(estPalindrome("A man a plan a canal Panama")); // true
console.log(estPalindrome("Ésope reste ici et se repose")); // true
```

---

# Scope (Portée) des variables

```js
// Scope global
let globalVar = "Je suis globale";

function testScope() {
  // Scope local (function scope)
  let localVar = "Je suis locale";
  
  console.log(globalVar); // ✅ Accessible
  console.log(localVar);  // ✅ Accessible
  
  if (true) {
    // Block scope (avec let/const)
    let blockVar = "Je suis de bloc";
    var functionVar = "Je suis de fonction";
    
    console.log(localVar);  // ✅ Accessible
  }
  
  console.log(functionVar); // ✅ Accessible (var ignore le block scope)
  // console.log(blockVar); // ❌ Erreur !
}

testScope();
// console.log(localVar); // ❌ Erreur !
```

---

# Hoisting (Remontée)

```js
// Avec var (hoisting - remonté en haut, initialisé à undefined)
console.log(x); // undefined (pas d'erreur !)
var x = 5;

// Équivalent à :
var x;
console.log(x); // undefined
x = 5;

// Avec let/const (hoisting mais pas d'initialisation)
console.log(y); // ❌ ReferenceError !
let y = 5;

// Fonctions déclarées (hoisting complet)
direBonjour(); // ✅ Fonctionne !

function direBonjour() {
  console.log("Bonjour !");
}

// Expressions de fonction (pas de hoisting)
direSalut(); // ❌ TypeError !

const direSalut = function() {
  console.log("Salut !");
};
```

---

# Closures (Fermetures)

```js
// Une closure = fonction + son environnement lexical
function creerCompteur() {
  let compte = 0; // Variable privée
  
  return {
    incrementer: function() {
      compte++;
      return compte;
    },
    decrementer: function() {
      compte--;
      return compte;
    },
    getValeur: function() {
      return compte;
    }
  };
}

const compteur = creerCompteur();
console.log(compteur.incrementer()); // 1
console.log(compteur.incrementer()); // 2
console.log(compteur.getValeur());   // 2
console.log(compteur.compte);        // undefined (privé !)
```

---

# 📝 EXERCICE 7

## Générateur de citations

**Objectif** : Créer une fonction qui génère des citations aléatoires

```js
// TODO: Créer une fonction creerGenerateurDeCitations()
// La fonction doit retourner une autre fonction
// Chaque appel génère une citation aléatoire

const citations = [
  "Le code, c'est comme l'humour. S'il fite l'expliquer, c'est mauvais.",
  "Premature optimization is the root of all evil.",
  "Talk is cheap. Show me the code.",
  "JavaScript is the world's most misunderstood programming language."
];

const obtenirCitation = creerGenerateurDeCitations(citations);

console.log(obtenirCitation()); // Citation aléatoire
console.log(obtenirCitation()); // Une autre citation
```

---

# Solution Exercice 7

```js
function creerGenerateurDeCitations(citations) {
  // Closure - citations est "capturé" dans la portée
  return function() {
    const index = Math.floor(Math.random() * citations.length);
    return citations[index];
  };
}

// Utilisation
const citations = [
  "Le code, c'est comme l'humour...",
  "Premature optimization is the root of all evil.",
  "Talk is cheap. Show me the code.",
  "JavaScript is the world's most misunderstood..."
];

const obtenirCitation = creerGenerateurDeCitations(citations);

console.log(obtenirCitation());
console.log(obtenirCitation());

// BONUS: Générateur sans répétition
function creerGenerateurSansRepetition(citations) {
  const utilisees = new Set();
  
  return function() {
    if (utilisees.size === citations.length) {
      utilisees.clear(); // Réinitialiser quand tout est utilisé
    }
    
    let citation;
    do {
      citation = citations[Math.floor(Math.random() * citations.length)];
    } while (utilisees.has(citation));
    
    utilisees.add(citation);
    return citation;
  };
}
```

---

# 📝 EXERCICE 8

## Validation de données

**Objectif** : Créer des fonctions de validation

```js
// TODO: Créer les fonctions suivantes :
// 1. estEmailValide(email) - Vérifie le format d'email
// 2. estMotDePasseValide(mdp) - Min 8 caractères, 1 majuscule, 1 chiffre
// 3. estNumeroValide(numero) - Format téléphone (10 chiffres)

// Testez avec :
console.log(estEmailValide("test@example.com"));     // true
console.log(estEmailValide("pas-un-email"));         // false
console.log(estMotDePasseValide("Password123"));     // true
console.log(estMotDePasseValide("weak"));            // false
console.log(estNumeroValide("0612345678"));          // true
console.log(estNumeroValide("123"));                 // false
```

---

# Solution Exercice 8

```js
// Validation email avec regex
const estEmailValide = email => {
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  return regex.test(email);
};

// Validation mot de passe
const estMotDePasseValide = mdp => {
  // Min 8 caractères, 1 majuscule, 1 minuscule, 1 chiffre
  const regex = /^(?=.*[a-z])(?=.*[A-Z])(?=.*\d).{8,}$/;
  return regex.test(mdp);
};

// Validation numéro de téléphone (français)
const estNumeroValide = numero => {
  // Accepte 0X XX XX XX XX ou 10 chiffres consécutifs
  const nettoye = numero.replace(/\s/g, '');
  return /^0[1-9]\d{8}$/.test(nettoye);
};

// Tests
console.log(estEmailValide("test@example.com"));     // true
console.log(estEmailValide("pas-un-email"));         // false
console.log(estMotDePasseValide("Password123"));     // true
console.log(estMotDePasseValide("weak"));            // false
console.log(estNumeroValide("0612345678"));          // true
console.log(estNumeroValide("123"));                 // false
```

---

# 🎮 MINI-PROJET Module 2

## Convertisseur de devises

**Objectif** : Créer un convertisseur multi-devises avec historique

```js
// TODO: Créer un système de conversion de devises
// Taux de change (exemple) :
const tauxDeChange = {
  EUR: { USD: 1.08, GBP: 0.85, JPY: 162.5 },
  USD: { EUR: 0.93, GBP: 0.79, JPY: 150.5 },
  GBP: { EUR: 1.18, USD: 1.27, JPY: 191.2 },
  JPY: { EUR: 0.0062, USD: 0.0066, GBP: 0.0052 }
};

// Fonctions requises :
// 1. convertir(montant, de, vers)
// 2. ajouterHistorique(conversion)
// 3. afficherHistorique()
// 4. Creer un système avec closure pour gérer l'historique
```

---

# Solution Mini-Projet Module 2

```js
function creerConvertisseur() {
  const historique = [];
  
  const tauxDeChange = {
    EUR: { USD: 1.08, GBP: 0.85, JPY: 162.5 },
    USD: { EUR: 0.93, GBP: 0.79, JPY: 150.5 },
    GBP: { EUR: 1.18, USD: 1.27, JPY: 191.2 },
    JPY: { EUR: 0.0062, USD: 0.0066, GBP: 0.0052 }
  };
  
  return {
    convertir(montant, de, vers) {
      if (de === vers) return montant;
      
      const taux = tauxDeChange[de]?.[vers];
      if (!taux) throw new Error(`Conversion ${de} → ${vers} non supportée`);
      
      const resultat = montant * taux;
      
      this.ajouterHistorique({
        date: new Date().toLocaleString(),
        montant,
        de,
        vers,
        resultat: Number(resultat.toFixed(2))
      });
      
      return resultat;
    },
    
    ajouterHistorique(conversion) {
      historique.push(conversion);
    },
    
    afficherHistorique() {
      console.log("📊 Historique des conversions :\n");
      historique.forEach((conv, i) => {
        console.log(`${i + 1}. [${conv.date}] ${conv.montant} ${conv.de} = ${conv.resultat} ${conv.vers}`);
      });
    },
    
    getNombreConversions() {
      return historique.length;
    }
  };
}

// Utilisation
const convertisseur = creerConvertisseur();
console.log(convertisseur.convertir(100, "EUR", "USD"));
console.log(convertisseur.convertir(50, "USD", "JPY"));
convertisseur.afficherHistorique();
```

---
layout: center
class: text-center
---

# Module 2 - Terminé !

## ✅ Ce que vous avez appris :

- Déclarations et expressions de fonctions
- Fonctions fléchées ES6
- Paramètres et valeurs de retour
- Scope et closures

## 🎯 Prochain module : Objets et Tableaux

---
layout: center
class: text-center
---

# Module 3
## Objets et Tableaux

Durée : 4 heures

---

# Module 3 - Objectifs

<v-clicks>

- ✅ Manipuler les tableaux avec les méthodes modernes
- ✅ Utiliser map, filter, reduce
- ✅ Créer et manipuler des objets
- ✅ Maîtriser la destructuring ES6
- ✅ Comprendre le spread operator

</v-clicks>

---

# Tableaux - Création et accès

```js
// Création d'un tableau
let fruits = ["pomme", "banane", "orange"];

// Accès aux éléments (index commence à 0)
console.log(fruits[0]);   // "pomme"
console.log(fruits[1]);   // "banane"
console.log(fruits[2]);   // "orange"

// Propriétés utiles
console.log(fruits.length);  // 3 (nombre d'éléments)
console.log(fruits[fruits.length - 1]); // "orange" (dernier élément)

// Modifier un élément
fruits[1] = "fraise";

// Tableaux mixtes (possible mais déconseillé)
let mixte = ["texte", 42, true, { nom: "Alice" }, [1, 2, 3]];
```

---

# Méthodes de base des tableaux

```js
let fruits = ["pomme", "banane"];

// Ajouter à la fin
fruits.push("orange");        // ["pomme", "banane", "orange"]

// Retirer le dernier
let dernier = fruits.pop();   // "orange" - fruits: ["pomme", "banane"]

// Ajouter au début
fruits.unshift("fraise");     // ["fraise", "pomme", "banane"]

// Retirer le premier
let premier = fruits.shift(); // "fraise" - fruits: ["pomme", "banane"]

// Trouver l'index
let index = fruits.indexOf("banane"); // 1

// Vérifier si existe
let existe = fruits.includes("pomme"); // true

// Joindre en string
let str = fruits.join(", "); // "pomme, banane"
```

---

# Méthodes modernes : map()

## Transformer chaque élément

```js
const nombres = [1, 2, 3, 4, 5];

// Multiplier chaque nombre par 2
const doubles = nombres.map(n => n * 2);
// [2, 4, 6, 8, 10]

// Extraire une propriété
const utilisateurs = [
  { nom: "Alice", age: 25 },
  { nom: "Bob", age: 30 },
  { nom: "Charlie", age: 35 }
];

const noms = utilisateurs.map(u => u.nom);
// ["Alice", "Bob", "Charlie"]

// Transformer en HTML
const items = utilisateurs.map(u => `<li>${u.nom}</li>`);
// ["<li>Alice</li>", "<li>Bob</li>", "<li>Charlie</li>"]
```

---

# Méthodes modernes : filter()

## Filtrer les éléments

```js
const nombres = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

// Nombres pairs uniquement
const pairs = nombres.filter(n => n % 2 === 0);
// [2, 4, 6, 8, 10]

// Nombres supérieurs à 5
const grands = nombres.filter(n => n > 5);
// [6, 7, 8, 9, 10]

// Filtrer des objets
const utilisateurs = [
  { nom: "Alice", age: 25, actif: true },
  { nom: "Bob", age: 30, actif: false },
  { nom: "Charlie", age: 35, actif: true }
];

const actifs = utilisateurs.filter(u => u.actif);
// [{ Alice... }, { Charlie... }]

const majeurs = utilisateurs.filter(u => u.age >= 18);
// Tous (car tous >= 18)
```

---

# Méthodes modernes : reduce()

## Réduire à une seule valeur

```js
const nombres = [1, 2, 3, 4, 5];

// Somme de tous les nombres
const somme = nombres.reduce((total, n) => total + n, 0);
// 15

// Produit de tous les nombres
const produit = nombres.reduce((total, n) => total * n, 1);
// 120

// Trouver le maximum
const max = nombres.reduce((max, n) => n > max ? n : max);
// 5

// Compter les occurrences
const fruits = ["pomme", "banane", "pomme", "orange", "banane", "pomme"];
const compteur = fruits.reduce((acc, fruit) => {
  acc[fruit] = (acc[fruit] || 0) + 1;
  return acc;
}, {});
// { pomme: 3, banane: 2, orange: 1 }
```

---

# Chaînage des méthodes

```js
const utilisateurs = [
  { nom: "Alice", age: 25, actif: true },
  { nom: "Bob", age: 17, actif: true },
  { nom: "Charlie", age: 30, actif: false },
  { nom: "David", age: 20, actif: true }
];

// Utilisateurs actifs ET majeurs, avec seulement leur nom en majuscules
const resultat = utilisateurs
  .filter(u => u.actif && u.age >= 18)
  .map(u => u.nom.toUpperCase());

// ["ALICE", "DAVID"]

// Calculer l'âge moyen des utilisateurs actifs
const ageMoyen = utilisateurs
  .filter(u => u.actif)
  .reduce((acc, u, i, arr) => acc + u.age / arr.length, 0);

// 20.67
```

---

# 📝 EXERCICE 9

## Liste de courses

**Objectif** : Manipuler une liste de courses

```js
let courses = ["lait", "pain", "œufs", "beurre"];

// TODO: Réaliser les opérations suivantes :
// 1. Ajouter "fromage" à la fin
// 2. Ajouter "café" au début
// 3. Retirer le dernier élément et l'afficher
// 4. Vérifier si "pain" est dans la liste
// 5. Trouver l'index de "œufs"
// 6. Transformer tout en majuscules avec map()
// 7. Filtrer les éléments qui contiennent la lettre "a"
```

---

# Solution Exercice 9

```js
let courses = ["lait", "pain", "œufs", "beurre"];

// 1. Ajouter "fromage" à la fin
courses.push("fromage");
console.log(courses); // ["lait", "pain", "œufs", "beurre", "fromage"]

// 2. Ajouter "café" au début
courses.unshift("café");
console.log(courses); // ["café", "lait", "pain", "œufs", "beurre", "fromage"]

// 3. Retirer le dernier élément
let dernier = courses.pop();
console.log(`Retiré: ${dernier}`); // "fromage"

// 4. Vérifier si "pain" existe
console.log(courses.includes("pain")); // true

// 5. Trouver l'index de "œufs"
console.log(courses.indexOf("œufs")); // 3

// 6. Transformer en majuscules
const majuscules = courses.map(item => item.toUpperCase());
console.log(majuscules);

// 7. Filtrer ceux avec la lettre "a"
const avecA = courses.filter(item => item.includes("a"));
console.log(avecA); // ["lait", "pain"]
```

---

# 📝 EXERCICE 10

## Filtrage et tri d'étudiants

**Objectif** : Manipuler un tableau d'étudiants

```js
const etudiants = [
  { nom: "Alice", note: 15, classe: "A" },
  { nom: "Bob", note: 8, classe: "B" },
  { nom: "Charlie", note: 12, classe: "A" },
  { nom: "David", note: 18, classe: "B" },
  { nom: "Eve", note: 10, classe: "A" }
];

// TODO:
// 1. Étudiants avec note >= 10
// 2. Noms des étudiants de la classe "A"
// 3. Moyenne des notes
// 4. Meilleur étudiant (note la plus haute)
// 5. Trier par note décroissante
// 6. Nombre d'étudiants ayant la moyenne
```

---

# Solution Exercice 10

```js
const etudiants = [
  { nom: "Alice", note: 15, classe: "A" },
  { nom: "Bob", note: 8, classe: "B" },
  { nom: "Charlie", note: 12, classe: "A" },
  { nom: "David", note: 18, classe: "B" },
  { nom: "Eve", note: 10, classe: "A" }
];

// 1. Étudiants avec note >= 10
const admis = etudiants.filter(e => e.note >= 10);
console.log("Admis:", admis.map(e => e.nom));

// 2. Noms des étudiants de la classe "A"
const classeA = etudiants
  .filter(e => e.classe === "A")
  .map(e => e.nom);
console.log("Classe A:", classeA);

// 3. Moyenne des notes
const moyenne = etudiants.reduce((sum, e) => sum + e.note, 0) / etudiants.length;
console.log(`Moyenne: ${moyenne.toFixed(2)}`);

// 4. Meilleur étudiant
const meilleur = etudiants.reduce((max, e) => e.note > max.note ? e : max);
console.log(`Meilleur: ${meilleur.nom} (${meilleur.note})`);

// 5. Trier par note décroissante
const tries = [...etudiants].sort((a, b) => b.note - a.note);
console.log("Par note:", tries.map(e => `${e.nom}: ${e.note}`));

// 6. Nombre d'étudiants ayant la moyenne
const nbMoyenne = etudiants.filter(e => e.note >= 10).length;
console.log(`Ont la moyenne: ${nbMoyenne}/${etudiants.length}`);
```

---

# Objets JavaScript

```js
// Création d'un objet (notation littérale)
const personne = {
  nom: "Alice",
  age: 25,
  email: "alice@example.com",
  adresse: {
    rue: "123 Main St",
    ville: "Paris",
    codePostal: "75001"
  },
  hobbies: ["lecture", "sport", "musique"],
  saluer: function() {
    return `Bonjour, je suis ${this.nom}`;
  }
};

// Accès aux propriétés
console.log(personne.nom);              // "Alice" (dot notation)
console.log(personne["age"]);           // 25 (bracket notation)
console.log(personne.adresse.ville);    // "Paris"
console.log(personne.hobbies[0]);       // "lecture"
console.log(personne.saluer());         // "Bonjour, je suis Alice"
```

---

# Manipulation des objets

```js
const personne = { nom: "Alice", age: 25 };

// Ajouter une propriété
personne.email = "alice@example.com";
personne["ville"] = "Paris";

// Modifier une propriété
personne.age = 26;

// Supprimer une propriété
delete personne.ville;

// Vérifier si propriété existe
console.log("nom" in personne);      // true
console.log(personne.hasOwnProperty("age")); // true

// Obtenir les clés, valeurs, entrées
console.log(Object.keys(personne));   // ["nom", "age", "email"]
console.log(Object.values(personne)); // ["Alice", 26, "alice@..."]
console.log(Object.entries(personne)); // [["nom", "Alice"], ["age", 26], ...]
```

---

# Destructuring (ES6)

## Extraire des valeurs d'objets/tableaux

```js
// Destructuring d'objet
const personne = { nom: "Alice", age: 25, ville: "Paris" };

// Ancienne méthode
// const nom = personne.nom;
// const age = personne.age;

// Avec destructuring
const { nom, age } = personne;
console.log(nom, age); // "Alice" 25

// Avec renommage
const { nom: prenom, ville: city } = personne;
console.log(prenom, city); // "Alice" "Paris"

// Valeurs par défaut
const { nom: n, pays = "France" } = personne;
console.log(pays); // "France" (valeur par défaut)

// Destructuring imbriqué
const { adresse: { ville } } = { adresse: { ville: "Lyon" } };
console.log(ville); // "Lyon"
```

---

# Destructuring de tableaux

```js
// Destructuring de tableau
const nombres = [1, 2, 3, 4, 5];

const [premier, deuxieme] = nombres;
console.log(premier, deuxieme); // 1 2

// Ignorer des éléments
const [a, , c] = nombres;
console.log(a, c); // 1 3

// Rest operator
const [first, ...reste] = nombres;
console.log(first);    // 1
console.log(reste);    // [2, 3, 4, 5]

// Échanger des variables
let x = 1, y = 2;
[x, y] = [y, x];
console.log(x, y); // 2 1

// Dans les fonctions
function afficherCoordonnees([x, y]) {
  console.log(`X: ${x}, Y: ${y}`);
}
afficherCoordonnees([10, 20]); // X: 10, Y: 20
```

---

# Spread Operator (ES6)

```js
// Spread avec tableaux
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

// Combiner tableaux
const combine = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]

// Copier un tableau
const copie = [...arr1]; // [1, 2, 3]

// Ajouter des éléments
const avecZero = [0, ...arr1, 4]; // [0, 1, 2, 3, 4]

// Spread avec objets
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };

// Fusionner objets
const fusion = { ...obj1, ...obj2 }; // { a: 1, b: 2, c: 3, d: 4 }

// Copier et modifier
const modifie = { ...obj1, b: 20, e: 5 }; // { a: 1, b: 20, e: 5 }

// ⚠️ Copie superficielle (shallow copy) !
const original = { user: { name: "Alice" } };
const copieObj = { ...original };
copieObj.user.name = "Bob"; // Modifie aussi original !
```

---

# 📝 EXERCICE 11

## Transformation de données

**Objectif** : Transformer un tableau en objet

```js
const produits = [
  { id: 1, nom: "Laptop", prix: 999, categorie: "Tech" },
  { id: 2, nom: "Souris", prix: 29, categorie: "Tech" },
  { id: 3, nom: "Café", prix: 5, categorie: "Food" },
  { id: 4, nom: "Clavier", prix: 79, categorie: "Tech" }
];

// TODO:
// 1. Créer un objet indexé par id : { 1: {nom, prix}, 2: {...} }
// 2. Grouper par catégorie : { Tech: [...], Food: [...] }
// 3. Calculer le prix total avec reduce()
// 4. Créer un nouveau tableau avec prix TTC (20%)
// 5. Trouver le produit le moins cher par catégorie
```

---

# Solution Exercice 11

```js
const produits = [
  { id: 1, nom: "Laptop", prix: 999, categorie: "Tech" },
  { id: 2, nom: "Souris", prix: 29, categorie: "Tech" },
  { id: 3, nom: "Café", prix: 5, categorie: "Food" },
  { id: 4, nom: "Clavier", prix: 79, categorie: "Tech" }
];

// 1. Objet indexé par id
const parId = produits.reduce((acc, p) => {
  acc[p.id] = { nom: p.nom, prix: p.prix };
  return acc;
}, {});
console.log("Par ID:", parId);

// 2. Grouper par catégorie
const parCategorie = produits.reduce((acc, p) => {
  if (!acc[p.categorie]) acc[p.categorie] = [];
  acc[p.categorie].push(p);
  return acc;
}, {});
console.log("Par catégorie:", parCategorie);

// 3. Prix total
const total = produits.reduce((sum, p) => sum + p.prix, 0);
console.log(`Total: ${total}€`);

// 4. Prix TTC (20%)
const avecTTC = produits.map(p => ({
  ...p,
  prixTTC: Number((p.prix * 1.2).toFixed(2))
}));
console.log("Avec TTC:", avecTTC);

// 5. Moins cher par catégorie
const moinsCherParCat = Object.entries(parCategorie).reduce((acc, [cat, items]) => {
  acc[cat] = items.reduce((min, p) => p.prix < min.prix ? p : min);
  return acc;
}, {});
console.log("Moins cher par cat:", moinsCherParCat);
```

---

# 🎮 MINI-PROJET Module 3

## Gestionnaire de contacts

**Objectif** : Créer un système complet de gestion de contacts

```js
// TODO: Créer un gestionnaire de contacts avec :
// 1. ajouterContact({nom, email, telephone})
// 2. supprimerContact(id)
// 3. rechercherContacts(critere) - recherche dans nom/email
// 4. modifierContact(id, nouvellesDonnees)
// 5. afficherTousLesContacts()
// 6. trierContacts(critere: "nom" | "date")
// 7. filtrerParDomaineEmail(domaine) - ex: "gmail.com"

// Utiliser un système avec closure et tableau de contacts
// Chaque contact doit avoir : id, nom, email, telephone, dateCreation
```

---

# Solution Mini-Projet Module 3

```js
function creerGestionnaireContacts() {
  let contacts = [];
  let idCompteur = 1;
  
  return {
    ajouterContact({ nom, email, telephone }) {
      const contact = {
        id: idCompteur++,
        nom,
        email,
        telephone,
        dateCreation: new Date()
      };
      contacts.push(contact);
      return contact;
    },
    
    supprimerContact(id) {
      const index = contacts.findIndex(c => c.id === id);
      if (index === -1) return false;
      contacts.splice(index, 1);
      return true;
    },
    
    rechercherContacts(critere) {
      const lowerCritere = critere.toLowerCase();
      return contacts.filter(c => 
        c.nom.toLowerCase().includes(lowerCritere) ||
        c.email.toLowerCase().includes(lowerCritere)
      );
    },
    
    modifierContact(id, nouvellesDonnees) {
      const contact = contacts.find(c => c.id === id);
      if (!contact) return null;
      Object.assign(contact, nouvellesDonnees);
      return contact;
    },
    
    afficherTousLesContacts() {
      console.log("\n📒 Liste des contacts:\n");
      contacts.forEach(c => {
        console.log(`${c.id}. ${c.nom} - ${c.email} - ${c.telephone}`);
      });
      return contacts;
    },
    
    trierContacts(critere = "nom") {
      return [...contacts].sort((a, b) => {
        if (critere === "date") return b.dateCreation - a.dateCreation;
        return a.nom.localeCompare(b.nom);
      });
    },
    
    filtrerParDomaineEmail(domaine) {
      return contacts.filter(c => c.email.endsWith(`@${domaine}`));
    },
    
    getNombreContacts() {
      return contacts.length;
    }
  };
}

// Utilisation
const gestionnaire = creerGestionnaireContacts();
gestionnaire.ajouterContact({ nom: "Alice", email: "alice@gmail.com", telephone: "0612345678" });
gestionnaire.ajouterContact({ nom: "Bob", email: "bob@yahoo.com", telephone: "0687654321" });
gestionnaire.afficherTousLesContacts();
```

---
layout: center
class: text-center
---

# Module 3 - Terminé !

## ✅ Ce que vous avez appris :

- Méthodes de tableau (map, filter, reduce)
- Manipulation d'objets
- Destructuring
- Spread operator

## 🎯 Prochain module : Asynchrone

---
layout: center
class: text-center
---

# Module 4
## Asynchrone et API

Durée : 4 heures

---

# Module 4 - Objectifs

<v-clicks>

- ✅ Comprendre la programmation asynchrone
- ✅ Maîtriser les Promises
- ✅ Utiliser async/await
- ✅ Consommer des API REST
- ✅ Gérer les erreurs asynchrones

</v-clicks>

---

# Pourquoi l'asynchrone ?

```js
// ❌ Code synchrone bloquant
console.log("Début");
const resultat = operationLongue(); // Bloque pendant 5 secondes
console.log(resultat);
console.log("Fin"); // S'affiche après 5 secondes

// ✅ Code asynchrone non-bloquant
console.log("Début");
operationLongueAsync().then(resultat => {
  console.log(resultat);
});
console.log("Fin"); // S'affiche immédiatement

// Résultat:
// Début
// Fin
// resultat (après 5 secondes)
```

---

# Callbacks (Ancienne méthode)

```js
// Fonction avec callback
function chargerDonnees(url, callback) {
  setTimeout(() => {
    const donnees = { id: 1, nom: "Alice" };
    callback(null, donnees); // (erreur, données)
  }, 1000);
}

// Utilisation
chargerDonnees("/api/user", (erreur, donnees) => {
  if (erreur) {
    console.error("Erreur:", erreur);
    return;
  }
  console.log("Données:", donnees);
});

// ⚠️ Callback Hell (à éviter !)
chargerA((err, a) => {
  chargerB(a, (err, b) => {
    chargerC(b, (err, c) => {
      // ... indentation excessive
    });
  });
});
```

---

# Promises

## L'alternative moderne aux callbacks

```js
// Créer une Promise
const maPromise = new Promise((resolve, reject) => {
  // Opération asynchrone
  setTimeout(() => {
    const succes = true;
    
    if (succes) {
      resolve("Opération réussie !"); // Succès
    } else {
      reject(new Error("Échec de l'opération")); // Échec
    }
  }, 1000);
});

// Consommer une Promise
maPromise
  .then(resultat => {
    console.log(resultat); // "Opération réussie !"
  })
  .catch(erreur => {
    console.error(erreur);
  })
  .finally(() => {
    console.log("Toujours exécuté");
  });
```

---

# Chaînage de Promises

```js
function chargerUtilisateur(id) {
  return fetch(`/api/users/${id}`).then(r => r.json());
}

function chargerCommandes(utilisateurId) {
  return fetch(`/api/users/${utilisateurId}/orders`).then(r => r.json());
}

// Chaînage
chargerUtilisateur(123)
  .then(utilisateur => {
    console.log("Utilisateur:", utilisateur);
    return chargerCommandes(utilisateur.id);
  })
  .then(commandes => {
    console.log("Commandes:", commandes);
    return calculerTotal(commandes);
  })
  .then(total => {
    console.log("Total:", total);
  })
  .catch(erreur => {
    console.error("Erreur:", erreur);
  });
```

---

# Promise.all() et autres utilitaires

```js
// Promise.all() - Attendre plusieurs promesses
const promesse1 = fetch('/api/users');
const promesse2 = fetch('/api/products');
const promesse3 = fetch('/api/orders');

Promise.all([promesse1, promesse2, promesse3])
  .then(([users, products, orders]) => {
    console.log("Toutes les données chargées");
  })
  .catch(erreur => {
    // Une seule erreur fait échouer tout le batch
  });

// Promise.allSettled() - Attendre toutes (succès ou échec)
Promise.allSettled([promesse1, promesse2])
  .then(resultats => {
    resultats.forEach(r => {
      if (r.status === 'fulfilled') console.log('Succès:', r.value);
      else console.log('Échec:', r.reason);
    });
  });

// Promise.race() - Premier à terminer (succès ou échec)
Promise.race([fetch('/api'), timeout(5000)])
  .then(resultat => console.log('Requête rapide !'))
  .catch(() => console.log('Timeout !'));
```

---

# Async/Await

## Syntaxe moderne et lisible

```js
// Fonction async
async function chargerDonnees() {
  try {
    // await "pause" l'exécution jusqu'à la résolution
    const reponse = await fetch('/api/data');
    const donnees = await reponse.json();
    
    console.log("Données:", donnees);
    return donnees;
    
  } catch (erreur) {
    console.error("Erreur:", erreur);
    throw erreur;
  }
}

// Fonction fléchée async
const getUser = async (id) => {
  const response = await fetch(`/api/users/${id}`);
  if (!response.ok) throw new Error('User not found');
  return response.json();
};

// Utilisation
chargerDonnees().then(d => console.log(d));
```

---

# Async/Await - Exemple complet

```js
async function processCommande(commandeId) {
  try {
    // Charger la commande
    const commande = await fetch(`/api/orders/${commandeId}`)
      .then(r => r.json());
    
    // Charger l'utilisateur
    const utilisateur = await fetch(`/api/users/${commande.userId}`)
      .then(r => r.json());
    
    // Charger les produits en parallèle
    const produits = await Promise.all(
      commande.productIds.map(id => 
        fetch(`/api/products/${id}`).then(r => r.json())
      )
    );
    
    return {
      commande,
      utilisateur,
      produits,
      total: produits.reduce((sum, p) => sum + p.prix, 0)
    };
    
  } catch (erreur) {
    console.error(`Erreur commande ${commandeId}:`, erreur);
    throw erreur;
  }
}
```

---

# 📝 EXERCICE 12

## Créer une Promise

**Objectif** : Créer une Promise qui simule un délai

```js
// TODO: Créer une fonction attente(ms) qui retourne une Promise
// La Promise doit se résoudre après ms millisecondes

// Utilisation attendue :
attente(2000)
  .then(() => console.log("2 secondes écoulées !"));

// BONUS: Créer attenteAvecValeur(ms, valeur) 
// qui retourne la valeur après le délai
```

---

# Solution Exercice 12

```js
// Fonction attente simple
function attente(ms) {
  return new Promise(resolve => {
    setTimeout(resolve, ms);
  });
}

// Avec valeur
function attenteAvecValeur(ms, valeur) {
  return new Promise(resolve => {
    setTimeout(() => resolve(valeur), ms);
  });
}

// Versions fléchées
const attente = ms => new Promise(resolve => setTimeout(resolve, ms));
const attenteAvecValeur = (ms, valeur) => 
  new Promise(resolve => setTimeout(() => resolve(valeur), ms));

// Utilisation
attente(2000).then(() => console.log("2 secondes écoulées !"));

attenteAvecValeur(1000, "Bonjour !")
  .then(message => console.log(message)); // "Bonjour !" après 1s

// Avec async/await
async function exemple() {
  console.log("Début");
  await attente(2000);
  console.log("Après 2 secondes");
  const msg = await attenteAvecValeur(1000, "Fini !");
  console.log(msg);
}
```

---

# 📝 EXERCICE 13

## Chaîner des opérations asynchrones

**Objectif** : Créer une chaîne d'opérations asynchrones

```js
// TODO: Créer 3 fonctions qui retournent des Promises :
// 1. recupererUtilisateur(id) - retourne {id, nom} après 500ms
// 2. recupererCommandes(utilisateurId) - retourne [...] après 800ms
// 3. calculerTotal(commandes) - retourne le total après 300ms

// Chaîner ces opérations pour obtenir le total des commandes
// d'un utilisateur

// BONUS: Gérer les erreurs si l'utilisateur n'existe pas
```

---

# Solution Exercice 13

```js
// Fonctions simulant des API
const recupererUtilisateur = (id) => 
  new Promise((resolve, reject) => {
    setTimeout(() => {
      if (id <= 0) reject(new Error("ID invalide"));
      else resolve({ id, nom: "Alice" });
    }, 500);
  });

const recupererCommandes = (userId) =>
  new Promise(resolve => {
    setTimeout(() => {
      resolve([
        { id: 1, montant: 100 },
        { id: 2, montant: 200 },
        { id: 3, montant: 150 }
      ]);
    }, 800);
  });

const calculerTotal = (commandes) =>
  new Promise(resolve => {
    setTimeout(() => {
      const total = commandes.reduce((sum, c) => sum + c.montant, 0);
      resolve(total);
    }, 300);
  });

// Version avec .then()
recupererUtilisateur(123)
  .then(user => {
    console.log(`Utilisateur: ${user.nom}`);
    return recupererCommandes(user.id);
  })
  .then(commandes => calculerTotal(commandes))
  .then(total => console.log(`Total: ${total}€`))
  .catch(err => console.error("Erreur:", err.message));

// Version avec async/await (plus lisible)
async function getTotalCommandes(userId) {
  try {
    const user = await recupererUtilisateur(userId);
    console.log(`Utilisateur: ${user.nom}`);
    
    const commandes = await recupererCommandes(user.id);
    const total = await calculerTotal(commandes);
    
    console.log(`Total: ${total}€`);
    return total;
  } catch (erreur) {
    console.error("Erreur:", erreur.message);
    throw erreur;
  }
}

getTotalCommandes(123);
```

---

# Fetch API

## Faire des requêtes HTTP

```js
// GET - Récupérer des données
fetch('https://jsonplaceholder.typicode.com/users')
  .then(response => {
    if (!response.ok) {
      throw new Error(`HTTP ${response.status}`);
    }
    return response.json(); // Parser le JSON
  })
  .then(data => console.log(data))
  .catch(error => console.error('Erreur:', error));

// POST - Envoyer des données
fetch('https://api.example.com/users', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'Authorization': 'Bearer token123'
  },
  body: JSON.stringify({ nom: 'Alice', email: 'alice@test.com' })
})
  .then(r => r.json())
  .then(data => console.log('Créé:', data));
```

---

# Fetch avec Async/Await

```js
async function apiClient(url, options = {}) {
  try {
    const response = await fetch(url, options);
    
    if (!response.ok) {
      throw new Error(`Erreur HTTP: ${response.status}`);
    }
    
    return await response.json();
    
  } catch (erreur) {
    console.error('Erreur API:', erreur);
    throw erreur;
  }
}

// Utilisation
async function chargerUtilisateurs() {
  const users = await apiClient('https://jsonplaceholder.typicode.com/users');
  console.log(`${users.length} utilisateurs chargés`);
  return users;
}

async function creerUtilisateur(data) {
  return await apiClient('https://jsonplaceholder.typicode.com/users', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
  });
}
```

---

# Gestion des erreurs avancée

```js
// Retry avec exponential backoff
async function fetchWithRetry(url, options = {}, maxRetries = 3) {
  for (let i = 0; i < maxRetries; i++) {
    try {
      const response = await fetch(url, options);
      if (response.ok) return response;
      
      // Si erreur serveur, on retry
      if (response.status >= 500) throw new Error(`Server error: ${response.status}`);
      
      // Si erreur client, on ne retry pas
      throw new Error(`Client error: ${response.status}`);
      
    } catch (erreur) {
      if (i === maxRetries - 1) throw erreur;
      
      // Attendre avant de retry (exponential backoff)
      const delay = Math.pow(2, i) * 1000;
      console.log(`Retry ${i + 1}/${maxRetries} dans ${delay}ms...`);
      await new Promise(resolve => setTimeout(resolve, delay));
    }
  }
}

// Utilisation
fetchWithRetry('https://api.example.com/data')
  .then(r => r.json())
  .then(data => console.log(data))
  .catch(err => console.error('Échec après retries:', err));
```

---

# 📝 EXERCICE 14

## Récupérer des données d'API

**Objectif** : Consommer une API publique

```js
// TODO: Utiliser l'API JSONPlaceholder (https://jsonplaceholder.typicode.com/)
// pour :

// 1. Récupérer la liste des posts
// 2. Récupérer les commentaires d'un post spécifique
// 3. Afficher le nombre de commentaires par post
// 4. Trouver l'utilisateur qui a écrit le plus de posts

// Endpoints disponibles :
// GET /posts
// GET /posts/{id}
// GET /posts/{id}/comments
// GET /users
// GET /users/{id}
```

---

# Solution Exercice 14

```js
const BASE_URL = 'https://jsonplaceholder.typicode.com';

// Fonction utilitaire
async function fetchJSON(url) {
  const response = await fetch(url);
  if (!response.ok) throw new Error(`HTTP ${response.status}`);
  return response.json();
}

async function analyserPosts() {
  try {
    // 1. Récupérer tous les posts
    const posts = await fetchJSON(`${BASE_URL}/posts`);
    console.log(`Total posts: ${posts.length}`);
    
    // 2. Commentaires du premier post
    const premierPost = posts[0];
    const commentaires = await fetchJSON(`${BASE_URL}/posts/${premierPost.id}/comments`);
    console.log(`Commentaires du post ${premierPost.id}: ${commentaires.length}`);
    
    // 3. Nombre de commentaires par post (pour les 5 premiers)
    console.log("\nCommentaires par post:");
    for (let i = 0; i < 5; i++) {
      const comments = await fetchJSON(`${BASE_URL}/posts/${posts[i].id}/comments`);
      console.log(`Post ${posts[i].id}: ${comments.length} commentaires`);
    }
    
    // 4. Utilisateur avec le plus de posts
    const users = await fetchJSON(`${BASE_URL}/users`);
    const postsParUser = posts.reduce((acc, post) => {
      acc[post.userId] = (acc[post.userId] || 0) + 1;
      return acc;
    }, {});
    
    const topUserId = Object.entries(postsParUser)
      .sort((a, b) => b[1] - a[1])[0][0];
    
    const topUser = users.find(u => u.id === parseInt(topUserId));
    console.log(`\nUtilisateur le plus actif: ${topUser.name} (${postsParUser[topUserId]} posts)`);
    
  } catch (erreur) {
    console.error("Erreur:", erreur.message);
  }
}

analyserPosts();
```

---

# 🎮 MINI-PROJET Module 4

## Application Météo

**Objectif** : Créer une application météo complète

```js
// TODO: Créer une application météo qui :

// 1. Recherche une ville par nom (API OpenWeatherMap ou Open-Meteo)
// 2. Affiche la température actuelle, description, humidité
// 3. Affiche les prévisions sur 5 jours
// 4. Gère les erreurs (ville non trouvée, etc.)
// 5. Met en cache les résultats (localStorage ou variable)
// 6. Permet de comparer plusieurs villes

// API gratuite suggérée : Open-Meteo (pas de clé API requise)
// https://open-meteo.com/
// Endpoint: https://api.open-meteo.com/v1/forecast?latitude=48.8566&longitude=2.3522&current=temperature_2m,relative_humidity_2m,weather_code
```

---

# Solution Mini-Projet Module 4

```js
function creerApplicationMeteo() {
  const cache = new Map();
  
  // API Open-Meteo (gratuite, pas de clé requise)
  const API_GEO = 'https://geocoding-api.open-meteo.com/v1/search';
  const API_WEATHER = 'https://api.open-meteo.com/v1/forecast';
  
  return {
    async rechercherVille(nom) {
      const cacheKey = `geo_${nom.toLowerCase()}`;
      if (cache.has(cacheKey)) return cache.get(cacheKey);
      
      try {
        const response = await fetch(`${API_GEO}?name=${encodeURIComponent(nom)}&count=1`);
        const data = await response.json();
        
        if (!data.results || data.results.length === 0) {
          throw new Error(`Ville "${nom}" non trouvée`);
        }
        
        const ville = data.results[0];
        cache.set(cacheKey, ville);
        return ville;
      } catch (erreur) {
        console.error("Erreur recherche:", erreur.message);
        throw erreur;
      }
    },
    
    async obtenirMeteo(latitude, longitude) {
      const cacheKey = `weather_${latitude}_${longitude}`;
      if (cache.has(cacheKey)) return cache.get(cacheKey);
      
      try {
        const url = `${API_WEATHER}?latitude=${latitude}&longitude=${longitude}&current=temperature_2m,relative_humidity_2m,weather_code`;
        const response = await fetch(url);
        const data = await response.json();
        
        cache.set(cacheKey, data.current);
        return data.current;
      } catch (erreur) {
        console.error("Erreur météo:", erreur.message);
        throw erreur;
      }
    },
    
    async afficherMeteoVille(nomVille) {
      try {
        console.log(`\n🌤️  Recherche de: ${nomVille}...`);
        
        const ville = await this.rechercherVille(nomVille);
        console.log(`📍 Trouvé: ${ville.name}, ${ville.country}`);
        
        const meteo = await this.obtenirMeteo(ville.latitude, ville.longitude);
        
        console.log(`\n🌡️  Température: ${meteo.temperature_2m}°C`);
        console.log(`💧 Humidité: ${meteo.relative_humidity_2m}%`);
        console.log(`📝 Code météo: ${meteo.weather_code}`);
        
        return { ville, meteo };
      } catch (erreur) {
        console.error(`❌ Erreur: ${erreur.message}`);
      }
    },
    
    async comparerVilles(...nomsVilles) {
      console.log("\n📊 Comparaison des villes:\n");
      
      const resultats = await Promise.all(
        nomsVilles.map(nom => 
          this.afficherMeteoVille(nom).catch(() => null)
        )
      );
      
      const valides = resultats.filter(r => r !== null);
      
      if (valides.length === 0) {
        console.log("Aucune ville trouvée");
        return;
      }
      
      // Trouver la plus chaude
      const plusChaude = valides.reduce((max, r) => 
        r.meteo.temperature_2m > max.meteo.temperature_2m ? r : max
      );
      
      console.log(`\n🏆 Ville la plus chaude: ${plusChaude.ville.name} (${plusChaude.meteo.temperature_2m}°C)`);
    },
    
    viderCache() {
      cache.clear();
      console.log("Cache vidé");
    }
  };
}

// Utilisation
const meteo = creerApplicationMeteo();
meteo.afficherMeteoVille("Paris");
meteo.comparerVilles("Paris", "Londres", "Tokyo");
```

---
layout: center
class: text-center
---

# Module 4 - Terminé !

## ✅ Ce que vous avez appris :

- Programmation asynchrone
- Promises (création et consommation)
- Async/await
- Fetch API
- Gestion des erreurs

## 🎯 Prochain module : DOM et Événements

---
layout: center
class: text-center
---

# Module 5
## DOM, Événements et Projet Final

Durée : 4 heures

---

# Module 5 - Objectifs

<v-clicks>

- ✅ Comprendre le DOM (Document Object Model)
- ✅ Sélectionner et manipuler des éléments HTML
- ✅ Gérer les événements utilisateur
- ✅ Utiliser le localStorage
- ✅ Créer une application complète

</v-clicks>

---

# Qu'est-ce que le DOM ?

```
HTML                    DOM (Arbre d'objets)
─────────────────       ─────────────────────────
<html>                  document
  <head>                  └── html
  </head>                     ├── head
  <body>                      └── body
    <div id="app">                └── div#app
      <h1>Titre</h1>                  ├── h1
      <p>Texte</p>                    └── p
    </div>
  </body>
</html>
```

<div class="mt-4">

Le DOM est une **interface de programmation** qui représente la structure du document HTML comme un arbre d'objets.

JavaScript peut **lire** et **modifier** ce DOM.

</div>

---

# Sélection d'éléments

```js
// Par ID (le plus rapide)
const element = document.getElementById('monId');

// Par classe (retourne une HTMLCollection)
const elements = document.getElementsByClassName('maClasse');

// Par nom de balise
const divs = document.getElementsByTagName('div');

// querySelector (CSS selector) - premier élément
const premier = document.querySelector('.maClasse');
const bouton = document.querySelector('#app button');
const lien = document.querySelector('a[href="/home"]');

// querySelectorAll - tous les éléments (NodeList)
const tous = document.querySelectorAll('.item');
const pairs = document.querySelectorAll('.item:nth-child(even)');

// Convertir NodeList en tableau
const tableau = Array.from(tous);
// ou
const tableau2 = [...tous];
```

---

# Modifier le contenu

```js
const element = document.getElementById('titre');

// Modifier le texte (sans HTML)
element.textContent = 'Nouveau titre';

// Modifier le HTML (attention aux XSS !)
element.innerHTML = '<span style="color: red">Titre</span>';

// Modifier l'attribut
element.setAttribute('data-id', '123');
element.id = 'nouvelId';
element.className = 'titre principal';

// Ajouter/retirer une classe
element.classList.add('actif');
element.classList.remove('inactif');
element.classList.toggle('visible');
element.classList.contains('actif'); // true/false

// Modifier le style (inline)
element.style.color = 'blue';
element.style.backgroundColor = '#f0f0f0';
element.style.fontSize = '24px';
```

---

# Créer et supprimer des éléments

```js
// Créer un nouvel élément
const nouveauDiv = document.createElement('div');
nouveauDiv.textContent = 'Nouveau contenu';
nouveauDiv.className = 'item';
nouveauDiv.id = 'item-1';

// Ajouter au DOM
document.body.appendChild(nouveauDiv);

// Ajouter à un élément spécifique
const container = document.getElementById('container');
container.appendChild(nouveauDiv); // À la fin
container.insertBefore(nouveauDiv, container.firstChild); // Au début

// Insertion moderne (ES6)
container.append(nouveauDiv); // Peut ajouter du texte aussi
container.prepend(nouveauDiv); // Au début

// Supprimer un élément
nouveauDiv.remove(); // Moderne
// ou
container.removeChild(nouveauDiv); // Ancienne méthode

// Cloner un élément
const clone = element.cloneNode(true); // true = avec les enfants
```

---

# Événements

```js
const bouton = document.getElementById('monBouton');

// Ajouter un écouteur d'événement (moderne)
bouton.addEventListener('click', function(event) {
  console.log('Bouton cliqué !');
  console.log('Élément:', event.target);
  console.log('Type:', event.type);
});

// Fonction fléchée
bouton.addEventListener('click', (e) => {
  e.preventDefault(); // Empêcher le comportement par défaut
  console.log('Clic !');
});

// Supprimer un écouteur (nécessite la référence de la fonction)
function handleClick(e) {
  console.log('Clic !');
}
bouton.addEventListener('click', handleClick);
bouton.removeEventListener('click', handleClick);
```

---

# Types d'événements courants

```js
// Souris
click       // Clic
mouseover   // Souris entre dans l'élément
mouseout    // Souris sort de l'élément
mousemove   // Souris bouge sur l'élément

// Clavier
keydown     // Touche enfoncée
keyup       // Touche relâchée
keypress    // (obsolète)

// Formulaire
submit      // Soumission du formulaire
change      // Valeur modifiée (input, select)
input       // Saisie en temps réel
focus       // Élément sélectionné
blur        // Élément désélectionné

// Document
DOMContentLoaded  // DOM chargé
load              // Page complètement chargée
resize            // Fenêtre redimensionnée
scroll            // Défilement

// Touch (mobile)
touchstart  // Début du toucher
touchmove   // Mouvement
touchend    // Fin du toucher
```

---

# Délégation d'événements

```js
// ❌ Mauvaise méthode : ajouter un écouteur à chaque élément
const items = document.querySelectorAll('.item');
items.forEach(item => {
  item.addEventListener('click', () => console.log('Clic !'));
});

// ✅ Bonne méthode : délégation d'événements
const liste = document.getElementById('maListe');

liste.addEventListener('click', (e) => {
  // Vérifier si le clic est sur un .item
  if (e.target.matches('.item')) {
    console.log('Clic sur:', e.target.textContent);
  }
});

// Avantages :
// - Fonctionne avec les éléments ajoutés dynamiquement
// - Moins d'écouteurs = meilleures performances
// - Plus simple à gérer
```

---

# localStorage

## Persistance des données côté client

```js
// Stocker des données
localStorage.setItem('nom', 'Alice');
localStorage.setItem('age', '25');

// Récupérer des données
const nom = localStorage.getItem('nom'); // "Alice"
const age = localStorage.getItem('age'); // "25" (string !)

// Supprimer
localStorage.removeItem('nom');

// Tout supprimer
localStorage.clear();

// Stocker des objets (JSON)
const utilisateur = { nom: 'Alice', age: 25 };
localStorage.setItem('user', JSON.stringify(utilisateur));

// Récupérer des objets
const user = JSON.parse(localStorage.getItem('user'));
console.log(user.nom); // "Alice"

// sessionStorage - même API mais persiste uniquement pendant la session
sessionStorage.setItem('temp', 'valeur');
```

---

# 📝 EXERCICE 15

## Manipulation basique du DOM

**Objectif** : Créer une page interactive simple

```html
<!-- HTML -->
<div id="app">
  <h1 id="titre">Mon Application</h1>
  <input type="text" id="inputTexte" placeholder="Entrez du texte">
  <button id="btnAjouter">Ajouter</button>
  <ul id="liste"></ul>
</div>
```

```js
// TODO: 
// 1. Sélectionner les éléments
// 2. Au clic sur le bouton, ajouter le texte dans la liste
// 3. Vider l'input après ajout
// 4. Permettre la suppression d'un item au clic
// 5. Compter et afficher le nombre d'items
```

---

# Solution Exercice 15

```js
// Sélectionner les éléments
const titre = document.getElementById('titre');
const input = document.getElementById('inputTexte');
const bouton = document.getElementById('btnAjouter');
const liste = document.getElementById('liste');

// Fonction pour mettre à jour le compteur
function mettreAJourCompteur() {
  const nombre = liste.children.length;
  titre.textContent = `Mon Application (${nombre} items)`;
}

// Ajouter un item
function ajouterItem() {
  const texte = input.value.trim();
  
  if (texte === '') {
    alert('Veuillez entrer du texte !');
    return;
  }
  
  // Créer l'élément
  const li = document.createElement('li');
  li.textContent = texte;
  li.style.cursor = 'pointer';
  li.title = 'Cliquez pour supprimer';
  
  // Ajouter au clic pour supprimer
  li.addEventListener('click', () => {
    li.remove();
    mettreAJourCompteur();
  });
  
  // Ajouter à la liste
  liste.appendChild(li);
  
  // Vider l'input
  input.value = '';
  input.focus();
  
  mettreAJourCompteur();
}

// Écouteurs d'événements
bouton.addEventListener('click', ajouterItem);

input.addEventListener('keypress', (e) => {
  if (e.key === 'Enter') ajouterItem();
});

// Initialisation
mettreAJourCompteur();
```

---

# 📝 EXERCICE 16

## Formulaire avec validation

**Objectif** : Créer un formulaire de contact avec validation

```html
<!-- HTML -->
<form id="contactForm">
  <input type="text" id="nom" placeholder="Nom" required>
  <input type="email" id="email" placeholder="Email" required>
  <textarea id="message" placeholder="Message" required></textarea>
  <button type="submit">Envoyer</button>
</form>
<div id="erreurs"></div>
```

```js
// TODO:
// 1. Intercepter la soumission du formulaire
// 2. Valider chaque champ (nom non vide, email valide, message > 10 caractères)
// 3. Afficher les erreurs dans #erreurs
// 4. Si valide, afficher un message de succès
// 5. Sauvegarder dans localStorage (optionnel)
```

---

# Solution Exercice 16

```js
const form = document.getElementById('contactForm');
const erreursDiv = document.getElementById('erreurs');

// Fonctions de validation
const validations = {
  nom: (valeur) => valeur.trim().length >= 2 ? null : 'Le nom doit avoir au moins 2 caractères',
  email: (valeur) => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(valeur) ? null : 'Email invalide',
  message: (valeur) => valeur.trim().length >= 10 ? null : 'Le message doit avoir au moins 10 caractères'
};

function validerFormulaire(donnees) {
  const erreurs = [];
  
  for (const [champ, valeur] of Object.entries(donnees)) {
    const erreur = validations[champ]?.(valeur);
    if (erreur) erreurs.push(erreur);
  }
  
  return erreurs;
}

function afficherErreurs(erreurs) {
  if (erreurs.length === 0) {
    erreursDiv.innerHTML = '';
    return;
  }
  
  erreursDiv.innerHTML = `
    <div style="color: red; margin: 10px 0;">
      <strong>Erreurs:</strong>
      <ul>${erreurs.map(e => `<li>${e}</li>`).join('')}</ul>
    </div>
  `;
}

function sauvegarderMessage(donnees) {
  const messages = JSON.parse(localStorage.getItem('messages') || '[]');
  messages.push({ ...donnees, date: new Date().toISOString() });
  localStorage.setItem('messages', JSON.stringify(messages));
}

// Gestion de la soumission
form.addEventListener('submit', (e) => {
  e.preventDefault();
  
  const donnees = {
    nom: document.getElementById('nom').value,
    email: document.getElementById('email').value,
    message: document.getElementById('message').value
  };
  
  const erreurs = validerFormulaire(donnees);
  
  if (erreurs.length > 0) {
    afficherErreurs(erreurs);
    return;
  }
  
  // Succès
  afficherErreurs([]);
  sauvegarderMessage(donnees);
  
  erreursDiv.innerHTML = '<div style="color: green; margin: 10px 0;">Message envoyé avec succès !</div>';
  form.reset();
  
  console.log('Message sauvegardé:', donnees);
});
```

---

# 🎮 PROJET FINAL

## Todo List Complète

**Objectif** : Créer une application Todo complète avec toutes les fonctionnalités

### Fonctionnalités requises :

```js
// Structure de l'application
const todoApp = {
  // 1. Ajouter une tâche
  ajouterTache(titre) { },
  
  // 2. Marquer comme complétée/non complétée
  toggleTache(id) { },
  
  // 3. Supprimer une tâche
  supprimerTache(id) { },
  
  // 4. Filtrer les tâches (toutes/actives/complétées)
  filtrerTaches(filtre) { },
  
  // 5. Rechercher des tâches
  rechercherTaches(recherche) { },
  
  // 6. Persistance avec localStorage
  sauvegarder() { },
  charger() { },
  
  // 7. Statistiques
  getStats() { },
  
  // 8. Rendu dans le DOM
  render() { }
};
```

---

# Solution Projet Final - HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Todo List</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { 
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      min-height: 100vh;
      padding: 20px;
    }
    .container { 
      max-width: 600px; 
      margin: 0 auto; 
      background: white;
      border-radius: 12px;
      padding: 30px;
      box-shadow: 0 20px 60px rgba(0,0,0,0.3);
    }
    h1 { text-align: center; color: #333; margin-bottom: 10px; }
    .stats { 
      text-align: center; 
      color: #666; 
      margin-bottom: 20px;
      font-size: 14px;
    }
    .input-group {
      display: flex;
      gap: 10px;
      margin-bottom: 20px;
    }
    input[type="text"] {
      flex: 1;
      padding: 12px;
      border: 2px solid #e0e0e0;
      border-radius: 8px;
      font-size: 16px;
      transition: border-color 0.3s;
    }
    input[type="text"]:focus {
      outline: none;
      border-color: #667eea;
    }
    button {
      padding: 12px 24px;
      background: #667eea;
      color: white;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-size: 16px;
      transition: background 0.3s;
    }
    button:hover { background: #5568d3; }
    .filters {
      display: flex;
      gap: 10px;
      margin-bottom: 20px;
      justify-content: center;
    }
    .filter-btn {
      padding: 8px 16px;
      background: #f0f0f0;
      color: #333;
    }
    .filter-btn.active {
      background: #667eea;
      color: white;
    }
    .search {
      margin-bottom: 20px;
    }
    .task-list {
      list-style: none;
    }
    .task-item {
      display: flex;
      align-items: center;
      padding: 15px;
      background: #f8f9fa;
      border-radius: 8px;
      margin-bottom: 10px;
      transition: all 0.3s;
    }
    .task-item:hover { background: #e9ecef; }
    .task-item.completed { opacity: 0.6; }
    .task-item.completed .task-text {
      text-decoration: line-through;
      color: #999;
    }
    .checkbox {
      width: 20px;
      height: 20px;
      margin-right: 15px;
      cursor: pointer;
    }
    .task-text {
      flex: 1;
      font-size: 16px;
    }
    .delete-btn {
      background: #dc3545;
      padding: 6px 12px;
      font-size: 14px;
    }
    .delete-btn:hover { background: #c82333; }
    .empty-state {
      text-align: center;
      color: #999;
      padding: 40px;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>📝 Ma Todo List</h1>
    <div class="stats" id="stats">0 tâches • 0 complétées</div>
    
    <div class="input-group">
      <input type="text" id="taskInput" placeholder="Ajouter une nouvelle tâche...">
      <button id="addBtn">Ajouter</button>
    </div>
    
    <div class="search">
      <input type="text" id="searchInput" placeholder="🔍 Rechercher une tâche...">
    </div>
    
    <div class="filters">
      <button class="filter-btn active" data-filter="all">Toutes</button>
      <button class="filter-btn" data-filter="active">Actives</button>
      <button class="filter-btn" data-filter="completed">Complétées</button>
    </div>
    
    <ul class="task-list" id="taskList"></ul>
  </div>

  <script src="app.js"></script>
</body>
</html>
```

---

# Solution Projet Final - JavaScript

```js
// app.js
class TodoApp {
  constructor() {
    this.taches = this.charger();
    this.filtre = 'all';
    this.recherche = '';
    this.init();
  }

  init() {
    // Sélectionner les éléments DOM
    this.taskInput = document.getElementById('taskInput');
    this.addBtn = document.getElementById('addBtn');
    this.searchInput = document.getElementById('searchInput');
    this.taskList = document.getElementById('taskList');
    this.statsDiv = document.getElementById('stats');
    this.filterBtns = document.querySelectorAll('.filter-btn');

    // Écouteurs d'événements
    this.addBtn.addEventListener('click', () => this.ajouterTache());
    this.taskInput.addEventListener('keypress', (e) => {
      if (e.key === 'Enter') this.ajouterTache();
    });
    
    this.searchInput.addEventListener('input', (e) => {
      this.recherche = e.target.value.toLowerCase();
      this.render();
    });

    this.filterBtns.forEach(btn => {
      btn.addEventListener('click', () => {
        this.filterBtns.forEach(b => b.classList.remove('active'));
        btn.classList.add('active');
        this.filtre = btn.dataset.filter;
        this.render();
      });
    });

    this.render();
  }

  genererId() {
    return Date.now().toString(36) + Math.random().toString(36).substr(2);
  }

  ajouterTache() {
    const titre = this.taskInput.value.trim();
    
    if (titre === '') {
      alert('Veuillez entrer une tâche !');
      return;
    }

    const tache = {
      id: this.genererId(),
      titre,
      completee: false,
      dateCreation: new Date().toISOString()
    };

    this.taches.unshift(tache);
    this.taskInput.value = '';
    this.sauvegarder();
    this.render();
  }

  toggleTache(id) {
    const tache = this.taches.find(t => t.id === id);
    if (tache) {
      tache.completee = !tache.completee;
      this.sauvegarder();
      this.render();
    }
  }

  supprimerTache(id) {
    this.taches = this.taches.filter(t => t.id !== id);
    this.sauvegarder();
    this.render();
  }

  getStats() {
    const total = this.taches.length;
    const completees = this.taches.filter(t => t.completee).length;
    const actives = total - completees;
    return { total, completees, actives };
  }

  getTachesFiltrees() {
    let taches = this.taches;

    // Appliquer le filtre
    if (this.filtre === 'active') {
      taches = taches.filter(t => !t.completee);
    } else if (this.filtre === 'completed') {
      taches = taches.filter(t => t.completee);
    }

    // Appliquer la recherche
    if (this.recherche) {
      taches = taches.filter(t => 
        t.titre.toLowerCase().includes(this.recherche)
      );
    }

    return taches;
  }

  sauvegarder() {
    localStorage.setItem('todos', JSON.stringify(this.taches));
  }

  charger() {
    const data = localStorage.getItem('todos');
    return data ? JSON.parse(data) : [];
  }

  render() {
    const taches = this.getTachesFiltrees();
    const stats = this.getStats();

    // Mettre à jour les stats
    this.statsDiv.textContent = 
      `${stats.total} tâches • ${stats.completees} complétées • ${stats.actives} actives`;

    // Rendre la liste
    if (taches.length === 0) {
      this.taskList.innerHTML = `
        <li class="empty-state">
          ${this.recherche ? 'Aucune tâche trouvée' : 
            this.filtre === 'completed' ? 'Aucune tâche complétée' :
            this.filtre === 'active' ? 'Aucune tâche active' : 
            'Aucune tâche. Ajoutez-en une !'}
        </li>
      `;
      return;
    }

    this.taskList.innerHTML = taches.map(tache => `
      <li class="task-item ${tache.completee ? 'completed' : ''}">
        <input type="checkbox" 
               class="checkbox" 
               ${tache.completee ? 'checked' : ''} 
               onchange="app.toggleTache('${tache.id}')">
        <span class="task-text">${this.escapeHtml(tache.titre)}</span>
        <button class="delete-btn" onclick="app.supprimerTache('${tache.id}')">
          Supprimer
        </button>
      </li>
    `).join('');
  }

  escapeHtml(text) {
    const div = document.createElement('div');
    div.textContent = text;
    return div.innerHTML;
  }
}

// Initialiser l'application
const app = new TodoApp();
```

---

# Félicitations !

## 🎉 Vous avez terminé les 5 modules !

### Récapitulatif de ce que vous avez accompli :

**Module 1** ✅ Fondamentaux (variables, conditions, boucles)
- Jeu "Plus ou Moins"

**Module 2** ✅ Fonctions et Scope  
- Convertisseur de devises avec historique

**Module 3** ✅ Objets et Tableaux
- Gestionnaire de contacts

**Module 4** ✅ Asynchrone et API
- Application météo avec caching

**Module 5** ✅ DOM et Événements
- **Todo List complète** avec :
  - CRUD des tâches
  - Filtres et recherche
  - Persistance localStorage
  - Interface responsive

---

# Prochaines étapes

## Continuez votre apprentissage :

### Frameworks JavaScript
- **React** - Le plus populaire
- **Vue.js** - Progressif et accessible
- **Angular** - Enterprise-grade

### Concepts avancés
- **TypeScript** - Typage statique
- **Tests** - Jest, Testing Library
- **Build tools** - Webpack, Vite, Parcel

### Projets suggérés
- 🎮 Jeu en navigateur (Snake, Tetris)
- 📊 Dashboard avec graphiques
- 🛒 E-commerce complet
- 💬 Chat en temps réel (WebSockets)

### Ressources
- [MDN Web Docs](https://developer.mozilla.org/fr/)
- [JavaScript.info](https://javascript.info/)
- [freeCodeCamp](https://www.freecodecamp.org/)

---
layout: center
class: text-center
---

# Merci !

## Questions ?

### Ressources
📚 Repo GitHub : [github.com/devalade/javascript-essentials-slides](https://github.com/devalade/javascript-essentials-slides)

🎨 Slides créées avec [Slidev](https://sli.dev)

---

# Annexe : Référence rapide

## Méthodes de tableau essentielles

| Méthode | Description | Exemple |
|---------|-------------|---------|
| `map()` | Transformer chaque élément | `[1,2,3].map(x => x*2)` → `[2,4,6]` |
| `filter()` | Garder certains éléments | `[1,2,3].filter(x => x>1)` → `[2,3]` |
| `reduce()` | Réduire à une valeur | `[1,2,3].reduce((a,b) => a+b, 0)` → `6` |
| `find()` | Trouver un élément | `[{id:1}].find(x => x.id===1)` |
| `some()` | Au moins un match ? | `[1,2,3].some(x => x>2)` → `true` |
| `every()` | Tous match ? | `[1,2,3].every(x => x>0)` → `true` |
| `includes()` | Contient une valeur ? | `[1,2,3].includes(2)` → `true` |
| `sort()` | Trier | `[3,1,2].sort((a,b) => a-b)` → `[1,2,3]` |

---

## Opérateurs et syntaxe ES6+

```js
// Template literals
const nom = `Bonjour ${prenom} !`;

// Destructuring
const { a, b } = objet;
const [x, y] = tableau;

// Spread
const nouveau = [...ancien, item];
const fusion = { ...obj1, ...obj2 };

// Fonction fléchée
const carre = x => x * x;
const somme = (a, b) => a + b;

// Paramètres par défaut
function saluer(nom = "Invité") { }

// Rest parameters
function somme(...nombres) { }

// Optional chaining
const nom = utilisateur?.profile?.nom;

// Nullish coalescing
const valeur = input ?? "défaut";
```

---

## Gestion d'erreurs

```js
// Try/Catch/Finally
try {
  // Code risqué
  const data = JSON.parse(jsonString);
} catch (erreur) {
  // Gestion de l'erreur
  console.error("Parsing error:", erreur.message);
} finally {
  // Toujours exécuté
  console.log("Cleanup");
}

// Throw
function diviser(a, b) {
  if (b === 0) throw new Error("Division par zéro !");
  return a / b;
}

// Async/Await avec try/catch
async function chargerDonnees() {
  try {
    const response = await fetch('/api/data');
    if (!response.ok) throw new Error('HTTP ' + response.status);
    return await response.json();
  } catch (erreur) {
    console.error("Erreur:", erreur);
    throw erreur;
  }
}
```

---

## Sélecteurs DOM

```js
// Un seul élément
document.getElementById('id');
document.querySelector('.classe');
document.querySelector('#id .enfant');

// Plusieurs éléments
document.getElementsByClassName('classe');
document.getElementsByTagName('div');
document.querySelectorAll('.items');

// Navigation dans le DOM
element.parentElement;
element.children;
element.firstElementChild;
element.lastElementChild;
element.nextElementSibling;
element.previousElementSibling;

// Vérification
element.matches('.classe');
element.closest('.parent');
```

---

## Événements - Référence

```js
// Ajouter un écouteur
element.addEventListener('click', handler);
element.addEventListener('click', handler, { once: true });
element.addEventListener('click', handler, { capture: true });

// Retirer
element.removeEventListener('click', handler);

// Empêcher le comportement par défaut
event.preventDefault();

// Arrêter la propagation
event.stopPropagation();

// Informations sur l'événement
event.target;      // Élément cliqué
event.currentTarget; // Élément avec l'écouteur
event.type;        // Type d'événement
event.key;         // Touche clavier
event.clientX;     // Position X souris
event.clientY;     // Position Y souris
```

---

# Fin de la présentation

**Bonne chance pour vos projets JavaScript ! 🚀**
