# MOPT · Raonament Lògic i Pseudocodi

Materials interactius del mòdul de Lògica i Programació (Cicle DAW, Institut La Mercè).

Web publicada: https://josep-merce.github.io/MOPT/public_html/index.html

És una web estàtica (HTML i CSS, sense compilació). GitHub Pages la publica
automàticament des de la branca `main`: el que s'hi fusiona surt a la web en pocs minuts.

## Estructura

- `public_html/index.html`: pàgina d'inici amb les targetes de les activitats.
- `public_html/estils.css`: estils comuns de les pàgines d'activitat.
- `public_html/A0_…` – `A4_…`: activitats de l'AEA1 (Raonament lògic).
- `public_html/a0-…` – `a3-…`: activitats de l'AEA2 (Pseudocodi), amb una pàgina per
  subactivitat (`a1-1-…`, `a2-1-…`…).
- `CLAUDE.md`: instruccions que Claude Code llegeix a l'inici de cada sessió.

## Com treballem dues persones amb Claude Code

Funciona igual que amb Git local: cada canvi va en una branca i passa per una pull
request que **revisa i fusiona l'altra persona**.

| Git local | Claude Code |
|---|---|
| Crear una branca | Obrir una sessió nova (Claude crea una branca `claude/…`) |
| Fer commits | Demanar els canvis; Claude fa els commits |
| Push i obrir la pull request | Demanar-li «fes la pull request» |
| L'altre revisa i fa el merge | Igual: l'altra persona revisa i fusiona |

### Repartiment de tasques

- Cada persona s'encarrega de les seves activitats (fitxers HTML propis), així no
  toquem els mateixos fitxers.
- `public_html/index.html` és compartit: qualsevol canvi a les targetes (activar,
  desactivar, reordenar) l'ha de revisar l'altra persona abans de fusionar-lo.
- Una tasca petita = una sessió = una pull request. Són més fàcils de revisar.

### Flux de cada tasca

1. Obre una sessió nova de Claude Code sobre el repositori (parteix de `main` actualitzat).
2. Demana el canvi. Si vols veure com queda, demana-li una captura.
3. Demana «fes la pull request» (sense fusionar).
4. Avisa l'altra persona. La revisa a GitHub (o en una sessió seva de Claude:
   «revisa la PR #N») i la fusiona.
5. Un cop fusionada, GitHub publica la web. Comprova-la amb Ctrl+F5.

### Configuració recomanada a GitHub

- **Settings → General → Pull Requests → «Automatically delete head branches»**: les
  branques s'esborren soles en fusionar la pull request.
- **Watch → All activity**: rebre avisos quan l'altra persona obre una pull request.
