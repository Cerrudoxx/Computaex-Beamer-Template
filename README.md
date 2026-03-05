# Plantilla Beamer - Fundación COMPUTAEX

Esta es una plantilla de presentaciones en LaTeX (Beamer) para la **Fundación COMPUTAEX**. 
---

## Características Principales

* **Formato Panorámico:** Configurada por defecto en **16:9**, puede cambiarse a la relación de aspecto que se desee.
* **Colores:** Uso automatizado del verde COMPUTAEX (`#4FA392`) y paleta de colores coherente.
* **Logotipos** Logo central en la portada y logo reducido automático en la esquina inferior derecha para el resto de diapositivas.
* **Paquetes Científicos:** Soporte nativo para:
    * Circuitos cuánticos (`quantikz`).
    * Notación de Dirac/Estados cuánticos (`braket`).
    * Tablas científicas (`booktabs`).
* **Navegación:** Eliminación de los iconos de navegación de Beamer.

---

## Cómo utilizar esta plantilla

Puedes empezar a trabajar con este recurso de dos maneras:

### Opción 1: Overleaf (Uso rápido)
1. Accede al **Proyecto Maestro** mediante el enlace de solo lectura: `https://www.overleaf.com/read/mfwmmxxhmnwm#b2a655`
2. En el panel superior izquierdo, ve a **File** > **Make a Copy**.
3. Dale un nombre a tu presentación y listo. Ya tienes una copia privada para editar.

### Opción 2: Git / Local (Usuarios avanzados)
1. Clona este repositorio en tu equipo:
   ```bash
   git clone https://github.com/Cerrudoxx/Computaex-Beamer-Template.git

   ```

2. Asegúrate de tener una distribución de LaTeX instalada.
3. Compila usando **pdfLaTeX**.

---

## �� Estructura del Proyecto

* `main.tex`: **Archivo de trabajo.** Contenido de las diapositivas.
* `computaex_theme.sty`: **Motor visual.** Contiene la configuración de colores, fuentes y posición de logos. 
* `logos/`: Carpeta con los archivos gráficos oficiales.


---

## �� Guía Rápida de Estilos

### Crear Secciones e Índice

Para que el índice se genere y actualice solo, utiliza el comando `\section` antes de tus diapositivas:

```latex
\section{Análisis de Resultados}
```


### Circuitos Cuánticos

Puedes insertar diagramas de circuitos directamente:

```latex
\begin{quantikz}
\lstick{$\ket{0}$} & \gate{H} & \gate{X} & \meter{}
\end{quantikz}

```

---


Esta plantilla se actualiza periódicamente. Si deseas proponer una mejora visual o has detectado un error:

1. Abre un **Issue** explicando el cambio.
2. Realiza un **Pull Request** si tienes una sugerencia de cambio.
