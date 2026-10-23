# Practica_clase_1

#AstroShield: constelación inteligente con algoritmo evolutivo

Un algoritmo evolutivo ubica 8 satélites para observar 6 regiones de la Tierra (Península de Yucatán, Amazonía, California, Sahel, Japón e Interior de Australia). Respeta 3 zonas de desechos espaciales y 2 posiciones ocupadas, y muestra el resultado en un globo 3D interactivo.

**Equipo:** Morales Mendez Shryley Nicoles, Jimenez Andrade Monserrat, Tejero Hernandez Rubi, Sarao Morales Rubi
**Curso:** Fundamentos de la IA

## Contenido
 
| Archivo | Descripción |
|---|---|
| `AstroShield.ipynb` | Definición del problema, implementación, pruebas, análisis de resultados y visualización 3D |

## Cómo funciona
 
- **Representación:** una configuración es una matriz de 8 × 2 (latitud y longitud de cada satélite).
- **Cobertura:** cada satélite observa un disco de 250 km. Una región (disco de 300 km) está cubierta si al menos la mitad de sus puntos queda dentro de alguna huella.
- **Puntuación:** promedio ponderado de la cobertura por prioridad (Alta = 3, Media = 2, Normal = 1).
- **Restricciones:** una configuración con un satélite dentro de una zona prohibida es inválida y siempre pierde contra una válida (reglas de Deb).
- **Algoritmo:** población de 80, selección por torneo, cruce por satélite, mutación de cuatro tipos y elitismo, durante 150 generaciones.

## Pruebas incluidas
 
Escenario inicial, evolución de la calidad, zonas restringidas, posiciones ocupadas, espacio reducido, condiciones inviables, cambio de condiciones, variación entre 10 ejecuciones (contra una búsqueda aleatoria), una prueba adicional con mutantes y la verificación de que el globo muestra los datos reales de la ejecución.
 
## Resultados principales
 
En 10 ejecuciones, la puntuación media fue 0.7967 (desviación estándar 0.0115), frente a 0.2136 de una búsqueda aleatoria con el mismo número de evaluaciones. El análisis completo, con sus limitaciones, está en las secciones 16 y 17 del notebook.
 
## Uso de IA
 
La declaración de herramientas de IA y de cómo se verificó el código está en la sección 17 del notebook.
