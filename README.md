# Simulación de Sistema Radar Pulsado con Múltiples Blancos en MATLAB
## Proyecto del Máster en Ingeniería de Telecomunicaciones - Asignatura de Sistemas de Radionavegación y Posicionamiento - EPS/UAM

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![MATLAB Version](https://img.shields.io/badge/MATLAB-R2024b%2B-blue.svg)

Este proyecto implementa una simulación completa de un sistema radar de vigilancia pulsado, desarrollado en MATLAB. Se enfoca en la detección de múltiples blancos móviles con Sección Radar Equivalente (RCS) fluctuante y visualización dinámica mediante interfaz gráfica.

**Desarrollado por:**
* [Miguel Carralero Lanchares](https://www.linkedin.com/in/miguel-carralero-lanchares/) <a href="https://www.linkedin.com/in/miguel-carralero-lanchares/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" width="16" style="vertical-align:middle; margin-left:4px"/></a>
* [Francisco Orcha Kovacs](https://www.linkedin.com/in/francisco-orcha-38a5831b3/) <a href="https://www.linkedin.com/in/francisco-orcha-38a5831b3/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" alt="LinkedIn" width="16" style="vertical-align:middle; margin-left:4px"/></a>

## Descripción General del Proyecto

El objetivo principal es simular el funcionamiento de un radar pulsado, inspirado en sistemas como el AN/MPQ-64 Sentinel, cubriendo desde el cálculo de parámetros fundamentales hasta la detección y representación de blancos en un entorno dinámico.

Características clave:
1.  **Cálculo de Parámetros Radar:** Determinación de alcance máximo (Rmax), resolución, PRF, alcance no ambiguo (Rmax_na), sensibilidad del receptor y umbral de detección.
2.  **Múltiples Blancos Móviles:** Simulación de hasta 5 blancos con trayectorias iniciales aleatorias (dirigidas hacia el radar) y velocidades variables.
3.  **RCS Fluctuante:** Implementación de fluctuación de la sección radar de los blancos (modelo Swerling I/II mediante `exprnd`) para un mayor realismo.
4.  **Modelo de Detección:** Inclusión de ruido térmico y proceso de detección basado en umbral, considerando Pfa y Pd.
5.  **Visualización Dinámica:** Interfaz gráfica con tres vistas actualizadas en tiempo real:
    *   **Posición Real:** Trayectorias verdaderas de los blancos.
    *   **PPI (Plan Position Indicator):** Detecciones radar en formato polar.
    *   **A-Scope:** Amplitud del eco vs. distancia para cada pulso.
6.  **Manejo de Fenómenos Radar:** Simulación de zona ciega, ambigüedad de rango, y comportamiento en distancia mínima (Rmin).

El informe técnico detallado del proyecto, incluyendo el fundamento teórico, análisis de casos de estudio y discusión de resultados, se encuentra en la carpeta `docs/`.

## Tecnologías Utilizadas

*   **Lenguaje y Entorno:** MATLAB (R2024b o superior)
*   **Toolboxes de MATLAB Requeridos:**
    *   **shnidman.m**: Necesario para el cálculo de la SNR requerida. Se puede instalar desde el Add-Ons Explorer de MATLAB. El script incluye una alternativa (aproximación de Albersheim) si este Add-Ons no está disponible.
    *   **Statistics and Machine Learning Toolbox**: Utilizado para la función `exprnd` (modelado de RCS fluctuante).
    *   Funciones gráficas y de cálculo de MATLAB estándar.

## Estructura del Repositorio
```
+-- .gitignore
+-- LICENSE
+-- README.md
+-- requirements.txt                                           (Lista de Toolboxes de MATLAB necesarios)
+-- docs/
|+-- Proyecto_Sistemas_Radionavegacion_Simulacion_Radar.pdf    (Informe completo del proyecto)
+--  src/
|+--  SimulacionProyectoSRP_MiguelCarralero_FranciscoOrcha.m   (Script principal de la simulación)
+-- ...
```
