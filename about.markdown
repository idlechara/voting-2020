---
layout: page
title: Acerca de
permalink: /about/
---
Repositorio de pruebas de Jekyll. Actualmente está siendo utilizado para la asignación solicitada por Ciudadanía Inteligente en el post de getnbrd. 

Utiliza una colección de "elecciones" las cuales traen información extra de estas, como el nombre, fecha, lugar, etc. Estas son ordenadas por fecha y por medio de la herencia de la plantilla
post, se renderiza cada entrada. 

Es necesario tener activado el mostrar posts futuros ya que también nos aprovechamos de esto. Los post van ordenados por fecha de ejecución de la votación.

Cada votación tiene un enlace a la entrada en wikipedia y el sitio donde se puede encontrar la información oficial de esta.

No se ocupó un `button` y a su vez se utilizó un tag `a` para el requisito del botón de ver más ya que un botón se utiliza cuando la acción se ejecuta en la misma página, mientras que `a` es utilizado
cuando se cambia al usuario del sitio (que es el caso de Jekyll).

La definición de los campos utilizados es la siguiente:

| Campo | Definición| Ejemplo |
|- |-|-|
|`title` |  Titulo a mostrar | *Plebiscito nacional de Chile* |
|`name` |  Nombre del evento | *Plebiscito nacional* |
|`country` | País Asociado | *Chile* |
|`date` | Fecha (para mostrar) | *26/04/2020* |
|`wikipedia` | Enlace a Wikipedia (para tener alguna fuente mas conocida) | *https://es.wikipedia.org/wiki/Plebiscito_nacional_de_Chile_de_2020* |
|`official_site` | Enlace a sitio oficial (para tener información  oficial) | *https://www.servel.cl/plebiscito-nacional-2020/* |
|`layout` | Layout en el que está basado | *details_post* |
