# 🐍 Fundamentos de Python: Estructuras de Datos (Listas, Tuplas, Sets y Diccionarios)

Este repositorio contiene el material teórico y práctico de la píldora extendida sobre **Estructuras de Datos en Python**. Está diseñado para aprender y reforzar los pilares básicos del almacenamiento y la manipulación de colecciones de datos: listas, tuplas, sets y diccionarios.

**Autora:** Karen García

## 📂 Contenido del Repositorio

El proyecto está organizado en cuatro recursos principales que combinan teoría visual, ejemplos ejecutables y ejercicios prácticos:

1. `Presentacion_Estructuras_Datos.pdf` (Presentación)
   * Material teórico y visual de cada estructura (sintaxis, orden e indexación, duplicados y anidados, mutabilidad, dinamismo, iterables, métodos y casos de uso), la comparativa final y la regla de decisión.
2. Cuaderno Interactivo (`demo_estructuras_datos.ipynb`)
   * Jupyter Notebook con celdas de código ejecutables que ilustran paso a paso los conceptos de la presentación, incluyendo ejemplos de errores comunes (`TypeError`, `KeyError`) marcados con ⚠️ y cómo resolverlos.
3. `reto_TODO.ipynb` (Notebook del reto)
   * Jupyter Notebook con el reto **Mini Spotify** en tres niveles de dificultad. Cada ejercicio incluye enunciado, pista, resultado esperado y un hueco `# TODO: Implementar aquí` para completar el código.
4. `reto_solucion.ipynb` (Notebook de soluciones)
   * Jupyter Notebook con las soluciones comentadas paso a paso, ya ejecutadas, una guía de corrección y la tabla de qué estructura se usa en cada ejercicio y por qué.

## 📚 Temario Cubierto

### 1. Listas `[ ]`

* Creación y acceso: elementos ordenados con índices positivos (desde `0`) y negativos (desde `-1`), `len()` y `type()`.
* Mutabilidad: modificación de elementos por posición.
* Añadir elementos:
   * `.append()`: añade **un** elemento al final.
   * `.extend()`: añade **cada elemento** de otra colección por separado.
   * `.insert(posición, valor)`: inserta en una posición concreta.
* Eliminar elementos:
   * `.remove()`: elimina por **valor**.
   * `del lista[i]`: elimina por **posición**.
   * `.pop()`: quita el último elemento y lo devuelve.
* Consultar y ordenar: `.index()`, `.count()`, `in`, `.sort()`, `.reverse()` y slicing `[inicio:fin]`.
* Funciones con números: `sum()`, `max()` y `min()`.
* Listas anidadas y adelanto de iterables con `for`.

### 2. Tuplas `( )`

* Inmutabilidad: no se pueden modificar ni cambiar de tamaño (`TypeError`), lo que protege los datos.
* Creación: paréntesis, tupla de un solo elemento con coma `("a",)` y conversión con `tuple()`.
* Desempaquetado: `x, y = tupla`.
* Operaciones con números: conversión de segundos a minutos con `/`, `round()`, `//` (cociente entero) y `%` (resto).
* Métodos disponibles: solo `.index()` y `.count()`.
* Ventaja de rendimiento: ocupan menos memoria que una lista (`sys.getsizeof`).

### 3. Sets `{ }`

* Elementos únicos, sin orden y sin índices.
* Creación: `{ }` con elementos o `set()` (el set vacío **no** es `{}`, que crea un diccionario).
* Añadir y eliminar: `.add()`, `.discard()` (no da error si no existe) frente a `.remove()` (da `KeyError`).
* Caso práctico: eliminar duplicados de una lista con `list(set(...))`.
* Operaciones entre sets para comparar grupos:
   * Intersección (`&` o `.intersection()`): lo que está en ambos.
   * Unión (`|` o `.union()`): todo, sin repetir.
   * Diferencia (`-` o `.difference()`): lo que está en el primero y no en el segundo.
   * Diferencia simétrica (`^`): lo que está en uno u otro, pero no en ambos.

### 4. Diccionarios `{clave: valor}`

* Pares clave-valor con claves únicas; conservan el orden de inserción y se accede por **clave**, no por posición.
* Consulta segura: `KeyError` frente a `.get(clave, valor_por_defecto)` e `in` (busca en las claves).
* Añadir y modificar: asignación directa, `+=` / `-=`, `.update()` y `.pop()`.
* Operar con los valores: `sum(dic.values())` y `max(dic.values())`.
* Vistas: `.keys()`, `.values()` e `.items()`.
* Estructuras anidadas: diccionarios cuyos valores son listas, tuplas u otros diccionarios; se puede usar `.append()` o `set()` sobre la lista de dentro.

### 5. Elegir la estructura y coste computacional

* Regla de decisión: ¿busco por nombre? → diccionario · ¿sin repetidos? → set · ¿datos fijos? → tupla · si no → lista.
* Coste computacional: buscar con `in` en una lista recorre los elementos uno a uno, mientras que en un set o diccionario es casi instantáneo.

## 🧪 Resumen de los Ejercicios (`reto_TODO.ipynb`)

El reto **Mini Spotify** se organiza en tres niveles; cada grupo avanza hasta donde llegue:

* 🟢 **Nivel 1 · Calentamiento** (~4 min)
   * Ejercicio 1.1 (Lista): Añadir una canción, ordenar la playlist y consultar primera, última y tamaño.
   * Ejercicio 1.2 (Tupla): Desempaquetar una canción y calcular su duración en minutos.
   * Ejercicio 1.3 (Set): Obtener los artistas distintos y comprobar si un artista existe.
