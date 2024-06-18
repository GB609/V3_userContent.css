# V3_userContent.css
Enthält userContent CSS Code für den Browser um die UI von VerbrannteZone 3 leicht zu verbessern. Rein clientseitig. Kann schon technisch gesehen keine Features ändern oder ergänzen.
Wer mir Rückmeldung dazu geben will, Wünsche oder Vorschläge hat, kann dies entweder ingame oder auf github als issue machen (falls ein Account besteht).

# Installation
Bevor der eigentliche Code verwendet werden kann, muss der verwendete Browser vorbereitet werden. Da ich nur den Firefox verwende, werde ich die nötigen Schritte nur für diesen beschreiben. Es gibt aber sicher für andere Browser ähnliche Möglichkeiten, die sich mittels einer kurzen Suche schnell finden lassen.

## Als userContent.css - nur Desktop PC
Man kann den Firefox so einrichten, dass zusätzliche Style-Informationen für Webseiten in einer speziellen Datei auf dem Rechner ausgelesen werden, der sogenannten "userContent.css". Damit das funktioniert, sind bei neueren Firefox Versionen folgende Schritte nötig.
1. In einem neuen Firefox Fenster oder Tab "about:config" in der Adresszeile eingeben und dann öffnen
2. Die Einstellung mit dem Namen "toolkit.legacyUserProfileCustomizations.stylesheets" suchen/anlegen als boolean mit dem Wert "true"
3. Die Eisntellung mit dem Namen "layout.css.moz-document.content.enabled" suchen/anlegen als boolean mit dem Wert "true"
4. Dann die Adresse "about:profiles" besuchen und bei "Wurzelordner" auf "Ordner öffnen" klicken. Es öffnet sich ein Fenster im Dateimanager.
5. In dem neuen Fenster den Unterordner "chrome" anlegen (falls nicht da) und dann öffnen.
6. Die [userContent.css](./userContent.css?raw=1) herunterladen.
7. Die heruntergeladene Datei in den zuvor geöffneten Unterorder "chrome" verschieben oder kopieren.
8. Firefox neu starten. Wenn alles geklappt hat, sind alle Änderungen jetzt direkt beim Einloggen in VZ3 da.
9. Bei weiteren Anpassungen wird die Datei "userContent.css" direkt mit einem einfachen Texteditor bearbeitet und gespeichert. Jetzt genügt es auch, alle Tabs mit VZ3 zu schließen und neu zu öffnen um die Änderungen zu übernehmen.

