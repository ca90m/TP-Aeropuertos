# Tráfico aéreo argentino, 2015–2019

[English](README.md) | **Español**

¿Cambió el mapa de la aviación comercial argentina entre 2015 y 2019?
Este proyecto explora los cambios en la actividad registrada y en las
conexiones entre ciudades, con especial atención al norte argentino.

[Leer el informe en español](https://ca90m.github.io/TP-Aeropuertos/TpAeropuertos_.html) | [Read in English](https://ca90m.github.io/TP-Aeropuertos/TpAeropuertos.en.html)

*Ambos informes incluyen un selector de idioma. El código está oculto por defecto; se puede mostrar desde el menú “Code”. La versión inglesa conserva los nombres de variables y comentarios originales del código R.*

## Datos

Los registros de vuelos provienen de EANA (Empresa Argentina de Navegación
Aérea) y fueron publicados a través del Ministerio de Transporte de la
Argentina.

Fuentes utilizadas para la comparación entre 2015 y 2019:

* **Fuente original:** [registros de despegues y aterrizajes de EANA, Ministerio de Transporte](https://servicios.transporte.gob.ar/gobierno_abierto/detalle.php?d=detalle&t=eana).
* **Archivos CSV utilizados en esta versión:** [copias conservadas en esta versión del repositorio](https://github.com/marouxet/visualizacion_vuelos_aeropuertos/tree/36b2137b789377a3352d3af48eaa3d705f2f1d5f). Las limitaciones de su cobertura se describen más abajo.
* **Metadatos de los aeropuertos:** ciudades, provincias y coordenadas de la [lista de aeropuertos de Argentina en Wikipedia, revisión del 3 de agosto de 2021](https://en.wikipedia.org/w/index.php?title=List_of_airports_in_Argentina&oldid=1036984107).

El análisis principal compara 2015 y 2019, con información anual de contexto
desde 2015 hasta 2020. Se seleccionan despegues de vuelos regulares y se
excluyen los registros clasificados como internacionales.

Análisis realizado en R con dplyr, ggplot2, igraph y networkD3.

## Qué se analiza

El informe compara los despegues registrados entre regiones y provincias,
examina las conexiones entre ciudades y analiza cómo se distribuyen las
operaciones entre aerolíneas.

La conectividad y la frecuencia de vuelos se tratan por separado: dos
ciudades pueden tener una conexión y muchos vuelos entre ellas. Los mapas,
los grafos de redes interactivos y los diagramas de Sankey muestran estos
distintos aspectos de la red.

El informe también conserva un ejercicio separado con registros de 2021,
incluido en el trabajo práctico original.

## Cobertura de los datos

Las copias de los CSV utilizadas para la comparación entre 2015 y 2019
tienen faltantes:

* Entre 2015 y 2018, no hay registros de los días 1–9 de ningún mes.
* En 2019, esos días faltan de enero a junio, pero están presentes a partir
  de julio.

Las fechas faltantes no deben interpretarse como días sin vuelos.
Como la cobertura difiere entre años, los cambios en los totales
registrados no pueden interpretarse directamente como crecimiento del
tráfico anual completo. Estos faltantes también pueden afectar qué rutas
aparecen en los datos.

## Autores

Cristian Antonio, Noe Hsueh y Pablo Manusovich.

Trabajo práctico de Laboratorio de Datos, Universidad de Buenos Aires, 2021.
