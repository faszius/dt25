---
tags:
  - foliensatz/07
  - cleaned
---

## Zuweisungen in SystemVerilog

- Die Synthese beider Module ergibt den gleichen Schaltplan

### Assign Statement

![[Pasted image 20251128191623.png]]

- Auch continuous assignment genannt
- Linke Seite (LHS, "left hand side"): Variable oder Port
- Rechte Seite (RHS, "right hand side"): logischer Ausdruck
- Zuweisung, wenn der Wert von RHS sich ändert

### `always_comb`

![[Pasted image 20251128191838.png]]

- `always_comb <instruction`
	- Zuweisung ebenfalls, wenn sich der Wert von RHS ändert
	- LHS Variablen dürfen nicht von anderen Blöcken geschrieben werden

### Eigenschaften von `assign` und `always_comb`

- Werden bei Simulation immer ausgeführt, wenn sich ein Signal auf der rechten Seite ändert
- Erlauben nur kombinatorische Logik
- Reihenfolge im Quellcode oft nicht relevant
	- Nebenläufige Signalzuweisungen ("concurrent signal assignments")
	- Aber: blockierende Signalzuweisungen (`a = b`) innerhalb von Blöcken (`begin`/`end`) werden nacheinander ausgeführt

![[Pasted image 20251128192759.png]]
