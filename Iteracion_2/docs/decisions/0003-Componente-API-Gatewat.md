---
# These are optional metadata elements. Feel free to remove any of them.
status: "proposed"
date: 2024-11-06
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Componente API Gateway

## Context and Problem Statement

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF02: Componente API Gateway

## Considered Options

* 0003-1-API-Gateway-centralizada
* 0003-2-API-Gateway-descentralizada

## Decision Outcome

Chosen option: "0003-1-Gateway-centralizada", because Al estar trabajando en una arquitectura de microservicios con parte cliente y servidor, es necesario una API centralizada para gestionar la comunicacion entre estos.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because El monitoreo del tràfico de datos se realiza desde un único punto 
* Good, because Al tener solo una API gateway centralizada, el sistema realiza las solicitudes de manera óptima.
* Bad, because La efectividad de la comunicacion entre clientes y microservicios depende de una unica API Gateway, afectando la disponibilidad del sistema.


<!-- This is an optional element. Feel free to remove. -->

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### 0003-2-API-Gateway-descentralizada

<!-- This is an optional element. Feel free to remove. -->
Permite una comunicacion independiente para cada tipo de cliente a través del uso distintas APIs.

* Good, because Cada API esta enfocada para un tipo de cliente.
* Bad, because En el caso de tener muchos tipos de clientes hay que crear una API por cada uno de ellos.
* Bad, because Al tener varias APIs con funcionalidades comunes, complica la implementacion y manteniemiento.

<!-- This is an optional element. Feel free to remove. -->
