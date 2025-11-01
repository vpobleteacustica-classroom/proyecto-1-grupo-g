# Hito 2: Prototipo Funcional de Sonificación Espacial (PGN a MIDI)

**Curso:** ACUS220 - Acústica Computacional con Python
**Integrantes:** Angelo Ortiz, Lorenzo Vera, Cristian Vera

---

## 1. Avances Realizados desde Hito 1

Este Hito 2 presenta un prototipo funcional avanzado, cumpliendo y expandiendo los objetivos iniciales de mapeo sonoro.

* **Implementación del Parser PGN (OE1):** Se utiliza `python-chess` para cargar una partida PGN real (`I IRT "Primavera por Equipos" 2025`) desde una cadena de texto e iterar por sus movimientos.
* **Implementación de Síntesis MIDI (OE3):** Se utiliza `mido` para generar un archivo `.mid` funcional.
* **Mapeo Sonoro Avanzado (OE2):** El prototipo implementa un sistema de "sonificación espacial":
    * **Paneo Estéreo:** La **columna** del tablero ('a'-'h') se mapea al **paneo estéreo** (Izquierda/Derecha).
    * **Octava (Tono):** La **fila** del tablero ('1'-'8') se mapea a la **octava** de la nota (sonidos más agudos al avanzar).
* **Detección de Eventos Especiales (OE2):**
    * **Enroque:** Se detecta (`is_castling`) y se sonifica con un **arpegio**.
    * **Promoción:** El código tiene la lógica para detectar (`move.promotion`) y sonificar con un **acorde mayor** (aunque no ocurre en la partida de prueba usada).
    * **Capturas y Jaques:** Se distinguen usando una *velocity* (intensidad) de nota más alta.
* **Entorno de Trabajo:** Se configuró el proyecto para operar sobre WSL (Ubuntu), gestionando las dependencias de Python con un entorno virtual (`.venv`).

---

## 2. Pendiente para Hito 3

* **Síntesis Directa a WAV (OE3):** Migrar la lógica de `mido` a síntesis directa usando `NumPy` y `SciPy`. Esto permitirá el control total del **timbre** (onda senoidal, cuadrada, etc.).
* **Personalización (OE4):** Crear una interfaz o archivo de configuración para que el usuario pueda cambiar los mapeos de sonido.
* **Evaluación (OE5):** Realizar pruebas auditivas formales del resultado.

---

## 3. Cómo Ejecutar el Prototipo

1.  **Dependencias:** Asegúrese de tener instaladas las librerías principales del proyecto.
    ```bash
    pip install python-chess mido jupyter
    ```
2.  **Ejecutar el Notebook:**
    * Abra el notebook `Hito2.ipynb`.
    * Seleccione el Kernel del entorno virtual (`.venv`).
    * Ejecute todas las celdas en orden.
    * Esto generará un archivo llamado **`partida_sonificada.mid`** en la carpeta `hito2/`.
    * Se recomienda **escuchar el archivo con audífonos** para apreciar el efecto de paneo estéreo.