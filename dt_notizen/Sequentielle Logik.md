---
tags:
  - foliensatz/08
  - "#MoC"
  - cleaned
aliases:
  - sequentiell
---

## Sequentielle Schaltungen

- Bei [[Kombinatorische Logik|kombinatorischer Logik]] hängen die Ausgänge nur von _aktuellen_ Eingangswerten ab
- Bei sequentiellen Schaltungen ist das anders
- Ausgänge hängen ab von 
	- Aktuellen Eingabewerten und
	- Vorherigen Eingabewerten
- Sequentielle Schaltungen speichern einen _internen_ Zustand
	- (Kurzzeit-)Gedächtnis repräsentiert bisherige Eingabesequenzen
	- Realisiert durch Rückkopplungen von Ausgängen
	- Nicht kombinatorisch

## Sequentielle Bauteile

[[Bistabile Grundschaltung]]
[[SR-Latch]]
[[JK-Latch]]
[[D-Latch]]
[[D-Flip-Flop]]
[[Flip-Flops mit Taktfreigabe]]
[[Zurücksetzbare Flip-Flops]]

## Sequentielle Logik

- Alle nicht-kombinatorischen Schaltungen
- Erlaubt Rückkopplungen, beispielsweise:

![[Pasted image 20251203195432.png]]

- Das Beispiel ist eine instabile (oszillierende) Schaltung
	- Verhalten abhängig von Herstellungsprozess, Spannung, Temperatur
	- Nicht vorhersagbar

## Entwurf synchroner sequentieller Logik

- Rückkopplungen durch Register aufbrechen
	- Halten den Zustand der Schaltung
	- Ändern Zustand nur zur Taktflanke
	- Gesamte Schaltung synchronisiert mit Taktflanke

![[Pasted image 20251203195807.png]]

## Synchrone sequentielle Schaltungen

- Regeln für Aufbau
	- Jedes Schaltungselement ist entweder Register oder kombinatorische Schaltung
	- Mindestens ein Schaltungselement ist ein Register
	- Alle Register werden durch das gleiche Taktsignal gesteuert
	- Jeder zyklische Pfad enthält mindestens ein Register
- Anwendungsbeispiele
	- [[Pipelines]]
	- [[Endliche Zustandsautomaten]]