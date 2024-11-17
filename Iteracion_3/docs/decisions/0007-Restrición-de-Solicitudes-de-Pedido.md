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

El sistema debe incluir restricciones en la cantidad de solicitudes de un pedido que puede realizar el cliente.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF5.1: Restricción de solicitudes de pedido

## Considered Options

* 0007-1-Patrón-Circuit-Breaker
* 0007-2-Patrón-Command (ArchMind)

## Decision Outcome

Chosen option: "0007-1-Patrón-Circuit-Breaker", because Este patrón rompe el flujo y maneja el límite de intentos evitando que el sistema experimente sobrecargas de solicitudes.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because Este patrón es ideal para el sistema de arquitectura de microservicios porque reintenta el flujo sin comprometer otros servicios.
* Good, because Este patrón responde rápidamente a los cambios de estado evitando hacer solicitudes innecesarias.
* Bad, because, al estar trabajando en un sistema con bases de datos, si este falla, el patrón bloquea el acceso al servicio para todos los usuarios hasta que este se recupere.


# Pros and Cons of the Options

### 0007-2-Patrón-Command

<!-- This is an optional element. Feel free to remove. -->
Este patrón convierte las solicitudes en un objeto independiente, dicho esto existe mas libertad al manejar la información de esta solicitud.

* Good, because Las solicitudes se pueden pasar como argumentos a métodos y admitir operaciones que se puedan deshacer.
* Bad, because Las solicitudes se pueden reatrasar lo cual perjudica al funcionamiento de nuestro sistema.
* Bad, because Genera una capa completamente nueva entre remitentes y receptores.
