# Comparador Nutricional de Alimentos Argentinos
Compara valores nutricionales entre productos y categorías del mercado argentino, con datos de Open Food Facts. 

**Autor:** Bruno Bracamonti




## Definición del Problema y Alcance

* **Problema:**  Dificultad para un consumidor promedio de comparar de forma rápida y estandarizada la calidad nutricional entre productos y categorías del mercado alimenticio en Argentina.

* **Solución propuesta:** Un catálogo consultable que permita buscar productos por código, seleccionar una categoría o un grupo de productos y exportar una comparación de nutrientes por cada 100 gramos.

* **Usuario y caso de uso:**  Consumidores conscientes, nutricionistas o estudiantes de ciencias de la salud que deseen analizar datos de productos locales para comparar opciones de consumo o estudiar perfiles nutricionales por categoría.

* **Pregunta guía del análisis:** ¿Cuál es la forma más eficiente de comparar valores nutricionales de alimentos que uno usualmente consume? ¿Cuáles son los más saludables? ¿Cuáles son los más nutritivos? ¿Existen diferencias significativas en los niveles promedio de valores nutricionales por cada 100g entre distintas categorías de productos del mercado argentino (por ejemplo, lácteos vs. galletitas), y cuáles son los productos con valores extremos?


* **Resultado del programa e interpretación:**  El programa procesa las fuentes de datos y genera tablas resumidas/reportes numéricos con promedios, medianas y rankings por categoría.

  

* **Alcance de la primera versión y trabajo futuro:**  
  * **Dentro del alcance:** Carga y validación de datos en formatos CSV y JSON; filtrado de productos del mercado argentino; cálculo de métricas descriptivas (promedios, máximos, mínimos) para calorías, azúcares y sodio por 100g/ml; identificación de outliers mediante expresiones regulares y validaciones numéricas.
  * **Fuera del alcance:** Interfaz gráfica web, recomendaciones nutricionales automatizadas, modelos de Machine Learning o integración en tiempo real vía API directa durante la ejecución.



## Datos y Procedencia

* **Fuente:** Database pública de [Open Food Facts](https://ar.openfoodfacts.org/) (sección Argentina).
* **Licencia:** Open Database License (ODbL).
* **Unidad de análisis:** Cada observación (fila) representa un producto alimenticio comercializado en Argentina registrado con su código de barras, categoría y composición nutricional.
* **Variables utilizadas:** 
  * `código` / `nombre_producto`: Identificador único y nombre del producto.
  * `categorias`: Categoría a la que pertenece.
  * `kcal_100g`,: Valores nutricionales por 100g/ml.
* **Limitaciones y sesgos:** Los datos son colaborativos y pueden presentar faltantes, nombres duplicados o valores erróneos/incoherentes cargados por los usuarios.



## Instalación y Ejecución

### Requisitos previos
* Python 3.10 o superior.

### Instalación
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/tu-repositorio.git](https://github.com/tu-usuario/tu-repositorio.git)
   cd tu-repositorio
