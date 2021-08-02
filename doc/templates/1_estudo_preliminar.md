# Estudo preliminar

## 1. Introdución

**ProxectOS** pretende dar cobertura á necesidade de organizar o traballo á hora de desenvolver e planificar tódalas fases de proxectos de software por parte dun equipo de desenvolvemento a través dunha interface de usuario web.

Tamén se contempla a posibilidade de que teñan acceso á información (ou parte da mesma) de **cada proxecto** e ó seu estado as distintas partes implicadas (clientes, comerciais, equipo de programación...) mediante o rexistro de `usuarios` e a asignación de `roles` de acceso ó aplicativo.

## 2. Obxectivo

O obxectivo é crear un software sinxelo que permita a xestión completa dunha colección de proxectos tal como se define na [introdución][introducion] por medio dunha [interface web][definicions] que ataque unha [API][apiWiki] para consultar a información almacenada.

A grandes rasgos manexarase a seguinte información para cada proxecto:

1. Datas de comezo e fin
2. Nome e descrición breve
3. Xestión dos usuarios que participan (clientes, comerciais, equipo de programación...)
4. Roles dos usuarios e permisos para acceder á información do proxecto (lectura, escritura e edición dunha parte ou da totalidade do proxecto)
5. Repositorios ou fontes do código
6. Rexistro de requerimentos
7. Definición das etapas ou fases comprometidas, tendo en conta as datas de comezo e fin reais e, no caso de existir, as datas da planificación (non teñen porque coincidir)
8. Estado actual do proxecto e de cada fase/requerimento
9. Rexistro do avance de cada requerimento (de xeito similar ó proxecto)
10. Histórico de actuacións para cada requerimento (de xeito similar ó proxecto)
11. Definición de usuarios que validen o cumprimento das especificacións para cada proxecto, etapa, requerimento ou actuación

## 3. Definicións

A continuación describiranse o vocabulario que se empregará no proxecto (sen entrar en moitos detalles)

- Termos que son propios do proxecto.
  - // TODO:
- Termos de ámbito técnico como abreviaturas, siglas, acrónimos, etc.
  - // TODO:

## 4. Audiencia

Este software vai dirixido principalmente a profesionais ou entusiastas do desenvolvemento de aplicacións informáticas, aínda que con pequenas adaptacións sería posible dar cobertura a un público maior.

O alcance é limitado pois non se pretende xestionar proxectos moi complexos e con moitas variables na súa proxección senón máis ben poder cubrir a necesidade que poida ter un pequeno equipo de desenvolvemento. Sen embargo ó estar esta ferramenta licenciada cunha [licenza][licenza] libre calquera podería adaptala para as súas necesidades específicas e así facer medrar o aplicativo.

## 5. Necesidades

**ProxectOS** desenvólvese co obxectivo de cubrir as necesidas que xurden á hora de xestionar, organizar, levar a trazabilidade e estimar os custes, tanto en tempo como económicos* dun proxecto de creación de software.

Na actualidade, como se comenta máis adiante no apartado [6.2. Competencia][competencia], existen varias alternativas para dar cobertura a estas necesidades e probablemente o fagan con suficiente robusted para o teu negocio, daquela por que empregar **ProxectOS**? Podes optar por esta solución por varios motivos, quizais porque buscas unha ferramenta sinxela de empregar, pode que queiras ter a posibilidade de adaptar unha ferramenta pequena ó teu modelo de negocio ou simplemente porque che guste empregar software libre.

O obxetivo deste proxecto é principalmente académico aínda que tamén hai unha compoñente persoal que influíu na decisión de acometelo. Ata o momento de comezar con este proxecto nunca me plantexara o uso un software específico para a xestión dos meu proxectos personais, sempre empreguei ferramentas como o panel de xestión de incidencias dun servidor na nube de git como o de [gitlab] ou o xestor de proxectos de [Odoo][odoo], pero por unha banda os xestor de incidencias de [gitlab] é pouco operativo para ter centralizada a información de tódolos proxectos que teño e a ferramenta de [Odoo][odoo] é demasiado pesada para este único propósito.

Outro motivo persoal para levar a cabo **ProxectOS** é que me apetece facer algo no que poida experimentar e facer probas sen a presión de que sexa un produto comercial ó cal lle tes que dar unha estabilidade rigurosa antes de liberar unha versión definitiva, non quero dicir que co software libre non haxa que ter ese mesmo compromiso pero considero que non é o mesmo nivel de responsabilidade que cun proxecto comercial.

