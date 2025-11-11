<!--
author:   André Dietrich; Sebastian Zug

email:    Andre.Dietrich@informatik.tu-freiberg.de;
          Sebastian.Zug@informatik.tu-freiberg.de

language: de

narrator: German Male

version:  0.0.1

comment:  Kurzvorstellung LiaScript im Vergleich zu Authoring-Tool in klassischen LMS

mode:     Slides

import:   https://raw.githubusercontent.com/liaTemplates/ABCjs/main/README.md

@style
@keyframes burn {
  0% { text-shadow: 0 0 5px #ff0, 0 0 10px #ff0, 0 0 15px #f00, 0 0 20px #f00, 0 0 25px #f00, 0 0 30px #f00, 0 0 35px #f00;
  }
  50% { text-shadow: 0 0 10px #ff0, 0 0 15px #ff0, 0 0 20px #ff0, 0 0 25px #f00, 0 0 30px #f00, 0 0 35px #f00, 0 0 40px #f00;
  }
  100% { text-shadow: 0 0 5px #ff0, 0 0 10px #ff0, 0 0 15px #f00, 0 0 20px #f00, 0 0 25px #f00, 0 0 30px #f00, 0 0 35px #f00;
  }
}
.burning-text {
  font-weight: bold;
  color: #fff;
  animation: burn 1.5s infinite alternate;
}
@end

@burn: <span class="burning-text">@0</span>
-->

# LiaScript – Offene OER im Browser

> *„LMS verwalten Bildung – LiaScript teilt sie.“*

## 🟩 1. Einführung: Warum LMS bei OER an ihre Grenzen stoßen

    --{{0}}--
Lernmanagementsysteme wie Moodle, ILIAS oder Canvas sind perfekt, um Kurse zu **verwalten**,  
aber sie sind **nicht ideal, um offene Lerninhalte zu erstellen**.

__Typische Probleme:__

- Inhalte werden in Datenbanken gespeichert → nicht offen
- Kein einfacher Export oder Wiederverwendung
- Hohe Einstiegshürden für Autor:innen
- Abhängigkeit von Plugins und Systemversionen

     {{1}}
> **These:** OER braucht eine eigene Sprache, offen, textbasiert und versionsfähig.

## 🟦 2. LiaScript – Eine neue Denkrichtung

    --{{0}}--
LiaScript ist eine **erweiterte Markdown-Sprache** zur Erstellung interaktiver Lerninhalte.

- 100 % im Browser – kein Server, keine Installation
- Inhalte bleiben **Markdown-Dateien**
- Läuft **offline**
- Unterstützt **Text-to-Speech, Quiz, Code, Animationen, Multimedia**

      {{1}}
> Kurz gesagt: *Markdown wird lebendig.*

## 🟥 3. Demo: Hello LiaScript 🎬

    --{{0}}--
Hallo, mein Name ist LiaScript. Ich bin eine auf Markdown basierende Sprache, die speziell zur Erstellung von Lernmaterialien entwickelt wurde.
Der Vorteil von Markdown ist, dass es bereits weit verbreitet, leicht zu schreiben und zu lesen ist und von vielen Plattformen unterstützt wird.
Der größte Nachteil ist jedoch, dass es @burn(statisch wie die Hölle) ist und keinerlei Interaktivität bietet.

    --{{1}}--
Also machten sich meine Entwickler daran, Markdown von Grund auf neu zu überdenken …

     {{1-2}}
> <marquee>... Once you free your mind about a concept of Harmony and of music being "correct" you can do whatever you want ...</marquee>
>
> -- Giorgio Moroder (Erfinder der Disco-Musik)

    --{{2}}--
Eigentlich sind Tabellen in Markdown leicht zu erstellen und, wie bereits erwähnt, ziemlich @burn(statisch).
Eine Tabelle kann jedoch auch einen Datensatz darstellen, der nach seiner idealen Visualisierung strebt.

      {{2}}
| Tier              | Gewicht in kg | Lebensdauer (Jahre) | Mitogen |
| ----------------- | ------------: | ------------------: | ------: |
| Maus              |         0.028 |                  02 |      95 |
| Flughörnchen      |         0.085 |                  15 |      50 |
| Braune Fledermaus |         0.020 |                  30 |      10 |
| Schaf             |            90 |                  12 |      95 |
| Mensch            |            68 |                  70 |      10 |


    --{{3}}--
Eine andere tabellarische Struktur kann eine völlig andere Visualisierung erzeugen, die vom Autor fein abgestimmt werden kann.
Insgesamt unterstütze ich 10 verschiedene Arten von Visualisierungen.


      {{3}}
