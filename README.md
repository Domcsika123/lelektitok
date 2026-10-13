# Lélektitok Műhely — Ladics Timi

Weboldal és webshop Ladics Timi transzformációs tréner és gyásztanácsadó számára.
Egyetlen, függőség nélküli HTML fájl: nincs build lépés, nincs csomagkezelő.

## Megnyitás

Nyisd meg az `index.html` fájlt böngészőben, vagy indíts egy helyi kiszolgálót:

```
python -m http.server 8000
```

Ezután: http://localhost:8000

## Felépítés

Egyoldalas alkalmazás hash-alapú útvonalakkal — minden útvonal külön aloldalként viselkedik,
és önállóan linkelhető:

| Útvonal | Oldal |
| --- | --- |
| `#/` | Főoldal |
| `#/rolam` | Rólam |
| `#/szolgaltatasok` | Szolgáltatások (női kör, egyéni mentorálás) |
| `#/esszencia` | Lélek Esszencia Program |
| `#/menedek` | Otthoni Lelki Menedék (webshop; a régi `#/webshop` link ide irányít) |
| `#/blog` | Blog (a bejegyzések helye, jelenleg „Hamarosan” jelöléssel) |
| `#/gyik` | Gyakori kérdések |
| `#/kapcsolat` | Kapcsolat |

## Funkciók

- **Kosár** — a böngésző `localStorage` tárolójában marad meg (kulcs: `lelektitok_cart_v2`).
  A megrendelés gomb egy előre kitöltött e-mailt nyit meg; nincs online fizetés.
- **Kapcsolati űrlap** — szintén e-mailt állít össze, nincs mögötte kiszolgáló.
- **Animációk** — visszafogottak: görgetésre felúszó tartalom és idézet-karusszel.
  Mind kikapcsol, ha a látogató rendszerében a csökkentett mozgás be van kapcsolva.

## Arculat

| Szerep | Érték |
| --- | --- |
| Alap | `#110A0D` sötét, bordós árnyalatú fekete |
| Arany | `#D4AF37` / `#C5A059` — logó, gombok, fontos címek |
| Szöveg | `#F5F5F0` pezsgőszín törtfehér |
| Kiegészítő | `#4A0E17` bársony-bordó — a gombok hover- és kijelölési színe |
| Főcímek | Cinzel |
| Alcímek, idézetek | Playfair Display |
| Szövegbetű | Montserrat |

Minimál, letisztult stílus: egyszínű felületek, vékony arany vonalak, színátmenetek, árnyékok és háttérdíszek nélkül.
A kehely-szimbólum (`images/kehely.jpg`) csak a hero-ban jelenik meg.

A színek és a betűtípusok a fájl elején, a `:root` blokk CSS változóiban módosíthatók.

## Teendők

- [ ] Új, az arculathoz illő (sötét, arany tónusú) termékfotók — a mostani képek még a régi, világos stílusban készültek
- [ ] Fotó a Meditációs Hanganyagtárhoz (jelenleg illusztráció, „Fotóhely" jelöléssel)
- [ ] Blogbejegyzések megírása és bekötése (most három „Hamarosan” kártya áll a helyükön)
- [ ] Automatikus számlázás vásárlás után — ehhez valódi webshop-rendszer és számlázó (pl. Számlázz.hu, Billingo) kell
- [ ] Facebook és Instagram linkek kitöltése (jelenleg `#/kapcsolat` helyettesíti őket)
- [ ] Valódi telefonszám a helykitöltő `+36 70 123 4567` helyett
- [ ] A következő női kör időpontjainak felvétele
- [ ] Online fizetés vagy webshop-rendszer bekötése, ha szükséges
- [ ] Adatkezelési tájékoztató és impresszum oldal
