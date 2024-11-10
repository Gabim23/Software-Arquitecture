---
# These are optional metadata elements. Feel free to remove any of them.
status: "proposed"
date: 2024-11-06
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Selección-Estilo-Arquitectónico

## Context and Problem Statement

Este MADR sustituye al 0001-Selección-Estilo-Arquitectura.md generado en la primera iteración con el objetivo de corregir errores.
La arquitectura del sistema pasará de ser monolítica a una basada en microservicios en la que hay clientes pc y móvil que utilizan http/REST.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF01: Migración de arquitectura monolítica a microservicios.

## Considered Options

* 0002-1-Estilo-Cliente-Servidor-con-HTTP/REST
* 0002-2-Estilo-REST-Por-Eventos
* 0002-3-Estilo-Por-Capas

## Decision Outcome

Chosen option: "0002-1-Estilo-Cliente-Servidor-con-HTTP/REST", because Permite que los cliente envíen peticiones al servidor y este le responde con los datos solicitados, como la confirmación de un pedido o el estado de una solicitud. Además al estar basado en protocolos HTTP/REST facilita la comprensión de las interacciones entre el cliente y servidor.

<!-- This is an optional element. Feel free to remove. -->
### Consequences

* Good, because Los clientes tienen acceso a los datos almacenados en los servidores.
* Good, because El uso del protocolo HTTP/REST nos proporciona compatibilidad con diversos dispositvos.
* Good, because Facilita la escablabilidad y adaptabilidad de cada módulo al funcionar de manera independiente.
* Bad, because No Existe una estandarización clara a la hora de estructurar un API REST.

<!-- This is an optional element. Feel free to remove. -->

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### 0002-2-Estilo-REST-Por-Eventos

<!-- This is an optional element. Feel free to remove. -->
Permite que el cliente envíe peticiones al servidor y este le responde con el resultado de la búsqueda. Al combinarlo con un estilo por eventos, permite detectar acciones de consulta o pago y actuar en consecuencia.

* Good, because Eventos Proporciona respuestas a eventos a tiempo real.
* Good, because el Estilo por eventos permite que los módulos reaccionen a los cambios de estado sin necesidad de llamadas directas
<!-- use "neutral" if the given argument weights neither for good nor bad -->
* Bad, because REST no es óptimo para actualizaciones en tiempo real.
* Bad, because El problema planteado no aplica el uso de sensores.

### 0002-3-Estilo-Por-Capas

El estilo por capas separa los componentes de la aplicación de una forma óptima y nos permite implementar el resto de los problemas aplicando patrones de diseño.

* Good, because Permite una fácil escalabilidad.
* Good, because Permite una buena separación de responsabilidades lo que permite una organización más clara.
* Bad, because Es más complejo de mantener e implementar en comparación con Cliente-Servidor.
* Bad, because Hace más complejo el desacoplamiento de módulos
<!-- This is an optional element. Feel free to remove. -->
## More Information

Debido a errores cometidos en el MADR 0001-Selección-Estilo-Arquitectura.md
será sustituido por el MADR 0002-Selección-Estilo-Arquitectura.md
