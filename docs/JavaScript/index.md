# 📘 JavaScript – Übersicht

## 🧠 Was ist JavaScript?

JavaScript ist eine **Programmiersprache für das Web**, mit der du:

* Webseiten **interaktiv** machen kannst
* Logik im Browser ausführen kannst
* auch **Server (Node.js)** programmieren kannst

---

# 🧱 Grundsyntax

```javascript
let name = "Max";
const alter = 20;

console.log(name);
```

👉 `let` = veränderbar
👉 `const` = konstant

---

# 🔢 Datentypen

## Primitive Typen:

```javascript
let text = "Hallo";   // String
let zahl = 42;        // Number
let bool = true;      // Boolean
let nix = null;       // Null
let undef;            // Undefined
```

---

## Komplexe Typen:

```javascript
let arr = [1, 2, 3];        // Array
let obj = {name: "Max"};    // Objekt
```

---

# 🔀 Bedingungen

```javascript
if (alter >= 18) {
  console.log("Erwachsen");
} else {
  console.log("Minderjährig");
}
```

👉 Alternative: `switch`

---

# 🔁 Schleifen

## for-Schleife

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i);
}
```

## while-Schleife

```javascript
while (i < 5) {
  i++;
}
```

---

# 📦 Funktionen

```javascript
function begruessung(name) {
  return "Hallo " + name;
}
```

👉 Moderne Schreibweise:

```javascript
const fn = (name) => "Hallo " + name;
```

---

# 📚 Arrays

```javascript
let zahlen = [1, 2, 3];

zahlen.push(4);   // hinzufügen
zahlen.pop();     // entfernen
```

👉 wichtige Methoden:

* `map()`
* `filter()`
* `reduce()`

---

# 🧩 Objekte

```javascript
let person = {
  name: "Anna",
  alter: 25
};

console.log(person.name);
```

---

# 🌐 DOM (Webseiten steuern)

```javascript
document.getElementById("titel").textContent = "Hallo!";
```

👉 damit kannst du:

* Inhalte ändern
* Events reagieren
* Elemente erstellen

---

# 🖱️ Events

```javascript
button.addEventListener("click", () => {
  console.log("Geklickt!");
});
```

---

# ⏳ Asynchrones JavaScript

## Promise

```javascript
fetch("api")
  .then(res => res.json())
  .then(data => console.log(data));
```

## async/await

```javascript
async function ladeDaten() {
  let res = await fetch("api");
  let data = await res.json();
}
```

---

# ⚙️ Wichtige Konzepte

## 🔹 Scope (Gültigkeitsbereich)

* `let` → Block-scope
* `var` → function-scope

---

## 🔹 Hoisting

Variablen werden „nach oben gezogen“ (nur bei `var` relevant)

---

## 🔹 Closures

Funktion merkt sich äußere Variablen

---

## 🔹 this

Kontextabhängig (oft verwirrend!)

---

# 🚀 Moderne Features (ES6+)

* Arrow Functions `=>`
* Template Strings `` `Hallo ${name}` ``
* Destructuring
* Spread Operator `...`

---

# ⚠️ Typische Fehler

❌ `==` statt `===`
❌ `const` falsch verwendet
❌ `this` falsch verstanden
❌ Arrays/Objekte werden als Referenz kopiert

---

# 🧭 Wann benutze ich was?

| Aufgabe             | Lösung     |
| ------------------- | ---------- |
| mehrere Werte       | Array      |
| strukturierte Daten | Objekt     |
| viele Bedingungen   | switch     |
| Berechnungen        | Funktionen |
| Wiederholung        | Schleifen  |

---

# 🧠 Kurz gesagt

JavaScript besteht aus:

* Variablen
* Bedingungen
* Schleifen
* Funktionen
* Arrays & Objekten
* Events & DOM
* Asynchroner Logik

---
