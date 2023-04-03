# KATALON

Herramienta para automatizar pruebas de software "integración/sistema" de tipo "funcional"

# Para qué sirven las pruebas?

- Para tratar de encontrar el mayor número posible de defectos en un sistema (buscando directamente DEFECTOS o FALLOS)
- Cuando aparece un FALLO -- debug --> Identificar el DEFECTO
    Aportar luz cuando hay un problema
    Pruebas deben ser atómicas: Se deben centrar en una única característica...
- Para garantizar la calidad del software
- Para garantizar que el sistem cumple con unos requisitos
- Identificar ERRORES
- Para conocer más de mi sistema

# Vocabulario que usamos en el mundo del testing

- ERROR     Es algo comedido por un ser humano
- DEFECTO   Al cometer un ERROR un humano, puede introducir un DEFECTO en el sistema
- FALLO     Ese defecto puede MANIFESTARSE o no en forma de FALLO

# Tipos de pruebas de software

## Tipos de pruebas en base al NIVEL DE LA PRUEBA

- Unitarias             Prueban un componente** AISLADO del sistema
- Integración           Prueban la COMUNICACION entre componentes                           KATALON
- Sistema (End2End)     Prueban EL COMPORTAMIENTO del sistema en su conjunto                KATALON ****
  - Aceptación            Las que se requieren para aceptar el producto/sistema

**componente???
- Clase
- Método
- Query

## Tipos de prueba en base al Objeto de prueba

- Pruebas estáticas                 Las que NO requieren poner el sistema en funcionamiento
    - Revisión de requisitos
                            R1. El sistema debe responder en unos tiempos adecuados
                            R2. El sistema debes responder en menos de 200ms cada petición
                            R3. El sistema, instalado en un equipo con éstas características XXXX
                                y sometido a una carga de trabajo YYYY
                                debe responder a un determinado flujo de trabajo con un percentil 95% inferior a 200ms
    - Calidad de código -> MANTENIBILIDAD DEL PRODUCTO.
                            Estas pruebas eran las que antes hacía un SENIOR
                            Hoy en día esto está AUTOMATIZADO: SONARQUBE
    - Revisión de un modelo de datos
- Pruebas dinámicas                 Las que SI requieren poner el sistema en funcionamiento
  - Funcionales                     Las que se centran en la funcionalidad                  KATALON ****
                                    JUNIT, TESTNG , MSTEST, TESTUNIT, MOCHA
                                    POSTMAN, SOAPUI, Cypress, Karate, ReadyAPI
  - No Funcionales                  Las que se centran en otros aspectos
      - Carga                           Degradación de los tiempos de respuesta ante: 
                                            - Volumenes grandes de datos
      - Estres                          Degradación de los tiempos de respuesta ante: un volumen alto de peticiones
      - Rendimiento                     Tiempos de respuesta de mi sistema
                                        JMETER, LOADRUNNER
      - Alta disponibilidad             Tolerancia a fallos del sistema
      - Pruebas de backups / restore
      - Experiencia de usuario

# En base a el mecanismo de comunicación con el sistema

- Pruebas de APIs                       Me comunico directamente con el código
- Pruebas de interfaz gráfica           Me comunico a través de una interfaz gráfica (navegador, teléfono móvil)     KATALON *
- Pruebas de APIs REST/SOAP             Me comunico a través de uno de esos mecanismos.                              KATALON

# Por qué queremos automatizar las pruebas?

Porque cuando las hacemos VARIAS VECES (la misma prueba) me sale más ECONÓMICO!
    Quiero la misma exacta prueba muchas veces (todos los días)
    Hay pequeñas variantes entre las pruebas.... que queremos ejecutar
        App web. (CITAS EN EL MINISTERIO DE HACIENDA)
            Pruebas de la web. En qué navegador las hago?
                - Firefox
                - Chrome
                - Chromium
                - Opera
                - Safari
            Sobre qué SO?
                - Windows 10
                - Windows 11
                - Windows 8
                - MacOS
                - Linux
                - iOS
                - Android
          - En qué tipo de dispositivo?
                - PC
                - Tablet
                - Movil
          - ** En internet tenemos granjas que podemos alquilar por 200€ con más de 800 configuraciones diferentes 

