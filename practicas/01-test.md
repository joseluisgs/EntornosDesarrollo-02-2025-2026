## Cuestionario Tipo Test: Evaluación de Entornos Integrados de Desarrollo

**Instrucciones:** Lea atentamente cada pregunta y seleccione la opción que considere correcta, basándose únicamente en el material de estudio.

### I. Fundamentos y Componentes del IDE

1. ¿Cuál es la fase del ciclo de vida del software donde se utilizan fundamentalmente los entornos de desarrollo (IDE)?
    a) Fase de análisis
    b) Fase de codificación
    c) Fase de explotación
    d) Fase de diseño

2. ¿Cuál de los siguientes no es un componente esencial de un Entorno Integrado de Desarrollo (IDE)?
    a) Editor de texto
    b) Compilador/Intérprete
    c) Constructor de interfaz gráfica
    d) Archivo `.jar`

3. ¿Qué componente de un IDE se encarga de traducir el código fuente a código máquina línea a línea, siendo generalmente más lento que el compilador?
    a) Depurador
    b) Enlazador
    c) Intérprete
    d) Analizador léxico

4. ¿Cuál es la principal función del depurador (*debugger*) en un IDE?
    a) Traducir el código a código binario.
    b) Crear el archivo ejecutable final (artefacto).
    c) Probar y eliminar posibles errores en un programa.
    d) Administrar la configuración del usuario.

5. En el editor de código, ¿qué herramienta de análisis de código se encarga de corregir si se ha escrito mal alguna palabra?
    a) Analizador sintáctico
    b) Analizador léxico
    c) Depurador
    d) Generador de artefactos

### II. Instalación y Requisitos

6. ¿Cuál es la herramienta recomendada por JetBrains para instalar y gestionar diferentes productos o varias versiones del mismo IDE, incluyendo *Early Access Program* (EAP) y *Nightly releases*?
    a) IDE Installer Wizard
    b) Toolbox App
    c) Snap Package
    d) JBR 21 Runtime

7. Aunque el *JetBrains Runtime* está incluido con IntelliJ IDEA, ¿qué es necesario instalar por separado para desarrollar aplicaciones Java?
    a) Máquina Virtual de Java (JVM)
    b) Java Development Kit (JDK)
    c) Java Runtime Environment (JRE)
    d) .NET SDK

8. ¿Qué servicio adicional se puede instalar en Windows durante el proceso de instalación de JetBrains Rider (o mediante la *Toolbox App*) y es requerido para el *Performance profiling* de código .NET y el Análisis Dinámico de Programas (DPA)?
    a) GitKraken
    b) JetBrains ETW Service
    c) .NET Core Runtime
    d) JDK 21

9. ¿Qué entorno de desarrollo soporta Visual Studio Code (VS Code) de forma nativa *out-of-the-box*?
    a) NetBeans
    b) Oracle JDeveloper
    c) Git
    d) .NET 8

### III. Anatomía y Estructura del IDE

10. Al utilizar IDEs del mismo fabricante (IntelliJ IDEA y JetBrains Rider), ¿cuál es el principal beneficio de la **Filosofía JetBrains**?
    a) Se elimina la necesidad de instalar el JDK.
    b) Se garantiza la compatibilidad con todos los plugins de Eclipse.
    c) Se ofrece una consistencia de la interfaz y uniformidad del flujo de trabajo.
    d) Se deshabilita el *Auto Save* por defecto.

11. ¿Cuál es el atajo de teclado en Windows/Linux para acceder rápidamente a la ventana de la Terminal integrada en los IDEs de JetBrains (IntelliJ IDEA y Rider)?
    a) `Ctrl+Shift+P`
    b) `Ctrl+Shift+L`
    c) `Ctrl+F9`
    d) `Alt+F12`

12. En los IDEs de JetBrains, ¿cómo se llama el panel ubicado a la izquierda del editor que contiene **números de línea, puntos de ruptura** (*breakpoints*) e **iconos de acción**?
    a) *Navigation Bar*
    b) *Activity Bar*
    c) *Gutter*
    d) *Status Bar*

13. En Visual Studio Code (VS Code), ¿cómo se llama la barra vertical ubicada en el extremo izquierdo que se utiliza para **cambiar entre las diferentes vistas** principales (Explorador, Extensiones, Control de Código Fuente)?
    a) *Primary Side Bar*
    b) *Panel*
    c) *Activity Bar*
    d) *Command Palette*

14. ¿Qué herramienta central de VS Code permite acceder a la mayoría de los comandos del IDE y buscar archivos en el *workspace*, a la que se accede mediante `Ctrl+Shift+P` (Windows/Linux)?
    a) *Terminal tool window*
    b) *Command Palette*
    c) *Explorer View*
    d) *Panel*

15. En la *Status Bar* de los IDEs JetBrains, ¿qué indican los *widgets* como "LF" o "UTF-8"?
    a) El progreso de las tareas en segundo plano (*Background Tasks*).
    b) El número de línea y columna del cursor.
    c) La rama actual del Control de Versiones.
    d) Las terminaciones de línea y la codificación utilizada en el archivo actual.

### IV. Plugins, Configuración y Personalización

16. ¿Qué atajo de teclado abre el menú de configuración (*Settings*) en IntelliJ IDEA y JetBrains Rider?
    a) `Ctrl+Shift+A`
    b) `Ctrl+Alt+S`
    c) `Ctrl+Shift+V`
    d) `Ctrl+W`

17. ¿Qué acción de VS Code permite que un usuario de otro editor (como Sublime Text, Atom o Vim) use los atajos de teclado de su editor anterior en VS Code?
    a) Instalar una extensión Keymap
    b) Configurar `editor.multiCursorModifier` a `"alt"`
    c) Usar la Paleta de Comandos
    d) Deshabilitar `files.hotExit`

18. En VS Code, ¿qué gesto se utiliza para añadir cursores secundarios (*multi-cursor*) en Windows y Linux de forma predeterminada?
    a) `Ctrl+Click`
    b) `Shift+Alt+Down`
    c) `Alt+Click`
    d) `Ctrl+D`

19. Si un módulo o *plugin* ya no se necesita en NetBeans, ¿qué dos opciones principales existen para retirarlo del entorno?
    a) Reiniciar o reconstruir
    b) Desactivar o desinstalar
    c) Exportar o importar
    d) Renombrar o extraer

20. En VS Code, ¿qué valor debe tener el ajuste `files.autoSave` para guardar archivos automáticamente cuando el foco se mueve fuera del editor del archivo modificado?
    a) `off`
    b) `afterDelay`
    c) `onWindowChange`
    d) `onFocusChange`

21. ¿Qué tipo de configuración en VS Code se aplica solo al *workspace* actual y tiene prioridad sobre las configuraciones de usuario?
    a) Configuración de Usuario (*User settings*)
    b) Configuración del Workspace (*Workspace settings*)
    c) Configuración de la *Activity Bar*
    d) Configuración de *Hot Exit*

### V. Operativa Básica del IDE

22. En los IDEs JetBrains, ¿qué atajo de teclado abre la lista de refactorizaciones disponibles contextualmente (*Refactor This*)?
    a) `Ctrl+Shift+A`
    b) `Ctrl+Alt+Shift+T`
    c) `Ctrl+Alt+M`
    d) `Ctrl+F9`

23. ¿Cuál de las siguientes es una refactorización disponible en IntelliJ IDEA que ayuda a reducir la duplicación de código?
    a) *Safe Delete*
    b) *Rename*
    c) *Extract Method*
    d) *Inline*

24. En IntelliJ IDEA, ¿cuál es el comando para realizar una **Reconstrucción (*Rebuild*)** del proyecto, que limpia el directorio de salida, elimina las cachés y construye el proyecto desde cero?
    a) `Build | Recompile 'class name'`
    b) `Build | Build Project`
    c) `Build | Build Artifacts`
    d) `Build | Rebuild Project`

25. ¿Cuál es el objetivo principal de la refactorización de código, según las fuentes?
    a) Añadir nueva funcionalidad y arreglar errores.
    b) Mejorar la facilidad de comprensión del código sin alterar su funcionalidad.
    c) Compilar el proyecto en modo depuración.
    d) Generar documentación automática.

26. En IntelliJ IDEA, ¿cuál es el nombre que recibe el archivo Java archivado y compilado (ej. `.jar`) destinado a la distribución?
    a) *Plugin*
    b) *Dependency*
    c) *Artifact*
    d) *Buildfile*

27. Durante una sesión de depuración en NetBeans, ¿qué comando permite ejecutar una línea de código y, si es una llamada a un método, **saltar a la primera línea** de ese método?
    a) *Step Over* (F8)
    b) *Step Into* (F7)
    c) *Step Out* (Ctrl + F7)
    d) *Continue* (F5)

28. En IntelliJ IDEA, si se desea compilar únicamente el archivo o clase que está abierto en el editor, ¿cuál es la acción o atajo de teclado?
    a) `Ctrl+F9`
    b) `Build | Recompile 'class name'` (`Ctrl+Shift+F9`)
    c) `Shift+F10`
    d) `Build | Build Artifacts`

29. En Visual Studio Code, si desea formatear el documento activo completo, ¿cuál es el comando o atajo de teclado en Windows o Linux?
    a) `Ctrl+K Ctrl+F` (Format Selection)
    b) `Shift+Alt+Left` (Shrink selection)
    c) `Shift+Alt+F` (Format Document)
    d) `Ctrl+Alt+Down` (Multi-cursor)

30. En VS Code, ¿cuál es el comando para buscar texto globalmente en todos los archivos del *workspace*?
    a) `⌘F` (Windows, Linux `Ctrl+F`)
    b) `⇧⌘F` (Windows, Linux `Ctrl+Shift+F`)
    c) `⌥⌘L` (Windows, Linux `Alt+L`)
    d) `⌘K ⌘F` (Windows, Linux `Ctrl+K Ctrl+F`)