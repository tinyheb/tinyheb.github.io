---
layout: page
title: Häufige Fragen
permalink: /faq
order: 2
---

## Häufig gestellte Fragen (F.A.Q.)

Das FAQ befindet sich im Aufbau, Hilfe dabei wird gerne entgegen genommen.

### Ich habe Probleme bei der Installation von _tinyHeb_ was soll ich tun?

Zunächst bitte einen Blick in dieses FAQ werfen, ob schon ein anderer Nutzer ein ähnliches Problem gemeldet hat. Hilft das nicht weiter schickt der Mailingliste eine E-Mail in der Ihr das Problem genau beschreibt. Wichtige Angaben sind u.a.:  

*   welches Betriebssystem wird genutzt
*   welche _tinyHeb_ Version benutzt ihr
*   Schickt zusätzlich bitte das Error-Log des Webservers, da finden sich wichtige Hinweise, was nicht funktioniert. Das Error Log findet sich auf Win* Systemen im Verzeichnis "C:\Programme\Apache Group\Apache2\logs" und heisst error.log

### Bei Funktion xy passiert in _tinyHeb_ nicht das was ich erwarte, was soll ich tun?

Zunächst bitte einen Blick in das _tinyHeb_ Handbuch werfen, was die Funktion wirklich machen soll. Hilft das nicht weiter, bitte eine Mail an die Mailingliste mit der Beschreibung was ihr machen möchtet. Ggf. haben andere ähnliche Anforderungen. Bitte schreibt in jedem Fall, welche _tinyHeb_ Version und welches Betriebssystem ihr benutzt.

### Klickt man in der Rechnungsbearbeitung auf Mahnung generieren, gelangt man in das Vorschaufenster. Sieht man sich diese Vorschau an, wird der Status der Mahnung (1\. Mahnung) korrekt angezeigt. Beim anschließenden Klick auf Mahnung fertigstellen wird jedoch gleich 2\. Mahnung geschrieben und so steht es anschließend auch im Status der Rechnungsbearbeitung.

Du benutzt vermutlich den Internet-Explorer als Browser. Der Fehler liegt im Internet-Explorer und tritt nur bei bestimmten Versionen des Browsers auf (welche???). Mit Firefox als Browser tritt das Problem nicht auf.

### Beim Rechnungen generieren habe ich leider festgestellt, dass sobald ich auf fertig stellen klicke erscheint eine Rechnung mit 0 EUR Betrag. In der Liste der versandten Rechnungen sehe ich dann, das zwei Rechnungen erstellt wurden, eine mit dem korrekten Betrag und sofort danach eine mit 0 EUR mangels Rechnungsposten,?.logisch. Ich bin nun so vorgegangen, dass ich die fehlerhaften Rechnungen storniert habe, is? aber nur ?ne Übergangslösung, denke ich, weil leider ja auch jedes Mal eine Rechnungsnummer vergeben wird.

Du benutzt vermutlich den Internet-Explorer als Browser. Der Fehler liegt im Internet-Explorer und tritt nur bei bestimmten Versionen des Browsers auf (welche???). Mit Firefox als Browser tritt das Problem nicht auf.

### Seit dem Jahreswechsel bekomme ich beim Versenden der elektronischen Rechnungen folgende Fehlermeldung:

<code>
Nutzdaten konnten nicht verschlüsselt werden, öffentlicher Schlüssel der Datenannahmestelle abgelaufen oder Zertifikat abgelaufen.  
Bitte OpenSSL Installation prüfen  
versenden wird abgebrochen.
</code>

Das Problem ist, dass die Zertifikate der Datenannahmestellen alle drei Jahre erneuert werden müssen. Dies war per 31.12.2008 der Fall. Du musst wie im Handbuch im Kapitel A.2.2 "Verarbeitung der öffentlichen Schlüssel der Datenannahmestellen" die aktuelle Schlüsseldatei einspielen, danach tritt das Problem nicht mehr auf.

Für die AOK Rheinland muss z.B.folgendes Ergebnis angezeigt werden:

<table border="1" style="empty-cells: show">

<tbody>

<tr>

<th>Feld</th>

<th>Wert</th>

</tr>

<tr>

<td>Seriennummer</td>

<td style="vertical-align:top">7301</td>

</tr>

<tr>

<td>Organisation</td>

<td style="vertical-align:top">AOK RHEINLAND</td>

</tr>

<tr>

<td>Ansprechpartner</td>

<td style="vertical-align:top">Hr. Thomas Schroeder</td>

</tr>

<tr>

<td>Gültig von</td>

<td>Sep 30 00:00:00 2008 GMT</td>

</tr>

<tr>

<td>Gültig bis</td>

<td>Dec 31 23:59:59 2011 GMT</td>

</tr>

<tr>

<td>Herausgeber</td>

<td>ITSG TrustCenter fuer sonstige Leistungserbringer</td>

</tr>

<tr>

<td>Länge des Schlüssels</td>

<td>2048 bit</td>

</tr>

<tr>

<td>Algorithmus des Schlüssels</td>

</tr>

<tr>

<td>Status Datenaustausch</td>

<td>Echtbetrieb/Erprobungsphase/Testphase</td>

</tr>

</tbody>

</table>

