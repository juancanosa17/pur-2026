# pur-2026

Material de estudio para la **Prueba Única de Residencias 2026** — Facultad de
Medicina, Universidad de la República (Uruguay).

Son ocho páginas HTML autocontenidas: un panel y un resumen por área del
**temario actualizado 2026**. El contenido está cifrado (AES-256-GCM) y se
descifra en el navegador con la contraseña.

**→ [juancanosa17.github.io/pur-2026](https://juancanosa17.github.io/pur-2026/)**

---

## Los documentos

### PUR 2026 · el panel

- **De un vistazo**: temas, cambios y progreso de estudio por área.
- **Temario 2026 y cambios**: los 68 temas, uno por uno, comparados con el
  temario anterior (nuevos, ampliados, modificados, movidos) y lo que salió.
- **Radiografía de los exámenes**: las 677 preguntas de PUR 2023–2025 y CIR
  2024–2026 clasificadas por área y por tema del temario 2026, y las claves
  oficiales que quedaron discutibles por guías o leyes posteriores.
- **Simulacro**: preguntas al azar (reales y nuevas), filtradas por área, con
  corrección al final, puntaje por área, revisión con explicación y enlace al
  capítulo de cada pregunta.
- **Bibliografía oficial 2026** y herramientas transversales (conversor de
  unidades al SI, clasificación KDIGO de ERC, Holliday-Segar).

### Los siete resúmenes

Medicina Familiar y Comunitaria · Medicina Interna · Ginecotocología · Cirugía ·
Pediatría · Psiquiatría · Medicina Legal y Bioética.

Cada capítulo es un tema del temario 2026 con su enunciado textual; lo que no
estaba en el temario anterior está marcado. Al final de cada capítulo hay una
autoevaluación con las preguntas reales de ese tema y preguntas nuevas del mismo
estilo (cuatro opciones, respuestas repartidas entre a, b, c y d), y la lista de
fuentes. Las cajas distinguen definiciones, recomendaciones de guía, perlas,
errores frecuentes, contenido nuevo 2026, complementos de guías externas y datos
a verificar.

El buscador (`Ctrl K`) busca en todo el sitio, no sólo en el documento abierto.

---

## Estructura del repositorio

```
index.html          la página del sitio (pide la contraseña y muestra los documentos)
data/               los documentos publicados, cifrados
tools/lock.js       regenera data/ a partir de los HTML locales
tools/sources.json  dónde están los originales en la máquina local
```

Los HTML en claro no viven acá: se arman con `contenido/build.js` fuera del
repositorio y este repositorio publica sólo el resultado cifrado.

## Publicar cambios

```bash
node ../contenido/build.js
node tools/lock.js
git add data && git commit -m "Actualiza el contenido" && git push
```
