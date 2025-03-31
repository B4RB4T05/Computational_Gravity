# Problemy 2 
# a)
# Problem Spadania Swobodnego Dwóch Punktowych Mas

## Opis Problemu
- **Masy**: Dwie punktowe masy, każda o masie $1 \, \text{kg}$.
- **Początkowa odległość**: $1 \, \text{m}$.
- **Początkowa prędkość**: Obie masy zaczynają od spoczynku ($v = 0 \, \text{m/s}$).
- **Punkt kolizji**: Ze względu na symetrię, masy zderzają się w środku ($x = 0$).

---

## Układ Współrzędnych
- Umieść początek układu współrzędnych w środku początkowej odległości.
- Jedna masa zaczyna w $x = -0.5 \, \text{m}$, a druga w $x = 0.5 \, \text{m}$.
- Zdefiniuj $r(t)$ jako odległość między masami w czasie $t$, gdzie $r(0) = 1 \, \text{m}$.
- Każda masa porusza się symetrycznie w kierunku środka, pokonując odległość $\frac{r(t)}{2}$.

---

## Prawo Grawitacji Newtona
- Siła grawitacyjna:
  $$
  F = \frac{G m_1 m_2}{r^2} = \frac{G}{r^2}, \quad G = 6.67430 \times 10^{-11} \, \text{m}^3 \, \text{kg}^{-1} \, \text{s}^{-2}.
  $$
- Przyśpieszenie jednej masy:
  $$
  a = \frac{F}{m} = \frac{G}{r^2}.
  $$

---

## Równanie Różniczkowe
- Przyśpieszenie względne dwóch mas:
  $$
  \frac{d^2 r}{dt^2} = -\frac{2G}{r^2}.
  $$
- Warunki początkowe:
  $$
  r(0) = 1 \, \text{m}, \quad \frac{dr}{dt}(0) = 0 \, \text{m/s}.
  $$

---

## Metoda Zachowania Energii
- Całkowita energia jest zachowana:
  $$
  E = U + K = -\frac{G}{r} + \frac{1}{2} \mu v^2,
  $$
  gdzie $\mu = \frac{m_1 m_2}{m_1 + m_2} = 0.5 \, \text{kg}$ (masa zredukowana), a $v = \frac{dr}{dt}$.
- W chwili $t = 0$, $E = -G$, więc:
  $$
  -\frac{G}{r} + \frac{1}{2} \cdot 0.5 \cdot v^2 = -G.
  $$
- Uprość dla $v$:
  $$
  v = \frac{dr}{dt} = -\sqrt{\frac{2G}{r} - 2G}.
  $$

---

## Całka Czasu Kolizji
- Rozwiąż dla czasu kolizji $T$:
  $$
  \int_{1}^{0} \frac{dr}{\sqrt{\frac{2G}{r} - 2G}} = -\int_{0}^{T} dt.
  $$
- Ta całka jest złożona i zwykle rozwiązywana numerycznie lub za pomocą całek eliptycznych.

---

## Rozwiązanie Numeryczne
- Przekształć równanie drugiego rzędu w układ pierwszego rzędu:
  $$
  v = \frac{dr}{dt}, \quad \frac{dv}{dt} = -\frac{2G}{r^2}.
  $$
- Warunki początkowe:
  $$
  r(0) = 1, \quad v(0) = 0.
  $$
- Rozwiąż numerycznie (np. używając `scipy.integrate.solve_ivp` w Pythonie lub `NDSolve` w Mathematica) aż do $r(t) = 0$.
- Zapisz $T$ w sekundach i przelicz na godziny:
  $$
  T_{\text{godziny}} = \frac{T_{\text{sekundy}}}{3600}.
  $$

---

## Szacowanie Czasu Kolizji
- Analityczne przybliżenie:
  $$
  T \approx \sqrt{\frac{\pi^2}{128G}} \approx 5.14 \times 10^5 \, \text{s}.
  $$
- Przelicz na godziny:
  $$
  T \approx \frac{5.14 \times 10^5}{3600} \approx 142.8 \, \text{godzin}.
  $$

---

## Funkcja Położenia $x(t)$
- Dla jednej masy zaczynającej w $x = 0.5 \, \text{m}$:
  $$
  x(t) = \frac{r(t)}{2}.
  $$
- Użyj rozwiązania numerycznego dla $r(t)$, aby obliczyć $x(t)$.

---

## Wykres $x(t)$
- Użyj wyników numerycznych dla $r(t)$, aby obliczyć $x(t) = \frac{r(t)}{2}$.
- W Pythonie (z Matplotlib):
---

```python
import 
```

![alt text](image.png)

----

marp - narzedzie z md robiona prezentacja w pdf
