# Análisis de la pobreza en el Perú en 2022: ingresos e informalidad
## 1. Introducción
El proyecto “Análisis de la pobreza en el Perú por el nivel de ingresos e informalidad” evalúa la pobreza en los hogares peruanos durante 2022 utilizando datos de la ENAHO del INEI. A través del análisis de más de 87,000 registros con Python, se identifican disparidades de ingresos, patrones de informalidad laboral y diferencias clave entre áreas urbanas y rurales. Este proyecto incluye limpieza de datos, creación de variables como "estado de pobreza", y visualizaciones que destacan la relación entre ingresos, informalidad y pobreza, ofreciendo insights para orientar políticas públicas.
## Proyecto en GitHub
Explora el proyecto completo en este enlace: [ProyectoPobrezaPeru.ipynb](https://github.com/WLozanoH/PovertyAnalysisPeru2022/blob/main/ProyectoPobrezaPeru.ipynb).
### 2. Resultados destacados:
- 38% de los hogares rurales son pobres, en comparación con el 17% en zonas urbanas.
- La desigualdad económica (Índice de Gini: 0.45) destaca como un desafío clave.
- Un mayor ingreso y la formalidad laboral reducen significativamente la probabilidad de pobreza.
  
![Gráfico de la tasa de pobreza por Ingresos promedio e informalidad](tasas%20de%20pobreza.png)

El gráfico de la tasa de pobreza en función de los ingresos promedio e informalidad muestra cómo la pobreza está fuertemente vinculada a los niveles de ingreso. También resalta que los trabajos formales tienden a proporcionar ingresos más altos, lo que destaca la importancia de políticas que promuevan la formalización laboral

## Objetivo

Evaluar la relación entre los ingresos, la informalidad laboral y la probabilidad de pobreza en los hogares peruanos, identificando disparidades económicas regionales y proponiendo estrategias para su mitigación.

## Hipótesis

* H0: El ingreso total no afecta la probabilidad de que un hogar sea clasificado como pobre.
* H1: Un mayor ingreso total reduce la probabilidad de que un hogar sea clasificado como pobre.

## Datos utilizados

### Origen:

* Encuesta Nacional de Hogares (ENAHO) del Instituto Nacional de Estadística e Informática (INEI) de Perú.

* [Descargar datos oficiales](https://www.datosabiertos.gob.pe/dataset/encuesta-nacional-de-hogares-enaho-2022-instituto-nacional-de-estad%C3%ADstica-e-inform%C3%A1tica-%E2%80%93)

## Módulos empleados:

* Módulo de ingresos y empleo (Enaho01a-2022-500)

El archivo principal analizado está disponible en este repositorio: [dataPobrezaPeru2022.csv](https://github.com/WLozanoH/PovertyAnalysisPeru2022/blob/main/dataPobrezaPeru2022.csv) (contiene datos limpios para análisis)

## 3. Metodología

### Limpieza de datos
1. 🧹 **Estandarización**:
   - Renombrado de columnas para facilitar su interpretación.
   - Creación de diccionarios para mapear variables categóricas.
2. 🛠️ **Manejo de valores nulos**:
   - Imputación de variables numéricas usando la mediana por conglomerado.
   - Imputación de variables categóricas usando la moda.
3. 🗑️ **Tratamiento de valores atípicos**:
   - Eliminación de outliers utilizando el rango intercuartil (IQR).
4. 🔍 **Eliminación de duplicados**:
   - Remoción de registros duplicados.
 
## 5. Exploración de datos (EDA)

1. Distribución de ingresos:

* Asimetría positiva con concentración de ingresos bajos.

* Densidad de ingresos significativamente más alta en áreas rurales.

2. Relación entre variables:

* Correlación negativa fuerte entre ingresos y pobreza (-0.56).

* La formalidad laboral presenta una correlación moderada con menores probabilidades de pobreza (-0.39).

3. Visualizaciones:

* Histogramas y boxplots para analizar la distribución de ingresos por dominio geográfico.

* Gráficos de barras para examinar las tasas de pobreza en zonas urbanas y rurales.

## 6. Resultados clave

**Regresión logística** **-0.027**
  * Aumentar ingresos reduce la probabilidad de pobreza (-0.027).

**Tasa de pobreza rural**: **38%**

**Tasa de pobreza urbana**: **17%**

**Índice de Gini**: **0.45**
  * (desigualdad moderada-alta)

**F-estadistic**: **7597**
**p-Value:**: **0.0** 

![Proporción de Hogares en Pobreza por Zona: rural y urbano](pobreza_por_zonas.png)
El gráfico de "Proporción de Hogares en Pobreza por Zona: rural y urbano" refleja una disparidad significativa en la pobreza entre las zonas rurales y urbanas en el Perú. Las áreas rurales tienen una tasa de pobreza mucho más alta, lo que sugiere que los hogares rurales enfrentan mayores desafíos económicos en comparación con los urbanos.

### Resumen: Resultados

```plaintext
| Aspecto Analizado               | Resultado Principal                                                            |  Indicador Clave                   |
|---------------------------------|--------------------------------------------------------------------------------|------------------------------------|
| Tasa de pobreza general         | 29% de los hogares son clasificados como pobres                                | Estado de pobreza                  |
| Tasa de pobreza rural           | 38% de los hogares rurales son pobres                                          | Zona: Rural                        |
| Tasa de pobreza urbana          | 17% de los hogares urbanos son pobres                                          | Zona: Urbana                       |
| Efecto de los ingresos          | Un incremento en ingresos reduce significativamente la probabilidad de pobreza | Regresión logística: coef = -0.027 |
| Desigualdad de ingresos         | Alta desigualdad económica (Índice de Gini)                                    | Índice de Gini: 0.45               |
| Disparidad entre percentiles    | Los ingresos del percentil 90 son 12 veces mayores que los del percentil 10    | P90/P10 Ratio: 12                  |

```
## 7. Recomendaciones:
1. Formalización laboral
   - Simplificar el registro en la seguridad social.
   - Incentivar la formalización en sectores rurales clave.

Ejemplo: **"MiPrimerEmpleo" en Colombia**

* Descripción: Este programa otorgó incentivos fiscales a empresas que contrataran jóvenes como su primer empleo formal. La medida redujo las tasas de informalidad entre jóvenes recién egresados y mejoró sus ingresos.
* Impacto: Disminución de la informalidad juvenil y aumento de ingresos promedio en jóvenes de sectores vulnerables.

2. Reducir la desigualdad
   - Diseñar programas redistributivos como transferencias condicionadas.
   - Incrementar la inversión en educación y capacitación laboral.

Ejemplo: **"Bolsa Familia" en Brasil**

* Descripción: Un programa de transferencias condicionadas de dinero a hogares en situación de pobreza. Las familias recibían apoyo económico si cumplían condiciones como la asistencia escolar y la vacunación de sus hijos.
* Impacto: Redujo significativamente la pobreza extrema en zonas rurales y urbanas, y mejoró indicadores de salud y educación.
    
## 8. Conclusión

* El análisis realizado utiliza regresión logística, que es una técnica estadística que nos permite entender la relación entre variables. En este caso, el modelo muestra cómo el ingreso total de un hogar influye en la probabilidad de ser pobre. El coeficiente negativo de -0.027 indica que, a medida que el ingreso total de un hogar aumenta, la probabilidad de que este hogar sea clasificado como pobre disminuye. En otras palabras, a mayor ingreso, menor es la probabilidad de pobreza.

* Además, el p-valor asociado es menor a 0.05, lo que significa que los resultados son estadísticamente significativos. Esto confirma que la relación entre el ingreso y la pobreza observada no es producto del azar, sino que es una relación real.

## Estructura del repositorio
El proyecto está organizado de la siguiente manera:

```plaintext
|-- data
|   |-- Enaho01a-2022-500.csv  # Datos originales
|-- scripts
|   |-- analisis.py            # Limpieza y análisis
|-- outputs
|   |-- visualizaciones/       # Gráficos y resultados
|-- README.md                  # Documentación del proyecto
```

- **data/**: Contiene los datos originales utilizados en el análisis.
- **scripts/**: Incluye el código de limpieza y análisis de datos.
- **outputs/**: Carpeta para guardar las visualizaciones y resultados.
- **README.md**: Archivo con la documentación del proyecto.

## Tecnologías utilizadas

* Python: Limpieza, análisis y visualización de datos (Pandas, NumPy, Matplotlib, Seaborn).

* GitHub: Documentación y publicación del proyecto.

## Cómo usar este repositorio

1.- Clona este repositorio:
 * git clone https://github.com/tu_usuario/analisis-pobreza-peru-2022.git

2.- Instala las dependencias necesarias:
 * pip install -r [requirements.txt](https://github.com/WLozanoH/PovertyAnalysisPeru2022/blob/main/requirements.txt)

3.- Ejecuta el script de análisis:
 * python scripts/analisis.py

### Contribuciones

Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, abre un pull request o contacta al autor.

### Autor

Wilmer Gastón Lozano Huamán

Correo: wglozanoh@gmail.com
