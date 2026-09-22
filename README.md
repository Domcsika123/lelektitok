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
| `#/webshop` | Webshop |
| `#/gyik` | Gyakori kérdések |
| `#/kapcsolat` | Kapcsolat |

## Funkciók

- **Kosár** — a böngésző `localStorage` tárolójában marad meg (kulcs: `lelektitok_cart_v2`).
  A megrendelés gomb egy előre kitöltött e-mailt nyit meg; nincs online fizetés.
- **Kapcsolati űrlap** — szintén e-mailt állít össze, nincs mögötte kiszolgáló.
- **Animációk** — görgetésre felúszó tartalom, idézet-karusszel, hangulati fények.
  Mind kikapcsol, ha a látogató rendszerében a csökkentett mozgás be van kapcsolva.

## Arculat

| Szerep | Érték |
| --- | --- |
| Alap | `#FCFAF7` meleg elefántcsont |
| Szöveg | `#332A38` mély szilva |
| Akcent | `#8C6F9B` levendula-mauve |
| Részletek | `#B08D57` antik arany |
| Címbetű | Fraunces |
| Szövegbetű | Montserrat |

A színek és a betűtípusok a fájl elején, a `:root` blokk CSS változóiban módosíthatók.

## Teendők

- [ ] Valódi fotók behelyezése a `.frame` keretekbe (jelenleg illusztrációk, „Fotóhely" jelöléssel)
- [ ] Facebook és Instagram linkek kitöltése (jelenleg `#/kapcsolat` helyettesíti őket)
- [ ] Valódi telefonszám a helykitöltő `+36 70 123 4567` helyett
- [ ] A következő női kör időpontjainak felvétele
- [ ] Online fizetés vagy webshop-rendszer bekötése, ha szükséges
- [ ] Adatkezelési tájékoztató és impresszum oldal
