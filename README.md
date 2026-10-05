# Evaluacion N°1

Herramientas Computacionales para Ingeniería II (OOCC) · David Creutez · Universidad de Santiago de Chile

## Descripción del proyecto

Entorno de trabajo reproducible para analizar la deflexión de una viga simplemente apoyada de sección rectangular con carga puntual centrada. Se calcula la deflexión teórica (Euler-Bernoulli), se compara con las deflexiones medidas y se comunica el resultado en una nota técnica en LaTeX. Los datos son sintéticos y de uso docente.

## Datos y parámetros

- L = 4,0 m, b = 0,2 m, h = 0,4 m, E = 25 GPa.
- Cargas de 0 a 40 kN en pasos de 5 kN; deflexión medida en el centro de la luz.


## Estructura 

- `Data/Raw/`: Conjunto de datos recibidos, sin realizar ningun cambio. (respaldo) 
- `Data/Data and parameters/`: datos para realizar los calculos correspondientes 
- `figures`: imagenes, graficos, etc utilizados. 
- `Report`: Archivos para documentar todo el trabajo 
- `README`: Descripción detallada del proyecto 

## Cómo reproducir los resultados

1. Los datos originales están en `Data/Raw/`; las copias de trabajo, en `Data/Data and parameters/`.
2. Abrir `Analysis/Cálculos.xlsx`: ahí se convierten las unidades (kN→N, mm→m, GPa→Pa) y se calculan I, δ_teo, la diferencia relativa y δ/P.
3. La figura `figures/carga_deflexion.png` se generó desde la planilla.
4. Compilar `Report/Maintex.tex` (Overleaf o pdflatex + bibtex) para obtener la nota técnica.

## Limitaciones

La transferencia de resultados desde la planilla a LaTeX se hizo de forma manual, sin script de automatización.