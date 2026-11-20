# Solucionario — Listado 1

#certamen1_estadistica

**Fuente:** [[Listado 1 523250 E y P_II_2026.pdf]]  
**Material relacionado:** [[Clase 1 - De los datos a su resumen]]

> Las frecuencias y las medidas para datos agrupados se calculan con las convenciones indicadas en cada ejercicio. Las proporciones dentro de un intervalo se estiman suponiendo distribución uniforme dentro de él.

## 1. Clasificación de variables

| Unidad estadística | Característica | Tipo de variable | Subtipo |
|---|---|---|---|
| Vivienda | Tipo de vivienda (madera, hormigón o mixta) | Cualitativa | Nominal |
| Vivienda | Número de integrantes | Cuantitativa | Discreta |
| Vivienda | Edad de cada integrante | Cuantitativa | Continua |
| Paciente | Isapre | Cualitativa | Nominal |
| Paciente | Estatura | Cuantitativa | Continua |
| Paciente | Peso | Cuantitativa | Continua |
| Paciente | Especialidad de consulta | Cualitativa | Nominal |
| Alumno PSU | Puntaje | Cuantitativa | Discreta (puntaje en puntos) |
| Alumno PSU | Preferencia de postulación a la carrera | Cualitativa | Ordinal (las preferencias tienen orden) |

Una codificación numérica no convierte por sí sola una categoría en una cantidad. En cambio, un puntaje en puntos es cuantitativo, y el número de integrantes es un conteo.

## 2. Tipo de consulta en el servicio de salud

### a) Tipo de variable

Es **cualitativa nominal**: las categorías son tipos de consulta y los códigos 1 a 5 solo las identifican.

### b) Tabla de frecuencias

Se contaron los 50 códigos de la lista. Como las categorías no tienen orden, no se interpreta una frecuencia acumulada.

| Código | Tipo de consulta | Frecuencia \(n_i\) | Frecuencia relativa \(h_i\) | Porcentaje |
|---:|---|---:|---:|---:|
| 1 | Médico general | 24 | 0,48 | 48 % |
| 2 | Nutricionista | 8 | 0,16 | 16 % |
| 3 | Ginecólogo | 6 | 0,12 | 12 % |
| 4 | Psicólogo | 3 | 0,06 | 6 % |
| 5 | Dentista | 9 | 0,18 | 18 % |
| **Total** |  | **50** | **1,00** | **100 %** |

Por ejemplo, para médico general \(h_1=24/50=0,48\).

### c) Gráficos apropiados

Un gráfico de barras conserva la identificación de cada categoría:

```text
Médico general  ████████████████████████ 24
Nutricionista   ████████                   8
Ginecólogo      ██████                     6
Psicólogo       ███                        3
Dentista        █████████                  9
                Cada █ representa 1 consulta
```

También se puede usar un gráfico circular. Los ángulos se obtienen con \(360^\circ h_i\):

| Tipo de consulta | Porcentaje | Ángulo |
|---|---:|---:|
| Médico general | 48 % | \(172,8^\circ\) |
| Nutricionista | 16 % | \(57,6^\circ\) |
| Ginecólogo | 12 % | \(43,2^\circ\) |
| Psicólogo | 6 % | \(21,6^\circ\) |
| Dentista | 18 % | \(64,8^\circ\) |

## 3. Edades de niños del jardín infantil

### a) Tipo de variable

La edad es **cuantitativa continua**, aunque las observaciones estén registradas con dos decimales.

### b) Tabla de frecuencias con cinco intervalos

Hay \(n=30\) edades, mínimo \(1,20\) años y máximo \(3,60\) años. El rango es \(3,60-1,20=2,40\); se usan cinco intervalos de amplitud \(2,40/5=0,48\) años. Para evitar solapamientos, se cierran los intervalos por la izquierda, salvo el último.

| Intervalo de edad (años) | Marca \(x_i\) | \(n_i\) | \(h_i=n_i/30\) | \(N_i\) acumulada | % acumulado |
|---|---:|---:|---:|---:|---:|
| \([1,20;\,1,68)\) | 1,44 | 2 | 0,0667 | 2 | 6,67 % |
| \([1,68;\,2,16)\) | 1,92 | 4 | 0,1333 | 6 | 20,00 % |
| \([2,16;\,2,64)\) | 2,40 | 2 | 0,0667 | 8 | 26,67 % |
| \([2,64;\,3,12)\) | 2,88 | 13 | 0,4333 | 21 | 70,00 % |
| \([3,12;\,3,60]\) | 3,36 | 9 | 0,3000 | 30 | 100,00 % |
| **Total** |  | **30** | **1,0000** |  |  |

El recuento por intervalo es, respectivamente, \(2,4,2,13,9\).

### c) Gráficos apropiados

Como los intervalos tienen igual amplitud, el histograma puede representarse con frecuencias:

```text
[1,20;1,68)  ██             2
[1,68;2,16)  ████           4
[2,16;2,64)  ██             2
[2,64;3,12)  █████████████ 13
[3,12;3,60]  █████████      9
             Cada █ representa 1 niño
```

Para el polígono de frecuencias se unen, en orden, las marcas de clase con sus frecuencias: \((1,44;2)\), \((1,92;4)\), \((2,40;2)\), \((2,88;13)\), \((3,36;9)\). Para cerrarlo sobre el eje horizontal se pueden añadir los puntos de frecuencia cero situados a media amplitud antes de la primera marca y después de la última.

## 4. Distribución de ventas de 100 vendedores

Se interpreta \(f_i\) como frecuencia relativa de la clase \(i\) y \(F_i\) como frecuencia relativa acumulada. Entonces:

- \(f_1=0,2\).
- \(F_2=f_1+f_2=0,5\), por lo que \(f_2=0,5-0,2=0,3\).
- \(f_3=0,1\), así que \(F_3=0,6\).
- \(F_5=1\) y \(F_4+F_5=1,9\), de donde \(F_4=0,9\).
- \(f_4=F_4-F_3=0,3\) y \(f_5=F_5-F_4=0,1\).

La marca de la primera clase es 75 y la amplitud es 50; por tanto, los límites de esa clase son \(75\pm25\), es decir, 50 y 100. Se expresan las ventas en miles de pesos.

| Clase | Intervalo (miles de pesos) | Marca \(x_i\) | \(f_i\) | Vendedores \(n_i=100f_i\) | \(F_i\) |
|---:|---:|---:|---:|---:|---:|
| 1 | \([50,100)\) | 75 | 0,20 | 20 | 0,20 |
| 2 | \([100,150)\) | 125 | 0,30 | 30 | 0,50 |
| 3 | \([150,200)\) | 175 | 0,10 | 10 | 0,60 |
| 4 | \([200,250)\) | 225 | 0,30 | 30 | 0,90 |
| 5 | \([250,300]\) | 275 | 0,10 | 10 | 1,00 |
| **Total** |  |  | **1,00** | **100** |  |

Los valores de los extremos describen límites de clase; el convenio exacto de inclusión de un extremo no cambia los cálculos agrupados.
