---
# These are optional metadata elements. Feel free to remove any of them.
status: "proposed"
date: 2024-11-06
decision-makers: Gabriel Miró-Granada Lluch, Alexander Pearson Huaycochea
consulted: RonaldS. Silvera Llimpe, Ikram El Jauhari Al Jaouhari
informed: Alberto Mayoral Gómez, Jorge Ramirez Gayo
---

# Acceso a los datos almacenados

## Context and Problem Statement
El sistema debe almacenar los datos de los clientes como email, nombre, número, id, al igual que el de los pedidos, los cuales tendrán id, dimensión, peso, precio y estado.

<!-- This is an optional element. Feel free to remove. -->
## Decision Drivers

* RF03: Acceso a los datos almacenados

## Considered Options

* 0004-1-2-Bases-de-datos-SQL

## Decision Outcome

Chosen option: "0004-1-2-Bases-de-datos-SQL", because los datos serán almacenados en dos bases de datos distintas, de tipo SQL. En una de ella se guardarán los datos de los clientes, y en la otra los datos de los pedidos.
