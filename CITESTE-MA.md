# SINAPSA — Site gata de publicat

Acest folder conține un singur fișier important: **index.html** — site-ul tău complet (design + conținut), gata de publicat gratuit.

---

## PAȘII COMPLEȚI — de la zero la site live (10-15 minute)

### Pasul 1 — Creezi cont pe GitHub
1. Mergi pe **https://github.com**
2. Apasă **Sign up**, completezi email, parolă, nume de utilizator (ex: `andrei-tech`)
3. Confirmi email-ul

### Pasul 2 — Creezi un "repository" (spațiul unde stă site-ul)
1. Din contul tău GitHub, apasă butonul verde **New** (sau **+** din dreapta sus → **New repository**)
2. La **Repository name** scrii exact: `nume-utilizator.github.io`
   - Exemplu: dacă utilizatorul tău e `andrei-tech`, numele trebuie să fie EXACT `andrei-tech.github.io`
   - Acest nume special face ca GitHub să publice automat site-ul, fără setări suplimentare
3. Bifezi **Public**
4. Apeși **Create repository**

### Pasul 3 — Urci fișierul index.html
1. Pe pagina noului repository, apeși **uploading an existing file** (sau **Add file → Upload files**)
2. Tragi fișierul `index.html` din acest folder în fereastra browserului
3. Jos, apeși **Commit changes**

### Pasul 4 — Activezi publicarea (Pages)
1. În repository, mergi la **Settings** (sus, în meniu)
2. În meniul din stânga, apeși **Pages**
3. La **Source**, alegi branch-ul **main** și folderul **/ (root)** → **Save**
4. Așteaptă 1-2 minute

### Pasul 5 — Gata!
Site-ul tău e live la:
```
https://nume-utilizator.github.io
```
(înlocuiește cu numele tău de utilizator real)

---

## Ce faci după publicare

- **Modifici conținutul**: deschizi fișierul `index.html` direct pe GitHub (creion-ul de editare), sau îl editezi local și îl re-urci
- **Adaugi domeniu propriu** (ex: sinapsa.ro): în Settings → Pages → Custom domain, introduci domeniul cumpărat de la un registrator (ex: RoTLD, Namecheap)
- **Adaugi Google AdSense** pentru monetizare: te înscrii pe adsense.google.com, adaugi codul primit în `index.html`, înainte de `</head>`

## Alternativă rapidă: Netlify (fără cont GitHub obligatoriu)

1. Mergi pe **https://app.netlify.com/drop**
2. Tragi acest folder întreg direct în pagină
3. Site-ul e live instant, cu un link de tipul `nume-random.netlify.app`
4. Poți schimba numele din Site settings → Change site name

---

## Articolele incluse

În folderul `articole/` găsești **6 articole complete**, gata de publicat:
- `ce-este-un-model-ai.md` — explică simplu ce e un model AI
- `primul-robot-arduino.md` — tutorial pas cu pas pentru un robot cu Arduino
- `automatizari-ai-2026.md` — 5 automatizări AI practice
- `perceptie-robotica-senzori.md` — cum „văd" roboții obstacolele (senzori, LiDAR, camere)
- `robotica-industriala-romania.md` — analiză despre automatizarea industrială locală
- `responsabilitate-algoritmica.md` — articol de opinie despre etica deciziilor automate

Le poți copia direct în paginile site-ului, sau mi le poți da înapoi ca să le transform în pagini HTML separate, cu link din pagina principală.

## Configurarea formularului de contact (about.html)

Formularul din pagina „Despre" folosește **Formspree** — un serviciu gratuit care trimite mesajele direct în email-ul tău, fără să ai nevoie de server propriu.

1. Mergi pe **https://formspree.io** și creezi cont gratuit (permite până la 50 de mesaje/lună gratuit)
2. Creezi un „New Form", introduci email-ul tău
3. Primești un link de tipul `https://formspree.io/f/xxxxxxxx`
4. În fișierul `about.html`, cauți linia:
   ```
   <form action="https://formspree.io/f/COMPLETEAZA-ID-UL-TAU" method="POST">
   ```
   și înlocuiești `COMPLETEAZA-ID-UL-TAU` cu ID-ul primit de la Formspree (partea de după `/f/`)
5. Publici din nou site-ul — formularul e funcțional imediat

## Pregătirea pentru Google AdSense

1. Site-ul trebuie să fie live cel puțin câteva zile/săptămâni, cu conținut real (articolele de mai sus sunt un început bun)
2. Ai nevoie de pagini de **Politică de confidențialitate** și **Despre/Contact** (pot să ți le generez dacă vrei)
3. Aplici pe **adsense.google.com**, introduci URL-ul site-ului
4. Adaugi codul de verificare primit de la Google în `index.html`, între `<head>` și `</head>`
5. Aștepți aprobarea, apoi inserezi codul de reclame în pagini

Succes cu SINAPSA! 🚀
