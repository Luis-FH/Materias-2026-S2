# 🎯 Centro de Control Académico

---

## 📅 Próximos Certámenes y Evaluaciones
```dataview
TABLE 
  Mecanica AS "Materia", 
  fecha AS "Fecha de Prueba", 
  dificultad AS "Dificultad"
FROM ""
WHERE tipo = "Test" AND estado = "Pendiente"
SORT fecha ASC
```

---

## 📝 Guías y Practicos Pendientes
```dataview
TABLE 
  materia AS "Materia", 
  dificultad AS "Dificultad"
FROM ""
WHERE tipo = "Práctico" AND estado = "Pendiente"
SORT materia ASC
```

---

## 📌 Lista de Tareas Rápidas en Apuntes
```dataview
TASK
WHERE !completed
SORT file.mtime DESC
```