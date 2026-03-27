# Anleitung zur Einrichtung des Projekts

## 1. Projektordner erstellen

```bash
mkdir my-docs
cd my-docs
```

> Alle Dateien aus der `.tar.gz` entpacken **oder** die vorhandenen Dateien in diesen Ordner verschieben.

Beinhaltete Dateien und Ordner:

```
/docs/assets/**/**          inkl. aller Unterordner und Dateien
/docs/examples/**           inkl. aller Dateien
/.release/README.md
/docs/images/**             inkl. aller Dateien
/docs/stylesheets/extra.css
/docs/index.md
/overrides/**               inkl. aller Unterordner und Dateien
/requirements.txt
/zensical.toml
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

> Nach der Aktivierung sollte `(venv)` im Terminal erscheinen.

---

## 3. Pip aktualisieren

```bash
python -m pip install --upgrade pip
```

---

## 4. Zensical installieren

```bash
pip install zensical
```

> Alternativ kannst du auch die Abhängigkeiten direkt aus `requirements.txt` installieren:

```bash
pip install -r requirements.txt
```

---

## 5. Zensical starten

```bash
zensical serve
```

> Danach sollte dein lokaler Server laufen, und du kannst die Dokumentation im Browser aufrufen.
