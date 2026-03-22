Hier ist ein **minimales Beispiel-Repo**, das genau deinen Workflow zeigt:
👉 Markdown → (mit deinem Tool, z. B. Zensical) → HTML in `/sites` → Hosting über **GitHub Pages**

---

# 📁 Repo-Struktur

```bash
my-site/
├── content/
│   └── index.md
├── sites/
│   └── index.html
├── zensical.toml
└── README.md
```

---

# 📄 `zensical.toml` (minimal)

```toml
[build]
input = "content"
output = "sites"

[site]
title = "Meine Seite"
base_url = "/"
```

👉 Idee:

* `content/` = deine Markdown-Dateien
* `sites/` = generiertes HTML (wird von GitHub Pages gehostet)

---

# 📝 `content/index.md`

```md
# Hallo Welt

Das ist meine erste Seite 🚀

[Zur nächsten Seite](blog.html)
```

---

# 🌐 `sites/index.html` (Beispiel-Output)

*(normalerweise von deinem Tool generiert)*

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Meine Seite</title>
</head>
<body>
  <h1>Hallo Welt</h1>
  <p>Das ist meine erste Seite 🚀</p>
  <a href="blog.html">Zur nächsten Seite</a>
</body>
</html>
```

---

# ⚙️ GitHub Pages Setup

In deinem Repo:

* **Settings → Pages**
* Source: `Deploy from a branch`
* Branch: `main`
* Folder: `/sites`

---

# 🔁 Workflow

1. Markdown schreiben:

   ```bash
   content/index.md
   ```

2. Build ausführen (z. B. mit Zensical):

   ```bash
   zensical build
   ```

3. Output landet in:

   ```bash
   /sites/index.html
   ```

4. Push zu GitHub → Seite ist live 🎉

---

# 💡 Optional (empfohlen)

Füge eine `.nojekyll` Datei hinzu:

```bash
touch sites/.nojekyll
```

👉 verhindert, dass **Jekyll** sich einmischt

---

# 🧾 README.md (optional)

```md
# My Site

Static site mit Markdown → HTML → GitHub Pages

## Build
zensical build
```

---

## 🚀 Ergebnis

Deine Seite ist erreichbar unter:

```
https://username.github.io/repo-name/
```

---

Wenn du willst, kann ich dir als nächsten Schritt noch:

* Auto-Build mit GitHub Actions bauen 🔄
* oder ein etwas „schöneres“ Layout mit Templates einbauen 🎨
