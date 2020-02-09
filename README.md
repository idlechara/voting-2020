# voting-2020

## Prerequisites
* [Ruby >= 2.6 ](https://www.ruby-lang.org/es/)

We assume that you already installed ruby in your machine. If not, we suggest you to use [rvm](https://rvm.io/) as your ruby version manager.

## Install dependencies
You'll need to install [Jekyll](https://jekyllrb.com/) in order to create the static site. you can do so by issuing the following command:

```
gem install bundler jekyll
```

## Running the project

```
bundle exec jekyll serve --watch --baseurl=
```

## Editing: Voting proceses

All voting proceses are located at the `_elections` folder. This folder is treated as a collection and it's rendering process depends on three elements:
* Inherited layout (`_layouts/details_post.md`)
* Election files (`_elections/*.md`)

### Inherited layout
The inherited layout renders a wikipedia link and the official link for a given voting process.

### Election files
Those files define the fields for each election. It's composed of a  [front matter](https://jekyllrb.com/docs/front-matter/) YAML declaration and it's content (given that there could be a case on which it could be needed).

Our current front matter fields are as follows:

| Campo | Definición| Ejemplo |
|- |-|-|
|`title` |  Titulo a mostrar | *Plebiscito nacional de Chile* |
|`name` |  Nombre del evento | *Plebiscito nacional* |
|`country` | País Asociado | *Chile* |
|`date` | Fecha (para mostrar) | *26/04/2020* |
|`wikipedia` | Enlace a Wikipedia (para tener alguna fuente mas conocida) | *https://es.wikipedia.org/wiki/Plebiscito_nacional_de_Chile_de_2020* |
|`official_site` | Enlace a sitio oficial (para tener información  oficial) | *https://www.servel.cl/plebiscito-nacional-2020/* |
|`layout` | Layout en el que está basado | *details_post* |

## Why the content is in Spanish whilst all commits, code and documentation are in English?

That's because I tend to write code in English as a standard, but the situation needed content in Spanish. 
