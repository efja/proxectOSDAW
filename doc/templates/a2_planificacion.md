# Planificación

## Metodoloxía prevista

Considero que o modelo de pasos que se describen na plantilla da documentación invita a unha metodoloxía de tipo cascada. Esta será a metodoloxía que siga na fase de creación destes documentos, despois, na fase de codificación, espero empregar metodolixías áxiles, ou cando menos intentareino.

Pretendo dividir o proxecto en Historias de produto e ir dividindo o traballo en sprints de 1 semana e ir avaliando como continuar ó rematar cada sprint segundo os problemas que vaia tendo no día a día e ó ritmo que dea seguido.

## Fases planificadas

Os recursos que se van a empregar son básicamente:

| Tarefas           | Común a tódalas tarefas *
| -                 |-
| Recursos hardware | 1 equipo de desenvolvemento / probas
| Recursos software | Visual Studio Code, Sistema Xestor de Bases de Datos // TODO: definir e 1 navegador web
| Recursos humanos  | 1 persoa

> **NOTAS:**
> *: O Sistema Xestor de Bases de Datos só sería para a fase de execución.
>
> As estimacións en tempo probablemente non se axusten moito á realidade pero tratarei de non ser moi "optimista" na súa estimación

### Fase 1: Estudo preliminar

| Tarefa        | Estudio de competencia
| -             |-
| Descrición    | Búsqueda por internet de software que cubra as mesmas necesidades que o proxecto
| Duración      | 1:30 - 2 horas

| Tarefa        | Plantexamento do modelo de negocio / licenza
| -             |-
| Descrición    | Valorar e sopesar que tipo de negocio de negocio se quere facer co proxecto e decidir o licenzamento co que se vai a publicar (ou non) o código
| Duración      | 1 - 2 días para sopesalos pros e os contras

| Tarefa        | Valoración de necesidades e definición dos obxectivos
| -             |-
| Descrición    | Unha vez resolto o modelo de negocio valorar en que nicho do mercado se vai a centrar o proxecto e cales son as necesidades que se pretenten satisfacer para ese nicho.
| Duración      | 2 - 3 horas

| Tarefa        | Viabilidade económica
| -             |-
| Descrición    | Facer unha estimación dos recursos que vai a absorver o proxecto e valorar a disposición dos mesmo.
| Duración      | 1 - 2 horas

### Fase 2: Requerimentos do sistema (análise)

| Tarefa        | Definición da estrutura xeral do proxecto
| -             |-
| Descrición    | Estudiarase en que partes se vai a dividir o proxecto e como se van a relacionar entre sí
| Duración      | 1 hora

| Tarefa        | Definición dos modelos de datos
| -             |-
| Descrición    | Definición preliminar dos modelos de información (como clases) que se desexan manexar
| Duración      | 2 - 3 horas

| Tarefa        | Definición do acceso á información
| -             |-
| Descrición    | Decidirase como se xestionará a seguidade decidindo a definición de tipos de usuario e roles nos que se vai a basear o sistema.
| Duración      | 1 - 1:30 horas

### Fase 3: Deseño

Nesta fase acometeranse de xeito máis profundo e concreto as tarefas da fase de análise:

| Tarefa        | Deseño formal da estrutura do proxecto
| -             |-
| Descrición    | Concretaranse as responsabilidades de cada parte do proxecto e deseñarase como se conectarán entre si
| Duración      | 2 - 3 horas

| Tarefa        | Definición dos casos de uso
| -             |-
| Descrición    | Aquí planificaranse os xeitos permitidos para cada usuario de interactuar co sistema
| Duración      | 4 - 5 horas

| Tarefa        | Definición do acceso á información
| -             |-
| Descrición    | En base os casos de uso definirase os tipos de usuario e roles que serán necesarios para garantir que cada usuario acceda só á información á que debe
| Duración      | 1 - 2 horas

| Tarefa        | Definición dos modelos de datos
| -             |-
| Descrición    | En base os casos de uso, á definición do acceso da información e a estrutura do proxecto definiranse formalmente os modelos de datos que se necesitan para a execución do proxecto. Esta definición poderá cambiar segundo vaia madurando a codificación do proxecto.
| Duración      | 3 - 4 horas

> **NOTAS:**
> Na **definición dos modelos de datos** non pretendo facer unha definición dun modelo relacional porque aínda non sei que tipo de persistencia vou a empregar, ademais creo que para o deseño da aplicación é máis interesante facer un modelado das clases e as súas relacións que son as que realmente van a interactuar entre si. Considero que o sistema no que logo se decida persistir a información non é algo crucial para o desenvolvemento do proxecto, se está claro e ben definido o modelo de clases pasar a un sistema relacional é algo máis ou menos sinxelo de acometer e pasar a un sistema non relacional baseado en documentos é algo directo.

### Fase 4: Execución

| Tarefa        | Definición de Historias de produto
| -             |-
| Descrición    | Valorar e definir as partes principias nas que se van a dividir as caracteríscas do proxecto
| Duración      | 3 - 4 horas

| Tarefa        | Facer unha estimación preliminar en tempo das Historios de produto
| -             |-
| Descrición    | Coas Historias xa definidas intentar valorar o tempo que se necesitará para cada unha definir a súa prioridade
| Duración      | 3 - 4 horas

#### Fase 4.1: Sprints

| Tarefa        | Definición da cola de Historias do sprint
| -             |-
| Descrición    | Decidir que Historias de produto entran en cada sprint
| Duración      | 15 - 20 minutos

| Tarefa        | Definición de Historias de sprint
| -             |-
| Descrición    | Subdividir cada Historia da cola do sprint en partes máis pequenas para poder alcanzar o seu obxectivo
| Duración      | 1 - 2 horas

| Tarefa        | Facer unha estimación en tempo das Historios do sprint
| -             |-
| Descrición    | Coas Historias xa definidas intentar valorar o tempo que se necesitará para cada unha e axustar mellor a estimación da Hitoria de produto ás que pertencen e decidir a súa prioridade
| Duración      | 2 - 3 horas

| Tarefa        | Desenvolvemento de cada Historia de sprint
| -             |-
| Descrición    | Atacar cada historia segundo a orde definida
| Duración      | Variable

## Calendario

Calendario que indique as datas nas cales se vai desenvolver a aplicación. Este calendario pódelo facer de dúas formas:

//TODO:

- Cunha **táboa** que recolla as diferentes accións a realizar xunto coas datas de inicio e fin de cada acción.
- Cun **cronograma** como pode ser un diagrama de Gantt, o cal permite visualizar de forma gráfica canto vai ocupar cada acción no tempo.

Trátase dunha estimación, moi probablemente se vai a modificar mentres se avance no proxecto.
