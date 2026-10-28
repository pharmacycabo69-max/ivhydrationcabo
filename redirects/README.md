# Migración de ivhydrationcabo.com a https://www.rmcpharmacy.com

Estado: **preparado, no desplegado.** Sitio de una sola página en Vercel.

- `vercel.json`: 2 reglas 301 (cada página con y sin barra final, patrones y un comodín al final).
  `robots.txt` y `sitemap*.xml` no se redirigen a propósito (Search Console los necesita).
- `redirects/redirects-map.csv`: 0 URLs viejas con su destino y el motivo.

Destinos más usados:


Antes de publicar
1. Revisa el CSV y cambia cualquier destino que no te convenza (después regenera o edita `vercel.json`).
2. Despliega la rama y comprueba con `curl -I https://www.ivhydrationcabo.com/<ruta>`: debe dar 301 a un solo salto.
3. En Vercel → Domains, el dominio sin www no debe redirigir a otro lado antes (un solo salto).
4. Agrega la propiedad en Search Console y mantén el dominio y las redirecciones al menos 12 meses.
