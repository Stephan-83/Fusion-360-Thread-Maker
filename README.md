
Danke an HyperionConstruct
https://www.thingiverse.com/HyperionConstruct/designs


# Fusion-360-Thread-Maker
https://www.thingiverse.com/thing:4768407

Zu 3Dprinting
r/3Dprinting
•
vor 6 Jahren
HyperionConstruct
Fusion 360 Gewindebibliothek und Vorlage
Design

TLDR: Willst du einfach Gewinde in Fusion 360 erstellen? Kopiere meine XML-Gewindebibliothek von https://www.thingiverse.com/thing:4768407 in deinen Fusion 360 Installationsordner und erstelle 45°-Gewinde mit spezifischen Freigaben, indem du den integrierten Gewindebefehl verwendest.

Hintergrund

Ich habe schon ein paar Mal Gewinde gedruckt, um Teile zusammenzufügen, aber all die Beispiele im Internet sind entweder dazu da, das integrierte ISO-Metrik-Gewinde zu nutzen und die 3 Gewindeoberflächen so lange zu versetzen, bis es für dich funktioniert, ODER das Spulentool zu verwenden und die Form deines Gewindes auf einer senkrechten Ebene zu zeichnen und dann um deinen Zylinder zu formen. Beides dauert viel zu lange, um ein Gewinde zu produzieren, und ist nervig, wenn du deine Meinung ändern möchtest. Also habe ich eine Gewindebibliothek erstellt...

Details

Ich habe eine Gewindebibliothek für 45°-Gewinde mit 0,2 mm Freigabe erstellt, um das Drucken zu erleichtern. Ich habe hier angefangen: https://knowledge.autodesk.com/support/fusion-360/learn-explore/caas/sfdcarticles/sfdcarticles/Custom-Threads-in-Fusion-360.html

Und habe festgestellt, dass ich nichts über Gewinde weiß, obwohl ich oft mit ihnen arbeite. Also habe ich eine Tabelle erstellt, um die korrekten Durchmesser zu bestimmen, die Fusion360 zum Erstellen von Gewinden verwendet.

Es stellt sich heraus, dass es ziemlich einfach ist: Wähle den Gewindewinkel, den Steigdurchmesser für die Mitte des Gewindes und kürze ihn dann mit dem großen und kleinen Durchmesser. Bisher so gut. Als Nächstes habe ich die Steigung unter Verwendung der ISO-Metrik-Serie als Basis berechnet. Ich habe Trendlinien für 2 Teile der M-Serie angepasst, um zurückzuberechnen, was meine Steigung pro Schraubendurchmesser sein könnte, und mich auf Folgendes festgelegt: Durchmesser <17 = 12%D+0.25 und >17 = 7.85%D+1. Ich habe die Höhen um 1/10 verkürzt, damit die scharfen Teile nicht gedruckt werden.

Dann habe ich eine Freigabe hinzugefügt, damit ich Gewinde verschiedener Größen einfach drucken kann, ohne raten zu müssen, ob es mit den Toleranzen meines Druckers funktioniert.

Ich habe eine Tabelle erstellt, um jedes Gewinde zu berechnen, die du von https://www.thingiverse.com/thing:4768407 herunterladen kannst.

Du kannst die Tabelle verwenden, um deine eigenen Gewinde zu erstellen, die nicht in der XML-Datei enthalten sind. Vielleicht brauchst du ein 8,75 mm Durchmessergewinde oder vielleicht verwendest du einen ersten Generation RepRap und möchtest größere Freigaben. In der Tabelle gibt es Hinweise zur Anpassung der Werte und zum Kopieren/Einfugen in die XML-Datei. Beachte, dass XML-Dateien streng im Hinblick auf das Format sind, daher halte die Leerzeichen gleichmäßig.

Ich habe die Tabelle verwendet, um die XML-Datei zu erstellen. Ich habe kleine Durchmessergewinde in der Datei belassen, obwohl ich nicht empfehlen würde, diese mit FDM zu drucken. Vielleicht hat SLA mehr Glück. Ich habe 0,1 mm Freigabe für sie sowie 0,2 mm angegeben, damit du sehen kannst, wie mehrere Freigabeklassen in der XML strukturiert sind.

Es ist erwähnenswert, dass Benutzer ohne installierte XML-Datei die Gewinde nicht sehen können, also musst du die XML-Datei mit der Fusion360-Datei teilen.

# Installation

Lade die 3DPrintThreads.xml von Thingiverse herunter und kopiere sie nach:

Windows:

%localappdata%\Autodesk\webdeploy\Production\<version ID>\Fusion\Server\Fusion\Configuration\ThreadData

Mac OS:

Macintosh HD> Benutzer> [Benutzername] > Bibliothek > Anwendungsunterstützung > Autodesk > Webdeploy > Produktion > [Versionsspezifische ID] > Dann klicke mit der rechten Maustaste auf "Autodesk Fusion 360" und wähle "Paketinhalt zeigen" > Inhalt > Bibliotheken > Anwendungen > Fusion > Fusion > Server > Fusion > Configuration >ThreadData

Starte Fusion neu und verwende das Gewindewerkzeug wie gewohnt.

Ich würde mich freuen, etwas Feedback dazu zu bekommen.
