# TP1 - Ejercicio 3: Análisis de Ventas del Supermercado de Don Francisco

## 📘 Consigna

Don Francisco es un pequeño comerciante de barrio que posee un supermercado, con el que sostiene a su familia.
Uno de sus hijos, Matías, quien recién comienza a cursar la Especialización en Inteligencia Artificial del LSE de la UBA, le propone hacer un análisis de las ventas durante el año anterior, con el fin de realizar pronósticos para el año siguiente, lo que a Don Francisco le parece una buena idea.

Don Francisco le entrega a Matías el cuaderno donde tiene registrado el valor total de sus ventas en cada día del año.
Con esta información, Matías construye una tabla en la cual la primera columna corresponde a la fecha y la segunda al monto de las ventas, expresado en dólares para evitar complicaciones con la inflación.

Matías no se siente muy seguro de la tarea a realizar, así que les pide ayuda a ustedes para abordar el problema.
A partir del archivo de datos correspondiente a su grupo, determinar una **función empírica de distribución** y una **aproximación a la función de densidad** de las ventas del supermercado de Don Francisco para cada año de registro (**2021**, **2022** y **2023**).

---

## 📊 Contenido del notebook

El notebook [`TP1_Analisis_Ventas.ipynb`](https://github.com/emiliano-ipa/CEIA-PEIA-TP1-3/blob/main/notebooks/TP1_Analisis_Ventas.ipynb) contiene:

### 1. Carga y exploración de los datos
- Archivo fuente: `Datos_primer_TP_20Co2025_a2010.xlsx`
- Se descompone la variable `Fecha` para extraer el `Año`
- Se valida que existan 365 registros por año

### 2. Estadísticos descriptivos por año
Se calculan los siguientes valores para cada año:
- Mínimo y máximo
- Media y mediana
- Desvío estándar
- Cuartiles

### 3. Visualizaciones
- **Función de densidad (KDE)**: muestra la distribución estimada de las ventas diarias.
- **Función empírica de distribución (ECDF)**: representa la acumulación de probabilidad.

---

## 📌 Conclusiones

### Análisis general

Las ventas diarias del supermercado presentan una distribución relativamente estable en los tres años analizados, con un patrón de comportamiento que sugiere una operación constante y predecible. Las medianas anuales se mantienen entre **18.800 y 19.000 USD**, con un rango de valores mínimos y máximos que no muestra saltos abruptos ni presencia de valores extremos significativos.

---

### Función empírica de distribución (ECDF)

- La ECDF permite visualizar cómo se acumula la frecuencia relativa de ventas a medida que aumenta el monto.
- En los tres años, la pendiente de la ECDF se muestra suave y continua, lo que indica una distribución amplia sin acumulaciones abruptas.
- Las curvas se superponen en gran parte, lo que refuerza la hipótesis de estabilidad interanual.
- Aproximadamente el **50% de los días** registraron ventas por debajo de los **19.000 USD**, lo que coincide con la mediana.
- Alrededor del **80% de las ventas** están concentradas entre **16.000 y 22.000 USD** según la forma de la ECDF.

---

### Función de densidad (KDE)

- La KDE suaviza la distribución observada y permite ver los modos (picos) en la frecuencia de ventas.
- Se observa una leve asimetría a la izquierda en algunos años, con una cola extendida hacia menores valores de ventas.
- Los máximos de densidad se ubican en torno a los **18.500–19.000 USD**, lo que refuerza el rol de ese rango como valor típico.
- La dispersión se mantiene moderada, lo que sugiere un comportamiento comercial estable sin grandes fluctuaciones.

---

### Consideraciones para el pronóstico de 2024

- La estabilidad en las distribuciones sugiere que es razonable asumir que el patrón de ventas puede mantenerse en el corto plazo.
- La función empírica puede ser útil para estimar probabilidades (por ejemplo: ¿cuál es la probabilidad de que un día se vendan menos de 17.000 USD?).
- La densidad estimada es útil para identificar rangos de mayor frecuencia esperada, ideal para establecer umbrales de control.
- La información está expresada en dólares, lo que facilita la proyección sin necesidad de ajustes por inflación.

---

## ⚙️ Ejecución del proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/emiliano-ipa/CEIA-PEIA-TP1-3.git
cd CEIA-PEIA-TP1-3
```
### 2. Crear entorno virtual

```bash
python -m venv CEIA-UBA-PEIA
```

### 3. Activar entorno virtual

- En Windows:
  ```bash
  .\CEIA-UBA-PEIA\Scripts\activate
  ```

- En Linux/Mac:
  ```bash
  source CEIA-UBA-PEIA/bin/activate
  ```

### 4. Instalar dependencias

```bash
pip install -r requirements.txt
```
### 5. Ejecutar el notebook

Abrir el archivo `notebooks/TP1_Analisis_Ventas.ipynb` con Jupyter o VS Code y correr las celdas.

---

## 🧾 Créditos

**Autor:** Emiliano Iparraguirre  
**Asignatura:** Probabilidad y Estadística para Inteligencia Artificial (PEIA)  
**Programa:** Especialización en Inteligencia Artificial (CEIA)  
**Institución:** Universidad de Buenos Aires (UBA)