# pci_cpu_bt_wifi

Placa projetada para o desenvolvimento das aulas de microcontrolador e programação em linguagem C da disciplina de Sistemas Eletrônicos Digitais (SELDI) no curso técnico em Eletroeletrônica no SENAI Jandira. 

## Recursos
* Microcontroladores alvo: PIC16F887 e PIC18F4550;
* Comunicação sem fio através de conexão com os módulos ESP01 ou HC05. A comunicação é prevista exclusivamente com um dos módulos, inclusive pelo fato de que ambos requerem conexão exclusiva via interface de comunicação serial (EUSART);
* Disponibilidade de conexão nos portes via terminais IDC e PIN HEADER;
* Alimentação: 5 Vcc com regulador de tensão para 3V3 para o módulo de comunicação serial;
* Conexão de gravação para gravador PICkit2 ou superior.

### Placa ainda não testada!!! Em fase de produção na JLCPCB!


|Figura 1: Visualização 3D da placa |
|:---------------------------------:|
| ![CPU em 3D](https://github.com/JoseWRPereira/pci_cpu_bt_wifi/blob/main/images/3d.gif)|
| Fonte: Próprio autor |


|Figura 2: Layout superior da placa |
|:---------------------------------:|
| ![Layout Frontal](https://github.com/JoseWRPereira/pci_cpu_bt_wifi/blob/main/images/layout_superior.svg)|
| Fonte: Próprio autor |


|Figura 3: Layout inferior da placa |
|:---------------------------------:|
| ![Layout Frontal](https://github.com/JoseWRPereira/pci_cpu_bt_wifi/blob/main/images/layout_inferior.svg)|
| Fonte: Próprio autor |


|Figura 4: Esquemático da CPU |
|:---------------------------------:|
| ![Layout Frontal](https://github.com/JoseWRPereira/pci_cpu_bt_wifi/blob/main/Schematic_cpu_esp01_2021-12-17.png)|
| Fonte: Próprio autor |


# Lista de materiais - BOM( *Bill Of Materials* )


| ID |	Name |	Designator | Footprint | Quantity |
|:--:|:--:|:--:|:--:|:--:|
|1|22p|C1,C2|C0805|2|
|2|1k|R12,R13,R14,R15,R9,R10,R11|R0805|7|
|3|LS4148|D1|LL-34_L3.5-W1.5-RD|1|
|4|470nF|C7|C0805|1|
|5|10uF|C3,C6|CASE-A_3216|2|
|6|10k|R8,R1,R2,R4,R5|R0805|5|
|7|100nF|C4,C5|C0805|2|
|8|BSS138_C193019|Q1,Q2|SOT-23-3_L3.0-W1.7-P0.95-LS2.9-BR|2|
|9|27R|R6,R7|R0805|2|
|10|AMS1117-3.3_C351784|U4|SOT-223-3_L6.5-W3.4-P2.30-LS7.0-BR|1|
|11|470R|R3|R0805|1|
|12|Header-Male-2.54_1x2|JMP|HDR-TH_2P-P2.54-V-M-1|1|
|13|LED-0805_G|LED_3V3,LED_5V,LED0,LED1|LED0805_GREEN|4|
|14|150R|R16|R0805|1|
|15|K4-6×6_SMD|ESP_RST,RESET|KEY-SMD_4P-L6.0-W6.0-P3.90-LS10.0|2|
|16|ESP-01|1|WIRELESS-WIFI-ESP-01|1|
|17|PIC16F887-E/P|U1|PDIP-40_L52.3-W13.8-P2.54-LS15.24-BL|1|
|18|PN61729-S|X2|PN61729-S|1|
|19|Header-female 1x6 R/A  2.54|U3|HEADER-FEMALE R/A 1X6 2.54|1|
|20|Header-Male-2.54_1x8|H3,H1,H2,H4|HDR-TH_8P-P2.54-V-M|4|
|21|Header-Female-2.54_1x6|BT|HDR-TH_6P-P2.54-V-F|1|
|22|Header-Female-2.54_1x3|GND,VCC|HEADER-FEMALE-2.54_1X3|2|
|23|HDR-IDC-2.54-2X7P|P1,P2,P3,P4|IDC-TH_14P-P2.54-V-R2-C7-S2.54|4|
|24|XTAL 20MHz|U2|SMD CRISTAL|1|



# Pinos disponíveis para conexão

## PIC16F887

| Pino |	PORT |	Função |
|:----:|:-----:|:-------:|
| 33 | RB0 | AN12 / INT |
| 34 | RB1 | AN10 / C12IN3-|
| 35 | RB2 | AN8 |
| 36 | RB3 | AN9 / PGM / C12IN2- |
| 37 | RB4 | AN11 |
| 38 | RB5 | AN13 / nT1G |
| 39 | RB6 | ICSPCLK |
| 40 | RB7 | ICSPDAT |
| |     | |
| 19 | RD0 | |
| 20 | RD1 | |
| 21 | RD2 | |
| 22 | RD3 | |
| 27 | RD4 | |
| 28 | RD5 | P1B |
| 29 | RD6 | P1C |
| 30 | RD7 | P1D |
| |     | |
|  2 | RA0 | AN0 / ULPWU / C12IN0- |
|  3 | RA1 | AN1 / C12IN1- |
|  4 | RA2 | AN2 / Vref- / CVref / C2IN+ |
|  5 | RA3 | AN3 / Vref+ / C1IN+ |
| 23 | RA4 | T0CKI / C1OUT |
| 24 | RA5 | AN4 / nSS| / C2OUT |
| 25 | RE0 | AN5 |
| 26 | RE1 | AN6 |
| |     | |
| 10 | RE2 | AN7 |
|  1 | RE3 | nMCLR / VPP |
| 15 | RC0 | T1OSO / T1CKI |
| 16 | RC1 | T1OSI / CCP2 |
| 17 | RC2 | P1A / CCP1 |
| 18 | RC3 | SCK / SCL |
| 23 | RC4 | SDI / SDA |
| 24 | RC5 | SDO |
