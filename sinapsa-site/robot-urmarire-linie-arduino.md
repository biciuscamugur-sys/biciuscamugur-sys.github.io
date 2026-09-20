# Al doilea tău robot: urmărire de linie cu Arduino

Dacă ai construit deja robotul din primul nostru tutorial (cel care evită obstacole), ești pregătit pentru următorul pas natural: un robot care **urmărește o linie trasată pe podea**, un proiect clasic în robotică, folosit inclusiv în competiții școlare și universitare.

## De ce acest proiect e pasul logic următor

Robotul cu evitare de obstacole ți-a arătat cum să controlezi motoare și să citești un senzor. Robotul cu urmărire de linie adaugă un concept nou, esențial în robotică: **controlul proporțional** — ajustarea continuă a comportamentului robotului, nu doar reacții de tip „da/nu".

## Ce cumperi în plus față de primul proiect

Poți refolosi șasiul, motoarele și driverul L298N din primul robot. În plus, ai nevoie de:
- 1× modul senzor de linie cu infraroșu (de obicei cu 3-5 senzori individuali, deja montați pe o singură placă)
- Fire de conexiune suplimentare

Un modul cu senzor de linie costă de obicei sub 25 de lei, semnificativ mai ieftin decât restul componentelor.

## Cum funcționează senzorul de linie

Fiecare senzor infraroșu de pe modul emite lumină și măsoară cât se reflectă înapoi. O suprafață albă reflectă mult, o linie neagră reflectă puțin. Cu mai mulți senzori așezați unul lângă altul (de obicei 3 sau 5), robotul poate determina nu doar „văd linia sau nu", ci și **de care parte** se află linia față de centrul robotului.

## Logica de bază a urmăririi

Ideea centrală: dacă linia e detectată de senzorul din centru, robotul merge drept înainte. Dacă linia „alunecă" spre stânga (detectată de senzorul din stânga), robotul trebuie să vireze ușor la stânga, ca să revină la centru. Invers pentru dreapta.

Structura conceptuală a codului:

```
Cât timp robotul funcționează:
  Citește toți senzorii de linie
  Dacă senzorul din centru detectează linia:
    Mergi drept înainte
  Dacă senzorul din stânga detectează linia:
    Virează ușor la stânga (motor stâng mai încet, motor drept normal)
  Dacă senzorul din dreapta detectează linia:
    Virează ușor la dreapta (motor drept mai încet, motor stâng normal)
  Dacă niciun senzor nu detectează linia:
    Oprește, sau continuă ultima direcție cunoscută
```

## De ce „controlul proporțional" contează

O abordare simplistă (viraj brusc, complet, de fiecare dată când linia „alunecă") face robotul să zigzag-eze vizibil, ineficient. O abordare mai avansată — numită control **PID** (Proporțional-Integral-Derivativ), un concept folosit pe scară largă în automatizare — ajustează intensitatea virajului proporțional cu cât de departe e linia de centru, rezultând o mișcare mult mai lină.

Pentru un al doilea proiect, nu ai nevoie de PID complet — o versiune simplificată, cu doar componenta proporțională, e suficientă pentru rezultate solide și te pregătește conceptual pentru control mai avansat în proiecte viitoare.

## Pregătirea traseului de test

Poți desena o linie neagră groasă (2-3 cm lățime) pe o coală albă mare, sau folosești bandă izolatoare neagră pe o suprafață deschisă la culoare. Traseul poate include curbe line, dar evită unghiuri prea ascuțite la început — robotul învață treptat să gestioneze curbe mai strânse pe măsură ce ajustezi codul.

## Probleme comune și soluții

- **Robotul pierde constant linia în curbe** → mărește viteza de reacție (verifică mai des senzorii) sau redu viteza generală de deplasare
- **Robotul „tremură" în loc să meargă lin** → ai nevoie de o tranziție mai gradată între „viraj" și „drept înainte", nu doar comenzi bruște
- **Senzorii nu disting linia de fundal** → verifică distanța dintre senzor și podea (de obicei optimă la 3-5 mm) și asigură-te că lumina ambientală puternică nu interferează

## Ce urmează, ca al treilea proiect

Odată stăpânit controlul proporțional, poți combina cele două proiecte anterioare — un robot care urmărește o linie, dar oprește sau ocolește dacă detectează un obstacol pe traseu, folosind ambii senzori împreună. Acesta e exact tipul de combinație care apare în competițiile școlare de robotică.

## Concluzie

Robotul cu urmărire de linie e un pas natural, accesibil, de la primul tău proiect — reutilizează majoritatea componentelor deja cumpărate, adaugă un singur senzor nou, dar introduce un concept fundamental în robotică (controlul proporțional) care va rămâne util în orice proiect mai avansat pe care-l vei construi în viitor.
