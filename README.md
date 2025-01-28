# Análisis de la pobreza en el Perú en 2022: ingresos e informalidad

## 1. Proyecto en GitHub
Explora el proyecto completo en este enlace: [ProyectoPobrezaPeru.ipynb](https://github.com/WLozanoH/PovertyAnalysisPeru2022/blob/main/ProyectoPobrezaPeru.ipynb).
### 2. Resultados destacados:
- 38% de los hogares rurales son pobres, en comparación con el 17% en zonas urbanas.
- La desigualdad económica (Índice de Gini: 0.45) destaca como un desafío clave.
- Un mayor ingreso y la formalidad laboral reducen significativamente la probabilidad de pobreza.

## Descripción del proyecto

Este proyecto evalúa la pobreza en los hogares peruanos durante 2022 utilizando datos de la Encuesta Nacional de Hogares (ENAHO) del Instituto Nacional de Estadística e Informática (INEI). Se analiza cómo los ingresos y la informalidad laboral influyen en la probabilidad de pobreza en diferentes regiones del país, con un enfoque en las diferencias entre áreas rurales y urbanas.

Se procesaron más de 87,000 registros utilizando Python para limpiar, analizar y visualizar los datos, generando insights clave para orientar políticas públicas.

## Objetivo

Evaluar la relación entre los ingresos, la informalidad laboral y la probabilidad de pobreza en los hogares peruanos, identificando disparidades económicas regionales y proponiendo estrategias para su mitigación.

## Hipótesis

Un aumento en los ingresos y la formalidad laboral disminuye significativamente la probabilidad de pobreza.

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

## 6. Métodos estadísticos avanzados

1. Regresión Logística:

*  Relación entre ingreso_total, es_formal y es_pobre.

#### 7. Resultados:

 1. Regresión logística:
  * Aumentar ingresos reduce la probabilidad de pobreza (-0.027).

  * La formalidad laboral tiene un efecto protector significativo (-1.083).

2. Índice de Gini:

* Valor: 0.45 (desigualdad moderada-alta).

3. Análisis de varianza (ANOVA):

Diferencias significativas entre ingresos en zonas urbanas y rurales (p-value = 0.0).

## Resultados clave

**Tasa de pobreza rural**: **38%**  
**Tasa de pobreza urbana**: **17%**  
**Índice de Gini**: **0.45** 

## Recomendaciones

1. Promover la formalización laboral:

* Simplificar el registro en la seguridad social.

* Incentivar la formalización en sectores rurales clave.

2. Reducir la desigualdad:

* Diseñar programas redistributivos como transferencias condicionadas.

* Incrementar la inversión en educación y capacitación laboral.

3. Fomentar el desarrollo rural:

* Invertir en infraestructura y conectividad para mejorar el acceso al mercado.

* Estimular la inversión privada en zonas rurales.

4. Ampliar el acceso a créditos:

* Fomentar programas de microcréditos para pequeños emprendedores.

5. Mejorar la educación:

* Implementar capacitaciones laborales enfocadas en habilidades técnicas.

## Tecnologías utilizadas

* Python: Limpieza, análisis y visualización de datos (Pandas, NumPy, Matplotlib, Seaborn).

* GitHub: Documentación y publicación del proyecto.

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


## Resumen: Resultados

```plaintext
| **Aspecto Analizado**         | **Resultado Principal**                                                        | **Indicador Clave**             |
|--------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| **Tasa de pobreza general**    | 29% de los hogares son clasificados como pobres                                | Estado de pobreza              |
| **Tasa de pobreza rural**      | 38% de los hogares rurales son pobres                                          | Zona: Rural                    |
| **Tasa de pobreza urbana**     | 17% de los hogares urbanos son pobres                                          | Zona: Urbana                   |
| **Efecto de los ingresos**     | Un incremento en ingresos reduce significativamente la probabilidad de pobreza | Regresión logística: coef = -0.027 |
| **Desigualdad de ingresos**    | Alta desigualdad económica (Índice de Gini)                                    | Índice de Gini: 0.45           |
| **Disparidad entre percentiles** | Los ingresos del percentil 90 son 12 veces mayores que los del percentil 10    | P90/P10 Ratio: 12              |
```
## Recomendaciones:
1. Formalización laboral
   - Simplificar el registro en la seguridad social.
   - Incentivar la formalización en sectores rurales clave.

2. Reducir la desigualdad
   - Diseñar programas redistributivos como transferencias condicionadas.
   - Incrementar la inversión en educación y capacitación laboral.

## Conclusión
Este proyecto destaca cómo la pobreza en el Perú está influenciada por factores económicos como los ingresos y la formalidad laboral. Al abordar las disparidades rurales y urbanas, y proponer recomendaciones prácticas, se establece una base sólida para diseñar políticas públicas orientadas a reducir la pobreza y fomentar la igualdad económica.
"Este análisis puede servir como base para decisiones informadas que impacten directamente en la reducción de la pobreza en el Perú"

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