> **NOTAS:**
> *: a estimación económica calcularase a través dunha relación de prezo por hora.

## 5.1. Cuestións

- Como se pode responder a esta necesidade?
  - // TODO:
- Que pode facerse para cambiar este estado de cousas?
- Como podemos contribuír desde a nosa situación a que o problema se resolva?
  - // TODO:
- Que medios, actividades e recursos van poñer en xogo?
  - // TODO:
- Que actividades van realizar?
  - Desenvolvemnto da aplicación.
- Con qué metodoloxía vai levar a cabo o traballo?
  - Vou a empregar metodolixías áxiles, ou cando menos intentareino. Pretendo dividir o proxecto en Historias de produto e ir dividindo o traballo en sprints de 1 semana.
- Que persoas serían precisas para realizar o proxecto con éxito?
  - Para os obexectivos básicos 1, para poder facer un produto de mellor calidade alomenos 2, unha para o desenvolvemento e outra para os test.
- Con canto tempo se conta?
  - 2 meses e medio.
- Canto tempo se necesita?
  - Estimo que con 2 meses de desenrolo e 15-20 días de probas sería suficiente.

Recurso: [Guía para a elaboración de proyectos. Gobierno Vasco.](https://www.pluralismoyconvivencia.es/upload/19/71/guia_elaboracion_proyectos_c.pdf) (páxina 26 e seguintes)

## 6. Modelo de negocio

Ó tratarse dun software libre a meta principal deste software non é acadar un benficio económico directo por medio da súa comercialización como produto final a clientes, senón de poder mellorar a profesionalidade e o rendemento dun pequeno equipo de programadores e programadoras que non estean en disposición de adquir licencias privativos de produtos máis grandes ou que simplemente desexen optar por una solición sinxela e adaptable ás súas necesidades presentes e futuras.

Tamén debido ó ámbito profesional ó que vai dirixido o aplicativo é díficil sacar un rendemento económico a través do soporte e/ou mantemento, aínda que podería darse o caso.

Se se quixese sacar un rendemento económico só vexo dúas posibilidade de negocio:

1. **Vender o produto como servizo** e así aforrarlle ó cliente a infraestrutura necesaria para mantelo funcionando. Para que esta sexa unha vía de comercialización real tamén considero que se debería ampliar o público obxectivo para ter un nicho de mercado sen as capacidades técnicas para o despregamento, mantemento e ampliación de características.
2. Deribada da anterior se se quixese ofrecer o servizo de xeito gratuíto poderíase **insertar publicidade** no sitio web que dea acceso ó mesmo.

Dito isto este non é un produto do que espere sacar un beneficio económico directo, senón, máis ben, académico e persoal polo que queda fora do obxectivo deste proxecto plantexar un modelo de negocio real.

### 6.1. Viabilidade

#### 6.1.1. Viabilidade técnica

Os requerimentos técnicos dependerán da escala na que se implante o aplicativo pero en termos xerais ó tratarse dun aplicativo enfocado á web non se precisará de equipos de grande potencia para a súa posta en marcha.

En canto ós requisitos de instalación e configuración pretendese facilitar a súa implantación acompañando o código con scripts que axuden á instalación e á configuración básica de **ProxectOS**.

#### 6.1.2. Viabilidade económica

Como xa comentei no apartado [6. Modelo de negocio][modeloNegocio] non se pretente sacar un beneficio económico polo que as posibles perdas son asumidas como unha parte natural do desempeño deste proxecto. En canto a se compensa ou non levar a cabo este traballo todo dependerá dos obxectivos que se plantexen ó comezar co mesmo. Como xa comentei anteriormente a motivación principal da posta en marcha deste proxecto non é económica senón académica e tamén personal. Como defensor da filosofía que hai detrás do software libre gustaríame aportar algo á comunidade, aínda que probablemente non teña unha difusión moi ampla, e de ahí o tipo de [licenzamento][licenza] de **ProxectOS**.

Por outra banda sempre é interesante ter unha ferramenta que se poida adaptara ás casuísticas concretas da túa empresa ou situación polo que tamén haberá que ter en conta a cantidade de tempo e recursos da que se dispón para esta materia.

De tódolos xeitos si é posible sacar un rendemento ecónomico indirecto e así "recuperar" esas perdas grazas as características do software libre, como por exemplo:

- Minimizar os custes de mantemento e actualización do software xa que o desenvolvemento de novas características e a resolución de bugs estaría en mans, potencialmente, dun gran número de programadores e programadoras
- Detección máis rápida de erros ó ter acceso a este software usuarios de todo o mundo, o cal facilita a súa solución
- Posibiliddade de abarcar máis sectores de mercado xa que calquera podería partir deste proxecto como base para adaptalo a un uso que non se contemplase inicialmente
- Mellora das capacidades profesionais propias ó ter acceso ó código escrito por multitude de persoas e así ver disintas solucións a un problema dado (esto tamén se pode aplicar a calquera que vexa o código deste proxecto)

Este último bloque depende en gran medida da aceptación e promoción que se lle dea ó proxecto dentro da comunidade de software libre, pero aínda que non se acadesen estes beneficios, obtelos só sería posible por medio desta vía de licenzamento e no peor dos casos non implicaría ningún custe adicional sobre a inversión necesaria para a mesma solución cunha licenza totalmente pechada, é polo tanto un punto de valor engadido o mero feito de ter a posibilidade de conseguir o apoio de máis xente para o mantemento e evolución do proxecto.

### 6.2. Competencia

Como se pode ver cunha rápida búsqueda pola web existen moitas solucións para cubrir as necesidades que **ProxectOS** intenta abordar, exemplos de comparativas:

- [Los 10 Mejores programas de Gestión de Proyectos][asesorias.com]
- [Mejor software de gestión de proyectos][softwarepara.net]

Entón por que interesarse por **ProxectOS**? Como se pode ver nos artigos de exmplo case tódolos aplicativos descritos teñen algunha función premium cun custe adicional e aínda que as súas versións gratuítas están máis maduras que **ProxectOS** en moi poucos casos ofrese a posibilidade de acceder ó código fonte para poder mellorar e ampliar as características da túa plataforma.

### 6.3. Promoción

Dado o carácter libre do proxecto non vexo ningunha causa que xustifique unha inversión económica directa na promoción do mesmo, debido a esto as fórmulas elixidas para a súa promoción serán as seguintes:

- Técnicas elixidas:
  - Redes sociais.
  - Páxina web.
  - Posicionamento web.
  - Participación en eventos de promoción do software libre.

Evidentemente todo gasto de tempo supón un custo pero ó ser un proxecto voluntario cada participante no proxecto poderá invertir a cantidade de esforzo que considere oportuna.

### 6.4. Modelo de negocio

Como se comentou anteriormente no apartado [Modelo de negocio][modeloNegocio] non hai un modelo de negocio como tal pero no caso de intentar sacar un rendemento económico obtaríase por:

1. **Vender o produto como servizo** e así aforrarlle ó cliente a infraestrutura necesaria para mantelo funcionando. Para que esta sexa unha vía de comercialización real tamén considero que se debería ampliar o público obxectivo para ter un nicho de mercado sen as capacidades técnicas para o despregamento, mantemento e ampliación de características.
2. Deribada da anterior se se quixese ofrecer o servizo de xeito gratuíto poderíase **insertar publicidade** no sitio web que dea acceso ó mesmo.

[//]: # (Listado dos links empregados)

   <!-- Licencia -->

   [licenza]: <../../LICENSE.md>

   <!-- Enlaces internos -->

   [introducion]: <#1_Introdución>

   [obxectivo]: <#2_Obxectivo>

   [definicions]: <#3_Definicións>

   [apiWiki]: <https://es.wikipedia.org/wiki/Interfaz_de_programaci%C3%B3n_de_aplicaciones>

   [audiencia]: <#4_Audiencia>

   [modeloNegocio]: <#6_Modelo_de_negocio>

   [competencia]: <#6_2_Competencia>

   <!-- Enlaces a terceiros -->

   [asesorias.com]: <https://asesorias.com/empresas/programas-gratis/software-gestion-proyectos/>

   [softwarepara.net]: <https://softwarepara.net/gestion-de-proyectos/>

   [gitlab]: <https://www.gitlab.com>

   [odoo]: <https://www.odoo.com/es_ES/>