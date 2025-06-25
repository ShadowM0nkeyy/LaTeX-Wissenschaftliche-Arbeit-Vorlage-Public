# 📄 LaTeX-Wissenschaftliche-Arbeit-Vorlage-Public

Diese Repository enthält eine einfache und anpassbare LaTeX-Vorlage für wissenschaftliche Arbeiten.

## ✨ Funktionen

Die Vorlage beinhaltet:

- 🔧 **Einfache Konfiguration**: 
Zentrale Metadaten-Datei zur Anpassung der wichtigsten Angaben (z. B. Titel, Autor, Abgabedatum)
- 📄 **Deckblatt**: Automatisch generiertes Titelblatt mit den wichtigsten Informationen
- 📚 **Automatisches Inhaltsverzeichnis**
- 🧾 **Abkürzungsverzeichnis**
- 🖼️ **Abbildungsverzeichnis**
- 📊 **Beispielhafter Inhalt**: 
Inklusive Abbildungen und Tabellen
- 📖 **Literaturverzeichnis**: 
Integration von `.bib`-Dateien via BibTeX
- 📝 **Eidesstattliche Erklärung**
- 📎 **Anhang**


## 📦 Setup & Voraussetzungen

Um diese Vorlage lokal nutzen und kompilieren zu können, wird folgende Umgebung empfohlen:

- **Visual Studio Code**
  - Erweiterung: `LaTeX Workshop`
- **MiKTeX**  
Lokale LaTeX-Distribution
- **Perl**  
  Wird für bestimmte automatische LaTeX-Skripte benötigt.
- Literaturverwaltung: **Citavi** (oder alternativ: Zotero)  
  Export der Literaturdatenbank als `.bib`-Datei zur Verwendung mit BibTeX.

### 📐 Zusatztools (optional, aber empfohlen)
- **Draw.io**  
  Erstellung von Diagrammen zur späteren Integration als Abbildungen.
- **Microsoft Excel**


## 📂 Projektstruktur

Die folgende Ordnerstruktur dient als Grundlage für deine wissenschaftliche Arbeit. Die Struktur ist modular aufgebaut und trennt klar zwischen Inhalt, Einstellungen, Abbildungen, Tabellen und Anhängen.

```text

├── 00_Base/                        ## Grundlegende Inhalte wie Deckblatt, Metadaten, Erklärungen
│   ├── 01_Metadaten.tex
│   ├── 02_Deckblatt_single.tex
│   ├── 03_Abkuerzungsverzeichnis.tex
│   └── 04_EidesstattlicheErklaerung_single.tex

├── 01_Inhalt/                      ## Hauptinhalt der Arbeit (mit Beispielkapitel)
│   ├── 01_Einleitung/
│   │   ├── 01_Einleitung.tex
│   │   ├── 01_01_Kapitel_in_Einleitung.tex
│   │   ├── 01_01_01_Unterkapitel_in_Einleitung.tex
│   │   ├── 01_StrukturInhalt.tex
│   │   └── StrukturInhalt.tex

├── 02_Datein/                      ## Grafiken, Tabellen und Bildmaterial
│   ├── 01_Bilder/00_Base/           ## Bilder für Metadaten (z. B. Logos, Hintergründe)
│   │   ├── background_hsHarz.png     
│   │   ├── LogoHochschule_Full.png
│   │   └── LogoSHHarz_Short.png
│   ├── 02_Abbildungen/              ## Alle im Projekt verwendeten Abbildungen inkl. Originaldateien
│   │   ├── 01_Originale/            ## Ursprünglich modellierte Diagramme (z. B. aus draw.io)
│   │   └── 02_Anhang/               ## Abbildungen, die nur im Anhang verwendet werden
│   │       ├── Anhang_Vereinfachte_Organigramm_BA.png
│   │       └── Vereinfachte_Organigramm_BA.png
│   └── 03_Tabellen/
│       ├── 01_Originale/            ## Ursprungsdateien der Tabellen (z. B. aus Excel)
│       └── 02_Anhang/               ## Tabellen, die nur im Anhang erscheinen
│           ├── Anhang_VereinfachteZeitplanung.tex
│           └── VereinfachteZeitplanung.tex

├── 03_Settings/                    ## Einstellungen und vordefinierte Befehle
│   ├── 01_Default/                  ## Standard-Einstellungen (für alle Projekte geeignet)
│   │   ├── 01_Packages.tex
│   │   ├── 02_Befehle.tex           ## Projektübergreifende Befehle (z. B. für Abbildungen, Tabellen)
│   │   ├── 03_Seitenstil.tex        ## Seitenränder, Kopf-/Fußzeilen, Einrückungen
│   │   └── 04_Colors.tex            ## Standard-Farben für Links, Tabellen usw.
│   └── 02_Projektspezifisch/        ## Anpassungen für das jeweilige Projekt
│       ├── 01_ProjektspezifischePackages.tex
│       ├── 02_ProjektspezifischeBefehle.tex
│       └── 03_ProjektspezifischeColors.tex

├── 04_Literaturverzeichnis/        ## Literaturdatenbank im BibTeX-Format
│   └── Literaturverzeichnis.bib     ## Empfehlung: mit Citavi oder Zotero erstellen/exportieren

├── 05_Anhang/                      ## Anhänge und ergänzende Inhalte (mit Beispielkapitel)
│   ├── 01_KapitelAnhang/
│   │   ├── 01_01_Unterkapitel_im_Anhang.tex
│   │   └── StrukturKapitelAnhang.tex
│   └── StrukturAnhang.tex

├── 06_Finale_Abgabe/               ## Formatvorgabe für finale Abgabedatei (wird nicht automatisch generiert)
│   └── Filename_Abgabe.txt

├── .gitignore                      ## Git-Konfiguration zur Ausblendung temporärer Dateien

├── Main.pdf                        ## Generierte PDF-Version der Arbeit (nach dem Kompilieren)

└── Main.tex                        ## Einstiegspunkt zur Kompilierung des gesamten Dokuments
