---
# These are optional metadata elements. Feel free to remove any of them.
status: "proposed"
date: 2024-11-06
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Elección de driver para el acceso a datos


## Context and Problem Statement
El sistema debe almacenar los datos de los cliente y de los pedidos. Se elegirá el driver más adecuado, que actuará como traductor entre los módulos y las bases de datos.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF03: Elección de driver para el acceso a datos

## Considered Options

* 0004-1-Driver-JDBC
* 0004-2-Driver-ODBC

## Decision Outcome

Chosen option: "0004-1-Driver-JDBC", because La comunicación de la base de datos cuando migramos de un sistema monolítico a uno de microservicios requiere el driver JDBC, ya que este ofrece el equilibrio ideal entre rendimiento y compatibilidad.

### Consequences

* Good, because Está optimizado para manejar las consultas SQL de datos críticos entre los módulos.
* Good, because Proporciona estandarización y uniformidad, lo cual facilita el uso de la API con múltiples bases de datos
* Good, because Proporciona flexibilidad para elegir la mejor base de datos para cada microservicio
* Bad, because Tiene dificultad para escalabilidad horizontal. A medida que el sistema crece y se necesitan más instancias de un microservicio, la gestión de las conexiones JDBC puede volverse más compleja.


<!-- This is an optional element. Feel free to remove. -->

<!-- This is an optional element. Feel free to remove. -->
## Pros and Cons of the Options

### 0004-2-Driver-ODBC

<!-- This is an optional element. Feel free to remove. -->
El driver ODBC es un controlador que permite a las aplicaciones conectarse y comunicarse con distintas bases de datos de manera estándar y uniforme.

* Good because, es compatible con una amplia gama de bases de datos SQL, y facilita el uso de multiples bases de datos para cada modulo.
* Bad because, El driver ODBC no tiene el mismo nivel de optimizacion y afectaria el rendimiento a nivel de consultas. 
* Bad, because Es menos adecuado para la arquitectura de microservicios.
<!-- This is an optional element. Feel free to remove. -->