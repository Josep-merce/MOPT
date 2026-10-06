# MOPT · Raonament Lògic i Pseudocodi

Web estàtica de materials del mòdul (Cicle DAW, Institut La Mercè). Es publica amb
GitHub Pages directament des de la branca `main`: tot el que es fusiona a `main` surt a
https://josep-merce.github.io/MOPT/public_html/index.html en pocs minuts. No hi ha cap
pas de compilació ni dependències.

Hi treballem dues persones, cadascuna amb les seves sessions de Claude Code:
Josep Dominguez (`Josep-merce`) i `rsort`.

## Estructura

- `index.html` (arrel): només redirigeix a `public_html/index.html`. No cal tocar-lo.
- `public_html/index.html`: pàgina d'inici amb les targetes de cada activitat. Té els
  estils dins del mateix fitxer. **És l'únic fitxer que compartim tots dos.**
- `public_html/estils.css`: estils comuns de les pàgines d'activitat.
- AEA1 (Raonament lògic): `A0_pensar_en_condicions.html` … `A4_resolucio_de_problemes.html`.
- AEA2 (Pseudocodi): una pàgina per activitat (`a1-estructures-de-control.html`) i una
  per subactivitat (`a1-1-fonaments-sequencials.html`, `a1-2-…`).
- Tot el contingut és en català (`<html lang="ca">`).

## Targetes de l'índex: activa o desactivada

Targeta activa (enllaç):

```html
<a class="card" href="a2-arrays-i-matrius.html">
  ...
  <span class="card-foot"><span class="crit">Criteris 2.2 · 2.5</span><span class="go">2 activitats →</span></span>
</a>
```

Targeta desactivada (sense enllaç, en gris):

```html
<div class="card disabled" aria-disabled="true">
  ...
  <span class="card-foot"><span class="crit">Criteris 2.2 · 2.5</span><span class="go">Properament</span></span>
</div>
```

En reactivar-la, recupera el text original del peu («Obrir →» o «N activitats →»).

## Normes de col·laboració

1. **Una sessió per tasca, sempre des de `main` actualitzat.** Abans de començar,
   `git fetch origin main` i parteix de `origin/main`.
2. **Tot canvi passa per una pull request.** No s'empeny mai directament a `main`.
3. **Repartiment de fitxers.** Cada persona s'encarrega de les seves pàgines
   d'activitat. Si cal tocar una pàgina de l'altra persona, digues-ho a l'usuari abans.
4. **`public_html/index.html` és compartit.** Abans de canviar-hi l'estat d'una
   targeta (activa/desactivada) o l'ordre de les targetes:
   - Mira qui l'ha canviat darrerament: `git log -5 --format='%h %an %ar %s' -- public_html/index.html`.
   - Si l'altra persona ha canviat la mateixa targeta fa poc, **avisa l'usuari** abans
     de fer res: probablement desfaràs una decisió de l'altre.
   - A la descripció de la pull request, indica clarament quines targetes canvien.
5. **Claude no fusiona pull requests.** La pull request la revisa i la fusiona l'altra
   persona. Si l'usuari demana fusionar, recorda-li aquesta norma i proposa-li que avisi
   l'altra persona; només fusiona si l'usuari hi insisteix.
6. Missatges de commit i descripcions de pull request en català.
