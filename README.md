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
| `#/blog` | Blog (az első írásig egy „hamarosan” üzenettel) |
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
A logó a felfelé ívelő arany nyíl (`images/logo.jpg`). A hero teljes háttere a fény felé vezető lépcső fotója (`images/hero-lepcso.jpg`), rajta a szöveg.

A színek és a betűtípusok a fájl elején, a `:root` blokk CSS változóiban módosíthatók.

## Teendők

- [ ] Valódi termékfotók, ha elkészül a kártyacsomag és az e-book borítója — a mostani termék- és Esszencia-képek
      AI-generált hangulatképek, a valódi termék kinézete eltérhet tőlük
- [ ] Automatikus számlázás vásárlás után — ehhez valódi webshop-rendszer és számlázó (pl. Számlázz.hu, Billingo) kell
- [ ] Facebook és Instagram linkek kitöltése (jelenleg `#/kapcsolat` helyettesíti őket)
- [ ] Új e-mail-cím, ha elkészül (most: `ladicstimea@gmail.com` — a `mailto:` linkekben és a kosár / űrlap szkriptjében is)
- [ ] A Szentély (a Műhely helyszíne) megadása, ha megvan — most csak „Budapest” szerepel
- [ ] Fotók a női körökről és a mentorálásról, ha elindulnak — most Timi saját kristályfa-fotói állnak a helyükön
- [ ] A következő női kör időpontjainak felvétele
- [ ] Online fizetés vagy webshop-rendszer bekötése, ha szükséges
- [ ] Adatkezelési tájékoztató és impresszum oldal
