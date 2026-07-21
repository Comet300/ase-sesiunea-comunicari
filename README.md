# Sesiunea de Comunicări Științifice — Facultatea de Marketing, ASE București

Frontend static (doar HTML), fără backend. CSS și JavaScript sunt incluse în
fiecare fișier — fără dependențe externe, fără build. Fonturi via Google Fonts,
icoane SVG inline. Imaginile sunt găzduite (preluate din designul original).

## Pagini

| Fișier | Pagină |
|---|---|
| `acasa.html` | Acasă — hero cu numărătoare inversă și calendarul evenimentului |
| `ghid-redactare.html` | Ghid de Redactare — structură IMRAD, tabele/figuri, politica AI |
| `inscriere.html` | Înscriere Lucrare — formular pe 4 pași |
| `program.html` | Program — agenda sesiunii, filtrare pe săli |

## Rulare

Orice server static, ex:

```bash
python3 -m http.server 8000
# apoi deschide http://localhost:8000/acasa.html
```

## Wiring backend

Fiecare buton/link apelează o funcție placeholder (ex. `saveDraft()`,
`submitForm()`, `joinTeams()`) marcată cu `// TODO backend`, pregătită pentru
conectarea logicii reale.
