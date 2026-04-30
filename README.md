# Spojená tenisová liga

Webová stránka pre správu amatérskej tenisovej ligy s 3 divíziami (A/B/C),
automatickými tabuľkami, rozpisom zápasov a štatistikami.

## Súbory

- `index.html` — celá stránka v jednom súbore (HTML + CSS + JS)
- `logo.svg` — hlavné logo
- `favicon.svg` — ikona do záložky prehliadača

## Ako stránku používať lokálne

Stačí dvakrát kliknúť na `index.html` — otvorí sa v prehliadači.
Dáta sa ukladajú v prehliadači (localStorage).

> Tip: Ak chceš mať dáta zálohované, v sekcii **Admin → Dáta** klikni na
> **Export JSON**. Súbor si odlož na disk alebo do cloudu.

---

## Ako stránku publikovať na internet zadarmo (GitHub Pages)

1. **Vytvor si účet na GitHub.com** (ak ešte nemáš).
2. Klikni vpravo hore na **+** → **New repository**.
3. Pomenuj repozitár napr. `spojena-tenisova-liga`, nastav **Public**, klikni **Create repository**.
4. Na stránke nového repozitára klikni **uploading an existing file** (modrý link v strede).
5. Pretiahni do okna všetky súbory z tohto priečinka:
   - `index.html`
   - `logo.svg`
   - `favicon.svg`
6. Klikni **Commit changes**.
7. Choď do **Settings** (záložka hore) → vľavo **Pages**.
8. V sekcii *Build and deployment* nastav:
   - **Source:** *Deploy from a branch*
   - **Branch:** `main`, priečinok `/ (root)` → klikni **Save**.
9. Po 1–2 minútach sa hore objaví adresa typu:
   `https://tvoj-username.github.io/spojena-tenisova-liga/`

Túto adresu môžeš poslať hráčom — uvidia rovnakú stránku ako ty.

> Pozor: dáta sú lokálne v *tvojom* prehliadači. Ak chceš, aby všetci videli
> tie isté výsledky, môžeš si uložiť `data.json` priamo do repozitára
> (rozšírenie pre neskôr) — pre začiatok stačí, že ty ako admin
> spravuješ ligu zo svojho zariadenia.

---

## Ako pracovať so stránkou

### 1. Hráči
V **Admin → Hráči a divízie** prepíš mená demo hráčov na svojich.
Skontroluj, že počty sedia (A: 7, B: 7, C: 6).
Klikni **Uložiť zmeny**.

### 2. Pre-generuj rozpis
V **Admin → Cyklus** klikni **Pre-generovať rozpis** — vytvorí všetky
zápasy systémom „každý s každým" v rámci divízie.

### 3. Pridávanie výsledkov
V **Rozpis** klikni na zápas → vyplň gemy v setoch → **Uložiť**.
Tabuľky a štatistiky sa prepočítajú automaticky.

### 4. Po skončení cyklu
V **Admin → Cyklus** klikni **Ukončiť cyklus a aplikovať postupy**.
Posledných 2 z A padnú do B, prví 2 z B postúpia do A, atď.
Stránka automaticky vygeneruje rozpis pre nový cyklus.

---

## Bodovanie

| Výsledok | Víťaz | Porazený |
|---|---|---|
| 2:0 v setoch | **3 body** | 0 bodov |
| 2:1 v setoch | **2 body** | 1 bod |

## Pravidlá poradia pri rovnosti bodov

1. Vyšší počet bodov
2. Vzájomný zápas
3. Rozdiel setov
4. Rozdiel gemov
5. Abeceda (záložná)

## Postupy / pády po cykle

- **A divízia** → posledných 2 padá do B
- **B divízia** → prví 2 postupujú do A, posledných 2 padá do C
- **C divízia** → prví 2 postupujú do B
