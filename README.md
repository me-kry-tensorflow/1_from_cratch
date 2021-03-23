# 1_from_cratch

`perception.py`

Mi egy olyan modellt fogunk hasznalni ami a tenyleges
bemeneten tul egy sajat bemenetet is hasznal (bias), ami sima
novekmeny.
https://en.wikipedia.org/wiki/Perceptron

https://vitalflux.com/wp-content/uploads/2020/10/Screenshot-2020-10-11-at-9.02.30-AM.png

* input1 OR input2 -> output1
* 0 OR 1 -> 1
* 1 OR 0 -> 1
* 1 OR 1 -> 1
* 0 OR 0 -> 0

## globalis ertekek letrehozasa

### definialj egy `learning_rate` valtozot
kell egy `learning_rate` valtozo `0.01` ertekkel

### definialj egy `bias` valtozot
kell egy `bias` valtozo `1` ertekkel

### belso weights suly tomb 
1. Hozz letre egy `weights` nevu, harom elemu tombot!
2. Toltsd fel veletlen ertekellel.
3. 1. suly az elso bemenete, 2. a masodik menete, 3. a bias-e

## `calculate` fuggveny
1. Kell egy metodus, ami az adott sulyokkal szamolva visszaadja
az adott erteket.
2. A szamolt kimenet a bementek sulyoyott osszege + a sulyozott bias 
3. Ezt a sulyozott kimenetet kell meg szurni a lepcso fuggvennyel. 
   0, ha kisebb, vagy egyenlo 0 az ertek, ha 0tol nagyobb, akkor 1

## `predict` fuggveny
1. ket parameter van: a ket szam (0 vagy 1)
2. visszateresi ertek egy szam 1 vagy 0
3. az elozo fv-t hasznalja

## `perceptron` fuggveny
Hozz létre egy fv-t, ami 3 parametert kap
* input1: elso bement
* input2: masodik bemenet
* output: kivant kimenet
* nincs visszateresi erteke

Ez a betanito fv, amivel a neuronok bementi es bias sulyait fogja hangolni.
1. Meghivja az aktualis bementekkel a `calculate` fv-t.
2. kiszamitja az elvart ertek es a kiszamolt ertek hibajat 
   (most hasznaljunk sima kulonbseget, eles kodban negyzetes kulonbseg vagy mas szokott lenni)
3. aktualis suly = error * learning_rate * amit_sulyoz


`main.py`

Hasznald az elozoleg letrehozott implementaciot!
1. Egy ciklusban hivd meg 100000 alkalommal az igazsag tablazat minden soraval
2. Hivd le a betanitott becslotol a 1 vagy 0, es a 0 vagy 0 eredmenyet


https://regi.tankonyvtar.hu/hu/tartalom/tamop425/0026_neuralis_4_4/ch01s02.html#id468279
https://hu.wikipedia.org/wiki/Mesters%C3%A9ges_neur%C3%A1lis_h%C3%A1l%C3%B3zat
https://hu.wikipedia.org/wiki/Neur%C3%A1lis_h%C3%A1l%C3%B3zat