# Vaja-1-posami-na-ADC-pretvorba-z-STM32F0-Discovery

b) V Pinout pogledu si oglejte prerazporeditev PIN-ov mikroprocesorja za vhodne in izhodne enote. Zelena LED je priključena na PC9 pin, MODRA pa na PC8 pin. Kaj je pa priključeno na pin PA0? odg: modra tipka

c) Glede na vašo razvojno ploščico in razširitveno vezje z tipkami ter potenciometri, izberite ustrezni analogni vhod. Kateri pin je to? odg: PC0

d) V Analog razdelku levo od sheme mikroprocesorja ugotovite, koliko ADC pretvornikov ima vaša razvojna ploščica? odg: 16 (IN0 - IN15)

e) Izbrani ADC pretvornik ima oznako s trikotnikom. Kaj to pomeni? odg: Pomeni, da je delno v konfliktu z drugim pinom. Kaj morate storiti, da razrešite to omejitev? Opišite in jo odpravite. odg: Pin (PIN PC0) moramo nastaviti na Analog ADC_IN10 in izberemo pretvornik IN10. Ostale pine, ki jih ne bomo uporabljali pa nastavimo na reset_state.

f) Razširite (kliknite) razdelek ADC. Koliko je vseh vhodnih kanalov (seštejte oznake INxx) ? odg: Razvojna plošča ima 16 pretvornikov (IN0 - IN15).

g) Glede na potenciometer na vaši ploščici izberite-obkljukajte ustrezni kanal/pin. Na zaslonu se vam morausterzno pobarvati izbrani pin v zeleno barvo. Kaj se izpiše poleg pina? odg: Poleg pina se izpiše ADC_IN10

i) Pod Configuration ADC enote gumb v Parameter settings izberite ločljivost pretvorbe na 8-bitno, torej jeobmočje vrednosti od 0 ÷ 255. Preglejte, kakšne so še ostale možne ločljivosti pretvorbe in območja vrednosti? a. 8bit_, od 0 do 255, b. ___ 10bit_____, od 0 do 1024, c. 12bit, od 0 do 4096.

Komentar: Program deluje tako, da pošilja podatke stanja potenciometra preko ADC pina v spremenljivko, ki se izpiše v programu STM studio z 100ms zakasnitvijo.
