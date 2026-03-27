![Test Status](https://github.com/sonnytricky/cheatsheets/actions/workflows/lint.yml/badge.svg)
[![Zensical Docs](https://img.shields.io/badge/Zensical-Docs-blue?style=flat-square)](https://zensical.org/docs/customization/)
![Release Status](https://github.com/sonnytricky/cheatsheets/actions/workflows/release.yml/badge.svg)
![Zensical Version](https://img.shields.io/github/v/release/sonnytricky/cheatsheets?label=version&style=flat-square)

---

# # cheatsheets

<p align="center">
  <img src="images/Cheat-Sheets.webp"
       alt="Ein Bild"
       width=""
       height="150">
</p>

---

# 🧭 Schritt-für-Schritt: Zensical Setup (inkl. venv)

---

## 1. Projektordner erstellen

```bash
mkdir my-docs
cd my-docs
```

---

## 2. Virtuelle Umgebung erstellen

```bash
python -m venv venv
```

### Aktivieren:

* **Linux / macOS / Code-Server:**

```bash
source venv/bin/activate
```

* **Windows:**

```bash
venv\Scripts\activate
```

👉 Danach sollte `(venv)` im Terminal stehen.

---

## 3️⃣ pip aktualisieren

```bash
python -m pip install --upgrade pip
```

---

## 4. Zensical installieren

```bash
pip install zensical
```

Optional prüfen:

```bash
zensical --help
```

---

## 5. Neues Zensical-Projekt erstellen

```bash
zensical new .
```

👉 Dadurch entsteht:

```
.
├─ .github/
├─ docs/
│  ├─ index.md
│  └─ markdown.md
└─ zensical.toml
```

---

## 6. Projekt starten (Live-Vorschau)

```bash
zensical serve
```

👉 Dann im Browser öffnen:

```
http://127.0.0.1:8000
```

💡 Wenn du im Code-Server bist und Port-Probleme hast:

```bash
zensical serve --host 0.0.0.0 --port 8080
```

---

## 7. Inhalte bearbeiten

* `docs/index.md` → Startseite
* `docs/markdown.md` → weitere Inhalte

Beispiel:

```markdown
# Hallo Welt

Das ist meine Zensical-Doku 🎉
```

---

## 8. Build für Deployment

```bash
zensical build
```

👉 Ergebnis im Ordner:

```
site/
```

Diesen kannst du hochladen zu:

* GitHub Pages
* Netlify
* Vercel

---

## 9. Abhängigkeiten speichern (empfohlen)

```bash
pip freeze > requirements.txt
```

---

### venv wieder deaktivieren

```bash
deactivate
```

---

# ⚠️ Typische Fehler & Tipps

* ❌ **venv vergessen zu aktivieren** → Pakete landen global
* ❌ **zensical new . in falschem Ordner** → Chaos 😅
* ❌ **Port blockiert** → anderen Port nutzen

---

# ✅ Kurz-Zusammenfassung

1. Ordner erstellen
2. `venv` erstellen & aktivieren
3. `pip install zensical`
4. `zensical new .`
5. `zensical serve`
6. Markdown bearbeiten
7. `zensical build` für Deployment

---

## Lizenz
Dieses Projekt ist unter der MIT-Lizenz lizenziert.


