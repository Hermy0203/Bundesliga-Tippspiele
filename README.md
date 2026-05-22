# ⚽ Bundesliga Tippbörse

KI-gestützte Bundesliga Tipps mit Punktewertung – als PWA auf dem iPad installierbar.

---

## 🚀 Deployment auf Vercel (kostenlos, ~5 Minuten)

### Schritt 1 – GitHub-Konto erstellen
1. Gehe zu [github.com](https://github.com) und erstelle ein kostenloses Konto (falls noch nicht vorhanden).

### Schritt 2 – Neues Repository anlegen
1. Klicke oben rechts auf **„+"** → **„New repository"**
2. Name: `bundesliga-tippboerse`
3. **Public** auswählen
4. Klicke auf **„Create repository"**

### Schritt 3 – Dateien hochladen
1. Im neuen Repository auf **„uploading an existing file"** klicken
2. Den gesamten Inhalt dieses ZIP-Ordners hochladen:
   - `package.json`
   - `vercel.json`
   - Ordner `public/` mit allen Dateien
   - Ordner `src/` mit allen Dateien
3. Klicke auf **„Commit changes"**

### Schritt 4 – Vercel verbinden
1. Gehe zu [vercel.com](https://vercel.com) und klicke auf **„Sign up"**
2. Wähle **„Continue with GitHub"** – mit deinem GitHub-Konto anmelden
3. Klicke auf **„Add New Project"**
4. Wähle dein Repository `bundesliga-tippboerse` aus
5. Klicke auf **„Deploy"** – Vercel erledigt den Rest automatisch!

### Schritt 5 – App-URL erhalten
Nach ca. 1-2 Minuten bekommst du eine URL wie:
`https://bundesliga-tippboerse.vercel.app`

---

## 📱 Auf dem iPad installieren

1. Öffne die Vercel-URL in **Safari** auf dem iPad
2. Tippe auf das **Teilen-Symbol** (□↑) in der Symbolleiste
3. Scrolle nach unten → **„Zum Home-Bildschirm"**
4. Name bestätigen → **„Hinzufügen"**

Die App erscheint jetzt als Icon auf dem Homescreen und öffnet sich im Vollbild ohne Browser-Leiste! ✅

---

## 🔑 Anthropic API Key einrichten

Die App nutzt Claude AI für die Tipps. Du benötigst einen API Key:

1. Gehe zu [console.anthropic.com](https://console.anthropic.com)
2. Erstelle einen Account und einen API Key
3. In Vercel: Gehe zu deinem Projekt → **Settings** → **Environment Variables**
4. Füge hinzu: `REACT_APP_ANTHROPIC_KEY` = dein API Key

**Hinweis:** Die App funktioniert aktuell direkt über Claude.ai ohne eigenen Key.
Für den selbst gehosteten Betrieb wird der Key benötigt.

---

## 📁 Projektstruktur

```
bundesliga-tippboerse/
├── public/
│   ├── index.html      ← HTML mit PWA Meta-Tags
│   ├── manifest.json   ← PWA Konfiguration
│   ├── sw.js           ← Service Worker (Offline)
│   └── icon.svg        ← App-Icon (ersetzbar)
├── src/
│   ├── index.js        ← React Einstiegspunkt
│   └── App.jsx         ← Hauptkomponente
├── package.json        ← Abhängigkeiten
└── vercel.json         ← Vercel Konfiguration
```
