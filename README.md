# LearnOps – Web vzdělávací agentury

Statický web pro fiktivní vzdělávací agenturu **LearnOps**. Vytvořeno jako cvičný projekt – čisté HTML a CSS, žádné závislosti.

## Spuštění

Otevřete `index.html` přímo v prohlížeči, nebo použijte jednoduchý lokální server:

```bash
npx serve .
# nebo
python -m http.server 8080
```

## Struktura

```
index.html      – homepage (hero, kurzy, o nás, kontakt)
course-1.html   – podstránka IT & AI kurzů
course-2.html   – podstránka soft skills kurzů
styles.css      – sdílený stylesheet pro všechny stránky
```

## Technologie

- Čisté HTML5 + CSS3
- CSS custom properties (design tokeny)
- Responzivní layout (CSS Grid, breakpointy 900 px a 680 px)
- Žádný JavaScript, žádný build nástroj
