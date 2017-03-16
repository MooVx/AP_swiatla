1) Legenda kolorów na obrazku z podgrafami.
2) W fazie 1 warunek przejœcia miêdzy S3 a S4: ((T=4s) i (Praca zwyk³a)) lub ((Praca inteligentna) i (T=4s) i (t_msg.t_S2 > 0)) 
   oznacza, ¿e po odliczeniu 4s, je¿eli system pracuje bez analizowania natê¿enia ruchu lub natê¿enie ruchu na pasach A1 lub B1 jest niezerowe,
   system nie omija nastêpnej fazy (fazy 2).
3) W fazie 1 warunek przejœcia miêdzy S3 a S5: (T=4s) i (Praca inteligentna)  i (t_msg.t_S2 == 0)
   oznacza, ¿e po odliczeniu 4s, je¿eli system analizuje natê¿enie ruchu i natê¿enie ruchu na pasach A1 oraz B1 jest zerowe,
   system omija fazê 2, a zatem wy³¹cza zielone œwiat³o dla pasów A2 i B2 w stanach S5 i S6.
4) W fazie 2 na pocz¹tku jest sprawdzana poprzednia faza; je¿eli by³a to faza 1, wtedy system za³¹cza tylko A1 i B1 na zielono, a je¿eli nie by³a to faza 1,
   to oprócz A1 i B1 zapala te¿ na zielono A2 i B2.

Changelog (Wersja 4)

- Wszystkie czasy przejœcia pomiêdzy fazami ustawione na 1s.
- Dodany nowy stan S1 na pocz¹tku fazy 4 (tak, aby zawsze by³y 2s przed w³¹czeniem siê zielonego œwiat³a dla pieszych,
  dodany sztucznie - niczego tak naprawdê nie zmienia, dodaje tylko dodatkow¹ sekundê).
- Dodane nowe stany S5 i S6 w fazie 1, na wypadek, gdyby nale¿a³oby omin¹æ fazê 2.
- Dodane nowe stany S1 i S2 w fazie 2, wyjaœnienie w pkt. 4).