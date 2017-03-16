1) Legenda kolor�w na obrazku z podgrafami.
2) W fazie 1 warunek przej�cia mi�dzy S3 a S4: ((T=4s) i (Praca zwyk�a)) lub ((Praca inteligentna) i (T=4s) i (t_msg.t_S2 > 0)) 
   oznacza, �e po odliczeniu 4s, je�eli system pracuje bez analizowania nat�enia ruchu lub nat�enie ruchu na pasach A1 lub B1 jest niezerowe,
   system nie omija nast�pnej fazy (fazy 2).
3) W fazie 1 warunek przej�cia mi�dzy S3 a S5: (T=4s) i (Praca inteligentna)  i (t_msg.t_S2 == 0)
   oznacza, �e po odliczeniu 4s, je�eli system analizuje nat�enie ruchu i nat�enie ruchu na pasach A1 oraz B1 jest zerowe,
   system omija faz� 2, a zatem wy��cza zielone �wiat�o dla pas�w A2 i B2 w stanach S5 i S6.
4) W fazie 2 na pocz�tku jest sprawdzana poprzednia faza; je�eli by�a to faza 1, wtedy system za��cza tylko A1 i B1 na zielono, a je�eli nie by�a to faza 1,
   to opr�cz A1 i B1 zapala te� na zielono A2 i B2.

Changelog (Wersja 4)

- Wszystkie czasy przej�cia pomi�dzy fazami ustawione na 1s.
- Dodany nowy stan S1 na pocz�tku fazy 4 (tak, aby zawsze by�y 2s przed w��czeniem si� zielonego �wiat�a dla pieszych,
  dodany sztucznie - niczego tak naprawd� nie zmienia, dodaje tylko dodatkow� sekund�).
- Dodane nowe stany S5 i S6 w fazie 1, na wypadek, gdyby nale�a�oby omin�� faz� 2.
- Dodane nowe stany S1 i S2 w fazie 2, wyja�nienie w pkt. 4).