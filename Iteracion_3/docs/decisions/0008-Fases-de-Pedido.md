---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-12
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Restricción de solicitudes de pedido

## Context and Problem Statement

El sistema verifica que los pedidos pasen por un proceso de tres fases, Preprocesado del pedido, Autorización y Aceptación

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF5.2: Fases del Pedido

## Considered Options

* 0008-1-Patrón-State
* 0008-2-Patrón-Command

## Decision Outcome

Chosen option: "0008-1-Patrón-State", because Permite a un objeto alterar su comportamiento cuando cambia su estado interno.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because El cambio de un estado a otro es secuencial y dependiente.
* Good, because Cada fase o estado se puede interpretar como una clase independiente.
* Good, because Simplifica el añadido o modificación de estados, sin alterar los estados ya existentes.
* Bad, because Incrementa considerablemte la cantidad de clases del sistema.
* Bad, becaise Puede llevar a sobrecargas en sistemas con muchas fases.


# Pros and Cons of the Options

### 0007-2-Patrón-Strategy

<!-- This is an optional element. Feel free to remove. -->
Este patrón convierte las solicitudes en un objeto independiente, dicho esto existe mas libertad al manejar la información de esta solicitud.

* Good, because Las solicitudes se pueden pasar como argumentos a métodos y admitir operaciones que se puedan deshacer.
* Bad, because Las solicitudes se pueden reatrasar lo cual perjudica al funcionamiento de nuestro sistema.
* Bad, because Genera una capa completamente nueva entre remitentes y receptores.
