
### Cuestionario de Investigación y Desarrollo (I+D)

1. **Investigación sobre la Configuración del Multi-Cursor en VS Code:**
    Visual Studio Code permite cambiar el modificador de teclado para las selecciones múltiples (*multi-cursor*) de **`Alt+Click`** (el valor predeterminado `alt`) a **`Ctrl+Click`** (usando el ajuste `ctrlCmd`). Investigue y justifique por qué un usuario que se familiariza con VS Code podría querer realizar este cambio en el ajuste `editor.multiCursorModifier`, y explique cómo el IDE resuelve automáticamente el **conflicto** para que acciones esenciales como **"Go to Definition"** y **"Open Link"** continúen funcionando sin interferir con la nueva acción de `Ctrl+Click`.

2. **Análisis de Opciones de Guardado en VS Code:**
    El ajuste `files.autoSave` en VS Code define cuándo se guardan automáticamente los archivos. Este ajuste puede tener valores como `afterDelay` (guardado tras un retraso configurado) o `onFocusChange` (guardado cuando el foco se mueve fuera del editor del archivo). Analice la diferencia entre estos dos modos y proponga una justificación de por qué un alumno principiante podría preferir la opción **`onFocusChange`** en lugar de `afterDelay` para asegurar la integridad de su código al trabajar con varios archivos a la vez.

3. **Evaluación de la Consistencia de la Interfaz JetBrains:**
    La **filosofía JetBrains** asegura un **flujo de trabajo familiar y consistente** entre IDEs como IntelliJ IDEA y Rider. Describa dos elementos de la interfaz compartidos por ambos IDEs (además del editor) y explique cómo esta uniformidad reduce la curva de aprendizaje cuando un alumno necesita cambiar de IntelliJ IDEA a Rider para trabajar en diferentes tipos de proyectos. Debe mencionar cómo se accede a la **Terminal integrada** en ambos entornos para demostrar la consistencia.

4. **Operativa de Construcción (Build) en IntelliJ IDEA:**
    IntelliJ IDEA distingue entre el comando de **Construcción Incremental** (*Build Project*, `Ctrl+F9`) y la **Reconstrucción** (*Rebuild Project*). Investigue y justifique detalladamente:
    a) ¿Cuál es el propósito del comando *Rebuild Project*?
    b) ¿En qué situación específica, relacionada con las dependencias del proyecto (SDKs o librerías), sería necesario ejecutar el comando **Reconstrucción** en lugar de una simple *Build* incremental?

5. **Generación y Distribución de Artefactos JAR:**
    Para compartir una aplicación compilada (ej. Java) con un usuario que no tiene instalado IntelliJ IDEA, el programador debe empaquetarla en un **artefacto JAR**. Describa el proceso esencial para configurar y generar este artefacto en IntelliJ IDEA (mencionando las opciones `File | Project Structure` y `Artifacts`) y explique por qué este proceso es necesario si el simple botón de ejecución (el icono *Run*) ya compila y ejecuta el código.

6. **Refactorización y la Seguridad del Código:**
    La refactorización es una herramienta de mantenimiento que no añade funcionalidad. Cuando IntelliJ IDEA encuentra problemas durante una refactorización (lo que se denomina un **conflicto**), ofrece al usuario dos opciones principales: **Refactor Anyway** o **Open in Find Window**. Investigue el propósito de cada una y explique por qué la opción **`Refactor Anyway`** implica un riesgo potencial para la estabilidad y corrección del código.

7. **Control Avanzado de Búsqueda Global en VS Code:**
    Visual Studio Code permite la **búsqueda a través de archivos** en el *workspace* (`Ctrl+Shift+F`). Esta funcionalidad puede ser filtrada usando **patrones *glob*** para incluir o excluir archivos. Explique con un ejemplo cómo el uso del patrón `**` (para coincidir con cualquier número de segmentos de ruta) en la **Vista de Búsqueda Global** funciona de manera diferente a como debe usarse en los archivos de configuración del IDE (como `files.exclude`).

8. **Optimización del Rendimiento en Instalación de Rider:**
    Durante la instalación de **JetBrains Rider** en Windows, se ofrece la opción de **"Add Rider executables to Windows Defender exclusions"** (añadir ejecutables de Rider a las exclusiones de Windows Defender). Investigue y justifique por qué esta opción es recomendada por JetBrains y qué beneficio directo en términos de **rendimiento** y **tiempo de arranque** del IDE obtiene el alumno al activarla.

9. **Gestión de la Legibilidad con Plegado de Código en VS Code:**
    La funcionalidad de **plegado de código** (*folding*) permite ocultar fragmentos de código, lo cual es útil para revisar código extenso. Describa el proceso para **plegar todas las regiones** en el editor de VS Code (`Ctrl+K Ctrl+0`) y explique cómo el IDE (por defecto) decide qué regiones se deben plegar cuando el código no tiene marcadores de región definidos explícitamente.

10. **Técnicas de Selección Múltiple en VS Code (I+D en Operativa):**
    Visual Studio Code ofrece dos métodos principales para crear selecciones de columna (*box selection*): arrastrar el cursor manteniendo pulsado **`Shift+Alt`**, o utilizando comandos de teclado específicos (`Shift+Down`, etc.). Describa cómo se ejecuta la selección por arrastre para crear un bloque vertical de texto. ¿Qué método podría ser más eficiente para un principiante que necesita seleccionar solo las primeras 5 letras de una lista de 50 líneas de texto, y por qué?.

11. **¿Visual Studio Code: IDE o Editor de código?**
    Analice y argumente si Visual Studio Code debe considerarse un **IDE completo** o simplemente un **editor de código avanzado**. En su respuesta, mencione al menos tres características que VS Code ofrece que son típicas de un IDE, y explique cómo estas características mejoran la experiencia del desarrollo en comparación con un editor de texto simple. Indique también alguna limitación que podría impedir que VS Code sea considerado un IDE completo en ciertos contextos de desarrollo.