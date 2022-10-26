# Obligatorisk oppgave 3 i Algoritmer og Datastrukturer

Denne oppgaven er en innlevering i Algoritmer og Datastrukturer. 
Oppgaven er levert av følgende student:
* Kristoffer Solberg, S331305, s331305@oslomet.no


# Oppgavebeskrivelse

I oppgave 1 kopierte jeg kildekoden som var spesifisert i oppgaven. Deretter sto det at man måtte gjøre noen endringer
så referansen forelder får rett verdi i hver node. Det var rød strek under opprett av ny node så jeg la en ekstra input
som var det den spurte om.

Oppgave 2 løste jeg ved å kjøre et par tester for så å bruke store deler av koden i inneholder som gjør mye av det
samme som metoden jeg lager skal gjøre. Måtte endre litt på koden da inneholder returnerer true or false, og jeg ønsker
å telle for hvert tilfelle istedet.

I oppgave 3 skal jeg finne førstepostorden og nestePostOrden. Vi vet at ved å tegne opp et binært tre så er første post 
orden lengst ned til venstre hvis det  finnes venstrebarn. Hvis det ikke finnes venstrebarn så går man til høyre og 
sjekker alle nodene for om de har venstrebarn. Hvis det ikke finnes venstrebarn så er nederste høyrebarn 
førstepostorden, hvis rot ikke har barn så er rot førstepostorden. 
I nestePostOrden så sjekka jeg først om p sin forelder er null. Hvis den er null så er p rot og nestePostOrden 
er da null. Så lagra jeg broren til p så jeg kunne bruke den senere. Dette gjorde jeg ved å ta p.forelder.høyre. 
Så sjekka jeg om broren til p er null for hvis den er det så vet jeg at p sin forelder er nestePostOrden. 
Jeg fant en bug i koden etter masse debugging fordi den gikk i loop og jeg skjønte ikke hvor. Til slutt klarte jeg å 
løse det ved å sjekke om p == q. Hvis dette er tilfellet så er nestePostOrden også p sin forelder. Til slutt går jeg ned
hele venstresiden.

I oppgave 4 så koda jeg først postorden-metoden ved å bruke førstePostorden og nestePostorden og utføre oppgave.
I postordenRecursive så sjekker jeg først om p er lik null og så kjører jeg postordenRecursive igjen mot venstre side 
og så mot høyre, og til slutt oppgave utført. 

I oppgave 5 serialize-metoden brukte jeg bredde først traversering for å traversere igjennom treet og legge hver enkelt
node inn i et array. I deserialize-metoden så lagde jeg et tre, og løp igjennom arrayet og brukte leggInn-metoden til
treet for å legge inn hver index fra arrayet inn i treet. 
