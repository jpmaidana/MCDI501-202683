# MCDI501-202683

**Estadística Computacional para la Toma de Decisiones (MCDI501)**
Magíster en Ciencia de Datos e Inteligencia Artificial, Universidad Andrés Bello (UNAB)
Periodo académico: **2026-83**

Repositorio personal de estudio y trabajo del curso: apuntes ejecutables en Jupyter,
diapositivas de apoyo, ejemplos de evaluaciones y plantillas de informe. El caso de
aplicación transversal es el dataset **Give Me Some Credit** (riesgo crediticio).

---

## Contenido

- [Estructura del repositorio](#estructura-del-repositorio)
- [Contenidos del curso](#contenidos-del-curso)
- [Evaluaciones](#evaluaciones)
- [Puesta en marcha](#puesta-en-marcha)
- [Datos](#datos)
- [Plantillas de informe](#plantillas-de-informe)
- [Convenciones](#convenciones)
- [Créditos y licencia](#créditos-y-licencia)

---

## Estructura del repositorio

| Carpeta | Qué contiene |
| --- | --- |
| [`01-apuntes/`](01-apuntes/) | Notebooks de clase, una subcarpeta por semana |
| [`02-diapositivas/`](02-diapositivas/) | PDF de apoyo por semana |
| [`03-evaluaciones/`](03-evaluaciones/) | Ejemplos y trabajo de cada evaluación (notebook + informe) |
| [`04-plantillas/`](04-plantillas/) | Plantillas de informe en LaTeX y Word |
| [`data/`](data/) | Instrucciones y ubicación del dataset |

Archivos de la raíz: [`LICENSE`](LICENSE) · [`requirements.txt`](requirements.txt) · [`.gitignore`](.gitignore)

Cada carpeta numerada responde a una pregunta distinta: *qué aprendí* (`01`),
*en qué me apoyé* (`02`), *qué entregué* (`03`) y *con qué formato* (`04`).

## Contenidos del curso

| Semana | Tema | Carpeta | Notebooks |
| --- | --- | --- | --- |
| 1 | Análisis exploratorio e inferencia | [`Semana01/`](01-apuntes/Semana01/) | Tipos de variables, visualización, tendencia central, dispersión, media, prueba *t*/*Z*, inferencia |
| 2 | Simulación, validación y remuestreo | [`Semana02/`](01-apuntes/Semana02/) | Aleatoriedad, simulación, Ley de los Grandes Números, Monte Carlo, estimación de parámetros, convergencia, datos sintéticos, bootstrap |
| 3 | Modelamiento predictivo | [`Semana03/`](01-apuntes/Semana03/) | Aprendizaje supervisado, preparación de datos, regresión lineal múltiple, diagnóstico de supuestos, regresión logística, selección de variables y comparación de modelos |

Diapositivas de apoyo: [`02-diapositivas/`](02-diapositivas/).

## Evaluaciones

| Evaluación | Fase | Ponderación | Foco | Carpeta |
| --- | --- | --- | --- | --- |
| Formativa 1 | 2 | 0 % | EDA e inferencia | [`formativa-1-eda-inferencia/`](03-evaluaciones/formativa-1-eda-inferencia/) |
| Sumativa 1 | 2 | 20 % | Análisis exploratorio e inferencial | [`sumativa-1-analisis-exploratorio-inferencial/`](03-evaluaciones/sumativa-1-analisis-exploratorio-inferencial/) |
| Formativa 2 | 3 | 0 % | Modelamiento predictivo | [`formativa-2-modelamiento-predictivo/`](03-evaluaciones/formativa-2-modelamiento-predictivo/) |
| Sumativa 2 | 3 | 20 % | Validación, simulación y remuestreo | [`Sumativa-2-validacion-simulacion-remuestreo/`](03-evaluaciones/Sumativa-2-validacion-simulacion-remuestreo/) |
| Sumativa 3 | 4 | 60 % | Modelamiento predictivo integrado | [`sumativa-3-modelamiento-predictivo-integrado/`](03-evaluaciones/sumativa-3-modelamiento-predictivo-integrado/) |

Los ejemplos incluidos corresponden a trabajos de referencia sobre *Give Me Some Credit*.
Úsalos como guía de estructura y nivel de análisis, no como base para copiar.

## Puesta en marcha

Requisitos: Python 3.10 o superior y Git.

```bash
git clone https://github.com/jpmaidana/MCDI501-202683.git
cd MCDI501-202683

python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt

jupyter lab
```

Librerías principales usadas en los notebooks: `numpy`, `pandas`, `scipy`,
`statsmodels`, `scikit-learn`, `imbalanced-learn`, `matplotlib`, `seaborn`, `joblib`.

También puedes abrir cualquier notebook en Google Colab o VS Code sin instalar nada local.

## Datos

El dataset **Give Me Some Credit** (`cs-training.csv`) se guarda en
[`data/raw/`](data/raw/). Si no está, descárgalo desde
[Kaggle — Give Me Some Credit](https://www.kaggle.com/c/GiveMeSomeCredit/data)
y déjalo como `data/raw/cs-training.csv`.

Diccionario de variables y detalles en [`data/README.md`](data/README.md).

## Plantillas de informe

Hay una plantilla por evaluación, en [LaTeX](04-plantillas/latex/) y en [Word](04-plantillas/word/).
Instrucciones detalladas de las plantillas LaTeX en
[`04-plantillas/latex/README.md`](04-plantillas/latex/README.md).

**LaTeX (recomendado: Overleaf)**
1. En Overleaf: *New Project → Upload Project*.
2. Sube `plantilla.tex` junto con el logo `logo_unab.png` (deben quedar en el mismo proyecto).
3. Completa los datos de portada y desarrolla cada sección donde dice `[Desarrollen aquí]`.

**LaTeX local**
```bash
cd 04-plantillas/latex/sumativa-1-analisis-exploratorio-inferencial
pdflatex plantilla.tex && pdflatex plantilla.tex
```

Paquetes LaTeX requeridos: `geometry`, `graphicx`, `xcolor`, `titlesec`, `fancyhdr`,
`tcolorbox`, `hyperref`, `booktabs`, `enumitem`, `array`.

## Convenciones

- **Nombres de archivo:** minúsculas, guiones, sin espacios ni tildes.
- **Notebooks:** se versionan con las salidas limpias (`nbstripout`); si se quiere conservar
  el resultado renderizado, exportar a PDF o HTML.
- **Semillas:** fijar `random_state` / `np.random.seed` para reproducibilidad.
- **Commits:** mensajes cortos en español en modo imperativo
  (`Agrega apunte de bootstrap`, `Corrige ruta de datos`).
- **Credenciales:** nada de claves ni archivos `.env` en el repositorio.

## Créditos y licencia

Material del curso MCDI501, UNAB. Las diapositivas y enunciados pertenecen a sus autores y
a la institución; el código y los apuntes propios se publican bajo la licencia
[MIT](LICENSE).

El dataset *Give Me Some Credit* pertenece a Kaggle / Credit Fusion y se rige por sus propios
términos de uso.
