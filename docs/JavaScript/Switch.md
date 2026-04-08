# 🧠 Was ist ein `switch`?

Ein `switch` ist eine **Kontrollstruktur**, mit der du **eine Variable mit mehreren möglichen Werten vergleichen** kannst.

👉 Es ist eine Alternative zu vielen `if...else if`-Abfragen.

---

# 🧱 Grundsyntax

```javascript
switch (ausdruck) {
  case wert1:
    // Code
    break;

  case wert2:
    // Code
    break;

  default:
    // Standard-Code
}
```

---

# 📌 Beispiel

```javascript
let tag = "Montag";

switch (tag) {
  case "Montag":
    console.log("Wochenstart 😩");
    break;

  case "Freitag":
    console.log("Fast Wochenende 🎉");
    break;

  default:
    console.log("Normaler Tag");
}
```

---

# 🔑 Wichtige Bestandteile

## 🔹 `case`

👉 prüft, ob der Wert übereinstimmt

```javascript
case "Montag":
```

---

## 🔹 `break`

👉 beendet den `switch`

⚠️ Ohne `break` läuft der Code weiter!

```javascript
case 1:
  console.log("Eins");
  break;
```

---

## 🔹 `default`

👉 wird ausgeführt, wenn kein `case` passt

```javascript
default:
  console.log("Unbekannt");
```

---

# ⚠️ Fallthrough (wichtige Besonderheit)

Ohne `break` passiert das:

```javascript
let x = 1;

switch (x) {
  case 1:
    console.log("Eins");
  case 2:
    console.log("Zwei");
}
```

👉 Ausgabe:

```
Eins
Zwei
```

➡️ Das nennt man **Fallthrough**

---

# 🎯 Mehrere Werte zusammenfassen

```javascript
let note = "B";

switch (note) {
  case "A":
  case "B":
    console.log("Gut 👍");
    break;

  case "C":
    console.log("Okay");
    break;
}
```

👉 mehrere Fälle → gleicher Code

---

# 🔍 Vergleichsart

👉 `switch` verwendet **strikten Vergleich (`===`)**

```javascript
switch (5) {
  case "5":
    console.log("String"); // wird NICHT ausgeführt
}
```

---

# 🧩 Alternative zu if/else

## if/else:

```javascript
if (x === 1) {
  ...
} else if (x === 2) {
  ...
}
```

## switch:

```javascript
switch (x) {
  case 1:
    ...
    break;
  case 2:
    ...
    break;
}
```

👉 `switch` ist oft **übersichtlicher bei vielen festen Werten**

---

# ⚡ Erweiterte Nutzung (Trick)

Man kann auch Bedingungen nutzen:

```javascript
let x = 10;

switch (true) {
  case x > 5:
    console.log("größer als 5");
    break;

  case x > 0:
    console.log("größer als 0");
    break;
}
```

👉 funktioniert wie `if/else`

---

# ⚠️ Typische Fehler

❌ `break` vergessen
❌ falscher Datentyp (`"5"` vs `5`)
❌ `switch` für komplexe Logik verwenden (dafür besser `if`)

---

# 🚀 Kurz zusammengefasst

`switch` ist:

* gut für **viele feste Werte**
* übersichtlicher als viele `if/else`
* basiert auf **=== Vergleich**

👉 Wichtig:

* immer `break` verwenden (außer bewusst)
* `default` nicht vergessen