# Deseño

> Os diagramas deste documento están escritos na linguaxe `plantuml`, para máis información de como renderizar estos gráficos podes acudir ó seu sitio web en [https://plantuml.com][plantuml-com], para consultar a súa [instalación][plantuml-starting].
>
> Para ver os diagramas integrados no documento empregar as seguintes extensións de vscode: [PlantUML][plantuml-extension] e [Markdown Preview Enhanced][markdown-preview-enhanced]. Tamén podes atopalos no apartado [3. deseño en SVG][desenho-svg] desta documentación en formato `svg`.

## Modelo conceptual do dominio da aplicación

```plantuml {r my-chunk, R.options = list(width = 50)}
!include ../diagramas/uml/plantuml/dominio.puml
```

<div style="page-break-after: always;"></div>

## Casos de uso

```plantuml
scale 1000 width

!include ../diagramas/uml/plantuml/casos_uso/casos_uso.puml
```

<div style="page-break-after: always;"></div>

## Deseño de interface de usuarios

// TODO:

Unha forma de axudar ó deseño da aplicación é realizar uns mockups: pódelos facer á man ou cunha aplicación ou a través dunha web do estilo: https://app.diagrams.net/

Os mockups deben incluir todas as vistas da aplicación, é dicir, todas as páxinas diferentes que un usuario (de calquera tipo) vai a poder ver. Un mockup permite ver como se verá unha páxina concreta da nosa aplicación web. O deseño de mockups vainos axudar a:

- Avanzar moi rápido na parte frontend: ao ter os mockups realizados, xa sabemos que elementos vai ter cada vista e onde colocalos. Podes empregar un framework CSS ou programar as follas de estilos.
- Visualizar a información que vai a ser necesaria mostrar. Sabendo con que información imos traballar e sabendo a información que necesitamos mostrar ao usuarios, podemos organizar os datos dunha forma axeitada para gardalos na base de datos.

## Diagrama de Base de Datos

Nesta fase tamén teremos que realizar:

- Modelo Entidade/relación
  - // TODO:
- Modelo relacional
  - // TODO:

## Modelo clases

```plantuml
scale 1000 width

!include ../diagramas/uml/plantuml/clases/00_main.puml
```

[//]: # (Listado dos links empregados)

   <!-- Enlaces a terceiros -->
   [plantuml-com]: <https://plantuml.com/es>

   [plantuml-starting]: <https://plantuml.com/es/starting>

   [plantuml-extension]: <https://marketplace.visualstudio.com/items?itemName=jebbs.puml>

   [markdown-preview-enhanced]: <https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced>

   <!-- Índice de seccións -->

   [estudio_preliminar]: <1_estudo_preliminar.md>

   [analise]: <2_analise.md>

   [desenho]: <3_deseno.md>

   [desenho-svg]: <3_deseno_svg.md>

   [codificacion_probas]: <4_codificacion_probas.md>

   [manuais]: <5_manuais.md>

   [estratexia_de_versionado]: <6_versionado.md>

   [changelog_api]: <../../CHANGELOG_API.md>
   [changelog_ui]: <../../CHANGELOG_UI.md>

   <!-- Anexos -->

   [referencias]: <a1_referencias.md>
   [planificacion]: <a2_planificacion.md>
   [orzamento]: <a3_orzamento.md>
