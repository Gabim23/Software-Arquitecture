---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-15
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---


# Gestión de incidencias

## Context and Problem Statement

El sistema debe tener una opción de reportar cualquier tipo de incidencias ocurridas a los gestores de las rutas.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF9.1: Gestión de incidencias.

## Decision Outcome

Se creará una clase incidencias, en las que se manejarán todos los tipos de incidencias, because no hemos encontrado un patrón de diseño que solucione este problema.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* ⁠Good, because Permite manejar todos los tipos de incidencias en un único componente.
* ⁠Good, because desacopla la lógica de incidencias manteniendo la modularidad.