toplotna-crpalka ohuvpuv
================
TOPLOTNA ČRPALKA
Ukvarjamo se z optimiziranjem gretja tople vode. Naš cilj je razviti strategije gretja, ki bodo dosegle najboljša razmerja cene in udobja. 
Vpliv imamo samo na to, ali boljer greje ali ne.

Bojlerji in toplotne črpalke imajo večinoma vgrajen en sam termometer, ponavadi na vrhu bojlerja. 
Med točenjem vode ter samim gretjem se v boljerju vzpostavi dinamika vode in drugi pojavi, s katerimi se mi ne bomo ukvarjali.
V vsakem trenutku so nam na voljo samo podatki: čas, termperatura in gretje (boljer greje ali ne). 
Iz teh podatkov bomo morali razbrati stanje vode v boljerju ter kdaj in koliko tople vode se porablja.

Lastnosti bojlerja in efekte raznih pojavov v njem bomo poskušali definirati s tabelami, ki jih bomo dobili od podjetja, 
ko bo projekt dovolj daleč. Do takrat si pomagamo s testnimi tabelami, ki jih konstruiramo sami ali pa najdemo na internetu. 
Primeri takšnih tabel:
- Bojler poln, začnemo točiti vodo, ne grejemo (temperatura v odvisnosti od količine iztočene vode)
- Bojler poln, ne grejemo (zanimajo nas izgube zaradi prevajanja) (temperatura v odvisnosti od časa)
- Bojler prazen, začnemo greti (temperatura v odvisnosti od časa)
Razmisliti moramo, katere tabele potrebujemo za popoln opis dogajanja. Želimo najmanjše možno število tabel.

S Tomažem sva že tudi sprogramirala preprost simulator boljerja, s katerim si lahko pomagamo pri testiranju.

Naslednja komponenta ki jo potrebujemo je simulator potrošnje. Ta naj bi simuliral navade 1-6 ljudi. Omogočal nam bo testiranje.

Z dejanskim razvojem strategij se bomo začeli ukvarjati v naslednji fazi.

Učinkovitost strategij bomo definirali z dvema parametroma: cena in udobje. Ceno je preprosto izračunati, če vemo kdaj je boljer grel. Upoštevati moramo tudi poceni/drag tok. (Ne)udobje definiramo z dolžino časa, ko je temperatura vode nižja od temperature, ki jo uporabnik želi.
Različne strategije gretja nam tvorijo točke na grafu neudobje(cena), kjer se da narisati krivuljo optimalnih strategij, kot nam jo je že risal g. Matjaž. Po tej krivulji se lahko uporabnik premika z nastavljanjem profilov gretja (lahko prioritizira ceno ali pa udobje). Naš cilj je krivuljo potisniti čim bližje koordinatnim osem.
