# BOM i komponenty

## Najważniejsze układy

| Element | Funkcja |
|---|---|
| DIR9001 | odbiornik S/PDIF i konwerter do I2S |
| SN74LVU04A | bufor i kształtowanie sygnałów logicznych |
| AD1955 | przetwornik cyfrowo-analogowy audio |
| AD797 | wzmacniacz operacyjny do konwersji I/V |
| STM32F103 | mikrokontroler sterujący DAC |
| MJL4281AG | tranzystor mocy NPN |
| BD139 | tranzystor drivera |
| BC557C | tranzystor pomocniczy PNP |
| REG1117-3.3 | stabilizator 3,3 V |
| L7805 | stabilizator +5 V |
| L7905 | stabilizator -5 V |
| MB6S | mostek prostowniczy |
| RCJ-043 | gniazdo RCA |
| ECS 24,576 MHz | rezonator / kwarc dla toru cyfrowego |

## Rola tranzystorów w końcówce mocy

### MJL4281AG

Tranzystor dużej mocy użyty jako element końcowy wzmacniacza. Daje duży zapas prądowy i napięciowy względem wymaganej mocy wyjściowej.

### BD139

Tranzystor średniej mocy używany jako driver, czyli element sterujący tranzystorem mocy.

### BC557C

Tranzystor PNP małej mocy używany w obwodach polaryzacji, sprzężenia lub funkcjach pomocniczych.

## Uwagi

W repozytorium warto utrzymać katalog `literatura/`, ponieważ zawiera noty katalogowe użytych elementów. Dobrą praktyką jest też dodanie uproszczonego pliku BOM w formacie CSV lub XLSX.
