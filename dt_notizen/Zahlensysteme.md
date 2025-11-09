---
tags:
  - foliensatz/01
  - cleaned
  - MoC
Related:
  - "[[Umrechnen zwischen Zahlensystemen]]"
  - "[[Binärsystem]]"
---

## Häufig Verwendete Basen

![[Screenshot 2025-10-17 at 10.08.28.png]]

## Eigenschaften der Zahlensysteme

Gegeben sei eine Zahl $a_{k-1} \ldots a_1 a_0$ mit $k$ Ziffern und der Basis $b$:

| Eigenschaft                                            | [[Vorzeichenloses Stellenwertsystem]]                                                                                      | [[Vorzeichenbehaftete Binärzahlen\|Zweierkomplement]]                                              |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| Niedrigwertigste Stelle (LSD, least significant digit) | $a_0$                                                                                                                      | $a_0$                                                                                              |
| Höchstwertigste Stelle (MSD, most significant digit)   | $a_{k-1}$                                                                                                                  | $a_{k-1}$                                                                                          |
| Kleinste darstellbare Zahl                             | $\sum_{i-0}^{k-1} 0 \cdot b^i = 0$                                                                                         | $1 \cdot (-2^{k-1})  + \sum_{i=0}^{k-2} 0 \cdot 2^i = -2^{k-1}$                                    |
| Größte darstellbare Zahl                               | $\sum_{i-0}^{k-1} (b-1) \cdot b^i = b^k-1$                                                                                 | $1 \cdot (-2^{k-1})  + \sum_{i=0}^{k-2} 1 \cdot 2^i = 2^{k-1}-1$                                   |
| Anzahl der darstellbaren Werte                         | $\vert Z_b^k \vert = {\vert Z_b \vert}^k = b^k$                                                                            | $2^k$                                                                                              |
| Weitere Eigenschaften                                  | - Polyadisches Zahlensystem<br>- Eindeutig (bijektiv) abbildbar auf Wertebereich $\{0, \ldots, b^k-1\}$ für ein festes $k$ | - Eindeutig (bijektiv) abbildbar auf Wertebereich $\{-2^{k-1}, \ldots, 2^{k-1}-1\}$ für festes $k$ |

