# Análise: Requerimentos do sistema

## 1. Descrición xeral

**ProxectOS** pretende dar cobertura á necesidade de organizar o traballo á hora de desenvolver e planificar tódalas fases de proxectos de software por parte dun equipo de desenvolvemento a través dunha interface de usuario web.

Tamén se contempla a posibilidade de que teñan acceso á información (ou parte da mesma) de **cada proxecto** e ó seu estado as distintas partes implicadas (clientes, comerciais, equipo de programación...) mediante o rexistro de `usuarios` e a asignación de `roles` de acceso ó aplicativo.

Este traballo dividirase en tres partes:

1. A `BD` (Base de Datos) onde se almacenará a información
2. Unha `API` que atacará a `BD` e devolverá a información permitida a través do estándar `http`
3. Unha `UI` (Interface de Usuario) que fará as peticións á `API` e lle presentará os datos ó usuario final
## 2. Funcionalidades

> Os diagramas están escritos na linguaxe `plantuml`, para máis información de como renderizar estos gráficos podes acudir ó seu sitio web en [https://plantuml.com][plantuml-com], para consultar a súa [instalación][plantuml-starting].
>
> Para ver os diagramas integrados no documento empregar as seguitnes extensións de vscode: [PlantUML][plantuml-extension] e [Markdown Preview Enhanced][markdown-preview-enhanced]. Tamén podes atopalos, nun diagrama máis completo, no apartado [3. deseño en SVG][desenho-svg] desta documentación en formato `svg`.

<div style="page-break-after: always;"></div>

### 2.1. Xestión de usuarios

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/usuario.puml
  ```

- Crear:

  ```js
    {
      nome,
      apelidos,
      nie,
      datos_contacto: [ { tipo, contacto } ],
      domicilios: [ { rua, concello, etc } ],
      [ roles ],
      salario,
      horario,
    }
  ```

- Modificar:

  ```js
    {
      id,
      nome,
      apelidos,
      nie,
      datos_contacto: [ { tipo, contacto } ],
      domicilios: [ { rua, concello, etc } ],
      [ roles ],
      salario,
      horario,
    }
  ```

  <div style="page-break-after: always;"></div>

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.2. Xestión de roles

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/rol.puml
  ```

- Crear:

  ```js
    {
      nome,
      descrición,
      alcance: enum SISTEMA, PROXECTO, ETAPA, HISTORIA, ACTUACION,
      permisos: [ lectura, creación, edición, eliminación ]
    }
  ```

- Modificar:

  ```js
    {
      id,
      nome,
      descricion,
      alcance: enum SISTEMA, PROXECTO, ETAPA, HISTORIA, ACTUACION,
      permisos: [ lectura, creación, edición, eliminación]
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

<div style="page-break-after: always;"></div>

### 2.3. Xestión de proxectos

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/proxecto.puml
  ```

- Crear:

  ```js
    {
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      repos: [],
      usuarios: [],
      validadores: [],
      roles: [],
      etapas: [],
      requisitos: [],
      comentarios: [],
    }
  ```

  <div style="page-break-after: always;"></div>

- Modificar:

  ```js
    {
      id,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      repos: [],
      usuarios: [],
      validadores: [],
      roles: [],
      etapas: [],
      requisitos: [],
      comentarios: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.4. Xestión de etapas

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/etapa.puml
  ```

  <div style="page-break-after: always;"></div>

- Crear:

  ```js
    {
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
    }
  ```

- Modificar:

  ```js
    {
      id,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

<div style="page-break-after: always;"></div>

### 2.5. Xestión de requisitos

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/requisito.puml
  ```

  <div style="page-break-after: always;"></div>

- Crear:

  ```js
    {
      historia_pai?,
      data_creacion,
      usuario_creacion,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      tempo_dev, // Exemplos: alto | medio | baixo - longo, medio ou curto
      prioridade, // Exemplo: alta | baixa
      tipo, // Exemplo: modificación | bug | mellora | ...
      repos: [],
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
      etapas: [],
      actuacions: [],
      dependencias: [ requisitos ],
    }
  ```

- Modificar:

  ```js
    {
      id,
      usuario_creacion,
      historia_pai?,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      repos: [],
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
      etapas: [],
      actuacions: [],
      dependencias: [ requisitos ],
    }
  ```

  <div style="page-break-after: always;"></div>

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.6. Xestión de Tempos

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/estimacion_tempo.puml
  ```

- Crear:

  ```js
    {
      nome,
      descricion,
      escala,
      duracion?,
    }
  ```

- Modificar:

  ```js
    {
      id,
      nome,
      descricion,
      escala,
      duracion?,
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

  <div style="page-break-after: always;"></div>

### 2.7. Xestión de Prioridades

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/prioridade.puml
  ```

- Crear:

  ```js
    {
      nome,
      descricion,
    }
  ```

- Modificar:

  ```js
    {
      id,
      nome,
      descricion,
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.8. Xestión de Tipos

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/tipo.puml
  ```

- Crear:

  ```js
    {
      nome,
      descricion,
    }
  ```

- Modificar:

  ```js
    {
      id,
      nome,
      descricion,
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.9. Xestión de Actuacións

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/actuacion.puml
  ```

  <div style="page-break-after: always;"></div>

- Crear:

  ```js
    {
      data_creacion,
      usuario_creacion,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      horas_estimadas,
      horas_consumidas,
      euros_estimados,
      euros_consumidos,
      etapa,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
    }
  ```

- Modificar:

  ```js
    {
      id,
      usuario_creacion,
      data_ini,
      data_fin,
      data_ini_prevista,
      data_fin_prevista,
      nome,
      descricion,
      estado,
      horas_estimadas,
      horas_consumidas,
      euros_estimados,
      euros_consumidos,
      etapa,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

<div style="page-break-after: always;"></div>

### 2.10. Xestión de cometarios

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/comentario.puml
  ```

- Crear:

  ```js
    {
      usuario,
      data,
      data_expiracion,
      titulo,
      mensaxe,
      roles_acceso: [],
    }
  ```

- Modificar:

  ```js
    {
      id,
      data_expiracion,
      titulo,
      mensaxe,
      roles_acceso: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

<div style="page-break-after: always;"></div>

### 2.11. Xestión de repositorios

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/repo.puml
  ```

- Crear:

  ```js
    {
      data_ini,
      data_expiracion,
      nome,
      descricion,
      uri,
      roles_acceso: [],
    }
  ```

- Modificar:

  ```js
    {
      id,
      data_ini,
      data_expiracion,
      nome,
      descricion,
      uri,
      roles_acceso: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.12. Xestión de históricos de estados

  ```plantuml
  !include ../diagramas/uml/plantuml/clases/estado.puml
  ```

En principio haberá un histórico por cada táboa que teña un estado.

- Crear:

  ```js
    {
      data,
      estado_previo,
      estado_novo,
      log,
    }
  ```

- Modificar:

  ```js
    {
      id,
      estado_novo,
      log,
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

<div style="page-break-after: always;"></div>

## 3. Requerimentos non funcionais

- Seguridade:
  - Autenticación
  - Caducidade de sesións

## 4. Acceso á información

### 4.1. Alacances

Os alcances definen a que partes da información almacenada se lle aplicarán as restriccións definidas para cada rol. Os alcances definidos serán:

- **SISTEMA**, definirase o acceso á información de xestión do sistema
- **PROXECTO**, definirase o acceso á información dun proxecto concreto
- **ETAPA**, definirase o acceso á información dunha etapa en concreto dun proxecto
- **HISTORIA**, definirase o acceso á información dunha historia concreta dun proxecto
- **ACTUACION**, definirase o acceso á información dunha actuación concreta dunha historia

### 4.2. Tipos de usuarios

O sistema poderá definir os tipos de usuarios que se precisen para cada proxecto en concreto pero a configuración típica constará de usuarios de tipo:

- Cliente
- Comercial
- Desenvolvedor

> Nota: os usuarios poderán acceder á información que definan os roles ós que pertenzan

### 4.3. Tipos de Roles

O sistema poderá definir os tipos de roles que se precisen para cada proxecto. Cada rol deberá definir explicitamente os seguintes datos:

- **Alcance**, será un de: `SISTEMA, PROXECTO, ETAPA, HISTORIA, ACTUACION`
- Unha colección de **permisos** que serán valores boolean para:
  - **lectura**, definirá se para el alcance establecido tendrá acceso para ver o no la información
  - **creación**, definirá se para el alcance establecido tendrá acceso para crear o no nuevos registros de información
  - **edición**, definirá se para el alcance establecido tendrá acceso para editar o no la información
  - **eliminación**, definirá se para el alcance establecido tendrá acceso para eliminar o no información

## 5. Entorno operacional

### 5.1. Dominio

Indica os dominios que se van a empregar.

// TODO:

### 5.2. Hardware

Para este proxecto empregarse un equipo de desenvolvemento e probas e un equipo virtual nun servizo de could computing online. Neste servizo despregarase un contenedor para cada servizo: `BD`, `API` e `servidor web`

### 5.3. Software

Os servizos de `BD`, de `API` e de `servidor web` montaranse en tres contenedores de `docker` independentes par poder planificar copias de seguridade por separado e tamén para permitir unha alta escalabilidade ó poder replicar as máquinas que fagan falla para atender á demanda.

Para desenvolver o proxecto empregarei como IDE lixeiro Visual Studio Code cobrendo sobre distro de GNU/Linux.

#### 5.3.1. Base de Datos

Empregarase unha base de datos `mongoDB` `PostgreSQL` // TODO: decidir cando se acometa o proxecto.

#### 5.3.2. API

Desenvolverase baixo `NodeJS`.

#### 5.3.2. Interface de Usuario

Abordarase con `Angular`.

## 6. Interfaces externos

Implementaráse unha API.

## 7. Melloras futuras

Sería interesante facer un estudio dos proxectos de distintas industrias e valorar a posibilidade de xeralizar os modelos de datos e o fluxo de traballo para poder ampliar horizontes a un maior rango de usuarios.

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
