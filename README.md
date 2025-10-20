## Diccionario de datos

| Nombre de la variable   | Descripción                                                                    | Valores                                   | Tipo de variable |
|-------------------------|----------------------------------------------------------------------------------|-------------------------------------------|------------------|
| ID_UNICO                | Identificador único de cada joven (CONGLOME_VIVIENDA_HOGAR_CODPERSO)            | Cadena de texto (e.g., `230001_01_002_0001`) | Identificador    |
| INFORMAL                | Indica si el joven tiene empleo informal                                        | Binario: 1 = Sí, 0 = No                   | Dependiente      |
| ingresos_jovenes        | Ingreso mensual total (dependiente o independiente) en soles en ocupación principal | Numérico (≥ 0)                             | Independiente    |
| SEXO                    | Sexo del joven                                                                   | Binario: 1 = Mujer, 0 = Hombre            | Independiente    |
| EDAD                    | Edad del joven en años cumplidos                                                | Numérico (15-29)                          | Independiente    |
| REGION                  | Región geográfica donde reside el joven                                          | Categórico: ‘Costa’, ‘Sierra’, ‘Selva’    | Independiente    |
| NIVEL_EDUCATIVO         | Nivel educativo más alto alcanzado por el joven                                  | Categórico: ‘Educación Básica’, ‘Educación Superior’ | Independiente |
| INTERNET                | Indica si el joven tiene acceso a internet                                      | Binario: 1 = Sí, 0 = No                   | Independiente    |
| mesestrab_antiguedad    | Antigüedad laboral en meses en ocupación principal                               | Numérico (> 0)                            | Independiente    |

**Codificación:** UTF-8  
**Separador:** coma `,`  
**Decimales:** punto `.`  

> *Fuente de datos:* ENAHO 2023, procesados para el análisis de informalidad laboral en jóvenes de 15 a 29 años.

