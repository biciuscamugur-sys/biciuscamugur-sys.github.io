# Cum funcționează cu adevărat modelele de limbaj mari (precum ChatGPT)

Am explicat, într-un articol anterior, ce este pe scurt un „model AI". Aici mergem mai adânc, specific pentru modelele de limbaj mari (LLM — Large Language Models), tehnologia din spatele ChatGPT, Claude, Gemini și alte sisteme similare. Dacă vrei să înțelegi cu adevărat de ce aceste sisteme se comportă cum se comportă, acest articol e pentru tine.

## Pasul 1 — Textul devine numere (tokenizare)

Un calculator nu „citește" litere așa cum le citim noi. Primul pas, pentru orice model de limbaj, e transformarea textului în bucăți mici numite **token-uri** — care pot fi cuvinte întregi, părți de cuvinte, sau chiar caractere individuale, în funcție de cât de comun e cuvântul respectiv.

De exemplu, cuvântul „calculator" ar putea fi un singur token, în timp ce un cuvânt rar sau un nume propriu neobișnuit ar putea fi împărțit în 2-3 token-uri mai mici. Fiecare token e apoi transformat într-un șir de numere — modelul lucrează exclusiv cu aceste numere, niciodată direct cu litere.

## Pasul 2 — „Vectorii" de sens (embeddings)

Fiecare token e transformat într-un **vector** — practic, o listă lungă de numere (adesea sute sau mii) care reprezintă „sensul" acelui token într-un spațiu matematic. Cuvinte cu sensuri similare ajung să aibă vectori matematic apropiați — de exemplu, „pisică" și „câine" au vectori mai apropiați între ei decât „pisică" și „calculator".

Această reprezentare numerică e cea care permite modelului să „înțeleagă" relații între cuvinte, fără să aibă vreodată acces la o definiție de dicționar explicită.

## Pasul 3 — Mecanismul de atenție (attention)

Aici se află inovația centrală care a făcut posibile modelele moderne de limbaj: mecanismul de **atenție** (attention), introdus printr-o arhitectură numită **Transformer**, în 2017.

Ideea de bază: când modelul procesează un cuvânt dintr-o propoziție, „atenția" îi permite să cântărească cât de relevant e fiecare alt cuvânt din context pentru înțelegerea cuvântului curent. De exemplu, în propoziția „Robotul a evitat obstacolul pentru că îl detectase din timp", pentru a înțelege la ce se referă „îl", modelul „acordă atenție" mai mare cuvântului „obstacolul" decât altor cuvinte din propoziție.

Acest mecanism se repetă de multe ori, în „straturi" succesive, fiecare rafinând puțin mai mult înțelegerea contextuală a textului.

## Pasul 4 — Predicția următorului token

La bază, tot ce face un model de limbaj, la nivelul cel mai fundamental, este să **prezică cel mai probabil token următor**, dat fiind tot textul de până atunci. Nu „gândește" un răspuns complet dintr-o dată — îl construiește token cu token, fiecare nou token fiind ales pe baza probabilităților calculate din tot ce a fost generat până în acel moment.

Acest lucru explică multe comportamente aparent ciudate: de ce un model poate începe o propoziție într-un fel și o poate termina inconsecvent, sau de ce poate „inventa" informații care sună plauzibil (sunt statistic probabile, dar nu neapărat corecte factual).

## Pasul 5 — Antrenarea: de unde vine toată această „cunoaștere"

Înainte de a putea prezice orice, modelul trece printr-un proces de **antrenare** pe cantități uriașe de text — cărți, articole, site-uri web, cod sursă — adesea sute de miliarde de cuvinte. În timpul antrenării, modelul încearcă constant să prezică următorul cuvânt din texte reale, iar de fiecare dată când greșește, parametrii lui interni (adesea sute de miliarde de numere) sunt ajustați ușor, ca să facă o predicție mai bună data viitoare.

Acest proces se repetă de un număr astronomic de ori, până când modelul devine suficient de bun la a prezice text plauzibil, coerent, pe aproape orice subiect prezent în datele de antrenare.

## Pasul 6 — Ajustarea fină (fine-tuning) și feedback uman

Un model antrenat doar să prezică următorul cuvânt din text brut ar produce rezultate utile, dar adesea nesigure sau greu de controlat. De aceea, majoritatea sistemelor moderne trec printr-o etapă suplimentară, numită **fine-tuning** (ajustare fină), în care modelul e antrenat specific să răspundă util, sigur și în formatul unei conversații — adesea folosind feedback direct de la oameni, care evaluează și clasează răspunsurile modelului, ajutându-l să învețe ce tip de răspuns e preferat.

## De ce modelul „halucinează" uneori

Termenul „halucinație", în contextul AI, se referă la generarea de informații care sună plauzibil, dar sunt de fapt incorecte sau inventate. Acest lucru se întâmplă pentru că modelul nu are o bază de date de „fapte verificate" pe care o consultă — el generează text pe baza tiparelor statistice învățate, iar uneori tiparul cel mai probabil statistic nu corespunde cu adevărul factual.

Înțelegerea acestui mecanism explică de ce e important să verifici informații factuale importante din alte surse, mai ales pentru date specifice (cifre exacte, citate, evenimente recente).

## De ce modelul nu „își amintește" conversații anterioare (de obicei)

Majoritatea modelelor de limbaj nu au memorie persistentă între conversații separate — fiecare conversație nouă pornește „de la zero", fără nicio urmă a interacțiunilor anterioare, decât dacă sistemul respectiv oferă explicit o funcție de memorie salvată separat. În cadrul aceleiași conversații, însă, modelul „vede" tot textul anterior din acea conversație de fiecare dată când generează un răspuns nou — nu pentru că își amintește, ci pentru că acel text îi e oferit din nou, ca parte din context.

## Concluzie

Un model de limbaj mare nu gândește în sensul uman — transformă text în numere, calculează relații contextuale complexe prin mecanisme de atenție, și prezice, token cu token, cea mai probabilă continuare a unui text, bazat pe tipare învățate din cantități uriașe de date. Rezultatul poate părea remarcabil de „inteligent", dar mecanismul de bază rămâne un calcul statistic sofisticat, nu o formă de gândire sau conștiință. Înțelegerea acestui proces te ajută să folosești aceste unelte cu discernământ — apreciind ce fac excelent (generare de text coerent, sinteză de informații), fără să le atribui capacități pe care nu le au.
