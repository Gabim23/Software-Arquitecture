# Selección-Estilo-Arquitectónico

* Status: Accepted
* Date: 2024-11-03
* decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
* consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari 


## Context and Problem Statement

Como el sistema debe migrar de una arquitectura monolítica a uno basada en microservicios, debemos decidir cuál es el estilo arquitectónico más óptimo en el que nos vamos a basar para realizar el diseño del problema dado. 
<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF01: Cambio de arquitectura.
<!-- numbers of drivers can vary -->

## Considered Options

* 0001-1-Estilo-REST-Por-Eventos
* 0001-2-Estilo-Por-Capas
* 0001-3-Estilo-Cliente-Servidor


<!-- numbers of options can vary -->

## Decision Outcome

Chosen option: "0001-1-Estilo-REST-Por-Eventos", because nos permite que el cliente envíe peticiones al servidor y este le responde con el resultado de la búsqueda. Al combinarlo con un estilo por eventos, permite detectar acciones de consulta o pago y actuar en consecuencia.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because REST utiliza el protocolo HTTP, que es bien conocido y ampliamente utilizado en la web. Esto facilita la integración y la comunicación entre microservicios, así como con clientes externos (como aplicaciones móviles y web).
* Good, because el estilo por eventos permite que los módulos reaccionen a los cambios de estado sin necesidad de llamadas directas.(Estado de los pedidos).
* Good, because REST es un estilo sin estado, por lo que cada solicitud del cliente contiene toda la información necesaria para que el servidor la procese. Esto simplifica la lógica del servidor, ya que no tiene que gestionar el estado de las sesiones.
* Bad, because el estilo por eventos es difícil de implementar.
* Bad, REST no óptimo para actualizaciones en tiempo real. 
 <!-- numbers of consequences can vary -->

<!-- This is an optional element. Feel free to remove. -->
### Confirmation

Los Arquitectos Senior se reunirán con los Arquitectos Cognitivos para discutir las decisiones. Una vez que ambas partes estén de acuerdo con la decisión, esta se confirmará.

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### 0001-2-Estilo-Por-Capas

<!-- This is an optional element. Feel free to remove. -->
El estilo por capas separa los componentes de la aplicación de una forma óptima y nos permite implementar el resto de los problemas aplicando patrones de diseño.

* Good, because permite una fácil escalabilidad
* Good, because permite una buena separación de responsabilidades lo que permite una organización más clara.
<!-- use "neutral" if the given argument weights neither for good nor bad -->
* Bad, because es más compleja de mantener e implementar en comparación con REST.
* Bad, because hace más complejo el desacoplamiento de módulos 

<!-- numbers of pros and cons can vary -->

### 0001-3-Estilo-Cliente-Servidor

Cliente-Servidor separa la presentación de la lógica de negocio y permite una gestión más centralizada de los datos y servicios.

* Good, because facilita la comunicación entre los clientes móviles o de PC y los módulos críticos, como Pedidos y Reparto.
* Bad, because hay limitaciones en la Escalabilidad del Sistema de Pedidos.
* Bad, because para el módulo de Pagos, que utiliza Stripe, el estilo cliente-servidor podría requerir intermediación constante para validar y procesar cada solicitud de pago, lo cual aumenta la carga en el servidor y puede añadir latencia a las transacciones de pago, haciendo que el sistema sea menos ágil.
