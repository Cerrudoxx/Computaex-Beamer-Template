# Plantilla Beamer - Fundación COMPUTAEX

Plantilla de presentaciones LaTeX (Beamer) para la Fundación COMPUTAEX.

## Características

* **Formato Panorámico:** Configuración base 16:9, modificable mediante los parámetros de clase en `main.tex`.
* **Identidad Visual:** Integración del color corporativo COMPUTAEX (`#4FA392`) y paleta derivada.
* **Logotipos:** Posicionamiento central en la portada y reducción automática en el cuadrante inferior derecho para las diapositivas de contenido.
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
   git clone [https://github.com/Cerrudoxx/Computaex-Beamer-Template.git](https://github.com/Cerrudoxx/Computaex-Beamer-Template.git)
   ```
2. Verificar la disponibilidad de una distribución LaTeX funcional y de los paquetes requeridos (`quantikz`, `braket`, `booktabs`, `xcolor`).
3. Compilar el documento `main.tex` utilizando `pdflatex`.

## Estructura del Repositorio

* `main.tex`: Documento principal. Contiene la estructura y los datos de las diapositivas.
* `computaex_theme.sty`: Archivo de estilo. Define directivas de color, tipografía y posicionamiento de elementos visuales.
* `logos/`: Directorio de recursos gráficos oficiales.

## Guía de Formato

### Secciones e Índice
La generación del índice es automática en base a las declaraciones de sección:
```latex
\section{Título de la Sección}
```

### Entornos Cuánticos
Inserción de circuitos mediante el entorno preconfigurado:
```latex
\begin{quantikz}
\lstick{$\ket{0}$} & \gate{H} & \gate{X} & \meter{}
\end{quantikz}
```

## Mantenimiento
La gestión de incidencias técnicas y las propuestas de modificación estructural se tramitan a través del sistema de Issues y Pull Requests del repositorio.

## Licencia y Derechos de Uso
El código fuente y de estilo LaTeX (`.tex`, `.sty`) se distribuye bajo la Licencia MIT.
Los recursos gráficos alojados en el directorio `logos/` y la denominación "Fundación COMPUTAEX" son propiedad exclusiva de la institución. Queda prohibido su uso, reproducción o distribución para fines ajenos a la actividad oficial de la Fundación.
