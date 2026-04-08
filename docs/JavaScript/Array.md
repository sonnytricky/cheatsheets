# 🧠 Was ist ein Array?

Ein **Array** ist eine spezielle Datenstruktur, mit der du **mehrere Werte in einer einzigen Variable speichern** kannst.

```javascript
let zahlen = [1, 2, 3, 4];
let namen = ["Anna", "Max", "Lisa"];
```

👉 Zugriff erfolgt über den **Index** (beginnt bei 0):

```javascript
console.log(namen[0]); // "Anna"
```

---

# 📦 Eigenschaften von Arrays

* Arrays können **verschiedene Datentypen mischen**:

```javascript
let mix = [1, "Hallo", true];
```

* Sie sind **dynamisch** (Größe kann sich ändern)

* Sie sind eigentlich **Objekte** in JavaScript

---

# 🔧 Wichtige Array-Methoden

## ➕ Elemente hinzufügen

```javascript
arr.push("neu");     // am Ende hinzufügen
arr.unshift("start"); // am Anfang hinzufügen
```

## ➖ Elemente entfernen

```javascript
arr.pop();     // letztes Element entfernen
arr.shift();   // erstes Element entfernen
```

---

## 🔍 Suchen & Prüfen

```javascript
arr.includes("Anna");  // true/false
arr.indexOf("Anna");   // Index oder -1
arr.find(x => x > 10); // erstes passendes Element
```

---

## 🔄 Iteration (Durchlaufen)

```javascript
arr.forEach(element => console.log(element));
```

oder:

```javascript
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

---

## 🔁 Transformation

```javascript
let neu = arr.map(x => x * 2);
```

👉 erstellt **neues Array**

---

## 🧹 Filtern

```javascript
let gefiltert = arr.filter(x => x > 5);
```

---

## 📊 Reduzieren (zusammenfassen)

```javascript
let summe = arr.reduce((acc, val) => acc + val, 0);
```

---

## 🔀 Sortieren

```javascript
arr.sort(); // alphabetisch

arr.sort((a, b) => a - b); // numerisch
```

---

## 🔗 Arrays verbinden & teilen

```javascript
arr.concat([5, 6]); // verbinden

arr.slice(1, 3); // Teilarray

arr.splice(1, 2); // entfernen/ersetzen
```

---

# 🧩 Arten von Arrays / verwandte Konzepte

## 1. Normale Arrays

```javascript
let arr = [1, 2, 3];
```

---

## 2. Mehrdimensionale Arrays

```javascript
let matrix = [
  [1, 2],
  [3, 4]
];

console.log(matrix[0][1]); // 2
```

---

## 3. Typed Arrays (für Performance)

```javascript
let buffer = new Int32Array([1, 2, 3]);
```

👉 werden z. B. für:

* Spiele
* Grafik (WebGL)
* große Datenmengen genutzt

---

## 4. Array-ähnliche Objekte

Beispiele:

* `arguments`
* `NodeList`

👉 können mit `Array.from()` in echte Arrays umgewandelt werden:

```javascript
let echtesArray = Array.from(nodeList);
```

---

# ⚠️ Wichtige Besonderheiten

### 🔹 Länge

```javascript
arr.length
```

👉 kann auch gesetzt werden:

```javascript
arr.length = 2; // kürzt das Array
```

---

### 🔹 Sparse Arrays (Lücken)

```javascript
let arr = [1, , 3];
```

👉 nicht empfohlen, kann zu Bugs führen

---

### 🔹 Referenzverhalten

```javascript
let a = [1, 2];
let b = a;

b.push(3);

console.log(a); // [1, 2, 3]
```

👉 Arrays werden **per Referenz** kopiert!

---

# 🚀 Kurz zusammengefasst

Arrays in JavaScript sind:

* flexibel
* dynamisch
* sehr mächtig durch viele Methoden

👉 Die wichtigsten Methoden:

* `push`, `pop`
* `map`, `filter`, `reduce`
* `forEach`
* `slice`, `splice`
* `sort`
