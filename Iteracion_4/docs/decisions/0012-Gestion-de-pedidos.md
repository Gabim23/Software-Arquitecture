---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-22
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Gestión de pedidos

## Context and Problem Statement

El sistema debe poder gestionar los pedidos asignandoles la ruta más óptima y una flota.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF 5.4: Gestión de pedidos

## Decision Outcome

Se creará la clase gestor de pedidos, que asignará la ruta y el camión para el pedido y la clase flota que contendrá los camiones.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* ⁠Good, because Es necesario crear la clase Gestor de Pedidos que sirva como medio de comunicación y asignación de los pedidos a las rutas y flotas.
* ⁠Good, because Permite manejar adecuadamente la gestión de pedidos manteniendo la modularidad.