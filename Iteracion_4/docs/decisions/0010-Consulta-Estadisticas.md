---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-10
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Consulta de estadísticas

## Context and Problem Statement

El sistema debe de crear esrtadísticas para acceder a datos útiles de forma sencilla.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF08.1: Módulo gestión de estadísticas.

## Decision Outcome

Se creará una clase GestorEstadisticas, because No hemos encontrado un patrón que resuelva el problema. La clase generará 3 tipos de estadísticas. La primera mostrará información sobre el estado del paquete. La segunda la situación en tiempo real de los camiones. Y la tercera información acerca de los clientes.

### Consequences

* Good, because La creación de la clase GestorEstadisticas centralizará la generación de gráficos, facilitando el mantenimiento y evolución del módulo de estadísticas.