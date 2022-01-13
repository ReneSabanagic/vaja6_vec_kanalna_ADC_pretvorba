Vaja 6_vec_kanalna_ADC_pretvorba

a)	Zaženite STM32CubeIDE in ustvarite nov STM32 projekt (pod zavihkom information Center). V zavihku Board selector s pomočjo filtrov Vendor, Type in MCU/MPU Series izberite ustrezno razvojno ploščo (v našem primeru Nucleo-L476RG), kliknite Next, projekt poimenujte vaja6_vec_kanalna_ADC_pretvorba in kliknite Finish (na možnosti opcije za prenastavitev periferije izberite Yes, izbrana naj bo tudi opcija perspektive za STM32CubeMX).
b)	Če ima Izbrani ADCx pretvornik oznako s trikotnikom, razrešite to omejitev (uporabljene pin-e postavite na Reset_State). 
c)	Razširite razdelek ADC1 v levem oknu CubeMX okolja.
d)	Določite in aktivirajte tri analogne vhode za kanale IN1, IN2 in IN3 za zunanje potenciometre kot Single-ended vhod. To bodo pini ___PC0_______, ___PC1______ in ____PC2______. 
Izbrani pini naj bodo vsi v isti grupi/skupini! Katera skupina je to? _skupina C___.
e)	Zunanja potenciometra pravilno priključite na Nucelo razvojno ploščo preko protoborda (potenciometer ima 3 priključke: GND, out in +5V). 
f)	Na zaslonu se vam mora usterzno pobarvati izbrani pin v zeleno barvo. Kaj se izpiše poleg pinov? ___adc1_in2___, _adc2_in2___ in _adc3_in2___.
g)	V Clock Configuration spremenimo takt pretvorbe FCLK (MHz) na 16 MHz.
h)	V oknu Configuration ADC pretvorbe V Parameter settings izberite ločljivost pretvorbe na 8-bitno, torej je območje vrednosti od 0 ÷ 255. Clock Prescaler nastavite tako, da bo izračunana frekvenca vzorčenja 4 MHz. Koliko bo izbrana vrednost parametra? __4__.
i)	Omogočimo ADC_Regular_Conversion_mode, omogočimo Continuos Conversion.
j)	Koliko je privzeta vrednost parametra Number of Conversion? _1_ .
k)	Čas vzorčenja Sampling Time izberite 92.5 cikla. Koliko je čas vzorčenja v mikro sekundah? ___26,125μs____. Enačba za izračun: tvz = (tvz_cik + 12) / ftakta_pretvorbe
l)	V zavihku DMA Settings kliknite Add in v nastalem polju »select« izberite možnost ADC1. Dolžina podatka pretvorbe bo 1 Byte, zato ustrezno popravite izbirno polje Data Width: ___byte____ (tako za Peripheral in Memory). Increment Address omogočite le v registru Memory. V izbirnem polju za način delovanja Mode izberite Circular. Kliknite Ok. Sedaj tudi omogočite DMA Continuos Requests v oknu Parameter Setttings.
e)	Kaj pomeni kratica DMA? _______direct memory access__________.
Rene Šabanagić, Filip Stanojević
