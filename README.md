# Plantilla Beamer - Fundación COMPUTAEX

Plantilla de presentaciones LaTeX (Beamer) para la Fundación COMPUTAEX.

## Características

* **Formato Panorámico:** Configuración base 16:9, modificable mediante los parámetros de clase en `main.tex`.
* **Identidad Visual:** Integración del color corporativo COMPUTAEX (`#4FA392`) y paleta derivada.
* **Logotipos:** Posicionamiento central en la portada y reducción automática en el cuadrante inferior derecho para las diapositivas de contenido.
* **Fondos Atenuados:** Soporte integrado mediante `tikz` para establecer imágenes de fondo con opacidad del 20%.
* **Fragmentos de Código:** Entorno `lstlisting` preconfigurado con el estilo `terminal` para código fuente y scripts.
* **Paquetes Científicos:** Soporte nativo para:
    * Circuitos cuánticos (`quantikz`).
    * Notación de Dirac y estados cuánticos (`braket`).
    * Tablas científicas estructuradas (`booktabs`).
* **Navegación:** Supresión de los controles de navegación nativos de Beamer.

## Instrucciones de Uso

### Opción 1: Overleaf (Portal Institucional)
1. Acceder al proyecto base en Overleaf mediante el enlace interno de la Fundación.
2. Ejecutar la acción **Menu > Copy Project** para generar una instancia privada y editable.

### Opción 2: Compilación Local
1. Clonar el repositorio en el directorio local:
   ```bash
   git clone https://github.com/Cerrudoxx/Computaex-Beamer-Template.git
   ```
2. Verificar la disponibilidad de una distribución LaTeX funcional y de los paquetes requeridos (`quantikz`, `braket`, `booktabs`, `xcolor`, `tikz`).
3. Compilar el documento `main.tex` utilizando `pdflatex`.

## Estructura del Repositorio

* `main.tex`: Documento principal. Contiene la estructura y los datos de las diapositivas.
* `computaex_theme.sty`: Archivo de estilo. Define directivas de color, tipografía, posicionamiento de elementos visuales y comandos auxiliares.
* `logos/`: Directorio de recursos gráficos oficiales.

## Guía de Formato

### Secciones e Índice
La generación del índice es automática en base a las declaraciones de sección:
```latex
\section{Título de la Sección}
```

### Gestión de Fondos
Los fondos se aplican de manera global desde el punto de declaración y mantienen una opacidad fija del 20%:
```latex
% Activar fondo para todas las diapositivas siguientes
\activarfondo{logos/Banner1.png}

% Desactivar fondo para todas las diapositivas siguientes
\desactivarfondo
```

### Entornos Cuánticos
Inserción de circuitos mediante el entorno preconfigurado:
```latex
\begin{quantikz}
\lstick{$\ket{0}$} & \gate{H} & \gate{X} & \meter{}
\end{quantikz}
```

### Fragmentos de Código
Inserción de bloques de código con resaltado sintáctico de terminal oscuro (requiere añadir el parámetro `[fragile]` en el frame):
```latex
\begin{frame}[fragile]
\begin{lstlisting}[style=terminal]
# Actualizar repositorios e instalar paquetes
sudo apt update
git clone https://github.com/usuario/proyecto.git
\end{lstlisting}
\end{frame}
```

## Mantenimiento
La gestión de incidencias técnicas y las propuestas de modificación estructural se tramitan a través del sistema de Issues y Pull Requests del repositorio.

## Licencia y Derechos de Uso
El código fuente y de estilo LaTeX (`.tex`, `.sty`) se distribuye bajo la Licencia MIT.
Los recursos gráficos alojados en los directorios `logos/`, `Fotos_CPD/` y la denominación "Fundación COMPUTAEX" son propiedad exclusiva de la institución. Queda prohibido su uso, reproducción o distribución para fines ajenos a la actividad oficial de la Fundación.