### Ich versuche derzeit tinyheb auf Windows XP zu installieren und bin nach der Installationsanleitung vorgegangen. Dies hat auch soweit funktioniert, aber nach Ausführung des setup.pl Scriptes wird MySQL nicht mehr gestartet. Inklusive Reboot und `mysql -u root < init.sql` und Versuchen den MySQL Service zu starten schlagen fehl. Die Fehlermeldung lautet: *Fehler 1067: Der Prozess wurde unerwartet beendet*

Wechsel ins Verzeichnis `c:\Programme\MySQL\MySQL Server 5.0\data`

Da findest Du eine Datei die auf .err endet. Sieh Dir den Inhalt mal an, steht da am Ende etwas wie:

    InnoDB: Error: log file .\ib_logfile0 is of different size ....  
    InnoDB: than specified in the .cnf file

Wenn dem so ist lösche `ib_logfile0` und `ib_logfile1`. Danach entweder Reboot oder Server neu starten, dies sollte jetzt gehen. Dann funktioniert `mysql -u root < init.sql`.

### Hat schon jemand per E-Mail Rechnungen an Inter-Forum verschickt ?

Inter-Forum besitzt seit dem 01.06.2007 einen gültigen PKCS#7 Schlüssel. Rechnungen müssen verschlüsselt und signiert sein.  
_tinyHeb_ muss Version >= 0.13.1 sein

### Abrechnung mit der AOK Niedersachsen über Inter-Forum

Inter-Forum besitzt seit dem 01.06.2007 einen gültigen PKCS#7 Schlüssel. Rechnungen müssen verschlüsselt und signiert sein.  
_tinyHeb_ muss Version >= 0.13.1 sein

Sollte bei Euch das AOK RZ Niedersachsen-Bremen als Datenannahmestelle für die AOK Niedersachsen angegeben sein, handelt es sich um ein Fehlverhalten von _tinyHeb_. Es gibt einen Bug Fix zu diesem Fehler, der in Beitrag 140 der [Mailingliste](https://lists.launchpad.net/tinouheb/) beschrieben ist. ist oder  
_tinyHeb_ muss Version >= 0.13.2 sein

### bei einer privatrechnung kann man bei uns in bayern den 1,8 fachen satz in rechnung stellen;wie ändert man die beträge, wenn ich bei den stammdaten "privat" angebe, ändert sich beim E-Preis nichts

Bei Anzeige des E-Preises wird immer die HebGV zu Grunde gelegt, d.h. erst wenn Du in die Maske Rechnungsgenerierung springst, siehst Du den korrekten Preis in der Rechnungsvorschau. Eine Änderung der Software, so dass direkt im E-Preis auch bei Privat Kunden der korrekte Preis angezeigt wird, ist etwas kompliziert. Ggf. kann ich den korrekten E.Preis in der Übersicht der erfassten Rechnungsposten anzeigen, aber auch diese Änderung werden ich erst vornehmen, wenn ich die neue Gebührenordnung programmiert habe.

### vom IKK Bundesverband erhielt ich die schriftliche Anmeldung zur Teilnahme am Datenaustausch; u.a. steht in dem Schreiben, dass ich bei der Datenlieferung das UNB-Segment mit "1" kennzeichnen soll; meine Frage, wo führe ich das durch?

Siehe dazu Kapitel 5.3.4 Datenannahmestellen im Handbuch, der Inhalt des Parameters IK, der in Tabelle 5.4 beschrieben ist, entspricht genau dem, was im UNB Segment übertragen wird.

### Hat schon jemand von Euch Erfahrungen mit der elektronischen Abrechnung der DAK?

Die DAK wickelt seit Mai 2007 über Inter-Forum ab. Inter-Forum besitzt seit dem 01.06.2007 einen gültigen PKCS#7 Schlüssel. Rechnungen müssen verschlüsselt und signiert sein.  
_tinyHeb_ muss Version >= 0.13.1 sein

### Seit dem 01.08.2007 gilt die Hebammen-Vergütungsvereinbarung (neue Hebammen-Gebührenordnung). Wirst Du die in _tinyHeb_ aufnehmen.

Die Programmierung ist fast fertig. Es fehlen noch Teile für den elektronischen Datenaustausch. Die kann ich erst programmieren, wenn die Spezifikation der Spitzenverbände vorliegt. Alle Rechnungen ohne selbst definierte Materialien sind möglich.  
_tinyHeb_ muss Version >= 0.15.0 sein

### Ich habe mir erstmals versucht _tinyHeb_ zu installieren. Bin nach Installationsanleitung vorgegangen. Bekomme unter Windows folgende Fehlermeldung beim Ausführen der setup.pl : "ERROR 1396 (HY000) at line 3: Operation DROP USER failed for 'wwwrun'@'localhost'"

Hier scheine ich einen Fehler in die Initialisierung eingebaut zu haben :-( Der kann leicht korrigiert werden:  
Damit das setup bis zum Ende durchläuft, musst Du die Datei `init.sql` aus dem Verzeichnis `...\cgi-bin\tinyheb\DATA` zur Bearbeitung aufrufen, z.B. mit Notepad.  

Ganz am Anfang steht:  

    CREATE DATABASE IF NOT EXISTS PRD_Hebamme;  

    drop user 'wwwrun'@'localhost';  
    create user 'wwwrun'@'localhost';  

Das müsstest Du ändern in:  

    CREATE DATABASE IF NOT EXISTS PRD_Hebamme;  

    #drop user 'wwwrun'@'localhost';
    create user 'wwwrun'@'localhost';

Also die # (Raute) vor dem drop user... einfügen, danach nochmal setup.pl laufen lassen und es sollte funktionieren.
