---
tags:
  - certamen2_termo
---

# Progreso de estudio — Certamen 2 de Termodinámica

[Certamen 2 — Contenidos y ruta](./01_Teoria_y_Conceptos/Certamen%202.md)

Marca **Estudiado** cuando hayas repasado cada apunte y trabajado los ejercicios asociados. Esta vista incluye los prácticos 6–8 que están disponibles en la carpeta; no representa por sí sola todo el temario indicado para el Certamen 2.

> [!tip] Cómo usarlo
> Activa la casilla de cada material en la propiedad **Estudiado**. El avance se calcula dando el mismo peso a cada apunte listado.

```base
filters:
  and:
    - file.hasTag("certamen2_termo")
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

## Alcance según el calendario

- **Semanas 10–11:** Segunda Ley y refrigeradores — prácticos 6 y 7.
- **Semanas 13–14:** entropía y flujo de entropía — práctico 8.
- **Semanas 15–16:** ciclo Rankine y motores recíprocos/turbina de gas — sin práctico específico disponible en la carpeta.
- **Semana 17:** Certamen 2.

La correspondencia entre prácticos y semanas se basa en los temas del programa y el contenido de los archivos disponibles. Añade al seguimiento los apuntes de Rankine y máquinas térmicas cuando estén disponibles.
