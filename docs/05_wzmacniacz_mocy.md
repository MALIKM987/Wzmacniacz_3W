# Wzmacniacz mocy

## Cel modułu

Końcówka mocy wzmacnia sygnał analogowy do poziomu umożliwiającego zasilenie głośnika. W projekcie zastosowano tranzystorową końcówkę mocy pracującą w klasie A, inspirowaną topologią Linsley-Hood 1969.

## Elementy aktywne

| Element | Typ | Rola |
|---|---|---|
| MJL4281AG | tranzystor mocy NPN | główne elementy wykonawcze końcówki |
| BD139 | tranzystor NPN średniej mocy | sterowanie tranzystorami mocy |
| BC557C | tranzystor PNP małej mocy | polaryzacja i funkcje pomocnicze |

## Schemat blokowy końcówki mocy

```mermaid
flowchart LR
    A[Sygnał z DAC / I/V] --> B[Stopien sterujacy]
    B --> C[Driver BD139]
    C --> D[Tranzystory mocy MJL4281AG]
    D --> E[Wyjscie glosnikowe]
    F[Sprzezenie zwrotne] --> B
    E --> F
```

## Klasa A

W klasie A tranzystory przewodzą przez cały okres sygnału. Ogranicza to zniekształcenia przejścia, ale powoduje duże straty mocy i wymaga dobrego chłodzenia.

## Podstawowe zależności

Wzmocnienie napięciowe:

$$
A_v = \frac{V_{out}}{V_{in}}
$$

Wzmocnienie w decybelach:

$$
A_{v,dB} = 20 \log_{10}(A_v)
$$

Moc skuteczna na obciążeniu:

$$
P_{RMS} = \frac{V_{RMS}^2}{R}
$$

albo:

$$
P_{RMS} = I_{RMS}^2 \cdot R
$$

THD:

$$
THD = \frac{\sqrt{U_2^2 + U_3^2 + U_4^2 + ...}}{U_1}
$$

Sprawność:

$$
\eta = \frac{P_{out}}{P_{supply}}
$$

Dla uproszczonego przypadku:

$$
\eta = \frac{P_{out,RMS}}{I_{spocz} \cdot V_{CC}}
$$

## Uwagi praktyczne

Końcówka klasy A wymaga szczególnej uwagi przy projektowaniu termicznym. Tranzystory mocy powinny pracować z odpowiednim radiatorem, a punkt pracy powinien być zweryfikowany pomiarowo.
