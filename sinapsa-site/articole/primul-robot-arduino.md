# Primul tău robot cu Arduino — pas cu pas

Nu ai nevoie de studii de inginerie ca să construiești un robot funcțional. Cu un buget de sub 150 de lei și un weekend liber, poți construi un robot mobil simplu, care evită obstacolele singur.

## Ce cumperi (lista de componente)

- 1× placă **Arduino Uno** (sau o clonă compatibilă, mai ieftină)
- 1× șasiu de robot cu 2 roți motoare (se găsește ca kit, cu tot cu motoare)
- 1× driver de motoare **L298N** (controlează motoarele)
- 1× senzor ultrasonic **HC-SR04** (detectează obstacolele)
- 1× suport pentru 4 baterii AA + baterii
- Fire de conexiune (jumper wires) tată-tată și tată-mamă

Toate aceste componente se găsesc împreună, ca „kit robot pentru începători", pe site-uri românești de electronică sau pe platforme internaționale.

## Pasul 1 — Montezi șasiul

Fixezi cele două motoare pe șasiu conform instrucțiunilor kit-ului (de obicei cu șuruburi incluse). Atașezi roțile pe axul motoarelor.

## Pasul 2 — Conectezi driverul de motoare

Driverul L298N stă între Arduino și motoare — Arduino nu poate alimenta motoarele direct, pentru că necesită mai mult curent decât poate oferi.

- Motoarele se conectează la ieșirile driverului (OUT1-OUT4)
- Driverul se conectează la Arduino pe 4 pini digitali (ex: 5, 6, 9, 10)
- Bateria alimentează driverul, nu direct Arduino

## Pasul 3 — Montezi senzorul ultrasonic

Senzorul HC-SR04 se montează în față, orientat înainte. Are 4 pini: VCC, GND, Trig, Echo — Trig și Echo se conectează la doi pini digitali de pe Arduino (ex: 7 și 8).

## Pasul 4 — Încarci codul

Codul de bază face următoarele: robotul avansează, senzorul măsoară constant distanța până la obstacol, iar când distanța scade sub un prag (ex: 15 cm), robotul oprește, dă înapoi puțin, și se rotește într-o direcție aleatorie înainte să continue.

Structura codului (simplificată, conceptual):

```
Cât timp robotul funcționează:
  Măsoară distanța cu senzorul
  Dacă distanța > 15 cm:
    Mergi înainte
  Altfel:
    Oprește
    Dă înapoi 0.5 secunde
    Rotește-te 90 de grade
```

Codul complet, în limbaj Arduino (C++), poate fi găsit ușor căutând „Arduino obstacle avoidance robot HC-SR04 L298N" — există zeci de variante open-source verificate de comunitate.

## Pasul 5 — Testezi

Pui robotul pe podea, într-o cameră cu câteva obstacole (cutii, perete). Ar trebui să se miște înainte, să detecteze obstacolele și să se rotească pentru a le evita.

## Probleme comune și soluții

- **Robotul nu se mișcă deloc** → verifică polaritatea bateriilor și conexiunile driverului
- **Motoarele se învârt în direcții greșite** → inversează firele de pe unul dintre motoare
- **Senzorul nu detectează corect** → verifică dacă pinii Trig/Echo sunt conectați corect, nu inversați

## Ce urmează

Odată ce ai robotul de bază funcțional, poți adăuga: control prin Bluetooth de pe telefon, o cameră mică pentru urmărire de linie, sau senzori suplimentari pentru navigare mai complexă. Fiecare adăugare e un pas natural următor, fără să schimbi structura de bază.
