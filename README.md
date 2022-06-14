![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# LAB | Funcions i matrius JS

<br>

## Introducció

La manipulació de matrius en codi és una operació molt habitual. Tant si esteu creant un total per a un carretó de la compra, agafant només els primers noms d'una llista de persones o movent una peça en un tauler d'escacs, és probable que modifiqueu o manipuleu una matriu d'alguna manera.

## Requisits

- Forca aquest repo
- Clonar-lo a la vostra màquina



## Presentació

- En acabar, executeu les ordres següents:

```bash
git add.
git commit -m "Lab resolt"
git push origin master
```

- Creeu una sol·licitud d'extracció perquè els vostres TA puguin comprovar el vostre treball.

<br>


## Instruccions

Treballareu amb el fitxer `src/functions-and-arrays.js`, que ja està carregat al fitxer `index.html`.

Per executar el codi JavaScript, obriu el fitxer `index.html`, utilitzeu l'extensió VSCode [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

Per veure la sortida del vostre codi JavaScript, obriu la [Consola a les eines per a desenvolupadors](https://developer.chrome.com/docs/devtools/open/#console).

Mentre seguiu les instruccions per a cada iteració, assegureu-vos de llegir atentament les instruccions per entendre completament els requisits de la tasca. No tinguis pressa. Hauríeu de prendre el vostre temps per llegir atentament cada iteració.



### Nota sobre les proves

Aquest LAB, juntament amb alguns dels laboratoris en els quals treballareu durant el bootcamp, està equipat amb proves unitàries per proporcionar comentaris automatitzats sobre el progrés del vostre laboratori.

**Un cop hàgiu completat les iteracions bàsiques**, aneu a la secció **"Prova el teu codi"** a la part inferior. Allà se us demanarà que instal·leu les dependències de prova i que executeu les proves per comprovar quantes proves està passant el vostre codi.



<br>

### Iteració #1: Trobeu el màxim

Implementeu la funció `maxOfTwoNumbers` que pren dos nombres com a arguments i retorna el més gran.

<br>

### Iteració #2: Trobeu la paraula més llarga

Implementeu la funció `findLongestWord` que pren com a argument una matriu de paraules i retorna la més llarga. Si n'hi ha 2 amb la mateixa longitud, hauria de tornar la primera ocurrència.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
const mots = ['misteri', 'germà', 'aviador', 'cocodril', 'perla', 'hort', 'crackpot'];
```

<br>

### Iteració #3: calcula la suma

Calcular una suma pot ser tan senzill com iterar sobre una matriu i sumar cadascun dels elements.

Implementeu la funció anomenada "sumNumbers" que pren una matriu de números com a argument i retorna la suma de tots els números de la matriu. Més endavant al curs aprendrem a fer-ho utilitzant el mètode de matriu `redueix`, que farà que el vostre treball sigui molt més fàcil. De moment, practiquem la manera _"declarativa"_ d'afegir valors, utilitzant bucles.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
numbers const = [6, 12, 1, 18, 13, 16, 2, 1, 8, 10];
```

<br>

#### Bonificació - Iteració #3.1: Una funció genèrica `sum()`

**L'objectiu: aprendre a refactoritzar el codi.** :muscle:

A la iteració 3, heu creat una funció que retorna la suma d'una matriu de nombres. Però, i si volguéssim saber quant és la suma de la longitud de totes les paraules d'una matriu? Què passaria si volguéssim afegir valors _booleans_ a la barreja? No podríem utilitzar la mateixa funció que l'anterior, o millor dit, hauríem de _ajustar_-la una mica perquè es pugui reutilitzar independentment del que hi hagi a la matriu que es passa com a argument quan la funció `sumNumbers( )` es diu.

Aquí estem aplicant un concepte que anomenem **polimorfisme**, és a dir, tractar l'entrada d'una funció independentment dels tipus que es transmetin.

Implementem la funció `sum()` que calcula la suma per a la matriu plena amb (_gairebé_) qualsevol tipus de dades. Tingueu en compte que la longitud de les cadenes s'hauria d'afegir al total i que els valors booleans s'haurien de forçar als seus valors numèrics corresponents. Consulteu les proves per obtenir més detalls.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
const mixedArr = [6, 12, 'miami', 1, true, 'barca', '200', 'lisboa', 8, 10];

// hauria de tornar: 57
```

<br>

### Iteració #4: calcula la mitjana

Calcular una mitjana és una tasca extremadament habitual. Practiquem-ho una mica.

**La lògica darrere d'això:**

1. Trobeu la suma tal com vam fer al primer exercici (o què tal si reutilitzarem els _sumNumbers()_?)
2. Agafa aquesta suma i divideix-la pel nombre d'elements de la llista.

<br>

#### Nivell 1: Matriu de números

Implementeu la funció `averageNumbers` que espera una matriu de nombres i retorna la mitjana dels nombres:

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
nombres const = [2, 6, 9, 10, 7, 4, 1, 9];
```

<br>

#### Nivell 2: matriu de cadenes

Implementeu la funció anomenada "AverageWordLength" que rep com a argument únic una matriu de paraules i retorna la longitud mitjana de les paraules:

Podeu utilitzar la matriu següent per provar-vos la teva solució:

```javascript
const words = ['seat', 'correspond', 'linen', 'motif', 'hole', 'smell', 'smart', 'chaos', 'fuel', 'palace'];
```

<br>

#### Bonificació - Iteració #4.1: una funció genèrica `avg()`

Creeu la funció `avg(arr)` que rep qualsevol matriu mixta i calcula la mitjana. Considereu com a matriu mixta una matriu plena de números i/o cadenes i/o booleans. Estem seguint una lògica similar a la aplicada a la iteració de bonificació 4.1. :fer l'ullet:

```javascript
const mixedArr = [6, 12, 'miami', 1, true, 'barca', '200', 'lisboa', 8, 10];

// hauria de tornar: 5.7
```

<br>

### Iteració #5: matrius úniques

Agafeu la matriu següent, elimineu els duplicats i torneu una nova matriu. És més que probable que vulgueu consultar el mètode de matriu [`indexOf`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf).

Feu-ho en forma d'una funció `uniquifyArray` que rep una matriu de paraules com a argument.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
const words = [
  'crab',
  'poison',
  'contagious',
  'simple',
  'bring',
  'sharp',
  'playground',
  'poison',
  'communion',
  'simple',
  'bring'
];
```

<br>

### Iteració #6: Troba elements

Creem una cerca de matriu senzilla.

Declara una funció anomenada `doesWordExist` que prendrà una matriu de paraules com un argument i una paraula per cercar com a altre. Retorna "true" si existeix, en cas contrari, retorna "fals". **No** feu servir `indexOf` per a aquest.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
const words = ['machine', 'subset', 'trouble', 'starting', 'matter', 'eating', 'truth', 'disobedience'];
```

<br>

### Iteració #7: Compte la repetició

Declara una funció anomenada `howManyTimes` que prendrà una matriu de paraules com a primer argument i una paraula per cercar com a segon argument. La funció retornarà el nombre de vegades que aquesta paraula apareix a la matriu.

Podeu utilitzar la matriu següent per provar la vostra solució:

```javascript
const words = [
  'machine',
  'matter',
  'subset',
  'trouble',
  'starting',
  'matter',
  'eating',
  'matter',
  'truth',
  'disobedience',
  'matter'
];
```

<br>

### Bonificació - Iteració #8: producte de nombres adjacents

Quin és el producte més gran de quatre nombres adjacents? Considerem quatre nombres adjacents qualsevol que estiguin un al costat de l'altre horitzontalment o verticalment.

Per exemple, si tenim una matriu 5x5 com:

```bash
[1, 2, 3, 4, 5]
[ 1, 20, 3, 4, 5]
[ 1, 20, 3, 4, 5]
[ 1, 20, 3, 4, 5]
[1, 4, 3, 4, 5]
```

El millor producte serà el `20`x`20`x`20`x`4` = `32000`.

Declara una funció anomenada "greatestProduct(matrix)" per trobar-la a la graella de 20 × 20 a continuació!

```javascript
matriu constant = [
  [08, 02, 22, 97, 38, 15, 00, 40, 00, 75, 04, 05, 07, 78, 52, 12, 50, 77, 91, 08],
  [49, 49, 99, 40, 17, 81, 18, 57, 60, 87, 17, 40, 98, 43, 69, 48, 04, 56, 62, 00],
  [81, 49, 31, 73, 55, 79, 14, 29, 93, 71, 40, 67, 53, 88, 30, 03, 49, 13, 36, 65],
  [52, 70, 95, 23, 04, 60, 11, 42, 69, 24, 68, 56, 01, 32, 56, 71, 37, 02, 36, 91],
  [22, 31, 16, 71, 51, 67, 63, 89, 41, 92, 36, 54, 22, 40, 40, 28, 66, 33, 13, 80],
  [24, 47, 32, 60, 99, 03, 45, 02, 44, 75, 33, 53, 78, 36, 84, 20, 35, 17, 12, 50],
  [32, 98, 81, 28, 64, 23, 67, 10, 26, 38, 40, 67, 59, 54, 70, 66, 18, 38, 64, 70],
  [67, 26, 20, 68, 02, 62, 12, 20, 95, 63, 94, 39, 63, 08, 40, 91, 66, 49, 94, 21],
  [24, 55, 58, 05, 66, 73, 99, 26, 97, 17, 78, 78, 96, 83, 14, 88, 34, 89, 63, 72],
  [21, 36, 23, 09, 75, 00, 76, 44, 20, 45, 35, 14, 00, 61, 33, 97, 34, 31, 33, 95],
  [78, 17, 53, 28, 22, 75, 31, 67, 15, 94, 03, 80, 04, 62, 16, 14, 09, 53, 56, 92],
  [16, 39, 05, 42, 96, 35, 31, 47, 55, 58, 88, 24, 00, 17, 54, 24, 36, 29, 85, 57],
  [86, 56, 00, 48, 35, 71, 89, 07, 05, 44, 44, 37, 44, 60, 21, 58, 51, 54, 17, 58],
  [19, 80, 81, 68, 05, 94, 47, 69, 28, 73, 92, 13, 86, 52, 17, 77, 04, 89, 55, 40],
  [04, 52, 08, 83, 97, 35, 99, 16, 07, 97, 57, 32, 16, 26, 26, 79, 33, 27, 98, 66],
  [88, 36, 68, 87, 57, 62, 20, 72, 03, 46, 33, 67, 46, 55, 12, 32, 63, 93, 53, 69],
  [04, 42, 16, 73, 38, 25, 39, 11, 24, 94, 72, 18, 08, 46, 29, 32, 40, 62, 76, 36],
  [20, 69, 36, 41, 72, 30, 23, 88, 34, 62, 99, 69, 82, 67, 59, 85, 74, 04, 36, 16],
  [20, 73, 35, 29, 78, 31, 90, 01, 74, 31, 49, 71, 48, 86, 81, 16, 23, 57, 05, 54],
  [01, 70, 54, 71, 83, 51, 54, 69, 16, 92, 33, 48, 61, 43, 52, 01, 89, 19, 67, 48]
];
```

<br>

### Bonificació - Iteració #8.1: Producte de diagonals

Seguint la lògica que heu utilitzat a la iteració #8, declareu una funció anomenada `greatestProductOfDiagonals(matrix)`. Pren una matriu com a paràmetre i retorna el producte més gran dels quatre valors disposats en diagonal, en qualsevol direcció.

<br>



## Prova el teu codi

<br>

### Proves automatitzades

La prova automatitzada de programari és el procés de prova automàtica d'una aplicació per tal de verificar que compleix els requisits tècnics i que es comporta com s'espera.

Tenir _suites de proves_ sòlides us pot proporcionar tranquil·litat, ja que podreu millorar amb confiança el vostre treball mentre sabeu que no esteu trencant una funció desenvolupada anteriorment.

<br>

### Prova amb Jest

Jest és un corredor de proves automatitzat per a JavaScript.

Per executar les vostres proves, obriu el vostre terminal al directori arrel del laboratori, executeu `npm install` per instal·lar les vostres dependències i `npm run test:watch` per executar les proves i generar el fitxer `lab-solution.html`.

```shell
$ cd lab-javascript-functions-and-arrays-cat
$ npm install
$ npm run test:watch
```

<br>

En cas que vulgueu comprovar les proves, es troben al fitxer `tests/functions-and-arrays.spec.js`.

Obriu el fitxer `lab-solution.html` amb l'extensió VSCode [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).

<br>

#### Aprovar les proves

Quan codifiqueu amb proves, és molt important que llegiu i entengueu atentament els errors que esteu tenint, d'aquesta manera sabreu amb seguretat què s'espera del vostre codi.

Tingueu en compte que **no cal que executeu les funcions vosaltres mateixos**, les proves s'encarreguen de fer-ho. L'únic que heu de fer és declarar-los, assegurar-vos que tracten amb els paràmetres passats i que retornin el que s'indica a les iteracions i als missatges de prova. Per a algunes iteracions us proporcionem una matriu de mostra, perquè pugueu fer algunes proves **manuals**, si ho voleu.

__Feliç codificació!__ :heart: