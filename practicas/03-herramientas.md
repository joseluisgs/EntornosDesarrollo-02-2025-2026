

## Práctica: Instalación y Configuración Unificada de Entornos de Desarrollo

**Objetivo:** Instalar los kits de desarrollo base (JDK, .NET), Git y las herramientas de terminal (*Oh My Posh*), e instalar y configurar los IDEs IntelliJ IDEA, JetBrains Rider y Visual Studio Code con una apariencia, fuente y tema idénticos (Material o Drácula, Fira Code y ligaduras), documentando el proceso con capturas.

- [Práctica: Instalación y Configuración Unificada de Entornos de Desarrollo](#práctica-instalación-y-configuración-unificada-de-entornos-de-desarrollo)
  - [PARTE I: Instalación de Plataformas Base y Herramientas Esenciales](#parte-i-instalación-de-plataformas-base-y-herramientas-esenciales)
    - [1. Instalación de Kits de Desarrollo](#1-instalación-de-kits-de-desarrollo)
      - [1.1. Instalación de JDK 21 (Java Development Kit)](#11-instalación-de-jdk-21-java-development-kit)
      - [1.2. Instalación de .NET 8 (SDK/Runtime)](#12-instalación-de-net-8-sdkruntime)
    - [2. Instalación de Herramientas de Control de Versiones](#2-instalación-de-herramientas-de-control-de-versiones)
      - [2.1. Instalación de Git](#21-instalación-de-git)
    - [3. Instalación y Personalización de la Terminal (Oh My Posh)](#3-instalación-y-personalización-de-la-terminal-oh-my-posh)
      - [3.1. Instalación de Oh My Posh](#31-instalación-de-oh-my-posh)
      - [3.2. Aplicación de un Tema](#32-aplicación-de-un-tema)
  - [PARTE II: Instalación de Entornos Integrados de Desarrollo (IDEs)](#parte-ii-instalación-de-entornos-integrados-de-desarrollo-ides)
    - [4. Instalación de IDEs JetBrains (IntelliJ IDEA y Rider)](#4-instalación-de-ides-jetbrains-intellij-idea-y-rider)
      - [4.1. Instalación de JetBrains Toolbox App](#41-instalación-de-jetbrains-toolbox-app)
      - [4.2. Instalación de IntelliJ IDEA (Community o Ultimate)](#42-instalación-de-intellij-idea-community-o-ultimate)
      - [4.3. Instalación de JetBrains Rider](#43-instalación-de-jetbrains-rider)
    - [5. Instalación de Visual Studio Code (VS Code)](#5-instalación-de-visual-studio-code-vs-code)
  - [PARTE III: Configuración Unificada de Apariencia](#parte-iii-configuración-unificada-de-apariencia)
    - [6. Instalación de Plugins y Fuentes Comunes](#6-instalación-de-plugins-y-fuentes-comunes)
      - [6.1. Instalación de Plugins de Apariencia (Tema)](#61-instalación-de-plugins-de-apariencia-tema)
      - [6.2. Instalación de la Fuente Fira Code](#62-instalación-de-la-fuente-fira-code)
    - [7. Aplicación de Estilos Unificados (Tema, Fuente y Ligaduras)](#7-aplicación-de-estilos-unificados-tema-fuente-y-ligaduras)
      - [7.1. Configuración de IntelliJ IDEA](#71-configuración-de-intellij-idea)
      - [7.2. Configuración de JetBrains Rider](#72-configuración-de-jetbrains-rider)
      - [7.3. Configuración de Visual Studio Code](#73-configuración-de-visual-studio-code)
    - [8. Captura Final de Apariencia Unificada](#8-captura-final-de-apariencia-unificada)


**Requisito de Documentación:** Se requiere realizar **capturas de pantalla de cada paso crucial** de instalación y configuración para verificar su correcta ejecución.

### PARTE I: Instalación de Plataformas Base y Herramientas Esenciales

Esta fase cubre la instalación de los kits de desarrollo necesarios para los IDEs seleccionados, así como la herramienta de control de versiones y la personalización de la terminal.

#### 1. Instalación de Kits de Desarrollo

##### 1.1. Instalación de JDK 21 (Java Development Kit)
El **JDK** es la plataforma necesaria para **desarrollar programas**. Aunque **JetBrains Runtime (JBR 21)** está incluido con IntelliJ IDEA, el **JDK standalone** es necesario para desarrollar aplicaciones Java.

**Pasos a realizar (con captura):**
1. Descargue el instalador de la versión **JDK 21** desde la fuente oficial.
2. Ejecute el instalador y siga el asistente hasta completar la instalación.
3. **[CAPTURAR]** La ventana que confirma la instalación exitosa del JDK.

##### 1.2. Instalación de .NET 8 (SDK/Runtime)
El SDK de **.NET 8** es un requisito fundamental para el desarrollo de proyectos C# y F# y es especialmente relevante para **JetBrains Rider**.

**Pasos a realizar (con captura):**
1. Descargue e instale el SDK de **.NET 8** (no solo el runtime) desde la fuente oficial.
2. **[CAPTURAR]** La línea de comandos que muestra la versión de .NET instalada (ejecutando `dotnet --version` en la terminal).

#### 2. Instalación de Herramientas de Control de Versiones

##### 2.1. Instalación de Git
**Git** es una herramienta esencial para el control de versiones, y su instalación es fundamental ya que **VS Code incluye soporte Git integrado**.

**Pasos a realizar (con captura):**
1. Descargue e instale Git para su sistema operativo, aceptando las opciones por defecto para añadirlo al *PATH*.
2. **[CAPTURAR]** La ventana de confirmación final de la instalación de Git.

#### 3. Instalación y Personalización de la Terminal (Oh My Posh)

##### 3.1. Instalación de Oh My Posh
**Oh My Posh** es una herramienta de terminal que permite la personalización.

**Pasos a realizar (con captura):**
1. Instale Oh My Posh siguiendo las instrucciones oficiales (ej. usando un gestor de paquetes como `winget`).
2. **[CAPTURAR]** La confirmación de la instalación de Oh My Posh.

##### 3.2. Aplicación de un Tema
1. Configure Oh My Posh para cargar un tema de su elección (ej. *Agnoster*, *Dracula*, etc.) al iniciar su terminal (PowerShell, Bash, etc.).
2. **[CAPTURAR]** Su terminal con el tema de Oh My Posh aplicado.

### PARTE II: Instalación de Entornos Integrados de Desarrollo (IDEs)

Se recomienda encarecidamente la **Toolbox App** de JetBrains para gestionar IntelliJ IDEA y Rider.

#### 4. Instalación de IDEs JetBrains (IntelliJ IDEA y Rider)

##### 4.1. Instalación de JetBrains Toolbox App
1. Descargue e instale la **JetBrains Toolbox App**.
2. **[CAPTURAR]** La interfaz de la Toolbox App.

##### 4.2. Instalación de IntelliJ IDEA (Community o Ultimate)
1. Use la Toolbox App para instalar **IntelliJ IDEA**.
2. **[CAPTURAR]** La pantalla de inicio de IntelliJ IDEA que le pide **elegir un tema**. *Elija el tema que utilizará para la configuración unificada (Material o Drácula).*

##### 4.3. Instalación de JetBrains Rider
1. Use la Toolbox App para instalar **JetBrains Rider**.
    *   *Nota:* Si está en Windows, asegúrese de seleccionar la opción de añadir los ejecutables de Rider a las **exclusiones de Windows Defender** si utiliza la instalación *standalone* o en los pasos post-instalación de la Toolbox App, ya que esto mejora el tiempo de arranque.
2. **[CAPTURAR]** La pantalla principal de JetBrains Rider (o la pantalla de bienvenida).

#### 5. Instalación de Visual Studio Code (VS Code)

1. Descargue el instalador de **Visual Studio Code**.
2. Ejecute el instalador y acepte las opciones por defecto.
3. **[CAPTURAR]** La pantalla principal de VS Code.

### PARTE III: Configuración Unificada de Apariencia

El objetivo es lograr la máxima similitud en los tres IDEs, aprovechando la capacidad de personalización de temas, fuentes y ligaduras, y la **consistencia de la interfaz** de los productos JetBrains.

#### 6. Instalación de Plugins y Fuentes Comunes

##### 6.1. Instalación de Plugins de Apariencia (Tema)
Para un tema unificado (ej. Material Theme o Drácula):

*   **IntelliJ IDEA / Rider:** Acceda a **`File -> Settings`** o **`Ctrl+Alt+S`**. Vaya a la sección **Plugins** y busque e instale el plugin de tema deseado.
*   **VS Code:** Acceda a la **Vista Extensiones** y busque e instale el tema deseado (ej. *Material Theme* o *Dracula*).

##### 6.2. Instalación de la Fuente Fira Code
Instale la fuente **Fira Code** en su sistema operativo. Esto se incluye en la necesidad de instalar **fuentes adicionales** para la mejora visual.

#### 7. Aplicación de Estilos Unificados (Tema, Fuente y Ligaduras)

Acceda al Panel de Configuración de cada IDE.

##### 7.1. Configuración de IntelliJ IDEA
1. Acceda a **`File -> Settings`** o **`Ctrl+Alt+S`**.
2. En **Appearance**, aplique el tema oscuro elegido (Material/Drácula).
3. En **Editor** $\rightarrow$ **Font** (Tipos de Letra y Colores):
    *   Seleccione **Fira Code**.
    *   Active el soporte para **Ligaduras**.
4. **[CAPTURAR]** El editor de código de IntelliJ IDEA mostrando el tema oscuro, la fuente Fira Code y las ligaduras (si el lenguaje lo permite).

##### 7.2. Configuración de JetBrains Rider
1. Acceda a **`File -> Settings`** o **`Ctrl+Alt+S`**.
2. En **Appearance**, aplique el tema oscuro elegido (debe ser el mismo que en IntelliJ IDEA, aprovechando la **consistencia de la interfaz**).
3. En **Editor** $\rightarrow$ **Font**:
    *   Seleccione **Fira Code**.
    *   Active el soporte para **Ligaduras**.
4. **[CAPTURAR]** El editor de código de Rider mostrando la configuración unificada.

##### 7.3. Configuración de Visual Studio Code
1. Acceda a la **Settings Editor** con **`Ctrl+,`**.
2. Aplique el tema oscuro elegido.
3. Configure el Editor:
    *   Ajuste la fuente del editor (`editor.fontFamily`) a **Fira Code**.
    *   Active el soporte para **Ligaduras** (`editor.fontLigatures`).
4. **[CAPTURAR]** El editor de código de VS Code mostrando la configuración unificada.

#### 8. Captura Final de Apariencia Unificada

*   **[CAPTURAR]** Una captura que muestre los **tres IDEs (IntelliJ IDEA, Rider, VS Code)** abiertos simultáneamente, demostrando que tienen la apariencia más similar posible en temas, fuentes e iconos (Gutter, etc.) [3.1.1].