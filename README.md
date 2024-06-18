# V3_userContent.css
Enthält userContent CSS Code für den Browser um die UI von VerbrannteZone 3 leicht zu verbessern. Rein clientseitig. Kann schon technisch gesehen keine Features ändern oder ergänzen.

# Installation
Bevor der eigentliche Code verwendet werden kann, muss der verwendete Browser vorbereitet werden. Da ich nur den Firefox verwende, werde ich die nötigen Schritte nur für diesen beschreiben. Es gibt aber sicher für andere Browser ähnliche Möglichkeiten, die sich mittels einer kurzen Suche schnell finden lassen.

## Als userContent.css - nur Desktop PC
Man kann den Firefox so einrichten, dass zusätzliche Style-Informationen für Webseiten in einer speziellen Datei auf dem Rechner ausgelesen werden, der sogenannten "userContent.css". Damit das funktioniert, sind bei neueren Firefox Versionen folgende Schritte nötig.
1. In einem neuen Firefox Fenster oder Tab "about:config" in der Adresszeile eingeben und dann öffnen
2. Die Einstellung mit dem Namen "toolkit.legacyUserProfileCustomizations.stylesheets" suchen/anlegen als boolean mit dem Wert "true"
3. Dann die Adresse "about:profiles" besuchen und bei "Wurzelordner" auf "Ordner öffnen" klicken. Es öffnet sich ein Fenster im Dateimanager.
4. In dem neuen Fenster den Unterordner "chrome" anlegen (falls nicht da) und dann öffnen.
5. Die [userContent.css](./userContent.css) herunterladen.
6. Die heruntergeladene Datei in den zuvor geöffneten Unterorder "chrome" verschieben oder kopieren.
7. Firefox neu starten. Wenn alles geklappt hat, sind alle Änderungen jetzt direkt beim Einloggen in VZ3 da.
8. Bei weiteren Anpassungen wird die Datei "userContent.css" direkt mit einem einfachen Texteditor bearbeitet und gespeichert. Jetzt genügt es auch, alle Tabs mit VZ3 zu schließen und neu zu öffnen um die Änderungen zu übernehmen.

## Mit Browser Addon - auch für Smartphone Browser
Ich habe mit [Stylus](https://addons.mozilla.org/de/firefox/addon/styl-us/) auf Firefox Android getestet. Wer lieber Chrome benutzt muss nach etwas ähnlichem dort suchen. Die folgende Anleitung stützt sich aber auf das was ich selbst gemacht habe.
1. Mit Firefox auf Android das Stylus Addon installieren. Entweder über den Link direkt hier im Vorwort des aktuellen Kapitels. Oder aber über eine entsprechende Suche bei einer Suchmaschine eigener Wahl, solange das Ergebnis dann auf die Webseite addons.mozilla.org verweist. Bitte stellt sicher, dass ihr auf keiner anderen Seite landet.

# Details
Screenshots und Erklärungen was genau wie geändert wird, befinden sich in den folgenden Unterkapiteln. 

Wer die Änderungen verfeinern oder nur Teile davon haben will, kann die anderen Sachen auskommentieren oder ganz entfernen. Die userContent.css ist vollständig kommentiert und beschrieben.

## Navigationsmenü links generell
Alle klickbaren Links werden zu größeren Schaltflächen umgewandelt und erhalten einen Rahmen. Das erleichtert die Bedienung auf Smartphones. Wahrscheinlich sogar mit der Maus, weil weniger genau gezielt werden muss.

## Links im Hauptfenster
Auf nahezu allen Unterseiten von VZ findet sich eine Vielzahl an einfachen Links, meistens mehrere eng beeinander in Tabellen. Das macht eine treffsichere Bedienung mit Touchpads sehr schwierig. 

Das "userContent.css" wandelt die Links an sehr vielen Stellen, wo es wirklich relevant ist, in "quasi"-Schaltflächen mit einem vergrößerten Klickbereich um. Hier allerdings ohne zusätzliche Rahmen, weil diese aufgrund ihrer schieren Zahl eher störend als hilfreich wären. Diese Vergrößerung hat jedoch etwas höhere Textzeilen zur Folge, es muss also mehr gescrollt werden.

## Zusätzlich im Provinzmenü
Die eingerahmten "Schnelllinks" zu den wichtigsten Funktionen, die aus je einem Buchstaben bestehen, werden in - hoffentlich selbsterklärende - Symbole umgewandelt und dadurch auch vergrößert. Diese tauchen dann sogar auf der Weltkarte bei einem Klick auf eine eigene Provinz auf.

## Klassische Provinzansicht (Tabelle zum Bauen)
Hier wird für die Gebäudefelder etwas ähnliches gemacht wie für die Menüs und anderen Ansichten: Der Klickbereich wird auf das ganze Kästchen ausgeweitet. 

Straßen und Kreuzungen sind davon aber ausgenommen. Es würde keinen Sinn machen, den Klickbereich hier zu vergrößern, weil die Felder selbst sehr klein sind und dann ebenfalls mit vergrößert werden müssten.
