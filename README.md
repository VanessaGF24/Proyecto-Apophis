# Análisis Dinámico de la Aproximación de Apophis (2029)

En abril de 2029, el asteroide **(99942) Apophis** pasará a menos de 32,000 km de la superficie terrestre. Este proyecto implementa un modelo computacional basado en la mecánica de dos cuerpos para analizar su trayectoria heliocéntrica y su encuentro cercano con el sistema Tierra-Luna.

##  Objetivo

Modelar y analizar la dinámica orbital de Apophis mediante el uso de **coordenadas de Jacobi** y **unidades canónicas**, aplicando algoritmos de resolución para el problema de los dos cuerpos relativo. Se busca validar las constantes del movimiento (energía, momento angular y vector de excentricidad) utilizando datos reales de efemérides.

##  Métodos y Teoría

En este proyecto se aplican los siguientes conceptos de Mecánica Celeste:

*   **Problema de los Dos Cuerpos Relativo:** Modelado de la interacción Sol-Apophis y Tierra-Apophis.
*   **Coordenadas de Jacobi:** Transformación de vectores de posición y velocidad al centro de masas del sistema para simplificar las ecuaciones de movimiento.
*   **Unidades Canónicas:** Implementación de un sistema de unidades donde $G = 1$, $M_{central} = 1$ y $L = 1 \, \text{UA}$ (o $R_{\oplus}$), facilitando la estabilidad numérica y la generalización del código.
*   **Cálculo de Constantes de Integración:** Determinación de la excentricidad ($e$), el momento angular específico ($h$) y la energía orbital ($\varepsilon$) a partir de vectores de estado 3D.
*   **Efemérides Reales:** Integración de la librería `astroquery` para obtener vectores de estado precisos desde **NASA JPL Horizons**.

## Experimentos

1.  **Simulación Heliocéntrica (Sol-Apophis):** Modelado de la órbita completa de Apophis, análisis de su periodicidad y validación de su excentricidad ($e \approx 0.19$).
2.  **Análisis de la Fuerza Gravitacional:** Estudio de la variación de la fuerza de atracción a lo largo de un periodo orbital para identificar el perihelio y el afelio.
3.  **Modelado del Encuentro Cercano (Tierra-Apophis):** Simulación de la trayectoria de aproximación en 2029 utilizando unidades de radios terrestres para analizar la deflexión de la trayectoria.
4.  **Validación de Constantes:** Verificación de la conservación del momento angular y la energía durante la simulación numérica.

##  Resultados

El proyecto genera los siguientes productos:
*   **Gráficas de Trayectorias:** Visualizaciones 2D y 3D de la órbita en el plano orbital y en el espacio eclíptico.
*   **Perfiles Cinéticos:** Gráficas de la variación de la fuerza gravitacional y velocidad en función del tiempo.
*   **Cálculo de Parámetros:** Determinación automática de $a, e, p, q$ y $Q$ a partir de cualquier fecha de observación.
*   **Animaciones:** Representación dinámica del movimiento relativo en coordenadas de Jacobi.

##  Estructura del Repositorio

*   `src/` → Scripts de procesamiento (conversión a unidades canónicas y álgebra de vectores).
*   `simulations/` → Notebooks con los experimentos Sol-Apophis y Tierra-Apophis.
*   `results/` → Gráficas de fuerzas, órbitas y archivos de datos exportados.
*   `docs/` → Documentación técnica sobre la deducción de las coordenadas de Jacobi y el vector de Runge-Lenz.
## Referencias
----

##  Referencias

- ...
- ...
- ...
