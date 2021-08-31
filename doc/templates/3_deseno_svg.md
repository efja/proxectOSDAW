# Deseño

> Os diagramas deste documento están en formato `svg`.
>
> No apartado [3. deseño][desenho] desta documentación pódense ver os diagramas escritos na linguaxe `plantuml`.

## Modelo conceptual do dominio da aplicación

![dominio]

## Casos de uso

![casos-uso]

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

![clases-main]

<div style="page-break-after: always;"></div>

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

   <!-- DIAGRAMAS -->
   [dominio]: <../diagramas/uml/svg/dominio.svg>

   [clases-main]: <../diagramas/uml/svg/clases/00_main.svg>

   [casos-uso]: <../diagramas/uml/svg/casos_uso/casos_uso.svg>
