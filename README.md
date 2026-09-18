# Argentine air traffic, 2015–2019

Did the Argentine commercial aviation map change between 2015 and 2019?
This project explores changes in recorded activity and connections between
cities, with a closer look at northern Argentina.

[Read the report](https://ca90m.github.io/c90m/TpAeropuertos_.html)

*Report in Spanish. Code is folded by default; use the “Code” menu to show it.*

## Data

Flight records come from EANA (Empresa Argentina de Navegación Aérea),
published through Argentina’s Ministry of Transport.

Sources used for the 2015–2019 comparison:

* **Original source:** [Ministry of Transport — EANA takeoff and landing records](https://servicios.transporte.gob.ar/gobierno_abierto/detalle.php?d=detalle&t=eana).
* **CSV files used in this version:** [copies preserved in this repository snapshot](https://github.com/marouxet/visualizacion_vuelos_aeropuertos/tree/36b2137b789377a3352d3af48eaa3d705f2f1d5f). Their coverage gaps are described below.
* **Airport metadata:** cities, provinces and coordinates from [Wikipedia’s list of airports in Argentina, revision dated August 3, 2021](https://en.wikipedia.org/w/index.php?title=List_of_airports_in_Argentina&oldid=1036984107).

The main analysis compares 2015 and 2019, with annual context from
2015 to 2020. It selects scheduled departures and excludes records
classified as international.

Analysis in R with dplyr, ggplot2, igraph and networkD3.

## What it looks at

The report compares recorded departures across regions and provinces,
examines connections between cities, and looks at how operations are
distributed among airlines.

Connectivity and flight frequency are treated separately: two cities
can have one connection but many flights between them. Maps, interactive
network graphs and Sankey diagrams show these different aspects of the
network.

The report also retains a separate exercise using 2021 records from the
original coursework.

## Data coverage

The CSV copies used for the 2015–2019 comparison have gaps:

* In 2015–2018, there are no records for days 1–9 of any month.
* In 2019, those days are missing from January through June, but are
  present from July onward.

Missing dates should not be interpreted as days without flights.
Because coverage differs between years, changes in the recorded totals
cannot be interpreted directly as full-year traffic growth. These gaps
may also affect which routes appear in the data.

## Authors

Cristian Antonio, Noe Hsueh and Pablo Manusovich.

Coursework for Laboratorio de Datos, Universidad de Buenos Aires, 2021.
