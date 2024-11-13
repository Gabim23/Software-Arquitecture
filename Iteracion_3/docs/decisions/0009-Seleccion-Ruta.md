---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-10
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---


# Decisión de un patrón para seleccionar el algoritmo de ruta

## Context and Problem Statement

Debemos de encontrar el mejor patrón para seleccionar uno de los dos algoritmos según la demora de los camiones.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF07.1: Optimización ruta camión

## Considered Options

* 0009-1-Patrón-Template
* 0009-2-Patrón-Strategy

## Decision Outcome

Chosen option: "0009-2-Patrón-Strategy", because Permite cambiar los algoritmos de optimización de rutas en tiempo de ejecución, proporcionando flexibilidad y modularidad. 

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because Es flexible, al permitir cambiar dinámicamente de algoritmo, adaptándose a las necesidades específicas de cada caso en tiempo real.
* Good, because Las clases que usan los algoritmos no necesitan conocer los detalles de implementación, lo que hace que el sistema sea más modular.
* Neutral, because Cada algoritmo requiere una clase específica pero en nuestro caso solo utilizaremos 2 algoritmos, por lo que no afectará al rendimiento.
* Bad, because Elegir estrategias dinámicamente en tiempo de ejecución puede tener un costo en términos de rendimiento, aunque generalmente es mínimo.



<!-- This is an optional element. Feel free to remove. -->

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### 0008-1-Patrón-Template

<!-- This is an optional element. Feel free to remove. -->


* Good, because {argument a}
* Good, because {argument b}
<!-- use "neutral" if the given argument weights neither for good nor bad -->
* Neutral, because {argument c}
* Bad, because {argument d}
* … <!-- numbers of pros and cons can vary -->