## Mit Browser Addon - auch für Smartphone Browser
Ich habe mit [Stylus](https://addons.mozilla.org/de/firefox/addon/styl-us/) auf Firefox Android getestet. Wer lieber Chrome benutzt muss nach etwas ähnlichem dort suchen. Die folgende Anleitung stützt sich aber auf das was ich selbst gemacht habe.

Zuerst muss das Addon Stylus in Firefox installiert werden. Entweder über den Link im Absatz über diesem. Oder aber über eine entsprechende Suche bei einer Suchmaschine eigener Wahl, solange das Ergebnis dann auf die Webseite addons.mozilla.org verweist. Bitte stellt sicher, dass ihr auf keiner anderen Seite landet und damit fakes installieren würdet.

Dann gibt es 2 Möglichkeiten, den eigentlichen Code zu installieren:
1. Klickt auf den folgenden Link und erlaubt Stylus die Installation: [v3-style.user.css](./v3-style.user.css?raw=1). Die Datei heißt anders, enthält aber den gleichen Text. Der Name dient nur dazu, dass sie von Stylus erkannt wird.
2. Danach kann sie bei Bedarf lokal bearbeitet werden. Empfehlenswert bei eigener Bearbeitung ist es, die automatische Suche nach skript updates im plugin auszuschalten. Ansonsten könnte eine neue Version von mir alle lokalen Änderungen überschreiben.
   
ODER:
1. Die [userContent.css](./userContent.css?raw=1) herunterladen und auf dem Smartphone mit einem Textbetrachter öffnen.
2. Alles markieren und kopieren.
3. V3 im Browser öffnen
4. Das Addon im Firefox Menü bei "..." -> Addons -> Stylus auswählen
5. Stelle sicher, dass in dem folgenden Fenster kein Häkchen gesetzt ist
6. Klicke dann auf die ausgegraute Zeile mit dem kleinen "user css" symbol.
7. Dann oben auf "Importieren"
8. Es öffnet sich ein Textfeld mit der Überschrift "Mozilla-Format Code einfügen". Hier dann den kopierten Text einfügen.
9. Zum Schluss unten auf "Style überschreiben" tippen.

# Details
Screenshots und Erklärungen was genau wie geändert wird, befinden sich in den folgenden Unterkapiteln. 

Wer die Änderungen verfeinern oder nur Teile davon haben will, kann die anderen Sachen auskommentieren oder ganz entfernen. Die userContent.css ist vollständig kommentiert und beschrieben.

## Navigationsmenü links generell
Alle klickbaren Links werden zu größeren Schaltflächen umgewandelt und erhalten einen Rahmen. Das erleichtert die Bedienung auf Smartphones. Wahrscheinlich sogar mit der Maus, weil weniger genau gezielt werden muss.
Seite | vorher | nachher |
|---|---|---|
Optionen|bild|bild|
Statistiken|bild|bild|

## Zusätzlich im Provinzmenü
Die eingerahmten "Schnelllinks" zu den wichtigsten Funktionen, die aus je einem Buchstaben bestehen, werden in - hoffentlich selbsterklärende - Symbole umgewandelt und dadurch auch vergrößert. Diese tauchen dann sogar auf der Weltkarte bei einem Klick auf eine eigene Provinz auf.
Seite | vorher | nachher |
|---|---|---|
Navigation|bild|![Ergänzung Provinzmenü](!images/provinzmenu.png)|
Weltkarte|bild|![Effekt Weltkarte](!images/weltkarte.png)|

## Links im Hauptfenster
Auf nahezu allen Unterseiten von VZ findet sich eine Vielzahl an einfachen Links, meistens mehrere eng beeinander in Tabellen. Das macht eine treffsichere Bedienung auf Touchpads bzw. mit den Fingern sehr schwierig. 

Das "userContent.css" wandelt die Links an sehr vielen Stellen, wo es wirklich relevant ist, in "quasi"-Schaltflächen mit einem vergrößerten Klickbereich um. Hier allerdings ohne zusätzliche Rahmen, weil diese aufgrund ihrer schieren Zahl eher störend als hilfreich wären. Diese Vergrößerung hat jedoch etwas höhere Textzeilen zur Folge, es muss also mehr gescrollt werden. An einigen Stellen sind die Links theoretisch kaum sinnvoll, ich könnte technisch gesehen jedoch nur mit sehr großem Aufwand Ausnahmen erzwingen.
Seite | vorher | nachher | Kommentar
|---|---|---|---|
Gebäudeinfo|bild|bild|
Routenübersicht|bild|bild|
Gebäudedetail|bild|bild| Hier ist der Nachteil in der Terrainliste bei Effizienz klar sichtbar

## In Arbeit: Routenübersicht
Ich suche derzeit passende Symbole für die Aktionen usw. in der Routenübersicht.

## Klassische Provinzansicht (Tabelle zum Bauen)
Hier wird für die Gebäudefelder etwas ähnliches gemacht wie für die Menüs und anderen Ansichten: Der Klickbereich wird auf das ganze Kästchen ausgeweitet. 

Straßen und Kreuzungen sind davon aber ausgenommen. Es würde keinen Sinn machen, den Klickbereich hier zu vergrößern, weil die Felder selbst sehr klein sind und dann ebenfalls mit vergrößert werden müssten.

## Warentransfer in Handelsrouten
Das kleine '+' in jeder Zeile wird zu einer etwas größeren Schaltfläche für einfacheres Treffen erweitert.
