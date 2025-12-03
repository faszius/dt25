---
tags:
  - foliensatz/08
  - cleaned
Related:
  - "[[Vergleich D-Latch mit D-Flip-Flop]]"
---

## D-Flip-Flop

- Wir schalten zwei [[D-Latch|D-Latches]] in Serie
	- First (F)
	- Second (S)
	- Sie werden von komplementären Taktsignalen gesteuert
- $\text{CLK = 0}$
	- First transparent $\rightarrow$ $n = D$
	- Second nicht transparent $\rightarrow$ $Q$ bleibt unverändert
- $\text{CLK}=1$
	- First nicht transparent $\rightarrow$ $n$ bleibt unverändert
	- Second transparent $\rightarrow$ $Q=n$
- Taktflanken-gesteuert
	- Genau bei steigender Flanke wird $Q = D$
	- Es wird der Wert von $D$ übernommen, der _unmittelbar vor_ der Taktflanke anliegt