<!--
data-type="heatmap"
data-title="Seattle Average Temperature in Fahrenheit"
data-show
-->
| Seattle |  Jan |  Feb |  Mar |  Apr |  May |  Jun |  Jul |  Aug |  Sep |  Oct |  Nov |  Dec |
| -------:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| ----:| ----:|
|       0 | 40.7 | 41.5 | 43.6 | 46.6 | 51.4 | 56.0 | 60.5 | 61.2 | 57.0 | 50.1 | 44.1 | 39.6 |
|       2 | 40.2 | 40.7 | 42.7 | 45.3 | 50.0 | 54.4 | 58.5 | 59.2 | 55.4 | 49.2 | 43.5 | 39.3 |
|       4 | 39.7 | 40.0 | 41.9 | 44.4 | 48.9 | 53.2 | 57.0 | 57.7 | 54.2 | 48.6 | 43.1 | 38.9 |
|       6 | 39.6 | 39.5 | 41.3 | 44.2 | 49.5 | 54.2 | 57.8 | 57.4 | 53.6 | 48.2 | 42.8 | 38.7 |
|       8 | 39.6 | 39.9 | 42.9 | 47.1 | 52.7 | 57.3 | 61.3 | 61.1 | 56.7 | 49.5 | 43.1 | 38.7 |
|      10 | 41.3 | 42.7 | 46.4 | 50.7 | 56.4 | 60.9 | 65.2 | 65.4 | 60.9 | 52.8 | 45.5 | 40.4 |
|      12 | 43.8 | 46.0 | 49.5 | 53.8 | 59.6 | 64.3 | 69.4 | 69.8 | 65.1 | 56.0 | 47.8 | 42.6 |
|      14 | 45.1 | 47.7 | 51.3 | 55.9 | 61.9 | 66.9 | 72.6 | 73.2 | 67.7 | 57.8 | 48.8 | 43.6 |
|      16 | 44.5 | 47.5 | 51.4 | 55.9 | 62.3 | 67.5 | 73.9 | 74.3 | 68.2 | 57.4 | 47.8 | 42.6 |
|      18 | 42.6 | 44.7 | 48.7 | 53.8 | 60.3 | 65.9 | 72.3 | 72.2 | 64.6 | 53.9 | 46.0 | 41.2 |
|      20 | 42.0 | 43.3 | 46.4 | 50.2 | 56.0 | 61.4 | 66.9 | 66.6 | 60.7 | 52.3 | 45.2 | 40.7 |
|      22 | 41.4 | 42.5 | 45.0 | 48.3 | 53.5 | 58.2 | 63.2 | 63.5 | 58.7 | 51.1 | 44.5 | 40.1 |

    --{{4}}--
Was Markdown schon immer gefehlt hat, war die Einbettung von multimedialen Inhalten …


    --{{5}}--
Ich unterstütze Audioinhalte …

      {{5}}