* 🟡 **Nivel 2 · Reto principal** (~9 min)
   * Ejercicio 2.1 (Diccionario): Actualizar y añadir reproducciones y calcular el total.
   * Ejercicio 2.2 (Diccionario de listas): Modificar y consultar las playlists de cada usuario.
   * Ejercicio 2.3 (Sets): Calcular canciones en común, exclusivas y totales entre dos usuarios con `&`, `-` y `|`.
   * Ejercicio 2.4 (Consulta segura): Usar `.get()` con valor por defecto y `max()` sobre los valores.
* 🔴 **Nivel 3 · Desafío** (extra)
   * Ejercicio 3.1 (Anidadas): Construir una ficha de canción con un diccionario que contiene una tupla.
   * Ejercicio 3.2 (Duplicados): Limpiar una cola de reproducción y contar las repeticiones eliminadas.
   * Ejercicio 3.3 (Resumen): Agrupar resultados en una tupla y desempaquetarla.
   * Ejercicio 3.4 (Razonamiento): Elegir la estructura adecuada para cuatro casos reales.

## 🚀 Cómo usar este material

1. Clona el repositorio:

```
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio
```

2. Explora el Jupyter Notebook del demo: Abre `demo_estructuras_datos.ipynb` utilizando Jupyter Notebook, JupyterLab, Visual Studio Code (con la extensión de Jupyter) o súbelo a Google Colab. Ejecuta **celda por celda** con `Shift + Enter`, en orden de arriba abajo.

3. Resuelve el reto: Abre `reto_TODO.ipynb`, completa las celdas marcadas con `# TODO: Implementar aquí` y compara con el resultado esperado de cada ejercicio.

4. Revisa las soluciones: Consulta `reto_solucion.ipynb` para comparar tu código con la solución comentada.

> ⚠️ En el notebook del demo hay celdas marcadas con ⚠️ que **dan error a propósito** para mostrar qué ocurre. Por eso no uses «Ejecutar todo» en ese notebook: se detendría en la primera de ellas.

Para abrir un notebook directamente en Google Colab: **Archivo → Abrir cuaderno → GitHub** y pega la URL del repositorio.

## 🩹 Primeros auxilios (Troubleshooting)

### Errores de Python

| Si ves... | Qué significa | Cómo solucionarlo |
|---|---|---|
| `TypeError: 'tuple' object does not support item assignment` | Las tuplas no se pueden modificar | Conviértela a lista con `list()` o crea otra tupla |
| `TypeError: 'set' object is not subscriptable` | Los sets no tienen índices | Conviértelo con `list(mi_set)` |
| `KeyError: 'clave'` | La clave no existe en el diccionario | Usa `dic.get("clave", valor_por_defecto)` |
| `KeyError` al hacer `remove` en un set | El elemento no existe | Usa `discard`, que no da error |
| `IndexError: list index out of range` | El índice es mayor que el tamaño de la lista | Comprueba el tamaño con `len()` |
| `ValueError: list.remove(x): x not in list` | Intentas quitar un valor que no está | Comprueba antes con `in` |
| `TypeError: unhashable type: 'list'` | Una lista no puede ser clave de un diccionario ni elemento de un set | Usa una tupla |
| `NameError: name '...' is not defined` | Ejecutaste una celda sin haber ejecutado antes la que crea esa variable | Ejecuta las celdas en orden desde el principio |

### Despistes habituales

| Si te pasa... | Por qué | Cómo solucionarlo |
|---|---|---|
| `{}` no crea un set | Crea un diccionario vacío | Usa `set()` |
| `("a")` no es una tupla | Son solo paréntesis | Añade la coma: `("a",)` |
| Cambias `b` y también cambia `a` | `b = a` no copia, apunta a la misma lista | Usa `b = a.copy()` |
| `append` mete una lista dentro de otra | `append` añade **un** elemento | Usa `extend` para añadir cada elemento por separado |
| `sort()` falla | La lista mezcla tipos (números y textos) | Asegúrate de que todos los elementos son del mismo tipo |
| El orden de un set cambia en cada ejecución | Los sets no tienen orden | Es normal; no dependas del orden |
| `list(set(...))` pierde el orden original | Los sets no conservan el orden | Si el orden importa, no uses un set |

### Problemas con el entorno

| Si te pasa... | Cómo solucionarlo |
|---|---|
| «Ejecutar todo» se detiene en el notebook del demo | Es normal: hay celdas ⚠️ que fallan a propósito. Ejecuta celda por celda |
| Los resultados de un ejercicio del reto no coinciden | Ejecuta todas las celdas anteriores en orden, sin saltarte ninguna |
| Ejecutaste una celda dos veces y los resultados cambian (por ejemplo, `append` añade dos veces) | En el reto, reinicia con **Kernel → Restart & Run All** (no lo uses en el demo) |
| El kernel no responde o no aparece | **Kernel → Restart**, o reinicia la sesión de Colab |
| `jupyter: command not found` | Instálalo con `pip install notebook` |
| La celda de coste computacional tarda unos segundos | Crea una lista de 5 millones de elementos; es normal |

## 📋 Requisitos

* Python 3.6 o superior (el demo usa números con guion bajo como `5_000_000`, disponibles desde esa versión).
* No requiere librerías externas; todo el código utiliza la biblioteca estándar de Python (`sys` y `time`).

## 📖 Fuentes

* Documentación oficial de Python: <https://docs.python.org/es/3/tutorial/datastructures.html>
* Curso gratuito de Python (lección de estructuras de datos) del canal de YouTube utilizado como referencia.
