<h1>🤔 RP - 323 - Programmation fonctionnelle</h1>

>[!TIP]
>**Référence Javascript:** <https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference>  
>**Tester du code JS** : <https://runjs.app/play>  
>**Convertir en PDF** : <https://marketplace.visualstudio.com/items?itemName=manuth.markdown-converter>

<h1>Table des matières</h1>

- [Introduction](#introduction)
- [Opérateurs javascript super-cooool 😎](#opérateurs-javascript-super-cooool-)
  - [opérateur `?:`](#opérateur-)
  - [opérateur `??`](#opérateur--1)
  - [opérateur `??=`](#opérateur--2)
  - [opérateur de décomposition 'spread' `...`](#opérateur-de-décomposition-spread-)
  - [Déstructuration](#déstructuration)
- [Date et Heure](#date-et-heure)
  - [Obtenir la date et/ou heure actuelle](#obtenir-la-date-etou-heure-actuelle)
- [Math](#math)
  - [`Math.PI` - la constante π](#mathpi---la-constante-π)
  - [`Math.abs()` - la |valeur absolue| d'un nombre](#mathabs---la-valeur-absolue-dun-nombre)
  - [`Math.pow()` - élever à une puissance](#mathpow---élever-à-une-puissance)
  - [`Math.min()` - plus petite valeur](#mathmin---plus-petite-valeur)
  - [`Math.max()` - plus grande valeur](#mathmax---plus-grande-valeur)
  - [`Math.ceil()` - arrondir à la prochaine valeur entière la plus proche](#mathceil---arrondir-à-la-prochaine-valeur-entière-la-plus-proche)
  - [`Math.floor()` - arrondir à la précédente valeur entière la plus proche](#mathfloor---arrondir-à-la-précédente-valeur-entière-la-plus-proche)
  - [`Math.round()` - arrondir à la valeur entière la plus proche](#mathround---arrondir-à-la-valeur-entière-la-plus-proche)
  - [`Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre](#mathtrunc---supprime-la-virgule-et-retourne-la-partie-entière-dun-nombre)
  - [`Math.sqrt()` - la racine carrée d'un nombre](#mathsqrt---la-racine-carrée-dun-nombre)
  - [`Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)](#mathrandom---générer-un-nombre-aléatoire-entre-00-compris-et-10-non-compris)
- [JSON](#json)
  - [`JSON.stringify()` - transformer un objet Javascript en JSON](#jsonstringify---transformer-un-objet-javascript-en-json)
  - [`JSON.parse()` - transformer du JSON en objet Javascript](#jsonparse---transformer-du-json-en-objet-javascript)
- [Chaînes de caractères](#chaînes-de-caractères)
  - [`split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau](#split---un-ciseau-qui-coupe-une-chaîne-là-où-un-caractère-apparaît-et-produit-un-tableau)
  - [`trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)](#trim-trimstart-et-trimend---épuration-des-espaces-en-trop-dans-une-chaîne-trimming)
  - [`padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères](#padstart-et-padend---aligner-le-contenu-dans-une-chaîne-de-caractères)
- [Console](#console)
  - [`console.log()` - Afficher un message sur la console](#consolelog---afficher-un-message-sur-la-console)
  - [`console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)](#consoleinfo-warn-et-error---afficher-un-message-sur-la-console-filtrables)
  - [`console.table()` - Afficher tout un tableau ou un objet sur la console](#consoletable---afficher-tout-un-tableau-ou-un-objet-sur-la-console)
  - [`console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution](#consoletime-timelog-et-timeend---chronométrer-une-durée-dexécution)
- [Tableaux](#tableaux)
  - [`forEach` - parcourir les éléments d'un tableau](#foreach---parcourir-les-éléments-dun-tableau)
  - [`entries()` - parcourir les couples index/valeurs d'un tableau](#entries---parcourir-les-couples-indexvaleurs-dun-tableau)
  - [`in` - parcourir les clés d'un tableau](#in---parcourir-les-clés-dun-tableau)
  - [`of` - parcourir les valeurs d'un tableau](#of---parcourir-les-valeurs-dun-tableau)
  - [`find()` - premier élément qui satisfait une condition](#find---premier-élément-qui-satisfait-une-condition)
  - [`findIndex()` - premier index qui satisfait une condition](#findindex---premier-index-qui-satisfait-une-condition)
  - [`indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond](#indexof-et-lastindexof---premierdernier-élément-qui-correspond)
  - [`push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprimer au début/fin dans un tableau](#push-pop-shift-et-unshift---ajoutersupprimer-au-débutfin-dans-un-tableau)
  - [`slice()` - ne conserver que certaines lignes d'un tableau](#slice---ne-conserver-que-certaines-lignes-dun-tableau)
  - [`splice()` - supprimer/insérer/remplacer des valeurs dans un tableau](#splice---supprimerinsérerremplacer-des-valeurs-dans-un-tableau)
  - [`concat()` - joindre deux tableaux](#concat---joindre-deux-tableaux)
  - [`join()` - joindre des chaînes de caractères](#join---joindre-des-chaînes-de-caractères)
  - [`keys()` et `values()` - les clés/valeurs d'un objet](#keys-et-values---les-clésvaleurs-dun-objet)
  - [`includes()` - vérifier si une valeur est présente dans un tableau](#includes---vérifier-si-une-valeur-est-présente-dans-un-tableau)
  - [`every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau](#every-et-some---vérifier-si-plusieurs-valeurs-sont-toutesquelques-présentes-dans-un-tableau)
  - [`fill()` - remplir un tableau avec des valeurs](#fill---remplir-un-tableau-avec-des-valeurs)
  - [`flat()` - aplatir un tableau](#flat---aplatir-un-tableau)
  - [`sort()` - pour trier un tableau](#sort---pour-trier-un-tableau)
  - [`map()` - tableau avec les résultats d'une fonction](#map---tableau-avec-les-résultats-dune-fonction)
  - [`filter()` - tableau avec les éléments passant un test](#filter---tableau-avec-les-éléments-passant-un-test)
  - [`groupBy()` - regroupe les éléments d'un tableau selon une règle](#groupby---regroupe-les-éléments-dun-tableau-selon-une-règle)
  - [`flatMap()` - chaînage de map() et flat()](#flatmap---chaînage-de-map-et-flat)
  - [`reduce()` et `reduceRight()` - réduire un tableau à une seule valeur](#reduce-et-reduceright---réduire-un-tableau-à-une-seule-valeur)
  - [`reverse()` - inverser l'ordre du tableau](#reverse---inverser-lordre-du-tableau)
- [Techniques](#techniques)
  - [\`\`(backticks) - pour des expressions intelligentes](#backticks---pour-des-expressions-intelligentes)
  - [`new Set()` - pour supprimer les doublons](#new-set---pour-supprimer-les-doublons)
- [Fonctions](#fonctions)
  - [Déclaration de fonction](#déclaration-de-fonction)
  - [Fonctions immédiatement invoquées (IIFE)](#fonctions-immédiatement-invoquées-iife)
- [Conclusion](#conclusion)

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Introduction

La programmation fonctionnelle est une façon de coder qui utilise des fonctions pour transformer les données plutôt que de modifier les données directement. Ce module (323) apprend à utiliser les méthodes `map()`, `filter()` et `reduce()` en JavaScript.

Les objectifs de ce module sont :
- Comprendre la programmation fonctionnelle
- Bien utiliser `map()`, `filter()` et `reduce()`
- Chaîner ces méthodes pour résoudre des problèmes
- Écrire du code plus clair et facile à lire
- Comparer le code procédural avec le code fonctionnel

# Opérateurs javascript super-cooool 😎

## opérateur `?:`

> L'expression `question?valeur1:valeur2` retournera `valeur1` si `question` vaut `true` sinon elle retournera `valeur2`.

```javascript
const age = 15;
const resultat = age >= 18 ? 'majeur' : 'mineur'; // 'mineur'
```

## opérateur `??`

Cet opérateur logique se nomme l'opérateur de "coalescence des nuls".

> Renvoie son opérande de droite lorsque son opérande de gauche vaut `null` ou `undefined` et qui renvoie son opérande de gauche sinon.

```javascript
const foo1 = null ?? 'default'; // "default"
const foo2 = 0 ?? 42; // 0
```

>[!CAUTION]
>Contrairement à l'opérateur logique OU (`||`), l'opérande de gauche sera également renvoyé s'il s'agit d'une valeur équivalente à `false` et pas seulement `null` et `undefined`.
>
>⚠️ En d'autres termes **ATTENTION** ‼️ lors de l'utilisation de `||` pour fournir une valeur par défaut à une variable, car on peut rencontrer des comportements inattendus lorsqu'on considère certaines valeurs comme correctes et utilisables (par exemple une chaine vide `''` ou `0`) ‼️

```javascript
const foo3 = 0 || 42; // 42 => ATTENTION !
const foo4 = 1 || 42; // 1
const foo5 = null || 'salut !'; // 'salut !'
const foo6 = '' || 'salut !'; // 'salut !' => ATTENTION !
```

## opérateur `??=`

Cet opérateur logique se nomme l'opérateur d'affectation de "coalescence des nuls", également connu sous le nom d'opérateur affectation logique nulle.

> Évalue l'opérande de droite et l'attribue à gauche **UNIQUEMENT si l'opérande de gauche est nulle** (`null` ou `undefined`).

```javascript
const a = { duration: 50 };
a.duration ??= 10; // pas fait
a.speed ??= 25; // fait => { duration: 50, speed: 25 }
```

## opérateur de décomposition 'spread' `...`

L'opérateur de décomposition spread `...` permet de décomposer un itérable (comme un tableau) en en ses éléments distincts. Cela permet de rapidement copier tout ou une partie d'un tableau existant dans un autre tableau ou d'en extraire facilement des parties.

```javascript
// Combiner des valeurs existantes dans un nouveau tableau
const numbersOne = [1, 2, 3];
const numbersTwo = [4, 5, 6];
const numbersCombined = [...numbersOne, ...numbersTwo];

// Extraire uniquement ce qui est utile d'un tableau
const numbers = [1, 2, 3, 4, 5, 6];
const [one, two, ...rest] = numbers;

// Mariage d'objets avec mise à jour :-)
const myVehicle = {
    brand: 'Ford',
    model: 'Mustang',
    color: 'red',
};
const updateMyVehicle = {
    type: 'car',
    year: 2021,
    color: 'yellow',
};
const myUpdatedVehicle = { ...myVehicle, ...updateMyVehicle };
```

## Déstructuration

L'opérateur de décomposition spread `...` sert aussi à isoler certains éléments afin de les utiliser ensuite, et de **mettre le reste** d'un coup ailleurs.

```javascript
const valeurs = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
const [a, b, ...c] = valeurs;
console.log(a); // 1
console.log(b); // 2
console.log(c); // [3, 4, 5, 6, 7, 8, 9, 10]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Date et Heure

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Date)

## Obtenir la date et/ou heure actuelle

```javascript
const maintenant = new Date(); // Obtenir l'un comme l'autre

console.log(maintenant.toLocaleDateString()); // ex: "06.06.2025"
console.log(maintenant.toLocaleTimeString()); // ex: "15:23:42"

const jour = maintenant.getDate();
const mois = maintenant.getMonth() + 1; // Attention : janvier = 0
const annee = maintenant.getFullYear();
const heure = maintenant.getHours();
const minute = maintenant.getMinutes();
const seconde = maintenant.getSeconds();
console.log(`${jour}/${mois}/${annee} - ${heure}h${minute}`);

// Au format ISO (standard international)
console.log(maintenant.toISOString()); // ex: "2025-06-06T13:23:42.123Z"
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Math

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math)

## `Math.PI` - la constante π

Donne la valeur de π (Pi), environ 3.14159. Utilisé pour les cercles et formes rondes.

```javascript
const rayon = 5;
const perimetre = 2 * Math.PI * rayon; // 31.41592653589793
const aire = Math.PI * rayon * rayon; // 78.53981633974483
```

## `Math.abs()` - la \|valeur absolue\| d'un nombre

Donne la valeur positive d'un nombre. Ignore le signe (- ou +).

```javascript
console.log(Math.abs(-5)); // 5
console.log(Math.abs(5)); // 5
console.log(Math.abs(-3.14)); // 3.14
```

## `Math.pow()` - élever à une puissance

Calcule un nombre à la puissance d'un autre : base^exposant.

```javascript
console.log(Math.pow(2, 3)); // 8 (2 puissance 3)
console.log(Math.pow(5, 2)); // 25 (5 au carré)
console.log(Math.pow(10, -2)); // 0.01
```

## `Math.min()` - plus petite valeur

Trouve le plus petit nombre dans une liste.

```javascript
console.log(Math.min(1, 5, 3, 9, 2)); // 1
console.log(Math.min(-10, -5, 0)); // -10
console.log(Math.min()); // Infinity
```

## `Math.max()` - plus grande valeur

Trouve le plus grand nombre dans une liste.

```javascript
console.log(Math.max(1, 5, 3, 9, 2)); // 9
console.log(Math.max(-10, -5, 0)); // 0
console.log(Math.max()); // -Infinity
```

## `Math.ceil()` - arrondir à la prochaine valeur entière la plus proche

Arrondit vers le haut. Donne toujours un entier égal ou plus grand.

```javascript
console.log(Math.ceil(4.2)); // 5
console.log(Math.ceil(4.9)); // 5
console.log(Math.ceil(-4.2)); // -4
console.log(Math.ceil(5)); // 5
```

## `Math.floor()` - arrondir à la précédente valeur entière la plus proche

Arrondit vers le bas. Donne toujours un entier égal ou plus petit.

```javascript
console.log(Math.floor(4.2)); // 4
console.log(Math.floor(4.9)); // 4
console.log(Math.floor(-4.2)); // -5
console.log(Math.floor(5)); // 5
```

## `Math.round()` - arrondir à la valeur entière la plus proche

Arrondit à l'entier le plus proche. Si >= 0.5, monte. Sinon, descend.

```javascript
console.log(Math.round(4.4)); // 4
console.log(Math.round(4.5)); // 5
console.log(Math.round(4.6)); // 5
console.log(Math.round(-4.5)); // -4
```

## `Math.trunc()` - supprime la virgule et retourne la partie entière d'un nombre

Enlève la partie après la virgule. Garde juste le nombre entier.

```javascript
console.log(Math.trunc(4.9)); // 4
console.log(Math.trunc(-4.9)); // -4
console.log(Math.trunc(4.1)); // 4
console.log(Math.trunc(-4.1)); // -4
```

## `Math.sqrt()` - la racine carrée d'un nombre

Calcule la racine carrée d'un nombre.

```javascript
console.log(Math.sqrt(9)); // 3
console.log(Math.sqrt(16)); // 4
console.log(Math.sqrt(2)); // 1.4142135623730951
console.log(Math.sqrt(-1)); // NaN (pas possible pour les nombres négatifs)
```

## `Math.random()` - générer un nombre aléatoire entre 0.0 (compris) et 1.0 (non compris)

Donne un nombre aléatoire entre 0 et 1. Utile pour créer du hasard.

```javascript
console.log(Math.random()); // ex: 0.123456789

// Un nombre aléatoire entre 0 et 9
const randomInt = Math.floor(Math.random() * 10);

// Un nombre aléatoire entre 1 et 6 (comme un dé)
const dice = Math.floor(Math.random() * 6) + 1;

// Un nombre aléatoire entre 10 et 20
const randomBetween = Math.random() * 10 + 10;
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# JSON

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/JSON)

## `JSON.stringify()` - transformer un objet Javascript en JSON

Convertit un objet JavaScript en texte JSON. Utile pour envoyer des données ou les sauvegarder.

```javascript
const personne = { nom: 'Alice', age: 25 };
const json = JSON.stringify(personne);
console.log(json); // {"nom":"Alice","age":25}

// Avec indentation pour lisibilité
const jsonFormaté = JSON.stringify(personne, null, 2);
```

## `JSON.parse()` - transformer du JSON en objet Javascript

Convertit du texte JSON en objet JavaScript. Inverse de stringify().

```javascript
const json = '{"nom":"Alice","age":25}';
const personne = JSON.parse(json);
console.log(personne.nom); // Alice
console.log(personne.age); // 25
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Chaînes de caractères

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/String)

## `split()` - un ciseau qui coupe une chaîne là où un caractère apparaît et produit un tableau

Coupe une chaîne en morceau selon un séparateur. Retourne un tableau.

```javascript
const texte = 'apple,banana,orange';
const fruits = texte.split(',');
console.log(fruits); // ['apple', 'banana', 'orange']

const phrase = 'Bonjour tout le monde';
const mots = phrase.split(' ');
console.log(mots); // ['Bonjour', 'tout', 'le', 'monde']
```

## `trim()`, `trimStart()` et `trimEnd()` - épuration des espaces en trop dans une chaîne (trimming)

Enlève les espaces au début et/ou à la fin d'une chaîne.

```javascript
const texte = '  Bonjour  ';
console.log(texte.trim()); // 'Bonjour'
console.log(texte.trimStart()); // 'Bonjour  '
console.log(texte.trimEnd()); // '  Bonjour'
```

## `padStart()` et `padEnd()` - aligner le contenu dans une chaîne de caractères

Ajoute des caractères au début ou à la fin pour atteindre une longueur désirée.

```javascript
const nombre = '5';
console.log(nombre.padStart(3, '0')); // '005'
console.log(nombre.padEnd(3, '.')); // '5..'

const nom = 'Alice';
console.log(nom.padStart(10, '-')); // '-----Alice'
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Console

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/API/console](https://developer.mozilla.org/fr/docs/Web/API/console)

## `console.log()` - Afficher un message sur la console

```javascript
console.log('Coucou !'); // Coucou !
```

## `console.info()`, `warn()` et `error()` - Afficher un message sur la console (filtrables)

Affichent des messages avec différents niveaux. Utile pour filtrer les messages importants.

```javascript
console.info('Information'); // Message blanc
console.warn('Attention'); // Message jaune
console.error('Erreur'); // Message rouge
```

## `console.table()` - Afficher tout un tableau ou un objet sur la console

Affiche un tableau ou un objet sous forme de table. Très lisible.

```javascript
const personnes = [
  { nom: 'Alice', age: 25 },
  { nom: 'Bob', age: 30 }
];
console.table(personnes);
```

## `console.time()`, `timeLog()` et `timeEnd()` - Chronométrer une durée d'exécution

Mesure le temps d'exécution d'un code.

```javascript
console.time('monCalcul');
// Faire du travail...
for (let i = 0; i < 1000000; i++) {}
console.timeEnd('monCalcul'); // monCalcul: 2.5ms
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Tableaux

Lien vers la documentation officielle : [https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Array)

## `forEach` - parcourir les éléments d'un tableau

Boucle sur chaque élément. Ne retourne rien.

```javascript
const fruits = ['apple', 'banana', 'orange'];
fruits.forEach((fruit, index) => {
  console.log(index, fruit);
});
```

## `entries()` - parcourir les couples index/valeurs d'un tableau

Retourne un iterateur avec l'index et la valeur.

```javascript
const fruits = ['apple', 'banana'];
for (const [index, value] of fruits.entries()) {
  console.log(index, value);
}
```

## `in` - parcourir les clés d'un tableau

Boucle sur les index (clés) du tableau.

```javascript
const fruits = ['apple', 'banana', 'orange'];
for (const index in fruits) {
  console.log(index);
}
```

## `of` - parcourir les valeurs d'un tableau

Boucle sur les valeurs du tableau.

```javascript
const fruits = ['apple', 'banana', 'orange'];
for (const fruit of fruits) {
  console.log(fruit);
}
```

## `find()` - premier élément qui satisfait une condition

Retourne le premier élément qui passe le test.

```javascript
const nombres = [10, 20, 30, 40];
const resultat = nombres.find(x => x > 25);
console.log(resultat); // 30
```

## `findIndex()` - premier index qui satisfait une condition

Retourne l'index du premier élément qui passe le test.

```javascript
const nombres = [10, 20, 30, 40];
const index = nombres.findIndex(x => x > 25);
console.log(index); // 2
```

## `indexOf()` et `lastIndexOf()` - premier/dernier élément qui correspond

Trouve la position d'une valeur dans un tableau.

```javascript
const fruits = ['apple', 'banana', 'orange', 'banana'];
console.log(fruits.indexOf('banana')); // 1
console.log(fruits.lastIndexOf('banana')); // 3
```

## `push()`, `pop()`, `shift()` et `unshift()` - ajouter/supprimer au début/fin dans un tableau

Ajoute ou enlève des éléments.

```javascript
const arr = [1, 2, 3];
arr.push(4); // Ajoute à la fin => [1, 2, 3, 4]
arr.pop(); // Enlève à la fin => [1, 2, 3]
arr.unshift(0); // Ajoute au début => [0, 1, 2, 3]
arr.shift(); // Enlève au début => [1, 2, 3]
```

## `slice()` - ne conserver que certaines lignes d'un tableau

Crée une copie d'une partie du tableau.

```javascript
const arr = [1, 2, 3, 4, 5];
const part = arr.slice(1, 4); // [2, 3, 4]
console.log(arr); // [1, 2, 3, 4, 5] (original inchangé)
```

## `splice()` - supprimer/insérer/remplacer des valeurs dans un tableau

Modifie le tableau en supprimant ou ajoutant des éléments.

```javascript
const arr = [1, 2, 3, 4, 5];
arr.splice(2, 1); // Enlève 1 élément à l'index 2
console.log(arr); // [1, 2, 4, 5]
```

## `concat()` - joindre deux tableaux

Crée un nouveau tableau en combinant plusieurs tableaux.

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const result = arr1.concat(arr2);
console.log(result); // [1, 2, 3, 4]
```

## `join()` - joindre des chaînes de caractères

Combine tous les éléments en une seule chaîne avec un séparateur.

```javascript
const fruits = ['apple', 'banana', 'orange'];
console.log(fruits.join(', ')); // "apple, banana, orange"
console.log(fruits.join('-')); // "apple-banana-orange"
```

## `keys()` et `values()` - les clés/valeurs d'un objet

Retourne les clés ou les valeurs d'un objet.

```javascript
const obj = { nom: 'Alice', age: 25 };
console.log(Object.keys(obj)); // ['nom', 'age']
console.log(Object.values(obj)); // ['Alice', 25]
```

## `includes()` - vérifier si une valeur est présente dans un tableau

Retourne true ou false selon si la valeur existe.

```javascript
const fruits = ['apple', 'banana', 'orange'];
console.log(fruits.includes('banana')); // true
console.log(fruits.includes('grape')); // false
```

## `every()` et `some()` - vérifier si plusieurs valeurs sont toutes/quelques présentes dans un tableau

every() = tous passent le test. some() = au moins un passe.

```javascript
const nombres = [2, 4, 6];
console.log(nombres.every(x => x % 2 === 0)); // true
console.log(nombres.some(x => x > 5)); // true
```

## `fill()` - remplir un tableau avec des valeurs

Remplit un tableau avec une valeur.

```javascript
const arr = [1, 2, 3, 4];
arr.fill(0);
console.log(arr); // [0, 0, 0, 0]

const arr2 = new Array(3).fill('x');
console.log(arr2); // ['x', 'x', 'x']
```

## `flat()` - aplatir un tableau

Aplatit un tableau imbriqué.

```javascript
const arr = [1, [2, 3], [4, [5, 6]]];
console.log(arr.flat()); // [1, 2, 3, 4, [5, 6]]
console.log(arr.flat(2)); // [1, 2, 3, 4, 5, 6]
```

## `sort()` - pour trier un tableau

Trie les éléments du tableau.

```javascript
const nombres = [30, 10, 20];
nombres.sort((a, b) => a - b);
console.log(nombres); // [10, 20, 30]

const fruits = ['banana', 'apple', 'orange'];
fruits.sort();
console.log(fruits); // ['apple', 'banana', 'orange']
```

## `map()` - tableau avec les résultats d'une fonction

Transforme chaque élément avec une fonction.

```javascript
const nombres = [1, 2, 3];
const doubles = nombres.map(x => x * 2);
console.log(doubles); // [2, 4, 6]
```

## `filter()` - tableau avec les éléments passant un test

Garde seulement les éléments qui passent le test.

```javascript
const nombres = [1, 2, 3, 4, 5];
const pairs = nombres.filter(x => x % 2 === 0);
console.log(pairs); // [2, 4]
```

## `groupBy()` - regroupe les éléments d'un tableau selon une règle

Groupe les éléments par catégorie.

```javascript
const personnes = [
  { nom: 'Alice', age: 25 },
  { nom: 'Bob', age: 25 },
  { nom: 'Charlie', age: 30 }
];
const groupes = Object.groupBy(personnes, p => p.age);
// { 25: [{nom: 'Alice', age: 25}, {nom: 'Bob', age: 25}], 30: [...] }
```

## `flatMap()` - chaînage de map() et flat()

Map() puis flat() en une seule étape.

```javascript
const nombres = [1, 2, 3];
const result = nombres.flatMap(x => [x, x * 2]);
console.log(result); // [1, 2, 2, 4, 3, 6]
```

## `reduce()` et `reduceRight()` - réduire un tableau à une seule valeur

Combine tous les éléments en une seule valeur.

```javascript
const nombres = [1, 2, 3, 4];
const somme = nombres.reduce((total, x) => total + x, 0);
console.log(somme); // 10
```

## `reverse()` - inverser l'ordre du tableau

Inverse l'ordre des éléments.

```javascript
const arr = [1, 2, 3, 4];
arr.reverse();
console.log(arr); // [4, 3, 2, 1]
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Techniques

## ``(backticks) - pour des expressions intelligentes

Permet d'insérer des variables directement dans une chaîne avec `${}`.

```javascript
const nom = 'Alice';
const age = 25;
console.log(`Bonjour ${nom}, tu as ${age} ans`);
// Bonjour Alice, tu as 25 ans

const prix = 19.99;
console.log(`Prix: ${prix.toFixed(2)} euros`);
// Prix: 19.99 euros
```

## `new Set()` - pour supprimer les doublons

Crée une collection qui n'accepte pas les doublons.

```javascript
const nombres = [1, 2, 2, 3, 3, 3, 4];
const unique = new Set(nombres);
console.log([...unique]); // [1, 2, 3, 4]

const fruitsUnique = [...new Set(['apple', 'banana', 'apple'])];
console.log(fruitsUnique); // ['apple', 'banana']
```

<svg height="12" width="100%" style="padding-top:2em;padding-bottom:1em">
  <rect y="5" width="100%" height="5" fill="#7191B8"/>
</svg>

# Fonctions

## Déclaration de fonction

**Standard**

```javascript
function doStuff(a, b, c) {
    return a + b + c;
}
```

**Sous forme d'expression de fonction**

```javascript
const doStuff = function (a, b, c) {
    return a + b + c;
};
```

**Sous forme d'expression de fonction anonyme**

```javascript
const doStuff = (a, b, c) => {
    return a + b + c;
};
```

**Sous forme raccourcie**

S'il n'y a qu'un seul argument et que son corps n'a qu'une seule expression, on peut omettre le return et le corps de la fonction :

```javascript
const doStuff = (a) => `Salut ${a} !`;
```

## Fonctions immédiatement invoquées (IIFE)

IIFE = Immediately Invoked Function Expressions.

Ces fonctions sont définies et **exécutées immédiatement**. Elles sont souvent utilisées pour créer un **contexte isolé** ou encapsuler du code sans polluer l’espace global.

```javascript
(function(){ ... })()
```

ou

```javascript
(() => { ... })()
```

# Conclusion

Ce document résume les concepts et les fonctions clés de JavaScript pour la programmation fonctionnelle. Les trois méthodes principales (`map()`, `filter()` et `reduce()`) sont essentielles pour transformer et analyser les données de manière efficace et lisible.

Les points clés à retenir :
- Utilisez `map()` pour transformer chaque élément d'un tableau
- Utilisez `filter()` pour garder seulement les éléments qui correspondent
- Utilisez `reduce()` pour combiner tous les éléments en une seule valeur
- Chaîner ces méthodes crée du code plus clair et puissant
- Les backticks rendent les chaînes plus lisibles
- Les Set sont utiles pour enlever les doublons

Avec la pratique, la programmation fonctionnelle devient naturelle et permet d'écrire du meilleur code.
