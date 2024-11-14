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

El sistema verifica que los pedidos pasen por un proceso de tres fases, Preprocesado del pedido, Autorización y Aceptación.
Además no se debe de permitir que un pedido pase de un estado a otro si el anterior no se ha completado correctamente.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF5.2: Fases del Pedido
* RF5.3: Verificación de Fases del Pedido

## Considered Options

* 0008-1-Patrón-State
* 0008-2-Patrón-Chain-of-Responsability

## Decision Outcome

Chosen option: "0008-2-Patrón-Chain-of-Responsability", because 
Permite a un objeto cambiar de estado sin que este modifique su comportamiento interno. Puediendo pasar de un estado a otro siguiendo una cadena.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because Permite el desacoplamiento de cada fase, haciendo que cada una se covierta en un manejador independiente.
* Good, because Incrementa la flexibilidad al tener la posiblidad abierta de agregar fases sin alterar las ya existentes.
* Good, because Si una solicitud de un pedido falla en una fase este no podrá continuar la cadena devolviendo un error.
* Bad, because Si la cadena de estados es larga se podrían experimentar retrasos en los procesamientos.


# Pros and Cons of the Options

### 0008-1-Patrón-State

<!-- This is an optional element. Feel free to remove. -->
Este patrón permite alterar el comportamiento de un objeto cuando cambia su estado interno.

* Good, because El cambio de un estado es secuencial y dependiente.
* Bad, because Incrementa considerablemente la cantidad de clases del sistema.
* Bad, because Puede lllevar a sobrecargas en sistemas con muchas fases.
