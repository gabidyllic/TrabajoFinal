#Abrimos la base de datos:
data_jovenes <- read.csv("https://docs.google.com/spreadsheets/d/e/2PACX-1vRBN3XyUbtmb31zRlbsKyaBcWOi0WIz6U2k5IRWZ5ky5SW9w-8W66RyiTGypUZpinACmOfZ9McC2xop/pub?output=csv")

# Diccionario de datos para el análisis de informalidad laboral en jóvenes peruanos

# Cargar paquetes necesarios
library(knitr)
library(kableExtra)
library(dplyr)

# Crear el diccionario de datos como un data frame
diccionario <- data.frame(
  `Nombre de la Variable` = c("ID_UNICO", "INFORMAL", "ingresos_jovenes", "SEXO", "EDAD", 
                             "REGION", "NIVEL_EDUCATIVO", "INTERNET", "mesestrab_antiguedad"),
  Descripción = c(
    "Identificador único de cada joven (CONGLOME_VIVIENDA_HOGAR_CODPERSO)",
    "Indica si el joven tiene empleo informal",
    "Ingreso mensual total (dependiente o independiente) en soles en ocupación principal",
    "Sexo del joven",
    "Edad del joven en años cumplidos",
    "Región geográfica donde reside el joven",
    "Nivel educativo más alto alcanzado por el joven",
    "Indica si el joven tiene acceso a internet",
    "Antigüedad laboral en meses en ocupación principal"
  ),
  Valores = c(
    "Cadena de texto (e.g., '230001_01_002_0001')",
    "Binario: 1 = Sí, 0 = No",
    "Numérico (≥ 0)",
    "Binario: 1 = Mujer, 0 = Hombre",
    "Numérico (15-29)",
    "Categórico: 'Costa', 'Sierra', 'Selva'",
    "Categórico: 'Educación Básica', 'Educación Superior'",
    "Binario: 1 = Sí, 0 = No",
    "Numérico (> 0)"
  ),
  `Tipo de Variable` = c(
    "Identificador",
    "Dependiente",
    "Independiente",
    "Independiente",
    "Independiente",
    "Independiente",
    "Independiente",
    "Independiente",
    "Independiente"
  )
)

# Generar la tabla del diccionario de datos con diseño mejorado
diccionario %>%
  kbl(
    caption = "Diccionario de datos para el análisis de informalidad laboral",
    align = c("l", "l", "l", "l"),
    col.names = c("Nombre de la variable", "Descripción", "Valores", "Tipo de variable")
  ) %>%
  kable_classic(full_width = FALSE, html_font = "Georgia", font_size = 15) %>%
  row_spec(0, bold = TRUE, color = "white", background = "#2C3E50", font_size = 16) %>%
  column_spec(1, bold = TRUE, color = "#34495E", background = "#ECF0F1") %>%
  column_spec(2:4, background = "#F7F9F9") %>%
  kable_styling(
    bootstrap_options = c("striped", "hover", "condensed"),
    stripe_color = "#DDE4E6",
    latex_options = c("striped", "hold_position"),
    position = "center"
  ) %>%
  footnote(
    general = "Nota: Datos provenientes de la ENAHO 2023, procesados para el análisis de informalidad laboral en jóvenes de 15 a 29 años.",
    general_title = "",
    footnote_as_chunk = TRUE
  )
