# CARBOOST Manaure

Planeación diaria de la desalinizadora solar · Manaure, La Guajira.

Aplicación web con Machine Learning (Gradient Boosting) para decidir, cada tarde, cuánta agua comprometer para mañana en una desalinizadora de ósmosis inversa alimentada con energía solar. Incluye una vista 3D de la planta con sus 14 equipos.

Proyecto final · Machine Learning aplicado a sistemas energéticos · Universidad de La Guajira
Autor: Carlos Mario Gonzales Solano · 2026-II

## Uso

Toda la aplicación está en un solo archivo, `index.html`: el modelo entrenado va incrustado y se ejecuta en el navegador.
Con internet se descargan solo las tipografías y la librería 3D (Three.js).

## Resultado principal (periodo de prueba oct. 2023 - dic. 2025)

| Método | MAE kWh | Costo COP/año |
|---|---|---|
| Persistencia (mañana = hoy) | 13,6 | 13 262 341 |
| Climatología mensual | 17,3 | 15 659 715 |
| Gradient Boosting P50 | 11,6 | 10 641 242 |
| **Gradient Boosting, plan en q* = 0,70** | 13,1 | **9 575 036** |

Límite: los datos son sintéticos calibrados; antes de usarlo en una planta real hay que reentrenar con su registro SCADA y con NASA POWER.
