# DAC i tor analogowy

## Cel modułu

Moduł DAC zamienia cyfrowe dane audio w formacie I2S na analogowy sygnał audio. W projekcie zastosowano przetwornik AD1955, który jest układem audio wysokiej jakości.

## Elementy modułu

| Element | Rola |
|---|---|
| AD1955 | przetwornik cyfrowo-analogowy |
| AD797 | konwersja prąd-napięcie i filtracja |
| Elementy RC | filtracja i kształtowanie pasma |
| SPI z MCU | konfiguracja parametrów pracy DAC |

## Przepływ sygnału

```mermaid
flowchart LR
    A[I2S: LRCK, BCK, DATA] --> B[AD1955]
    B --> C[Wyjscia pradowe IOUT]
    C --> D[Konwersja I/V AD797]
    D --> E[Filtracja analogowa]
    E --> F[Wejscie wzmacniacza mocy]
```

## AD1955

AD1955 odbiera dane PCM, wykonuje cyfrową filtrację i konwersję sigma-delta, a następnie generuje analogowe sygnały prądowe. Układ może być konfigurowany przez SPI, co pozwala sterować formatem danych, głośnością i trybem mute.

## Konwersja I/V

Wyjścia DAC są prądowe, dlatego wymagają konwersji na napięcie. W projekcie wykorzystano wzmacniacze operacyjne AD797, które pełnią rolę konwerterów I/V oraz elementów filtracji analogowej.

## Znaczenie modułu

Ten blok ma duży wpływ na jakość całego wzmacniacza. Błędy w torze I/V, filtracji lub prowadzeniu masy mogą pogorszyć szumy, zniekształcenia i separację kanałów.
