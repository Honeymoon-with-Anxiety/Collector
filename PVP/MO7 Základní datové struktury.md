#programove_vybaveni_pocitacu
* důležité vlastnosti struktur
	* rychlost vyhledání prvku
	* rychlost vložení prvku
	* rychlost odstranění prvku
# Proměnné
* představuje pojmenované místo v paměti počítače
* typ proměnné
	* určuje množinu hodnot, kterých proměnná může nabývat
	* množství paměti potřebné pro její uložení.
	* operace, které lze s proměnnou provádět
* globální proměnná - vzniká při spuštění programu
* lokální proměnná - vzniká při spuštění podprogramu
* dynamická proměnná - vzniká na základě příkazu (v C++ `new`)

```cpp
int i; double k; //Deklarace
i = 7; k = 3.0; //Inicializace
int l = 4; //Deklarace s inicializací
```

* typy
	* znakové - mohou reprezentovat jednotlivé znaky; např.: `A` nebo `$`
	* celočíselné - mohou reprezentovat celá čísla; např.: `7` nebo `1024`; existují v různých velikostech a mohou být jak se znaménkem, tak bez něj
	* s plovoucí desetinou čárkou - mohou reprezentovat reálná čísla; např.: `3.14` nebo `0.01`
	* logické - obsahují vždy jeden ze dvou stavů `true` nebo `false`

| Skupina                         | Jména typů               | Poznámka                                                               |
| ------------------------------- | ------------------------ | ---------------------------------------------------------------------- |
| Znakové                         | `char`                   | Přesně jeden bajt                                                      |
| Znakové                         | `char16_t`               | Ne menší než `char`; alespoň 16 bitů                                   |
| Znakové                         | `char32_t`               | Ne menší než `char16_t`; alespoň 32 bitů                               |
| Znakové                         | `wchar_t`                | Tak velký, aby dokázal reprezentovat největší existující znakovou sadu |
| Celočíselné se znaménkem        | `signed char`            | Stejně velký jako `char`; alespoň 8 bitů                               |
| Celočíselné se znaménkem        | `signed short int`       | Ne menší než `char`; alespoň 16 bitů; `signed` je možno nepsat         |
| Celočíselné se znaménkem        | `signed int`             | Ne menší než `short`; alespoň 16 bitů; `signed` je možno nepsat        |
| Celočíselné se znaménkem        | `signed long int`        | Ne menší než `int`; alespoň 32 bitů; `signed` je možno nepsat          |
| Celočíselné se znaménkem        | `signed long long int`   | Ne menší než `long`; alespoň 64 bitů; `signed` je možno nepsat         |
| Celočíselné bez znaménka        | `unsigned char`          | Stejně velké jako obdobný typ se znaménkem                             |
| Celočíselné bez znaménka        | `unsigned short int`     | Stejně velké jako obdobný typ se znaménkem                             |
| Celočíselné bez znaménka        | `unsigned int`           | Stejně velké jako obdobný typ se znaménkem                             |
| Celočíselné bez znaménka        | `unsigned long int`      | Stejně velké jako obdobný typ se znaménkem                             |
| Celočíselné bez znaménka        | `unsigned long long int` | Stejně velké jako obdobný typ se znaménkem                             |
| S plovoucí deset. čárkou        | `float`                  |                                                                        |
| S plovoucí deset. čárkou        | `double`                 | Přesnost nejméně jako `float`                                          |
| S plovoucí deset. čárkou        | `long double`            | Přesnost nejméně jako `double`                                         |
| Logické                         | `bool`                   |                                                                        |
| Void                            | `void`                   | nulová velikost                                                        |
| Null pointer - prázdný ukazatel | `decltype(nullptr)`      |                                                                        |
# Pole
* datová struktura - kolekce elementů (hodnot či proměnných), identifikovatelných jedním nebo více indexy, ze kterých je adresa každého elementu spočitatelná; počet indexů koresponduje s dimenzí pole
	* předem stanovená velikost, prvky stejné velikosti
	* přímý přístup na prvek pomocí indexu v konstantním čase
	* vyhledání a zrušení prvku: $O(n)$ - nutné projít (posunout) celé pole
	* přidání/zrušení na začátku a na konci: $O(1)$
	* nalezení nejmenšího a největšího prvku: $O(n)$
* setříděné pole
	* vyhledání prvku v $O(log\ n)$
	* smazání prvku v $O(log\ n)$, pokud je implementováni jako označení prvku za neplatný (jinak v $O(n)$)
	* přidání prvku v $O(n)$
	* nalezení nejmenšího v $O(1)$ a největšího prvku v $O(n)$

```cpp
int a[10]; //deklarace pole a o deseti hodnotách

for(int i = 0; i < 10; i++) //ukázka naplnění pole
{
	a[i] = i;
}
```

# Struktura
* obal pro více různých proměnných s možností mít u jednotlivých proměnných různý typ

```cpp
struct ukazka //deklarace
{
	int i;
	bool b;
}
```

# [[M11 Objektově orientované programování|Objekt]]
