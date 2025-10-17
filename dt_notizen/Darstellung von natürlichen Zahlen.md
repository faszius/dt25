---
tags:
  - foliensatz/01
  - cleaned
---

## Häufig Verwendete Basen

![[Screenshot 2025-10-17 at 10.08.28.png]]

## Vorzeichenloses Stellenwertsystem

### Beispiele

#### Beispiel 1

![[Screenshot 2025-10-17 at 10.07.54.png]]

##### Erklärung

Gegeben die Dezimalzahl $5347$ fragen wir uns, wie sie sich sonst darstellen lässt. Jede Stelle beschreibt, wie oft wir eine $1$ oder $10$ oder $100$ addieren - wir haben 7 mal die $1$, 4 mal die $10$, 3 mal die $100$ und 5 mal die $1000$. Wenn wir uns $1$, $10$, $100$ und $1000$ angucken, merken wir, dass das nichts anderes sind als Zehnerpotenzen - wir haben also 7 mal die $10^0$, 4 mal die $10^1$, 3 mal die $10^2$ und 5 mal die $10^3$:
$$\begin{align*}
5347 & = 7 \cdot 1  + 4 \cdot 10  + 3 \cdot 100  + 5 \cdot 1000 \\
& = 7 \cdot 10^0 + 4 \cdot 10^1 + 3 \cdot 10^2 + 5 \cdot 10^3 \\
& =: 5347_{10}
\end{align*}$$
Genau so können wir Binärzahlen betrachten. Schauen wir uns die Binärzahl $1101$ an. Im [[Binärsystem]] haben wir nicht 10 Zahlen, sondern nur 2 - $0$ und $1$. Im Grunde genommen können wir also genau so vorgehen wie im Dezimalsystem, nur dass wir statt Zehnerpotenzen [[Zweierpotenzen]] betrachten:
$$\begin{align*}
1101_2 & = 1 \cdot 2^0 + 0 \cdot 2^1 + 1 \cdot 2^2 + 1 \cdot 2^3 \\
& = 1 \cdot 1 + 0 \cdot 2 + 1 \cdot 4 + 1 \cdot 8 \\
& = 13_{10}
\end{align*}$$
### Beispiel 2

![[Screenshot 2025-10-17 at 10.09.10.png]]


### Definition

![[Screenshot 2025-10-17 at 10.34.32.png]]

Was die Funktion ausdrückt, lässt sich auch einfach in Worte fassen. Wenn wir eine Basis $b$ und eine Zahl $a$ in dieser Basis haben, dann lässt sich die zugehörige Dezimalzahl ausrechnen, indem wir die Ziffern von vorne bis hinten (von rechts nach links) durchgehen. Für die Ziffer $a_i$, die wir uns gerade angucken (wobei $i$ der Index der Ziffer ist), rechnen wir $a_i \cdot b^i$ und addieren die Zahl zu unserem Ergebnis. Nachdem wir alle Ziffern durchgegangen sind, ist das Ergebnis unsere Dezimalzahl. 

### Eigenschaften

Gegeben sei eine Zahl $a_{k-1} \ldots a_1 a_0$ mit $k$ Ziffern und der Basis $b$ im vorzeichenloses Stellenwertsystem:

| Eigenschaft                                            |                                                 |
| ------------------------------------------------------ | ----------------------------------------------- |
| Niedrigwertigste Stelle (LSD, least significant digit) | $a_0$                                           |
| Höchstwertigste Stelle (MSD, most significant digit)   | $a_{k-1}$                                       |
| Kleinste darstellbare Zahl                             | $\sum_{i-0}^{k-1} 0 \cdot b^i = 0$              |
| Größte darstellbare Zahl                               | $\sum_{i-0}^{k-1} (b-1) \cdot b^i = b^k-1$      |
| Anzahl der darstellbaren Werte                         | $\vert Z_b^k \vert = {\vert Z_b \vert}^k = b^k$ |

- Polyadisches Zahlensystem
- Eindeutig (bijektiv) abbildbar auf Wertebereich $\{0, \ldots, b^k-1\}$ für ein festes $k$
