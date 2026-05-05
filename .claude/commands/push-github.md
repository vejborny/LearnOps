# Push na GitHub

Proveď git commit a push aktuálních změn na GitHub podle těchto pravidel:

## Větev
Vždy commituj a pushuj na větev **master**.

## Naming convention pro commit zprávy

Formát: `<typ>: <stručný popis v češtině>`

### Typy commitů

| Typ | Kdy použít |
|-----|-----------|
| `feat` | Nová funkce nebo obsah (nová stránka, sekce, komponent) |
| `fix` | Oprava chyby (broken link, špatné zobrazení, překlep) |
| `style` | Čistě vizuální změna bez dopadu na funkcionalitu (barvy, odsazení, fonty) |
| `refactor` | Přepsání/přestrukturování kódu bez změny chování |
| `content` | Aktualizace textového obsahu, cen, dat kurzů |
| `docs` | Změna v dokumentaci (CLAUDE.md, README) |
| `chore` | Ostatní — konfigurace, soubory, které neovlivňují web |

### Pravidla

- Popis píš **malými písmeny** (kromě vlastních jmen)
- Maximálně **72 znaků** na prvním řádku
- Pokud je potřeba více kontextu, přidej prázdný řádek a pak odstavec s detaily
- Piš **česky**

### Příklady

```
feat: přidat stránku s kontaktním formulářem
fix: opravit nefunkční odkaz v navigaci
style: sjednotit padding u karet kurzů
content: aktualizovat ceny a termíny kurzů pro Q3
refactor: sloučit duplicitní CSS bloky pro sidebar
```

## Postup

1. Zkontroluj změněné soubory: `git status`
2. Projdi diff: `git diff`
3. Zastage relevantní soubory (nikdy `git add -A` slepě — vynech `.env` a jiné citlivé soubory)
4. Vytvoř commit podle naming convention výše
5. Push na master: `git push origin master`
6. Potvrď úspěch výpisem posledního commitu