# Hoy en día hacemos las pruebas muchas veces? Repetimos las pruebas?

Por qué? Cambio en la forma de trabajo que usamos hoy en día. METODOLOGIAS TRADICIONALES (en cascada) ---> AGILES

# Metodología ágil

SCRUM, Extreme programming

Y el producto lo entrego al cliente de forma incremental!

Queremos hacer entregas en producción cada 2 - 8 semanas

2 semanas de comenzar tengo el primer paso a producción, de una app 100% funcional
    5% de la funcionalidad < PRUEBAS
    
4 semanas de comenzar tengo el segundo paso a producción, de una app 100% funcional
    +5% de la funcionalidad < PRUEBAS
        Repetir las pruebas del 5% anterior <<<< PRUEBAS DE REGRESION
      
6 semanas de comenzar tengo el tercer paso a producción, de una app 100% funcional
    +5% de la funcionalidad
    
De dónde saco la pasta para tanta prueba??? NO LA HAY !!! ~~> AUTOMATIZAR !

# Qué significa AUTOMATIZAR UNA PRUEBA?

Definir los pasos que son necesario realizar para ejecutar una prueba: DEFINIR UNA PRUEBA 
(para hacerla automáticamente o en manual)

Que no requiera intervencación / interacción de una persona física para su ejecución...
Y cómo conseguimos eso?
HACIENDO UN PROGRAMA PARA QUE PRUEBE OTRO PROGRAMA
                                      ^^^^^^^^^^^
                                    SISTEMA PRINCIPAL

Hoy en día los testers los hemos convertido en PROGRAMADORES (que no en desarrolladores)

# Tipos de programas

- Sistema operativo
- Driver
- Libreria
- App web
- Servicio
- Comando
- Script        <<< Una prueba automatizada es un script

# DEVOPS

CI/CD son fases en la adopción de una filosofía DEVOPS

DEVOPS es una filosofía, cultura, un movimiento en pro de la AUTOMATIZACION !

Jenkins... 


# Selenium

Es una herramienta que nos permite automatizar operaciones en un navegador. No es una herramienta de pruebas !

Podemos montar pruebas sobre un navegador WEB usando SELENIUM para automatizar unos trabajos sobre un navegador 
+ JUNIT (para hacer las pruebas)

En lugar de escribir CODIGO DE PROGRAMACION  ( que podríamos y mucha gente lo hace)
En nuestro caso vamos a estar usando KATALON STUDIO, para que sea KATALON el que vaya construyuendo ese programa por nosotros
de forma encubierta... pero sin perder de vista que estamos montando un PROGRAMA !!!!!

Y como tal, hemos de acogernos a las BUBENAS PRACTICAS QUE LLEVAN AÑOS USANDO los desarrolladores de software:
- Nuestro programa tendrá VERSIONES
- Estará controlado en un SISTEMA DE CONTROL DE CODIGO FUENTE (git)

## PRODUCTOS QUE OFRECE SELENIUM

- Selenium IDE          ESTE ES UN POCO DE JUGUETE... Nos echa una manilla a la hora de escribir esos SCRIPTS de pruebas
                        En su lugar vamos a usar nosotros KATALON STUDIO
