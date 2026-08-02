# Ghid de promovare — primii vizitatori pentru SINAPSA

Un site nou, oricât de bine făcut, nu primește vizitatori automat. Google are nevoie de timp (săptămâni, uneori luni) să te descopere și să te claseze. Între timp, trebuie să aduci tu însuți primii cititori. Iată un plan realist, pas cu pas.

---

## Google Analytics — deja pregătit tehnic în site

Codul de urmărire Google Analytics (GA4) a fost deja adăugat în **toate cele 9 pagini** ale site-ului (`index.html`, toate articolele, `about.html`, `privacy.html`). Tu trebuie doar să:

1. Mergi pe **analytics.google.com**, te loghezi cu contul tău Google
2. Creezi cont nou → nume „SINAPSA" → creezi o proprietate cu URL-ul site-ului tău
3. Primești un cod de forma `G-XXXXXXXXXX`
4. **Deschizi fiecare fișier `.html`** din site și înlocuiești `G-XXXXXXXXXX` (apare de 2 ori per fișier) cu codul tău real
   - Cel mai simplu: pe GitHub, folosești funcția „Find and replace" din editorul web, sau editezi local și re-urci fișierele
5. Publici din nou site-ul — Analytics începe să înregistreze vizitatori automat

## Google Search Console — pașii tăi (necesită login personal)

Acest pas chiar necesită contul tău Google direct, nu poate fi pre-pregătit tehnic:

1. Mergi pe **search.google.com/search-console**
2. Adaugi URL-ul site-ului (tip „Prefix URL")
3. Pentru verificare, cea mai simplă metodă e prin **eticheta HTML** (Google îți dă o linie de cod `<meta name="google-site-verification" content="...">`) — trimite-mi acel cod și ți-l adaug instant în toate paginile, la fel cum am făcut cu Analytics
4. Apeși Verify, apoi „Request Indexing" pentru pagina principală



---

## Partea 2 — Canalele de promovare (repetate constant)

### 1. Grupuri de Facebook relevante
Există zeci de grupuri românești pe teme de tehnologie, IT, electronică, robotică, AI. Caută grupuri precum „Pasionați de electronică România", „Inteligență Artificială România", „Arduino & Robotică România".

**Cum faci corect, fără să pari spam:**
- Nu posta doar linkul — scrie 2-3 propoziții despre ce oferă articolul, apoi linkul
- Participă și la discuții fără link, din când în când — construiește încredere, nu doar autopromovare
- Verifică regulile grupului înainte (unele interzic linkuri directe)

### 2. Reddit
Subreddit-uri precum r/Romania sau comunități internaționale de robotică/AI (r/robotics, r/artificial) — dar comunitatea Reddit e foarte sensibilă la autopromovare. Regula de aur: participă organic mult timp înainte să postezi propriul conținut, altfel riști să fii banat.

### 3. Grupuri și forumuri de nișă
Forumuri românești de electronică (ex: comunități pe teme Arduino/Raspberry Pi) sunt adesea mai primitoare față de conținut educațional de calitate decât rețelele sociale mari.

### 4. LinkedIn
Dacă articolele tale au și o componentă profesională (ex: „Roboții din fabricile românești"), LinkedIn e un canal bun — audiența e interesată de business și industrie, nu doar de hobby.

### 5. Newsletter-ul propriu
Site-ul are deja un formular de abonare. Fiecare vizitator nou e o oportunitate să-l convingi să se aboneze — asta transformă vizitatori întâmplători în cititori care revin constant, fără efort suplimentar de promovare.

---

## Partea 3 — Planul primelor 30 de zile

| Săptămâna | Acțiune |
|---|---|
| 1 | Publici site-ul, îl trimiți în Google Search Console, îl distribui în 2-3 grupuri relevante |
| 2 | Postezi câte un articol pe zi în diferite comunități (nu același articol peste tot în aceeași zi) |
| 3 | Analizezi în Google Analytics ce a funcționat, repeți ce a adus trafic |
| 4 | Publici un articol nou, promovezi din nou toate cele 6 articole existente + cel nou |

**Realitate importantă:** primele 100 de vizitatori sunt cei mai greu de obținut. După ce ai un nucleu de cititori constanți și câteva articole care „prind" pe rețele, procesul devine mai ușor — oamenii încep să distribuie singuri conținutul.

---

## Ce să NU faci

- **Nu cumpăra trafic sau followeri falși** — Google detectează tipare artificiale și te poate penaliza
- **Nu posta același link în 15 grupuri în aceeași oră** — pare spam, poți fi blocat de moderatori
- **Nu renunța dacă primele 2 săptămâni nu aduc mult trafic** — e normal, procesul e lent la început

---

## SEO de bază — ca Google să te găsească mai ușor

- Fiecare articol are deja titluri clare (h1, h2) — asta ajută Google să înțeleagă structura
- Adaugă, dacă poți, o propoziție cu cuvintele cheie principale în primele 2 rânduri ale fiecărui articol (ex: „robotică", „inteligență artificială", „Arduino")
- Publică constant — Google favorizează site-urile active, nu cele abandonate după 3 articole

Succes cu promovarea! Cel mai important lucru: consistența bate perfecțiunea — un articol nou pe săptămână, distribuit constant, aduce mai mult decât 10 articole publicate o dată și apoi tăcere.
