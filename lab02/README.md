# Lab02 - Data Flow & Mensagens

## Tarefa sobre catálogo de componentes

### [Notebook File](components-01-catalog.ipynb)


## Tarefa Web Components 1

```
<dcc-trigger label="Mundo" action="noticia/mundo/politica"
             value="Brasil elimina a corrupção do governo!">
</dcc-trigger>
<dcc-trigger label="Brasil P" action="noticia/brasil/politica"
             value="Todos os governantes são honestos">
</dcc-trigger>
<dcc-trigger label="Brasil E" action="noticia/brasil/esporte"
             value="Rubens Barrichelo é campeão na F1">
</dcc-trigger>
<dcc-trigger label="Bahia" action="noticia/bahia/esporte"
             value="Bahia é tetra campeão brasileiro">
</dcc-trigger>

<dcc-lively-talk character="doctor" speech="" >
  <subscribe-dcc topic="noticia/#/politica"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk character="nurse" speech="" >
  <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk character="patient" speech="" >
  <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>

```

## Tarefa Web Components 2

```
<dcc-trigger label="News" action="next/rss">
</dcc-trigger>


<dcc-rss source="https://www.wired.com/category/science/feed" publish="noticia/ciencia">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-rss source="https://www.wired.com/category/design/feed" publish="noticia/design">
  <subscribe-dcc topic="next/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="noticia/ciencia"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk character="doctor" speech="" >
<subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk character="nurse" speech="" >
<subscribe-dcc topic="noticia/ciencia"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk character="patient" speech="" >
<subscribe-dcc topic="noticia/design"></subscribe-dcc>
</dcc-lively-talk>

```
