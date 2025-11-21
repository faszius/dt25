---
tags:
  - foliensatz/06
  - cleaned
---

## Zeitverhalten einer [[Kombinatorische Logik|kombinatorischen Schaltung]]

- Kombinatorisch: Werte der Ausgänge hängen nur von Werten an Eingängen ab
- Reale Schaltungselemente benötigen aber endliche Zeit, um Änderungen am Eingang auf Ausgang zu übertragen
	- Z.B. für Umladen von MOSFET Gate-Kapazitäten
- Zentrale Fragen
	- Wann sind die Ausgänge stabil?
	- Gibt es funktional äquivalente Schaltungen mit geringerer Verzögerung?
- Timing-Analyse anspruchsvoll, denn
	- Eingang kann Ausgang über verschiedene Pfade beeinflussen
	- Verzögerung kann für steigende/fallende Flanken unterschiedlich sein
	- Verzögerungen im (Sub-)Nanosekundenbereich

## Ausbreitungs- und Kontaminationsverzögerung

$t_{pd}$
	Maximale Zeit vom Eingang zum Ausgang (Ausbreitungsverzögerung, propagation delay)
$t_{cd}$
	Minimale Zeit vom Eingang zum Ausgang (Kontaminationsverzögerung, contamination delay)

![[Pasted image 20251121110649.png]]

- Ursachen für Verzögerung
	- Kapazitäten, Induktivitäten und Widerstände in der Schaltung
	- Lichtgeschwindigkeit als maximale Ausbreitungsgeschwindigkeit: 30 cm/ns
- Warum können $t_{pd}$ und $t_{cd}$ unterschiedlich sein?
	- Mehrere Ein- und Ausgänge mit unterschiedlich langen Pfaden
	- Unterschiedliche Verzögerungen für steigende $(t_{pd, LH})$ und fallende ($t_{pd, HL}$) Flanken
	- Schaltungen werden
		- Langsamer bei Erwärmung (Hitze erhöht Widerstand des leitfähigen Materials)
		- Schneller bei Abkühlung

## Lange (kritische) und kurze Pfade

Wir betrachten folgende Schaltung:
![[Pasted image 20251121111021.png]]

Dann ist der kritische (also der Pfad, der die meiste Zeit braucht):
$$\begin{aligned} t_{pd, Y} = 
\max(&t_{pd, \text{AND}} + t_{pd, \text{OR}} + t_{pd, \text{AND}}, \\ 
& t_{pd, \text{OR}} + t_{pd, \text{AND}}, \\
& t_{pd, \text{AND}}) = 2t_{pd, \text{AND}} + t_{pd, \text{OR}}
\end{aligned}$$
Und der kürzeste Pfad:
$$\begin{aligned}
t_{cd, Y} = \min(
& t_{cd, \text{AND}} + t_{cd, \text{OR}} + t_{cd, \text{AND}}, \\
& t_{cd, \text{OR}} + t_{cd, \text{AND}}, \\
& t_{cd, \text{AND}}
) = t_{cd, \text{AND}}
\end{aligned}$$

## Störimpulse (Glitches)

- Eine Änderung eines Eingangs verursacht mehrere Änderungen des Ausgangs
- Können durch geeignete Entwurfsdisziplin entschärft werden
	- Ausgänge nur zu bestimmten Zeiten auswerten (synchroner Entwurf)
	- Pfade modifizieren / hinzufügen
	- Nicht alle Störimpulse können eliminiert werden (z.B. gleichzeitiges Schalten mehrerer Eingänge)
- Können durch Timing- und Karnaugh-Diagramme analysiert werden

### Beispiel für Störimpuls: Erkennen

- Was passiert, wenn $ABC$ von $011$ nach $001$ schaltet?
- $t_{pd, \text{NOT/OR}}=1, t_{pd, \text{AND}}=2$

![[Pasted image 20251121112237.png]]

![[Pasted image 20251121112246.png]]


- Wir erkennen, dass der Ausgang $Y$ kurz auf $0$ springt, obwohl sich eigentlich nichts am Wert der Gleichung ändert
- Der Glitch entsteht, wenn wir im Karnaugh-Diagramm zwischen zwei benachbarten Rechtecken springen
- Wir können die kritische Stelle im Karnaugh-Diagramm mit einem zusätzlichen Implikanten $\overline{A}C$ überdecken

![[Pasted image 20251121112458.png]]

![[Pasted image 20251121112508.png]]