?[ein Pferd](https://www.w3schools.com/html/horse.mp3 "ein Pferd hören")

    --{{6}}--
Ich kann auch mit Videos umgehen – und natürlich funktioniere ich sogar auf Feature-Phones, selbst wenn sie offline sind.

      {{6}}
!?[LiaScript auf Nokia](https://www.youtube.com/watch?v=U_UW69w0uHE)

    --{{7}}--
Ich kann außerdem versuchen, andere Arten von Inhalten einzubetten, die weder in die eine noch in die andere Kategorie fallen.

      {{7}}
??[Esthers Schriftrolle in einer Hülle](https://sketchfab.com/3d-models/esthers-scroll-in-a-cover-21a13eba33cb4343bab56f0c0f982876 "Historisches Museum der Stadt Krakau")

    --{{8}}--
Programmieren muss nicht langweilig sein – wie wäre es mit etwas Musik als Code?

      {{8}}
```abc
X: 1
M: 4/4
L: 1/8
K: Emin
|:D2|"Em"EBBA B2 EB|~B2 AB dBAG|"D"FDAD BDAD|FDAD dAFD|
"Em"EBBA B2 EB|B2 AB defg|"D"afe^c dBAF|"Em"DEFD E2:|
```
@ABCJS.eval

    --{{9}}--
Du hast vielleicht bemerkt, dass dieses Dokument wie eine PowerPoint-Präsentation verwendet wird.
Unsere Absicht war es jedoch, LiaScript in verschiedenen Kontexten nutzbar zu machen.
Mit LiaScript kannst du Präsentationen erstellen, Selbstlernkurse mit browserbasierter Sprachausgabe anbieten oder den Inhalt einfach als interaktives Lehrbuch lesen – ganz ohne Animationen.

      {{9}}
> ## Quiz?
>
> **Wirst du LiaScript in Zukunft verwenden?**
>
> - [(X)] Ja, natürlich
> - [( )] Nicht sicher …
> - [( )] Nein, ich bleibe lieber bei einem klassischen LMS

## 🟪 4. Der Browser ist das neue Betriebssystem 🌐

    --{{0}}--
Moderne Browser können heute nahezu alles, was früher Server oder native Apps erledigten.

| Fähigkeit                                                                        | Beschreibung                      | Beispiel                        |
| -------------------------------------------------------------------------------- | --------------------------------- | ------------------------------- |
| [IndexedDB](https://de.wikipedia.org/wiki/Indexed_Database_API)                  | Lokale Datenbank                  | Speichern von Lernfortschritt   |
| [WebRTC](https://de.wikipedia.org/wiki/WebRTC)                                   | Realtime-Kommunikation            | Kollaboration, Chat             |
| [Sensor APIs](https://developer.mozilla.org/en-US/docs/Web/API/Sensor)           | Zugriff auf Kamera, GPS, Mikrofon | Experimente, Standort           |
| [WebAudio / TTS](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) | Text-to-Speech                    | Barrierefreie (narrative) Kurse |
| [JavaScript](https://de.wikipedia.org/wiki/JavaScript)                           | Interaktive Logik                 | Simulationen, Code-Übungen      |

    --{{1}}--
Der Browser wird zur **Lernplattform**, LiaScript ist seine Sprache.


## 🟫 5. Kollaboration & KI-Co-Creation 🤝🤖

    --{{0}}--
Kollaboration funktioniert über **Git** und offene Editoren:

- [LiaScript LiveEditor](https://liascript.github.io/LiveEditor)
- [HedgeDoc / CodiMD](https://hedgedoc.org/)
- GitHub / GitLab Repositories

    --{{1}}--
Zusätzlich können **KI-Systeme** wie ChatGPT, Copilot oder Claude  
direkt mitarbeiten – ohne Plugins!

    --{{2}}--
KI versteht Markdown, generiert Quizfragen, Texte, Übersetzungen oder Makros.

Was macht LiaScript besonders?

- [[X]] Läuft im Browser ohne Server
- [[X]] Inhalte bleiben als Markdown offen
- [[ ]] Benötigt proprietäre Plugins

## 🟨 6. Vergleich: LMS vs. LiaScript ⚖️

| Aspekt          | Klassisches LMS    | LiaScript                          |
| :-------------- | :----------------- | :--------------------------------- |
| Erfassung       | Formulare, Plugins | Markdown /Text                     |
| Kollaboration   | Intern, beschränkt | Git + kollaborative Editoren       |
| Standards       | SCORM, IMS         | SCORM, IMS, PDF, Web               |
| Export          | oft proprietär     | SCORM / IMS / Standalone           |
| Erweiterbarkeit | Plugins            | Makros & JavaScript & Bibliotheken |
| Kompatibilität  | versionsabhängig   | Markdown = zukunftssicher          |

    --{{1}}--
LiaScript **ersetzt kein LMS**, es **befreit** es.

## 🟧 7. Rolle des LMS – Ergänzung statt Konkurrenz 🧩

    --{{0}}--
Das LMS bleibt wichtig für:

- Nutzerverwaltung
- Tracking (SCORM / xAPI)
- Reporting & Zertifizierung

    --{{1}}--
LiaScript ergänzt:

- Offene Kurserstellung
- Dezentrale Veröffentlichung
- Browserbasiertes Lernen

    --{{2}}--
Gemeinsam können sie ein offenes und nachhaltiges Ökosystem bilden.
Das Hauptproblem heutiger LMS ist, dass sie mit sehr hoher Wahrscheinlichkeit irgendwann nicht mehr gepflegt/geupdated und abgeschaltet werden.
In diesem Fall sind alle darin enthaltenen Kurse verloren.

![Adresse nicht gefunden](media/adresse-nicht-gefunden.png "Report: E-Learning: Eine Zwischenbilanz Kritischer Rückblick als Basis eines Aufbruchs -- 2009 -> [Download](https://www.pedocs.de/volltexte/2011/3215/pdf/Haug_Wedekind_Adresse_nicht_gefunden_D_A.pdf)")<!-- style="border: 1px solid black" -->


## 🟦 8. OER-Ökosystem & Veröffentlichung 🌍

    --{{0}}--
Kurse können direkt veröffentlicht werden über:

* GitHub / GitLab
* Nextcloud
* Öffentliche Repositorien

    --{{1}}--
Exportformate:

* **SCORM 1.2 / 2004**
* **IMS CP**
* **PDF**
* **Standalone WebApp**

> OER bleiben damit **nachnutzbar, remixbar und zukunftssicher**.

## 🟩 9. Fazit 🌱


* LiaScript = offenes, browserbasiertes Authoring-Tool
* Keine Plugins, keine Server, keine Lock-ins
* Vollständig offen und standardkompatibel

    --{{1}}--
"Der Browser ist das neue Betriebssystem – LiaScript ist seine Sprache für Bildung."


## 🧾 Mehr Informationen

* 🌐 Website: [https://LiaScript.github.io](https://LiaScript.github.io)
* 📘 Dokumentation: [LiaScript Docs](https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/docs/master/README.md)
* 🧰 LiveEditor: [https://liascript.github.io/LiveEditor](https://liascript.github.io/LiveEditor)
* 💡 Beispiele: [https://github.com/topics/liascript-course](https://github.com/topics/liascript-course)
