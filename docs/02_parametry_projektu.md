# Parametry projektu

## Założenia projektowe

| Parametr | Wartość |
|---|---|
| Moc wyjściowa | powyżej 3 W |
| Wejście | koaksjalne S/PDIF |
| Konwersja S/PDIF do I2S | DIR9001 |
| Przetwornik C/A | AD1955 |
| Sterowanie | mikrokontroler STM32F103, SPI |
| Stopień mocy | tranzystorowy, klasa A |
| Topologia końcówki | inspirowana Linsley-Hood 1969 |
| Zasilanie końcówki mocy | +36 V |
| Zasilanie analogowe | +/-12 V |
| Zasilanie pomocnicze | +/-5 V, +3,3 V |
| Narzędzia projektowe | Altium Designer, LTspice |

## Wyniki z symulacji

| Badany parametr | Wynik |
|---|---|
| Pasmo przenoszenia | ok. 11,14 Hz - 5,18 MHz |
| Wzmocnienie napięciowe | ok. 16,25 V/V |
| Wzmocnienie w dB | ok. 24,22 dB przy 1 kHz |
| Moc RMS | ok. 12,9 W |
| THD | ok. 4,22E-03 |
| Sprawność | ok. 25,32% |
| Obciążenie symulacyjne | 8 ohm |

## Uwaga o interpretacji wyników

Wyniki symulacji pokazują potencjalne parametry układu, ale nie zastępują pomiarów rzeczywistego prototypu. W przypadku końcówki mocy klasy A szczególnie ważne są pomiary temperatury, stabilności punktu pracy oraz rzeczywistego THD.
