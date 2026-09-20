# Bias algoritmic: de ce un sistem AI poate fi părtinitor, chiar fără intenție

Ai citit despre responsabilitatea algoritmică — cine răspunde când un sistem greșește. Aici mergem mai adânc pe un mecanism specific: cum ajunge, de fapt, un algoritm să fie părtinitor, fără ca nimeni să fi programat explicit acea discriminare.

## Ce este bias-ul algoritmic

**Bias-ul** (părtinirea) apare atunci când un sistem AI produce rezultate sistematic diferite pentru grupuri diferite de oameni, nu pe baza unor factori relevanți, ci din cauza tiparelor din datele de antrenare sau din designul sistemului. Important: acest lucru se întâmplă frecvent **fără ca vreun programator să fi intenționat discriminarea** — bias-ul apare adesea „ascuns" în date, nu în cod.

## De unde vine bias-ul, concret

### Date istorice care reflectă inegalități existente
Dacă un sistem de recrutare e antrenat pe zeci de ani de decizii de angajare istorice, iar acele decizii au favorizat, chiar și subtil, anumite grupuri, sistemul „învață" acest tipar ca fiind „normal" — nu pentru că înțelege discriminarea, ci pentru că reproduce statistic ce a văzut în date.

### Reprezentare inegală în datele de antrenare
Un sistem de recunoaștere facială antrenat predominant pe fotografii ale unui singur grup demografic va performa, de regulă, mai slab pentru grupuri sub-reprezentate în acele date — nu din cauza unei intenții, ci pentru că a „văzut" mult mai puține exemple din acel grup în timpul antrenării.

### Alegerea variabilelor măsurate
Uneori bias-ul apare din ce anume alege un sistem să măsoare ca „succes". Dacă un algoritm de evaluare medicală folosește costul istoric al tratamentului ca proxy pentru gravitatea bolii, iar anumite grupuri au avut istoric acces inegal la tratament (deci costuri mai mici, nu boală mai ușoară), sistemul poate subestima nevoile reale ale acelor grupuri.

## Un exemplu documentat, cunoscut public

Sisteme de recrutare automată folosite de companii mari au fost documentate public că penalizau CV-uri care conțineau cuvinte asociate mai frecvent cu candidate femei (de exemplu, apartenența la anumite cluburi sau activități), pentru că sistemul fusese antrenat pe date istorice de angajare dominate de candidați bărbați în acele roluri specifice. Nimeni nu a programat explicit „respinge femeile" — sistemul a „descoperit" singur acest tipar din date.

## De ce e greu de detectat

Bias-ul algoritmic nu apare de obicei ca o regulă explicită, ușor de găsit citind codul („dacă X, respinge"). E distribuit statistic, prin mii sau milioane de parametri ajustați subtil în timpul antrenării — motiv pentru care testarea riguroasă, pe grupuri diverse de utilizatori, e esențială pentru a-l descoperi, nu doar citirea codului sursă.

## Ce se poate face, practic

**Testare pe grupuri diverse** — verificarea explicită a performanței sistemului separat pentru diferite categorii demografice, nu doar performanța medie generală.

**Diversificarea datelor de antrenare** — asigurarea unei reprezentări echilibrate, nu doar cantitativ mare, ci divers distribuită.

**Auditare externă** — evaluarea sistemului de către o echipă independentă, nu doar de cei care l-au construit, reduce riscul de a rata probleme „invizibile" pentru creatori.

**Transparență asupra limitărilor** — comunicarea clară a contextelor în care sistemul a fost testat și validat, versus contexte unde performanța rămâne incertă.

## De ce nu există o soluție „completă"

Eliminarea totală a bias-ului rămâne un obiectiv dificil, parțial pentru că definițiile de „echitate" pot varia și uneori chiar intra în conflict între ele (tratament identic vs. rezultate identice, de exemplu, pot cere abordări tehnice diferite, uneori incompatibile). Nu există un consens tehnic universal despre care definiție de echitate ar trebui prioritizată în orice context.

## Concluzie

Bias-ul algoritmic nu e, de regulă, rezultatul unei intenții rău-voitoare, ci al modului în care sistemele statistice reproduc și amplifică tiparele existente în datele pe care le procesează. Înțelegerea acestui mecanism e esențială atât pentru cei care construiesc sisteme AI, cât și pentru oricine e afectat de deciziile lor — recunoașterea faptului că „algoritmul a decis" nu înseamnă automat „decizia a fost neutră sau corectă".
