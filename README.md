# Wayward German Translation Mod

Eine umfassende deutsche Übersetzung für das Survival-Roguelike **Wayward**.

## Über dieses Projekt
Dieser Mod übersetzt die gesamte Spieloberfläche, Gegenstände, Kreaturen und Mechaniken von Wayward ins Deutsche. Ziel ist es, eine grammatikalisch korrekte und atmosphärisch passende Lokalisierung zu bieten, die das Spielerlebnis für deutschsprachige Spieler verbessert.

- **Basis:** Englische Sprachdatei (v2.15.2-beta)
- **Status:** In aktiver Entwicklung

## Kernmerkmale
- **Vollständige Übersetzung:** Menüs, Dialoge, Item-Beschreibungen und Nachrichten.
- **Intelligente Grammatik:** Nutzung von Waywards Lokalisierungssystem zur korrekten Handhabung von Artikeln und Pluralformen.
- **Genus-System:** Eigens implementierte Regeln zur Erkennung von männlichen, weiblichen und neutralen Substantiven mittels Tags (`{m}`, `{f}`, `{n}`).
- **Kontextsensitive Texte:** Anpassung von Satzstrukturen an die deutsche Grammatik (z. B. Verbpositionen).

## Technische Details & Mitwirkung
Der Mod nutzt komplexe `pluralizationRules` und `articleRules`, um die Besonderheiten der deutschen Sprache abzubilden.

### Geschlechts-Tags
Um die korrekten Artikel (`der`, `die`, `das`) zuzuweisen, verwenden wir im Quelltext spezielle Tags:
- `Gegenstand{m}` -> **der** Gegenstand
- `Axt{f}` -> **die** Axt
- `Floß{n}` -> **das** Floß

Diese Tags werden automatisch von der Engine verarbeitet und im Spiel ausgeblendet.

### Richtlinien für Mitwirkende
1. **Platzhalter:** Variablen wie `{TARGET}` oder `{ITEM}` dürfen nicht übersetzt werden.
2. **Pfade:** Strings, die mit `@` beginnen, sind technische Referenzen und bleiben unverändert.
3. **Formatierung:** Tags wie `{$STAT:...}` behalten ihren englischen Bezeichner, nur der angezeigte Text wird übersetzt.

## Installation
### Steam Workshop
*(Demnächst verfügbar)* - Suche im Steam Workshop nach "Wayward German Translation" und abonniere den Mod.

### Manuelle Installation
1. Lade das Repository herunter.
2. Kopiere den Ordner in dein Wayward-Mod-Verzeichnis (meist unter `Wayward/mods/`).
3. Aktiviere die Sprache in den Spieleinstellungen unter **Sprache (Language)**.

## Autor
**Alexander Kose (twonky4)**
- [GitHub Repository](https://github.com/twonky4/wayward-game-german-language)

## Lizenz
Dieses Projekt steht unter der [MIT License](LICENSE).
