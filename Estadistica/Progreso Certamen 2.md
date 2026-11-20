# Progreso de estudio — Certamen 2 de Estadística

#certamen2_estadistica

Marca **Estudiado** en la tabla cuando hayas repasado el apunte y trabajado los ejercicios asociados. Los porcentajes se calculan automáticamente sobre los materiales marcados; todos tienen el mismo peso. Puedes alternar entre el resumen por tema y la lista completa desde el selector de vistas.

> [!tip] Cómo usarlo
> En la columna **Estudiado**, activa la casilla de cada material completado. Si ya estudiaste alguno, márcalo ahora para que el porcentaje refleje tu avance actual.

```base
filters:
  and:
    - file.hasTag("certamen2_estadistica")
    - note.seguimiento_certamen2 == true
formulas:
  avance_pct: if(note.progreso_certamen2, 100, 0)
properties:
  file.name:
    displayName: Material
  note.bloque_certamen2:
    displayName: Tema
  note.progreso_certamen2:
    displayName: Estudiado
  formula.avance_pct:
    displayName: Avance (%)
views:
  - type: table
    name: Por tema
    groupBy:
      property: bloque_certamen2
      direction: ASC
    order:
      - file.name
      - progreso_certamen2
      - formula.avance_pct
    summaries:
      formula.avance_pct: Average
  - type: table
    name: Progreso general
    order:
      - file.name
      - bloque_certamen2
      - progreso_certamen2
      - formula.avance_pct
    summaries:
      formula.avance_pct: Average

```

## Qué incluye el seguimiento

- **Intervalos:** apunte de la Clase 5 y solucionarios de los Listados 7 y 8.
- **Pruebas de hipótesis:** apunte de la Clase 6 y solucionario del Listado 9.
- **Regresión:** apuntes de las Clases 7 y 8 y solucionario del Listado 10.

El porcentaje global es el promedio de los ocho materiales; cada tema también muestra su propio porcentaje. Completar un solucionario significa intentar los ejercicios antes de revisar su desarrollo.
