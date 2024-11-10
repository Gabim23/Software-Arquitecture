---
# These are optional metadata elements. Feel free to remove any of them.
status: "proposed"
date: 2024-11-06
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Creación Modulos

## Context and Problem Statement
La lógica de negocio de la empresa cuenta con varios módulos con distintos grados de criticidad.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF04: Módulo gestión de clientes
* RF05: Módulo gestión de pedidos
* RF06: Módulo gestión de repartos y rutas
* RF07: Módulo gestión de estadísticas
* RF08: Módulo gestión de incidencias
* RF09: Módulo gestión de pagos

## Considered Options

* 0004-1-2-Bases-de-datos-SQL

## Decision Outcome

Chosen option: "0004-1-2-Bases-de-datos-SQL", because se creará un módulo por cada agrupación de clases y componentes que se relacionan entre sí.
