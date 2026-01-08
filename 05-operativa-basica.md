- [5. Operativa Básica del IDE](#5-operativa-básica-del-ide)
  - [5.1. Edición Asistida y Refactorización](#51-edición-asistida-y-refactorización)
    - [5.1.1. Edición Asistida (IntelliSense y Sugerencias)](#511-edición-asistida-intellisense-y-sugerencias)
    - [5.1.2. Funciones Avanzadas de Edición (VS Code)](#512-funciones-avanzadas-de-edición-vs-code)
    - [5.1.3. Refactorización (Operativa JetBrains)](#513-refactorización-operativa-jetbrains)
  - [5.2. Generación de Ejecutables (Build)](#52-generación-de-ejecutables-build)
  - [5.3. Depuración (Debugging)](#53-depuración-debugging)
  - [5.4. Integración de Control de Versiones](#54-integración-de-control-de-versiones)
      - [5.4.1. Visual Studio Code (VS Code)](#541-visual-studio-code-vs-code)
      - [5.4.2. IntelliJ IDEA y JetBrains Rider](#542-intellij-idea-y-jetbrains-rider)


# 5. Operativa Básica del IDE

## 5.1. Edición Asistida y Refactorización

### 5.1.1. Edición Asistida (IntelliSense y Sugerencias)

- **IntelliSense (VS Code):** Las sugerencias aparecerán al escribir. Se pueden navegar usando las teclas `Up` y `Down`, y se aceptan con `Tab` o `Enter`. Se puede activar manualmente con **Ctrl+Space**.

> **💡 Tip:** IntelliSense funciona mejor si el archivo está bien formado. Errores de sintaxis previos pueden afectar las sugerencias.

- **Soporte CamelCase:** El filtrado de sugerencias soporta *CamelCase*, permitiendo teclear solo las letras en mayúscula de un nombre de método para limitar las sugerencias (ej. "cra" para "createApplication").

> **📝 Ejemplo CamelCase:**
> ```java
> // Escribes "cra" y IntelliSense sugiere:
> createApplication()
> createArray()
> // Porque "c" de create, "r" de Application, "a" de Application
> ```

- **Code Actions (VS Code):** El icono del "bombillo" (*lightbulb icon*) indica sugerencias de corrección rápida o refactorizaciones. Se accede mediante **Ctrl+Space**.

```mermaid
graph LR
    A[Typing] --> B[IntelliSense popup]
    B --> C[Select suggestion]
    B --> D[Ctrl+Space for more]
    D --> E[Code actions bulb]
    E --> F[Quick Fix]
    F --> G[Refactor]

    style A fill:#e1f5ff
    style B fill:#e1ffe1
    style E fill:#ffe1f5
```

### 5.1.2. Funciones Avanzadas de Edición (VS Code)

- **Búsqueda y Reemplazo:** **Ctrl+F** abre el control de Búsqueda y Reemplazo en el archivo actual. **Ctrl+Shift+F** permite buscar y reemplazar globalmente a través de todos los archivos del *workspace*.

| Atajo | Función | Alcance |
|-------|---------|---------|
| `Ctrl + F` | Buscar | Archivo actual |
| `Ctrl + H` | Reemplazar | Archivo actual |
| `Ctrl + Shift + F` | Buscar | Proyecto completo |
| `Ctrl + Shift + H` | Reemplazar | Proyecto completo |

- **Selección por Columna (*Box Selection*):** Se realiza colocando el cursor en una esquina y arrastrando mientras se mantiene pulsado **Shift+Alt**.

> **💡 Ejemplo práctico:** Añadir `//` a múltiples líneas simultáneamente
> ```
> línea 1
> línea 2
> línea 3
>     ↓ Con box selection
> // línea 1
> // línea 2
> // línea 3
> ```

- **Controles de Formato:** VS Code tiene soporte para formatear código:

| Atajo | Función |
|-------|---------|
| `Shift + Alt + F` | Format Document (todo el archivo) |
| `Ctrl + K Ctrl + F` | Format Selection (solo selección) |

**Configuraciones de formato automático:**
```json
{
    "editor.formatOnType": true,
    "editor.formatOnSave": true,
    "editor.formatOnPaste": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
}
```

- **Plegado (*Folding*):** Se pueden plegar regiones de código usando los iconos en el *gutter*. Se puede plegar la región más interna no colapsada en el cursor con **Ctrl+Shift+[** (Windows/Linux).

| Atajo | Función |
|-------|---------|
| `Ctrl + Shift + [` | Plegar región |
| `Ctrl + Shift + ]` | Desplegar región |
| `Ctrl + K Ctrl + 0` | Plegar todo |
| `Ctrl + K Ctrl + J` | Desplegar todo |

### 5.1.3. Refactorización (Operativa JetBrains)

La refactorización se invoca con **Ctrl+Alt+Shift+T**.

> **📝 Acceso rápido:** Haz clic derecho en el código → "Refactor" o usa el atajo directo si lo conoces.

- **Tipos de Refactorización (IntelliJ IDEA):** Se soportan acciones como:

| Atajo | Refactorización | Descripción |
|-------|-----------------|-------------|
| `Shift + F6` | Rename | Renombrar variable/símbolo |
| `Alt + Delete` | Safe Delete | Eliminar sin romper referencias |
| `Ctrl + Alt + M` | Extract Method | Crear método desde código |
| `Ctrl + F6` | Change Signature | Modificar firma del método |
| `Ctrl + Alt + V` | Extract Variable | Crear variable desde expresión |
| `Ctrl + Alt + C` | Extract Constant | Crear constante |
| `Ctrl + Alt + P` | Extract Parameter | Crear parámetro |

> **💡 Ejemplo Extract Method:**
> ```java
> // Antes
> double area1 = Math.PI * radius1 * radius1;
> double area2 = Math.PI * radius2 * radius2;
> 
> // Después de Extract Method
> double area1 = calculateArea(radius1);
> double area2 = calculateArea(radius2);
> 
> private static double calculateArea(double radius) {
>     return Math.PI * radius * radius;
> }
> ```

- **Previsualización:** IntelliJ IDEA permite **previsualizar los cambios** antes de aplicarlos en el diálogo *Refactoring Preview*.

> **📝 Importante:** Siempre usa la previsualización antes de refactorizaciones grandes. Así puedes ver qué archivos serán afectados.

- **Deshacer:** Se puede **deshacer la refactorización** con **Ctrl+Z**.

## 5.2. Generación de Ejecutables (Build)

El proceso de **Construcción (*Build*)** implica compilar y enlazar el código.

```mermaid
graph TD
    A[Código Fuente] --> B[Compilar]
    B --> C[Resolver dependencias]
    C --> D[Generar bytecode]
    D --> E[Ejecutable/JAR/DLL]

    B --> B1[Build incremental]
    B --> B2[Clean build]
    
    style A fill:#e1f5ff
    style E fill:#e1ffe1
```

**5.2.1. Métodos de Construcción (IntelliJ IDEA)**

- **Recompilar Archivo Único:** **Build | Recompile** (`Ctrl+Shift+F9`).

- **Construcción Incremental (*Build*):** Compila todas las clases dentro del objetivo y solo las clases que han cambiado, además de sus dependencias. Se ejecuta con **Build | Build Project** (`Ctrl+F9`). IntelliJ IDEA recomienda usar su *incremental build* para proyectos Java/Kotlin por su velocidad.

> **💡 Build incremental vs Clean:**
> - **Incremental:** Solo recompila lo que cambió (segundos)
> - **Clean:** Borra todo y recompila desde cero (minutos)

- **Reconstrucción (*Rebuild*):** Limpia el directorio de salida, elimina las cachés y construye el proyecto **desde cero**. Es útil si el *classpath* ha cambiado (ej. se añadieron/eliminaron SDKs). Se ejecuta con `Build | Rebuild Project`.

- **Compilación Automática (*Auto-build*):** Se puede configurar en `Settings | Build, Execution, Deployment | Compiler` seleccionando **Build project automatically**.

**5.2.2. Empaquetado de Artefactos JAR (IntelliJ IDEA)**

Un archivo JAR (*Java archive*) compilado es llamado un **artefacto**. Para crearlo:

1. Ir a **`File | Project Structure`** (`Ctrl+Alt+Shift+S`) y seleccionar **Artifacts**.
2. Clic en `+` → **JAR** → **From modules with dependencies**.
3. Seleccionar la clase principal (*Main Class*).
4. Para construirlo, ir a **`Build | Build Artifacts`** → **Build**. El archivo `.jar` se alojará en la carpeta `out/artifacts`.
5. **Añadir Archivos:** Se pueden añadir archivos adicionales (imágenes, configuraciones, otros JARs) al artefacto a través de la sección *Output Layout* en el diálogo *Artifacts*.

> **💡 Ejecutar el JAR:**
> ```bash
> java -jar miaplicacion.jar
> ```

## 5.3. Depuración (Debugging)

El depurador (*debugger*) interfiere con la ejecución para obtener información sobre el estado del programa y facilitar la detección y corrección de *bugs*.

> **💡 Frase célebre:** "Si debuguear es el proceso de eliminar bugs, entonces programar es el proceso de ponerlos." - Edsger Dijkstra

**5.3.1. Puntos de Ruptura (*Breakpoints*)**

- Son marcadores que indican al depurador que debe **detener la ejecución** (*suspender*) del programa.
- **Establecimiento:** En **IntelliJ IDEA**, se establece un punto de ruptura pulsando en el margen (*Gutter*) junto al número de línea; la línea queda resaltada en color rojo. En **VS Code**, se establece un *breakpoint* presionando **F9**.

| Tipo de breakpoint | Uso |
|-------------------|-----|
| **Line** | Detener en línea específica |
| **Conditional** | Detener si se cumple condición |
| **Exception** | Detener cuando lanza excepción |
| **Logpoint** | Escribir log sin detener |

**5.3.2. Ejecución Controlada y Comandos**

El depurador se utiliza para controlar la ejecución paso a paso.

| Comando | Atajo (IntelliJ) | Atajo (VS Code) | Función Principal |
| :------ | :--------------- | :-------------- | :---------------- |
| **Step Over** | `F8` | `F10` | Ejecuta línea, no entra en métodos |
| **Step Into** | `F7` | `F11` | Entra dentro del método |
| **Step Out** | `Shift + F8` | `Shift + F11` | Sale del método actual |
| **Continue** | `F9` | `F5` | Continúa hasta siguiente breakpoint |
| **Evaluate** | `Alt + F8` | - | Evalúa expresión |
| **Stop** | `Ctrl + F2` | `Shift + F5` | Termina depuración |

```mermaid
graph TD
    A[Start Debug] --> B[Hit Breakpoint]
    B --> C{¿Qué hacer?}
    C --> D[Step Over F8]
    C --> E[Step Into F7]
    C --> F[Step Out Shift+F8]
    C --> G[Continue F9]

    D --> H[Ejecuta línea actual]
    H --> B
    
    E --> I[Entra al método]
    I --> B
    
    F --> J[Sale del método]
    J --> B

    style A fill:#e1f5ff
    style B fill:#ffe1f5
    style G fill:#e1ffe1
```

**5.3.3. Ventana de Variables Locales**

- Esta ventana muestra el **nombre, tipo y valor actual** de las variables durante la suspensión.
- El depurador permite **cambiar el valor de una variable local** en esta ventana y continuar la ejecución con el nuevo valor.

> **💡 Truco de depuración:**
> ```java
> // Durante debug, puedes cambiar:
> contador = 100;  // Para probar caso límite
> nombre = "TEST"; // Para verificar lógica
> ```

## 5.4. Integración de Control de Versiones

#### 5.4.1. Visual Studio Code (VS Code)

- VS Code incluye **Source Control Management (SCM) integrado** y soporta Git *out-of-the-box*.

> **📝 Acceso:** `Ctrl+Shift+G` abre el panel de control de versiones.

- **Operaciones:** La vista de **Source Control** se abre desde la *Activity Bar*. Permite inicializar un repositorio, **preparar cambios** (*stage*) y realizar **confirmaciones** (*commits*).

```mermaid
graph LR
    A[Modified Files] --> B[Stage Changes]
    B --> C[Write Commit Message]
    C --> D[Commit]
    D --> E[Push to Remote]
    
    style A fill:#e1f5ff
    style B fill:#fff4e1
    style C fill:#ffe1f5
    style D fill:#e1ffe1
    style E fill:#f5e1ff
```

**Atajos Git VS Code:**

| Atajo | Función |
|-------|---------|
| `Ctrl + G` | Source Control |
| `Ctrl + Enter` | Commit |
| `Ctrl + Shift + P` → "git push" | Push |
| `Ctrl + Shift + P` → "git pull" | Pull |

#### 5.4.2. IntelliJ IDEA y JetBrains Rider

- **VCS Widget:** En los IDEs JetBrains, existe un *VCS widget* en la barra de herramientas que muestra la **rama actual** y ofrece acciones como actualizar, confirmar y empujar cambios.

| Atajo | Función |
|-------|---------|
| `Ctrl + K` | Commit |
| `Ctrl + T` | Update |
| `Ctrl + Shift + K` | Push |
| `Alt + BackQuote` | VCS Quick Popup |

- **Historial Local (*Local History*):** Herramienta útil en IntelliJ IDEA que muestra las distintas versiones guardadas, destacando visualmente en **color verde** los cambios que ha sufrido el código en cada versión seleccionada.

> **💡 Local History vs Git:**
> - **Local History:** Automático, guardado frecuente, solo local
> - **Git:** Manual, historial permanente, compartible
>
> Usa Local History para recover cambios no-committed. Usa Git para control de versiones real.
