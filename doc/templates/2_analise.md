# Análise: Requerimentos do sistema

## 1. Descrición xeral

**ProxectOS** pretende dar cobertura á necesidade de organizar o traballo á hora de desenvolver e planificar tódalas fases de proxectos de software por parte dun equipo de desenvolvemento a través dunha interface de usuario web.

Tamén se contempla a posibilidade de que teñan acceso á información (ou parte da mesma) de **cada proxecto** e ó seu estado as distintas partes implicadas (clientes, comerciais, equipo de programación...) mediante o rexistro de `usuarios` e a asignación de `roles` de acceso ó aplicativo.

Este traballo dividirase en tres partes:

1. A `BD` (Base de Datos) onde se almacenará a información
2. Unha `API` que atacará a `BD` e devolverá a información permitida a través do estándar `http`
3. Unha `UI` (Interface de Usuario) que fará as peticións á `API` e lle presentará os datos ó usuario final

## 2. Funcionalidades

### 2.1. Xestión de usuarios

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
      xornadas_semanais
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
      xornadas_semanais
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.2. Xestión de roles

- Crear:

  ```js
    {
      nome,
      descrición,
      alcance: enum SISTEMA, PROXECTO, ETAPA, HISTORIA, ACTUACION,
      permisos: [ lectura, creación, edición, eliminación]
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

### 2.3. Xestión de proxectos

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
      historias: [],
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
      repos: [],
      usuarios: [],
      validadores: [],
      roles: [],
      etapas: [],
      historias: [],
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

### 2.5. Xestión de historias

- Crear:

  ```js
    {
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
      dependencias: [ historias ],
    }
  ```

- Modificar:

  ```js
    {
      id,
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
      dependencias: [ historias ],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.6. Xestión de Actuacións

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
      horas_estimadas,
      horas_consumidas,
      euros_estimados,
      euros_consumidos,
      etapa,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
      actuacions: [],
      dependencias: [ historias ],
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
      horas_estimadas,
      horas_consumidas,
      euros_estimados,
      euros_consumidos,
      etapa,
      usuarios: [],
      validadores: [],
      roles: [],
      comentarios: [],
      actuacions: [],
      dependencias: [ historias ],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.7. Xestión de cometarios

- Crear:

  ```js
    {
      usuario,
      data,
      data_expiracion,
      titulo,
      descricion,
      roles_acceso: [],
    }
  ```

- Modificar:

  ```js
    {
      id,
      data_expiracion,
      titulo,
      descricion,
      roles_acceso: [],
    }
  ```

- Eliminar:

  ```js
    {
      id
    }
  ```

### 2.8. Xestión de repositorios

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

### 2.9. Xestión de históricos de estados

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

Indicar elementos hardware que se usarán. Por exemplo: ordenador para desenvolver a aplicación, smartphone para probar a aplicación na súa versión móbil, servidor web, servidor de bases de datos, CDN, etc.

// TODO:

### 5.3. Software

Indicar software que haberá que instalar en cada elemento hardware. Por exemplo: aplicacións de desenvolvemento, aplicacións para o servidor, etc.

// TODO:

## 6. Interfaces externos

Indicar como se comunicará o noso software co exterior. Os diferentes tipos son:

// TODO:

- De usuario. Por exemplo: as diferentes vistas da apliación, comandos de terminal, etc.
- Hardware. Por exemplo: un lector de código de barras.
- Software. Por exemplo: unha API.

## 7. Melloras futuras

É posible que o noso proxecto se centre en resolver un problema concreto que se poderá ampliar no futuro con novas funcionalidades, novas interfaces, etc.

// TODO:


[//]: # (Listado dos links empregados)

   <!-- Enlaces a terceiros -->

   <!-- Índice de seccións -->

   [estudio_preliminar]: <1_estudo_preliminar.md>

   [analise]: <2_analise.md>

   [desenho]: <3_deseno.md>

   [codificacion_probas]: <4_codificacion_probas.md>

   [manuais]: <5_manuais.md>

   [estratexia_de_versionado]: <6_versionado.md>

   [changelog_api]: <../../CHANGELOG_API.md>
   [changelog_ui]: <../../CHANGELOG_UI.md>

   <!-- Anexos -->

   [referencias]: <a1_referencias.md>
   [planificacion]: <a2_planificacion.md>
   [orzamento]: <a3_orzamento.md>
