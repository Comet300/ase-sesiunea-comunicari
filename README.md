# Sesiunea de Comunicări Științifice — Facultatea de Marketing, ASE București

Frontend static (doar HTML), fără backend. CSS și JavaScript sunt incluse în
fiecare fișier — fără dependențe externe, fără build. Fonturi via Google Fonts,
icoane SVG inline. Imaginile sunt găzduite (preluate din designul original).

## Pornire

Ai nevoie de **Node.js 22+** — o singură dată, de la <https://nodejs.org>
(versiunea „LTS”). Apoi:

```bash
git clone https://github.com/Comet300/ase-sesiunea-comunicari.git
cd ase-sesiunea-comunicari
npm start
```

Atât: nu se instalează nimic (`npm install` nu are ce face — proiectul nu are
dependențe) și nu se construiește nimic. Site-ul se deschide la
**<http://localhost:8000>**.

Dacă portul e ocupat: `PORT=8080 npm start`.

### Fără terminal

Site-ul este numai HTML, iar legăturile dintre pagini sunt fișiere obișnuite:
**dublu clic pe `acasa.html`** îl deschide în browser, fără Node și fără nimic
altceva. Singura diferență față de `npm start` este că adresele arată
`acasa.html` în loc de `/acasa`, ca în producție.

### Cu Docker

Aceeași imagine ca în producție — nginx cu regulile din `nginx.conf`:

```bash
docker build -t ase-sesiunea-comunicari .
docker run --rm -p 8000:80 ase-sesiunea-comunicari
```

## Pagini

| Fișier | Pagină |
|---|---|
| `acasa.html` | Acasă — hero cu numărătoare inversă și calendarul evenimentului |
| `ghid-redactare.html` | Ghid de Redactare — structură IMRAD, tabele/figuri, politica AI |
| `inscriere.html` | Înscriere Lucrare — formular pe 4 pași |
| `program.html` | Program — agenda sesiunii, filtrare pe săli |

## Wiring backend

Fiecare buton/link apelează o funcție placeholder (ex. `saveDraft()`,
`submitForm()`, `joinTeams()`) marcată cu `// TODO backend`, pregătită pentru
conectarea logicii reale.
