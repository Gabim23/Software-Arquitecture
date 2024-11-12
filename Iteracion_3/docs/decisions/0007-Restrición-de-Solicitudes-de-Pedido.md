---
# These are optional metadata elements. Feel free to remove any of them.
status: "Accepted"
date: 2024-11-12
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Componente de conexión STRIPE

## Context and Problem Statement

El sistema debe tener un componente para conectarse con una pasarela de pago externa,en este caso proporcionado por la empresa STRIPE, a la hora de hacer un pago.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF10.1: Componente de conexión STRIPE

## Considered Options

* 0006-1-Componente-STRIPE-JAVA

## Decision Outcome

Chosen option: "0006-1-Componente-STRIPE-JAVA", because Este componente lo proporciona la empresa STRIPE, y al estar trabajando en un sistema basado en java, este compomponente es la mejor opción.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because Este componente utiliza una API basada en HTTP/REST, por lo que es compatible con la arquitectura de microservicios.
* Good, because Este componente brinda flexibilidad y posibilidad de expansión debido a su variedad de funciones.
* Good, because Este componente reduce el procesamiento de pagos mejorando el flujo del módulo de pedidos.
* Bad, because El sistema depende de una pasarela STRIPE para el procesamiento del pago, si esta experimenta interrupciones podría causar problemas en los pagos de los clientes.