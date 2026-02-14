# Wayward German Translation Mod

## Projektbeschreibung
Dieses Projekt ist ein Übersetzung-Mod für das Spiel **Wayward**, der die Spieloberfläche und Inhalte in die deutsche Sprache übersetzt.

- **Hauptübersetzungsdatei:** `lang/germanLanguage.json`
- **Basis:** Englische Sprachdatei der Version **2.15.2-beta**
- **Autor:** Alexander Kose (twonky4)
- **Repository:** [GitHub](https://github.com/twonky4/wayward-game-german-language)
- **Veröffentlichung:** Geplant für den Steam Workshop (publishedFileId: TODO)

## Technische Details
Der Mod nutzt das integrierte Lokalisierungssystem von Wayward:
- **Sprachdefinition:** Registriert in `mod.json` unter dem `languages` Feld.
- **Struktur:** Die Übersetzung erfolgt über Dictionaries (z. B. `items`, `creatures`), die in der JSON-Datei definiert sind.
- **Pluralisierung:** Wayward unterstützt komplexe `pluralizationRules` (Singular/Plural-Regeln, Artikelregeln), was für die deutsche Sprache besonders relevant ist.
- **Erweiterbarkeit:** Der Mod kann als eigenständige Sprache fungieren oder bestehende Sprachen erweitern.

## Interpolation & Platzhalter
Die Übersetzung nutzt ein mächtiges Interpolationssystem für dynamische Texte:
- **Argumente:** Zugriff über Index `{0}` oder Eigenschaftsnamen `{item.name}`.
- **Bedingungen:** Logische Abfragen wie `{likesVeggies?mag:hasst}` für variantenreiche Texte.
- **Formatierung:** Unterstützung für Farben (`{#f00:text}`), Fettdruck, Kursivschrift und Listen.
- **Noun Reformatting:** Automatische Anpassung von Substantiven (wichtig für Fälle und Geschlechter im Deutschen).

## Wichtige Richtlinien für die Übersetzung
Um die technische Integrität und grammatikalische Korrektheit zu gewährleisten, müssen folgende Regeln strikt befolgt werden:

1.  **Variablen & Platzhalter:** 
    - Die Namen von Variablen (z. B. `{TARGET}`, `{TOOL}`, `{ITEM}`, `{0}`) dürfen **niemals** übersetzt werden.
    - Fallback-Texte innerhalb von Platzhaltern (z. B. das "Doodad" in `{0??Doodad}`) **müssen** übersetzt werden (z. B. `{0??Objekt}`).
2.  **Technische Referenzen:**
    - Strings, die mit `@` beginnen (z. B. `"@wayward/game/germinating"`), sind technische Pfade und dürfen **nicht** übersetzt werden.
3.  **Grammatik & Satzbau:**
    - Die Position von Platzhaltern im Satz muss an die deutsche Grammatik angepasst werden. 
    - Beispiel: `"Pick Up {0??Item}"` (Englisch) -> `"{0??Gegenstand} aufheben"` (Deutsch), da das Verb im Deutschen oft am Ende steht.
4.  **Tags & Formatierung:**
    - Tags wie `{$STAT:...}`, `{$MAGIC:...}`, `BINDINGS:...` oder `{(HELP/...)}` sind Funktionselemente. Die Bezeichner darin bleiben Englisch, nur der angezeigte Text (nach einem Doppelpunkt) wird übersetzt.

## Über Wayward
Wayward ist ein herausforderndes, rundenbasiertes Survival-Roguelike in der Top-Down-Perspektive. Der Spieler strandet als Schiffbrüchiger auf einer feindseligen, prozedural generierten Insel und muss dort überleben, erkunden und bauen.

### Kernmerkmale:
- **Survival-Roguelike:** Fokus auf Überleben in einer unbarmherzigen Umgebung mit optionalem Permadeath.
- **Rundenbasiertes Gameplay:** Ermöglicht strategisches Vorgehen ohne Zeitdruck.
- **Umfangreiches Crafting:** Über 600 Gegenstände zum Entdecken und Herstellen.
- **Skill-basiertes System:** Keine klassischen Klassen; Fortschritt durch Interaktion und Nutzung von Fähigkeiten.
- **Dynamische Welt:** Tag-Nacht-Zyklus, Temperatureffekte und verschiedene Biome.
- **Reputationssystem:** Die Insel reagiert auf das Handeln des Spielers (z. B. Abholzen von Bäumen beeinflusst die Schwierigkeit).

Weitere Informationen zum Spiel und zur Modding-API finden sich im [Wayward Wiki](https://github.com/WaywardGame/types/wiki).
