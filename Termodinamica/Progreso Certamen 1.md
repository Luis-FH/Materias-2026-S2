---
tags:
  - certamen1_termo
---

# Progreso de estudio — Certamen 1 de Termodinámica

[Certamen 1 — Contenidos y ruta](./01_Teoria_y_Conceptos/Certamen%201.md)

Marca **Estudiado** en cada apunte cuando hayas repasado la teoría y trabajado los ejercicios asociados. La tabla agrupa los prácticos de acuerdo con los temas del programa hasta el Certamen 1 (semana 9).

> [!tip] Cómo usarlo
> Activa la casilla de cada material en la propiedad **Estudiado**. El avance se calcula dando el mismo peso a cada apunte.

```base
filters:
  and:
    - file.hasTag("certamen1_termo")
    - note.seguimiento_certamen1 == true
formulas:
  avance_pct: if(note.progreso_certamen1, 100, 0)
properties:
  file.name:
    displayName: Material
  note.bloque_certamen1:
    displayName: Tema
  note.progreso_certamen1:
    displayName: Estudiado
  formula.avance_pct:
    displayName: Avance (%)
views:
  - type: table
    name: Por tema
    groupBy:
      property: bloque_certamen1
      direction: ASC
    order:
      - file.name
      - progreso_certamen1
      - formula.avance_pct
    summaries:
      formula.avance_pct: Average
  - type: table
    name: Progreso general
    order:
      - file.name
      - bloque_certamen1
      - progreso_certamen1
      - formula.avance_pct
    summaries:
      formula.avance_pct: Average
```

## Alcance según el calendario

- **Semanas 1–5:** prácticos 1–4, desde conceptos básicos hasta gas ideal y sistemas cerrados.
- **Semanas 7–8:** práctico 5, sistemas abiertos y dispositivos de flujo estacionario.
- **Semana 9:** Certamen 1.

La correspondencia se basa en los temas del programa y los títulos de los prácticos disponibles; confirma cualquier ajuste de alcance anunciado en clases.