- Selenium Webdriver    Es una librería que tenemos disponible en MUCHOS LENGUAJES DE PROGRAMACION (PY, JAVA, C#...)
                        que nos permite controlar (a través de un driver) un navegador de internet
- Selenium GRID         Nos permite montar una granja de navegadores, junto con sus drivers,
                        para que pueda ser usada REMOTAMENTE desde un script con Selenium Webdriver

                                                                                            KATALON STUDIO, SELENIUM IDE
                                                                                                VVVV
    SITIO WEB(app) <<<<< NAVEGADOR DE INTERNET <<<< DRIVER <<<<<< SELENIUM WEBDRIVER <<<<< SCRIPT DE PRUEBA
    app mia                 chrome (v.X)            chromedriver(v.X)
                            firefox (v.Y)           ghekodriver(v.Y)
                            edge

Los navegadores tienen una funcionalidad que no solemos usar mucho.
PERMITEN SER CONTROLADOR POR LO QUE LLAMAMOS UN DRIVER DE NAVEGADOR

## Cómo se le dan las órdenes al driver de un navegador

A través del driver, podemos pedir una nueva pestaña o ventana de un navegador.
Y también que navegue a una determinada URL.
La URL se cargará en el navegador... y se mostrará una pantalla (de una web)

Y cómo interactuo ahora con esa WEB???
- El navegador , al final, va a cargar un fichero HTML (página web)
- Ese fichero puede ser ESTATICO, o DINAMICO (haber sido generado por un programa)

Ese HTML le carga el navegador... y genera lo que se denomina un DOM

DOM: Document Object Model.
Es la representación en memoria RAM de un documento HTML...
lo que habitualmente vemos en el navegador cuando damos al botón "INSPECCIONAR" > Herramietas de desarrollador.

El DOM tiene una estructura JERÁRQUICA.

Dentro de esa estructura estan los COMPONENTES sobre los que vamos a interacturar (realizar operaciones):
- Click a un link
- Rellenar un campo de un formulario
- Click en un boitón para enviar un formulario
- Leer un texto de un sitio de la pantalla

HAbitualmente esos COMPONENTES con los que interactuamos los identificamos usando CON NUESTROS OJOS !!!!
Los programas NO TIENEN OJOS !!!!
Y queremos que sea UN PROGRAMA el que interactue con mi página WEB.

Necesitamos buscar una forma de IDENTIFICAR COMPOENENTES Dentro del DOM para que nuestro programa (script de automatización de pruebas) interactúe con ellos

# Cómo puedo identificar un elemento dentro de un DOM?

Hay varias formas:
- Los elementos pueden tener un IDENTIFICADOR... Si lo tiene ES MI MEJOR ALTERNATIVA.
  Según el estandar el ID debe ser UNICO. Si el ID no es único, los desarrolladores la han CAGADO: BUG!!!! DEFECTO !!!
  
    Busca el elmento del DOM cuyo id es "LOGIN" y haz click ahí en ese elemento.

- Si no tengo IDs, tengo que buscar alternativas... 
  En selenium (katalon) se ofrecen varias... SOLO NOS INTERESA 1 de ellas... el resto RUINA GIGANTE !!!!
    - La alternativa se llama XPATH: qué es un estandar del W3C
    XPATH por si solo no me resuelve el problema de identificar elementos... ES SOlO UNA LENGUAJE PARA IDENTIFICARLOS. NADA MAS
    Podré usar ese lenguaje de muchas formas... 
    - Algunas GUAYS
    - Otras RUINOSAS 
  Nada que se genere de forma AUTOMATICA ME VA A SERVIR !!!! TODO TENDRE QUE REVISARLO MANUALMENTE ... TODO <<< LO MAS CRITICO DE USAR SELENIUM / KATALON... y si no tengo experiencia... lo últmo que haré y a lo que menos importancia le daré
            
            //*[@id="pt-login"]/a/span
            /html/body/div[4]/div[1]/nav/div/ul/li[5]/a/span                **** TOTALMENTE FUERA !!!!
                                                                            Es muy frágil... Depende de muchas cositas
            //*[@id="pt-login"]//span
            //*[equals(text(),"Acceder")]

NOTA: IMPORTANTISIMO... 
El principal problema que nos vamos a encontrar al usar Selenium (desde Katalon o no) es
que un script, después de haberlo montado, a los pocos días (o muchos días) nos va a dejar de funcionar.
Y esto va a ocurrir porque los elementos van a dejar de identificarse de la misma en la que anteriormente se estaban IDENTIFICANDO.
Debería de haber CONSENSO entre desarrollo y TESTING en cuanto a la forma de identificar los elementos con los que se va a interactuar en un sitio web:
- TODO ELEMENTO CON EL QUE SE PUEDA INTERACTUAR DEBERIA TENER UN ID !!!!
  Y el equipo de desarrollo DEBE SER CONSCIENDE DE LA RELEVANCIA DE ESTO y actuar en consecuencia!
  Esto es algo que pocas veces va a ocurrir... Sobre todo:
  - En sistemas legacy
  - Cuando desarrollo y testing están desacoplados.

# XPATH

Es un lenguage que nos permite identificar elementos en un dom mediante una RUTA

# TDD. Test Driven Development

Metodología de desarrollo, que consiste en:
- Desarrollar primero las pruebas (Unitarias)
- Empiezo a escribir código hasta que las pruebas se superan... Cuando las tengo en VERDE = TRABAJO CONCLUIDO

# BDD. Behaviour driven development

Metodología de desarrollo, paralela a TDD, que consiste en:
- Desarrollar primero las pruebas de Sistema. Estas habitualmente las hace el equipo de TESTING -> desarrolladores

En esta metodología usamos un lenguaje que se utiliza para expresar las pruebas y los requerimientos (el comportamiento)

Ese lenguaje sse llama Gherkin... y la herramienta que procesa ese lenguaje se llama CUCUMBER
                        vvvv
                        En español



# Me imagino que todos trabajais en apps monolóticas 

Usais JSPs para generar el HTML? Esto es obsoleto a día de hoy.

Antaño, el HTML también se generaba en el SERVIDOR (jsp, asp, php)

Hoy en día hay una división MUY GRANDE entre lo que es 
- FrontEnd          > JS (angularJS, reactJS, vueJS, polymer...)
                        Y esos programas JS donde se ejecutan? En el navegador.
                        Dentro del navegador se generan los HTML que se van a ver en ese navegador
- BackEnd           > Servicios WEB ... que proveen al frontend(esos programas JS) de los datos que deben 
                      represntar en la pantalla

Hoy en día usamos el concepto de SPA (single Page Application)
Una página HTML va MUTANDO. USamos programas JS para solicitar a un servidor (backend) datos
Esos programas generan TROZOS de HTML que se inyectan / modifican en el HTML que está presentando el navegador en pantalla.


# W3C

World Wide Web Consortium

Es una organización que ofrece/publica ESTANDARES que se usan en el mundo WEB:
- HTML
- CSS
- XML
- XPATH *****


# Creando un proyecto en KATALON

Nuestro proyecto irá almacenado dentro de un Sistema de Control de Código fuente : Git
.gitignore: Archivo estandar de git, donde se detallan los arhivos del proyecto que NO DEBEN almacenarse en git
    Se configura bien por defecto.

build.gradle

# Gradle (equivalente a MAVEN, sbt). Microsoft dotnet msbuild. Python poetry. JS: npm, yarn

Es una herramienta que usamos en lenguajes como JAVA o KOTLIN para:
- Ayudar con la gestión de dependencias de mi proyecto
- Ayudan a automatizar algunas tareas repetitivas del proyecto:
  - Su compilación
  - El empaquetado (generar lo que voy a distribuir)
  - Su ejecución
  - La ejecución de pruebas automatizadas sobre mi proyecto

Nosotros estamos montando un software. Y nuestro software (que encubiertamente lo gestiona KATALON)
será un proyecto JAVA que se compila y gestiona a través de GRADLE.

De hecho en un momento dado, no querremos ser nosotros los que ejecutemos este proyecto (estos programas de pruebas)
Quién se encargará de ejecutar los programas de pruebas? GRADLE solicitará la ejecución de los programas de prueba ... y gestionará los mismos... pero a su vez... quién va a allamar a gradle? Un servidor de AUTOMATIZACION:
- JENKINS
- BAMBOO (atlassian)
- TEAMCITY (jetbrains)
- GITHUB Actions
- GITLAB CI/CD
- Travis CI


# Por dejado de Katalon

Tenemos selenium para automatizar trabajo en un navegador.
Además tenemos JUNIT, para realizar pruebas.

JUNIT es una framework (que incluye un montón de librerias) JAVA 


# Framework vs Librería

Librería:  Es un conjunto de funciones reutilizables, que alguien monta... para hacer operaciones muy concretas
           que yo puedo invocar desde mi proeycto.
Framework: Es un conjunto de librerías.... pero además impoenen una metodología de uso para esas librerías.
           Es decir, no es sólo una librería que yo uso y llamos desde mi código
           Es que para usar esa librería tengo que usar ciertas directrices... y organizar mi proyecto de una forma concreta.

En JUnit, nosotros definimos funciones de prueba <- SCRIPTS DE PRUEBAS
Esos métodos siempre tienen la misma estructura:
- Realizo algunas operaciones contra un sistema
- Pruebo que el sistema se ha comportado de la forma adecuada

En JUnit las pruebas (esas funciones o scripts) siempre van a acabar en uno de 3 estados posibles:
- Éxito                             Success: Prueba ejecutada correctamente y se ha verfificado el comportamiento esperado
- No éxito                          Failure: Prueba ejecutada correctamente y NO se ha verfificado el comportamiento esperado
                                             Hemos encontrado un comportamiento diferente al esperado
- Error al ejecutar la prueba       Error:   Prueba no se ha ejecutado correctamente

Al trabajar con JUnit, tendremos el concepto de ASSERTIONS. Aseguraciones <<< ESTO ES LA PRUEBA EN SI MISMA

## Caso de prueba TERUEL EXISTE

1. Abre en un navegador la página web de wikipedia          |
2. En la caja de búsqueda escribe TERUEL                    |   Tareas que hago en un sistema
3. Pulsa sbre el botón de la lupa                           |   En nuestro caso tareas que queremos realizar en AUTOMATICO 
4. Extrae el título de la página a la que has llegado       |   dentro de un navegador: SELENIUM WEBDRIVER
   
5. Asegura que el título ESE que has extraido es: Teruel!   |   Esta es la prueba: JUNIT
    Aseguración (ASSERTION)
        - Asegurame que un texto es igual a otro texto
        - Asegurame que un número es mayor o menos que otro.

Este guión de pruebas (1-4)... define acciones que vamos a realizar sobre algunos componentes
                                                     ACCION                 DATOS                   COMPONENTE              GENERAN RESULTADO
1. Abre en un navegador la página web de wikipedia   Abrir un navegador
                                                     Ir a una URL           https://wikipedia.es

2. En la caja de búsqueda escribe TERUEL             Escribir               Teruel                  Caja búsqueda

3. Pulsa sbre el botón de la lupa                    Pulsar (click)         ~                       Bóton de la lupa

4. Extrae el título de la página                     Recuperar un texto     ~                       Título de la página     TITULO-DE-LA-PAGINA


## Donde queremos que se ejecuten estas pruebas?

Las pruebas que hacen los desarrolladores en su PC me sirven para algo? No me fio.... están maleados
Las pruebas que hacen los testers en su PC me sirven para algo?         No me fio.... están maleados

Queremos un entorno controlado, limpio, parecido al de la realidad...
Tradicionalmente hemos usado lo que llamábamos un ENTORNO DE PRUEBAS, Q&A, PRE-PRODUCCION, INTEGRACION

LA tendencia a día de hoy... es a generar ese entorno desde CERO cada vez que quiero hacer pruebas...
Si del PC del desarrollador no me fio... y del PC del tester tampoco...
De un entorno donde ya he reaklizado 50 instalaciones y pruebas, me fío???? POCO !

Y hoy en día la tendencia es tener entornos de prueba de USAR Y TIRAR.... aqui nos ayudan mucho los CONTENEDORES.

Más adelante montaremos un grid de selenium con contenedores:
- Chrome
- Firefox
- Edge

## Integración Continua... Cuando hablábamos de DEVOPS (Entrega Continua > Despliegue Continuo)

Quiero la última versión que los desarrolladores hayan subido al repo de git, continuamente 
en el entorno de Integración, siendo sometida a PRUEBAS AUTOMATIZADAS.

