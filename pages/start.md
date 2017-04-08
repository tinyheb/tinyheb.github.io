---
layout: page
title: Was ist tinyHeb?
permalink: /
order: 1
---

## Was ist tinyHeb?

Mit der Abrechnungssoftware _tinyHeb_, die unter Linux und Windows läuft, können Hebammen ihre Abrechnung am Computer erstellen und am elektronischen [Datenaustausch](http://www.datenaustausch.de) mit den gesetzlichen Krankenkassen nach [§302 SGB V](http://www.sozialgesetzbuch-sgb.de/sgbv/302.html) teilnehmen. Die Hebammen-Vergütungsvereinbarung ist für _tinyHeb_ kein Problem.

Die Software _tinyHeb_ steht unter der [GNU General Pubic License](http://www.gnu.org/copyleft/gpl.html) und ist damit _kostenfrei_.

Fragen und Anregungen zu _tinyHeb_ können gerne in der [Mailingliste](https://lists.launchpad.net/tinouheb/) diskutiert werden. Eine Installations- und Gebrauchsanleitung ist im [Handbuch]({{ "/assets/tinyheb-handbuch.pdf" | relative_url }}) (PDF) enthalten. Bei Problemen werft einen Blick in das [_tinyHeb_ FAQ](/faq) (häufig gestellte Fragen).

## Welche "Features" sind im Programm enthalten?

*   Erfassung von Stammdaten zu den Kundinnen
*   Umfangreiche Plausiprüfungen bei der Erfassung von Rechnungsposten
*   Ermittlung des Wochentages und ggf. automatischer Wechsel der erfassten Positionsnummer bei Samstag, Sonntag oder Feiertag
*   automatische Anwahl von Materialpauschalen,
    *   z.B. Vorsorgeuntersuchung
    *   Wochenbett (vor/nach) 4\. Tag p.p. in Abhängigkeit des Geburtsdatum
*   Bearbeitung von Kassen- und Privatpatientinnen möglich
*   Generierung von Rechnungen nach §301a bzw. §302 SGB V per E-Mail
*   Korrekte Ermittlung der Rechnungsanschrift bei Papierrechnungen auf Basis der Kostenträgerdateien
*   Korrekte Ermittlung der Datennahmestelle bei elektronischen Rechnungen auf Basis der Kostenträgerdateien
*   Beschreibung, wie man zum elektronischen Datenaustausch zugelassen wird
*   Einlesen der Kostenträgerdateien mit allen Krankenkassen (ca. 1900)
*   Einlesen der Schlüsseldateien der Datenannahmestellen
*   einfache Bedienung (sagt meine Frau und andere Hebammen)
*   Tool zur Generierung einer Zertifikatsanfrage an die ITSG
*   Hebammen-Vergütungsvereinbarung ab Version 0.15.0
*   Wer alles genau wissen möchte, kann dies im [Handbuch]({{ "/assets/tinyheb-handbuch.pdf" | relative_url }}) nachlesen.

## Was kostet die Software?

*   Die Software steht unter der GPL, d.h. es fallen keine Lizenzgebühren an.
*   Für die Verschlüsselung bei elektronischen Rechnungen wird [OpenSSL](http://www.openssl.org) genutzt, auch an dieser Stelle fallen keine Kosten an.
*   Es ist nicht nötig eine zusätzliche Software, wie z.B. Dakota zu installieren.
*   Es ist nicht nötig, Geld für die Zulassung zum Datenaustausch zu bezahlen.
*   Ein Zertifikat wird für die Rechnungsstellung per E-Mail benötigt.

## Welche Voraussetzungen müssen erfüllt sein?

*   Als Betriebssystem sollte Linux, Mac OS X oder Windows installiert sein.
*   Unter Linux müssen die Standardpakete der Distribution vorhanden sein.
*   Es werden [Apache](http://www.apache.org/), [MySQL](http://www.mysql.com/), [Perl](http://www.perl.com/), [OpenSSL](http://www.openssl.org/) und [Ghostscript](http://ghostscript.com/) benötigt.
