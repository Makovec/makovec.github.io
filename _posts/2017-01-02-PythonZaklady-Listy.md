---
layout: post
title:  "Python základy - listy"
date:   2017-01-02 15:35
comments: false
description: "Python základy - listy"
categories: 
    - Python
tags: 
    - Python
    - list
---

O Vánocích jsem měl trochu času, tak jsem si říkal, že se podívám na [Python](https://www.python.org/). Abych nezpomněl, co 
jsem si přečet, zakládám další kategorii zde na blogu: **Python**.


## Instalace a verze
Všude jsem četl, že doporučené je podívat se na verzi 2.x. Jelikož mi to přišlo jako ztráta času (uvidím později), skočil jsem
rovnýma nohama do verze 3.x (u mne momentálně *3.6.0b1*).

Instalaci jsem již měl jako součást nějakého předchozího experimentu, nicméně se dá stáhnout přímo z 
[Python 3.6.0](https://www.python.org/downloads/release/python-360/) stránky, kde je i návod.

Jelikož se chystám na review knihy o Pythonu, zatím jsem prolétl letem světem základy a zastavím se u listů, které mi přišly
zatím jako zajímavé.

## Rychle na listy

Pro následující příklady předpokládejme tyto proměnné:

``
 x=[1,2,3,4]
 y=['pet,'sest','sedm']
``

* Index je od nuly - žádné překvapení
* Listy jsou vlastně pole v jiných jazycích (jak je znám já)
* Velikost listu: `len(x)` je 4
* Indexovat lze i od konce: `x[-1]` je 4
* Získání části pole (slicing) lze dělat několika způsoby
  * `x[1:3]` je [2,3], protože od indexu 1(včetně) do indexu 3(bez)
  * `x[:2]` je od začátku do indexu 2(bez), tedy [1,2]
  * `x[2:]` je od indexu 2(včetně) do konce, tedy [3,4]
* Přidání na konec listu: `x[len(x):] = [5,6,7]`
* Přidání na začátek listu: `x[:0] = [-1,0]`
* Zajímavé funkce pro práci s listy: `append()`, `insert()`, `extend()`, `del()`, `remove()`

To je prozatím vše, na další zajímavosti se podívám příště.
