---
title: "Sicherheitseinrichtungen Fuer Registrierkassen Die Umsetzung Der Kassensichv Aus Technischer Sicht"
date: 2018-09-08T17:07:42+03:00
classId: grid-2
image: register.jpg
---

{{% htmlblock %}}

![](/images/register.jpg)

## Einleitung – die Kassensicherungsverordnung
Seit August 2018 unterstütze ich das Bundesamt für Sicherheit in der Informationstechnik (BSI) bei der Erstellung der Technischen Richtlinie, mit der die technischen Anforderungen umgesetzt werden, die sich aus der [KassenSichV](http://www.bundesrat.de/drs.html?id=487-17) ergeben.

Sofern die Regelungen zur Vertraulichkeit dies zulassen, werde ich auf diesem Blog über die technischen Entwicklung in diesem Bereich berichten.

Mit der KassenSichV hat der Gesetzgeber die Einführung einer technischen Sicherheitseinrichtung für Registrierkassen beschlossen.
Die KassenSichV definiert dabei bereits eine Reihe technischer Eigenschaften für die Technische Sicherheitseinrichtung:

* Die Technische Sicherheitseinrichtung verwendet ein Sicherheitsmodul
* Die Technische Sicherheitseinrichtung enthält ein Speichermedium, an das bestimmte Anforderungen gestellt werden
* die Technische Sicherheitseinrichtung muss eine einheitliche digitale Schnittstelle unterstützen, mit der die Daten – insbesondere zum Zwecke der Kassenschau – exportiert werden können
Durch die KassenSichV werden bereits grundlegende Anforderungen an die Funktionalität der Technischen Sicherheitseinrichtung definiert und es werden den einzelnen Komponenten Funktionen und Eigenschaften zugewiesen.

## Das Sicherheitsmodul
Die zentrale Funktionalität, die durch die KassenSichV für das Sicherheitsmodul festgelegt wird, ist die Vergabe von manipulationssicheren Transaktionsnummern. Durch diese Transaktionsnummern kann später nachgewiesen werden, dass die Aufzeichnungen der Technischen Sicherheitseinrichtungen lückenlos und vollständig sind.

Außerdem wird dem Sicherheitsmodul die Funktionalität der Bildung des Prüfwertes über die Transaktionsdaten zugeschrieben. Je nach technischer Ausprägung dürfte es sich dabei wohl um einen Hash-Wert oder eine kryptografische Signatur handeln.

{{% /htmlblock %}}

{{% htmlblock %}}

## Das Speichermedium
Die Anforderungen an das Speichermedium ergeben sich im Wesentlichen aus §3 der KassenSichV.

#### §3 Speicherung der Grundaufzeichnungen
1. Die Speicherung der laufenden Geschäftsvorfälle oder anderen Vorgänge im Sinne des § 146a Absatz 1 Satz 1 der Abgabenordnung muss vollständig, unverändert und manipulationssicher auf einem nichtflüchtigen Speichermedium erfolgen.
2. Die gespeicherten Geschäftsvorfälle oder andere Vorgänge im Sinne des § 146a Absatz 1, Satz 1 der Abgabenordnung müssen als Transaktionen so verkettet sein, dass Lücken in den Aufzeichnungen erkennbar sind.
3. Werden die gespeicherten digitalen Grundaufzeichnungen ganz oder teilweise von einem elektronischen Aufzeichnungssystem in ein externes elektronisches Aufbewahrungssystem übertragen, so muss sichergestellt werden, dass die Verkettung aller Transaktionen nach Absatz 2 und die Anforderungen an die einheitliche digitale Schnittstelle nach §4 erhalten bleiben.
4. Eine Verdichtung von Grundaufzeichnungen in einem elektronischen Aufzeichnungssystem ist für die Dauer der Aufbewahrung nach §147 Absatz 3 der Abgabenordnung unzulässig, wenn dadurch deren Lesbarkeit nicht mehr gewährleistet ist.

Interessanterweise wird in §3 der KassenSichV damit im Wesentlichen die Verwendung einer verketteten Liste als Datenformat für die Speicherung der Daten vorgegeben. Andere Vorgaben bezüglich der Performanz oder Langlebigkeit des Speichers sind als Teil der Technischen Richtlinie zu erwarten.

#### Die einheitliche digitale Schnittstelle
Die Anforderungen an die einheitliche digitale Schnittstelle werden in §4 der KassenSichV definiert.

**§4 Einheitliche digitale Schnittstelle**

*Die einheitliche digitale Schnittstelle ist eine Datensatzbeschreibung for den standardisierten Datenexport aus dem Speichermedium nach §3 Absatz 1 und dem elektronischen Aufbewahrungssystems zur Übergabe an den den mit der Kassen-Nachschau oder Außenprüfer betrauten Amtsträger der Finanzbehörde. Sie stellt eine einheitliche Strukturierung und Bezeichnung der nach § 146a Absatz 1 der Abgabenordnung aufzuzeichnenden Daten in Datenschema und Datenfelderbeschreibung für die Protokollierung nach §2 und die Speicherung nach §3 sicher. Dies gilt unabhängig vom Programm des Herstellers.* 

Wichtig ist an dieser Stelle sicherlich die Fokussierung des Verordnung auf den Export der Daten. Wie auch an anderen Stellen der Verordnung ist es nicht das primäre Ziel, detaillierte Vorgaben über die technischen Eigenschaften der Technischen Sicherheitseinrichtung zu machen. Stattdessen erfolgt eine Fokussierung auf die Aspekte, die für einen interoperablen Betrieb absolut notwendig sind.

## Ausblick
Über die nächsten Monate sollen an dieser Stelle weitere Artikel zu Details der Technischen Sicherheitseinrichtung folgen. Geplant sind Detailartikel zum Sicherheitsmodul und zu einheitlichen digitalen Schnittstelle. Über Kommentare oder Anmerkungen freue ich mich natürlich auch jetzt schon

{{% /htmlblock %}}
