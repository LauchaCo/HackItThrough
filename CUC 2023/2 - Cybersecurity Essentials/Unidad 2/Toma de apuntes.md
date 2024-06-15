## Los principios de seguridad

- __Confidencialidad__: Previene la divulgacion de informacion a las personas los recursos o procesos no autorizados.
- __Integridad__: Hace referencia a la precision, la uniformidad y la confiabilidad de datos. 
- __Disponibilidad__: Se refiere a que el recurso o informacion este disponible cuando sea necesaria.

### Estados de los datos

- __Datos en transito__
- __Datos almacenados__
- __Datos en proceso__

### Medidas para proteger los datos

- __Tecnologias__: Significa saber manejar una gran diversidad de herramientas para mantener a las personas lejos de los recursos que se desea proteger.
- __Politicas y practicas__: Son establecidas para permitir a los usuarios de un recurso mantenerse seguros y seguir practicas adecuadas.
- __Personas__: Los especialistas deben esforzarse en siempre estar aprendiendo y actualizandose en los nuevos ataques y tecnicas que surgen.

## Principio de confidencialidad

La __confidencialidad__ previene la divulgacion de informacion a las personas, los recursos o procesos no autorizados. Las organizaciones restringen el acceso a la informacion para que solo operarios autorizados puedan acceder a esta.
Es una labor de la organizacion el entrenar a los empleados en las mejores practicas para asi protegerse no solo para beneficio propio sino de toda la organizacion en si. Alguno de los metodos mas comunes para mantener la confidencialidad son el cifrado de datos, la autenticacion y el control de acceso.

### Proteccion de la privacidad de los datos

En una organizacion hay 2 grandes tipos de datos: los publicos y los confidenciales. Estos ultimos son los que toda organizacion debe esforzarse en resguardar. Los datos confidenciales a su vez se separan en 3 grupos:
- La informacion personal es la informacion de identificacion personal (PII) que lleva hacia una persona. Ej.: Numero de seguridad social, Historias clinicas, Numeros de tarjetas de credito y Registros financieros.
- La informacion comercial es la informacion que incluye todo lo que representa un riesgo para la organizacion si el publico o competencia lo descubre. Ej.: Secretos comerciales, Planes de adquisicion, Datos financieros y Informacion del cliente.
- La informacion clasificada es informacion que pertenece a una entidad gubernamental clasificada por su nivel de confidencialidad. Ej.: Maxima confidencialidad, Secretos, Registros confidenciales y Restringidos.

### Control de acceso

Este define varios esquemas de proteccion de datos que evita el acceso no autorizado. El concepto de AAA involucra tres servicios de seguridad: Autenticacion, Autorizacion y Auditoria. Estos servicios son el principal marco para controlar el acceso.

- Autenticacion: Verifica la identidad de un usuario para evitar el acceso no autorizado. Los usuarios deben probar su identidad mediante unas credenciales o:
	- Algo que saben: Una contraseña
	- Algo que tienen: Un token o tarjeta
	- Algo que son: Una huella digital
- Autorizacion: Los servicios determinan a que recursos pueden acceder los usuarios, junto con las acciones que estos pueden realizar. Algunos administradores de sistemas logran esto con una lista de control de acceso (ACL). Una ACL determina si un usuario puede o no acceder a un recurso dependiendo de un criterio previamente establecido como horas de trabajo, si esta autenticado, etc.
- Contabilidad: Rastrea toda la actividad del usuario, incluyendo los sitios que visita, que cambios realizo y cuanto estuvo en ellos. En la ciberseguridad el sistema funciona de la misma manera. Este se encarga de registrar cada una de las transferencias de datos y proporciona resultados de auditoria. Un administrador puede habilitar estas auditoria mediante las politicas de una computadora.

### Leyes y responsabilidades

La confidencialidad y la privacidad a nivel legal son tratadas de distinta forma, siendo la privacidad el uso adecuado de datos pertenecientes a un usuario. Debido a la naturaleza de pertenecer a un tercero la organizacion debe solicitar el acceso a estos datos a su respectivo dueño, el cual mediante una firma puede autorizar o denegar su uso. Pasando a la confidencialidad, esta hace referencia a mantener la informacion lejos del alcance de un tercero no autorizado al uso de la informacion.
Debido al creciente numero de datos que son generados dia a dia es crucial que las empresas que analizan y recopilan datos tengan una buena politica en cuanto a la seguridad y manejo de datos.

## Principio de integridad de los datos

La integridad es la precision, uniformidad y confiabilidad de los datos durante su ciclo de vida. Los datos sufren una gran cantidad de cambios y operaciones, por lo cual es crucial que las entidades no autorizadas no tengan ningun tipo de poder sobre estos datos.
Algunos de los metodos para mantener la integridad son: funcion de Hash, comprobaciones de validacion de datos, comprobaciones de consistencia de los datos y los controles de acceso. 

#### La necesidad de contar con la integridad de datos

La integridad es un componente fundamental de la seguridad y su necesidad se hace cada vez mas notoria a medida que la informacion de las organizaciones sea mas sensible y necesite ser mas exacta. Hay varios niveles de criticidad:
- Nivel critico: Aplicado en entes como Servicios de salud y de emergencia
- Nivel alto: Aplicado en comercio electronico y analisis
- Nivel medio: Ventas en linea y motores de busqueda
- Nivel bajo: Blogs y sitios de publicaciones personales.

### Verificaciones de la integridad

Una verficacion de la integridad es una manera de medir la uniformidad de una recopilacion de datos. Un ejemplo de esto son los checksums. Este metodo se lleva a cabo en ambas puntas de la comuniciacion (Lo realiza la persona que envia los archivos y la que los recibe) y consta en convertir todos los archivos a sistema binario y sumarlos para asi obtener un numero, si despues de realizar la misma operacion en la maquina destino los numeros coinciden la informacion es correcta.
Las funciones actuales de hash mas conocidas son MD5, SHA-1, SHA-256 y SHA-512. Estas actuan de la misma forma que la citada anteriormente con el unico cambio de que en vez de convertir los archivos a binario y sumarlos se aplican algoritmos complejos de hashing.
Una de las principales maneras de mantener los datos con una integridad precisa es la de tener copias de seguridad periodicas y precisas para asi siempre tener los datos resguardados en caso de un imprevisto.

## Principio de disponibilidad

Es el principio que se utiliza para describir la necesidad de mantener las disponibilidad de los sistemas y servicios de informacion en todo momento. Algunos ataques conocidos a este principio es el DDoS. Luego, pasando con los metodos de mitigacion, incluyen la redundancia del sistema, las copias de seguridad del sistema, mayor recuperabilidad del sistema, mantenimiento del equipo, sistemas operativos y software actualizados y planes para recuperarse facilmente de imprevistos.

### Los cinco nueves

En la actualidad siempre estamos conectados, por lo cual, es necesario tener una continua disponibilidad. El termino "Alta disponibilidad" describe los sistemas diseñados para evitar el tiempo de inactividad. La alta disponibilidad asegura un nivel de rendimiento por un periodo mas alto de lo normal. Los sistemas de este estilo suelen incluir tres principios de diseño:
- Eliminar puntos sencillos de falla: Hardware propenso a fallar, tener varias rutas o conexiones, tener componentes redundantes, etc.
- Proporcionar una conexion cruzada confiable: Fuentes de alimentacion redundantes, sistemas de energia de respaldo y sitemas de comunicacion de respaldo.
- Detecte fallas a medida que se producen.
El objetivo es seguir funcionando en capacidades extremas. Una de las practicas mas conocidas es la de los cinco nueves. Esta practica hace referencia a tener una efectividad del 99.999%, es decir, estar inactivo menos de 5,26 minutos al año.

### Asegurar la disponibilidad

Las organizaciones pueden hacer los siguiente para mantener la disponibilidad:
- Realizar el mantenimiento del equipo
- Realizar actualizaciones del SO y del sistema
- Realizar las pruebas de copia de respaldo
- Realizar una planificación para evitar desastres
- Realizar implementaciones de nuevas tecnologías
- Realizar el monitoreo de actividades inusuales
- Realizar la prueba de disponibilidad

## Datos almacenados

### Tipos de almacenamiento de datos

Los datos almacenados hacen referencia a datos que se encuentran en algun espacio de almacenamiento mientras no son requeridos por ningun usuario o proceso. Estos datos pueden ser almacenados de manera local o en red. Existen varias formas de almacenar datos.
- __Almacenamiento de conexion directa__ (DAS): Proporciona almacenamiento conectado a una computadora. Una unidad de disco duro o una unidad de memoria flash USB son un ejemplo de almacenamiento de conexion directa.
- La __Matriz redundante de discos independientes__ (RAID): Utiliza varios discos duros en una matriz, que es un metodo para combinar varios discos duros de modo que el sistema operativo los vea como un solo disco. RAID proporciona un mejor rendimiento y una mejor tolerancia a fallos
- Un __Dispositivo de almacenamiento conectado a la red__ (NAS): Es un dispositivo de almacenamiento conectado a la red que permite el almacenamiento y recuperacion de datos de manera centralizada por parte de los usuarios autorizados de la red. Estos dispositivos son flexibles y escalables, lo cual significa que los administradores puede aumentar el tamaño segun sea necesario. 
- Una __Arquitectura de red de area de almacenamiento__ (SAN): Es un sistema de almacenamiento con base en red. Estos se conectan a la red mediante interfaces de alta velocidad que permiten un mejor rendimiento y la capacidad de conectarse varios servidores a un repositorio centralizado de almacenamiento en disco.
- __Almacenamiento en la nube__.

### Desafios en la proteccion de datos almacenados

Esta es una tarea dificil. Para mejorar este almacenamiento normalmente las empresas se encargan de automatizar y centralizar las copias de respaldo de los datos.
El almacenamiento mas dificil de proteger es el de conexion directa, esto es debido a que estos datos son propensos a ataques de host local llevados a cabo por atacantes externos. Estos datos locales tambien pueden incluir datos de copias de respaldo manuales o automaticas. Las organizaciones deben establecer reglas para asi limitar los tipos de datos que pueden ser almacenadas de forma conexion directa. Estos tipos de datos son los previamente marcados "Datos confidenciales".
Los sistemas de almacenamiento en red ofrecen una alternativa mas segura. Dentro de estos dispositivos estan los RAID, NAS y SAN, sistemas los cuales ofrecen un mejor rendimiento y redundancia. A pesar de parecer gozar de solo ventajas estos sistemas son mas complejos de configurar y administrar. Ademas, son encargados de manipular mas datos, por lo cual, si el dispositivo falla, podria conllevar una gran perdida de datos. Los principales desafios de la proteccion son: la configuracion, prueba y supervision del sistema.

## Datos en transito

### Metodos de transmision de datos

La transimision de datos implica el envio de info de un dispositivo a otro. Algunos de los metodos de trasmision son:
- __Red de transferencia__: Utiliza medios extraibles para mover fisicamente los datos de una computadora a otra
- __Redes cableadas__: Utilizan cables para transmitir datos
- __Redes inalambricas__: Utilizan ondas de radio para transmitir datos.
Las organizaciones nunca podran eliminar el uso de una red de transeferencia. 
Las redes cableadas utilizan cables de fibra optica o cobre para transmitir datos y segun la distancia que abarcan pueden ser __redes de area local__ (area geografica local) o __redes de area amplia__ (abarcan grandes distancias).
Las redes inalambricas cada vez reemplazan mas a las redes cableadas debido a su constante crecimiento y mejora en cuanto a velocidades y ancho de banda. Las redes de este tipo extienden la cantidad de usuarios invitados con los dispositivos moviles en la oficina pequeña y oficina domestica (SOHO) y redes empresariales.
Las redes cableadas e inalambricas utilizan paquetes o unidades de datos. El termino se refiere a una unidad de datos que se desplaza entre un origen y un destino de la red. Los protocolos estandar como el protocolo de internet (IP) y el Hypertext Transfer Protocol (HTTP) definen la estructura y formacion de paquetes de datos. Estos estandares son de codigo abierto y estan disponibles para el publico. 

### Desafios en la proteccion de datos en transito

La proteccion de los datos en transmitidos es uno de los trabajos mas desafiantes para un profesional de la ciberseguridad. Algunos de los desafios que afronta un especialista pueden ser: 
- __Proteccion de la confidencialidad de los datos__: Los delincuentes pueden capturar, guardar y robar datos en transito. Los profesionales deben tomar acciones para evitar que esto suceda.
- __Proteccion de la integridad de los datos__: Los ciberdelincuentes pueden interceptar y modificar los datos en transito. Los profesionales implementan sistemas de integridad de los datos que evaluen la integridad y autenticidad de los datos transmitidos para responder a estas acciones.
- __Proteccion de la disponibilidad de los datos__: Los atacantes pueden usar dispositivos falsos para interrumpir la disponibildad de los datos. Un dispositivo movil simple puede presentarse como un punto de acceso inalambrico local y engañar a los usuarios desprevenidos al asociarse con un dispositivo falso. Los delincuentes pueden secuestrar una conexion a un servicio o un dispositivo protegido. Los especialistas pueden implementar sistemas de autenticacion mutua para responder a estas acciones. Estos sistemas requieren que el usuario se autentique con el servidor y solicita que el servidor autentique al usuario.
Algunas contramedidas pueden ser: 
- VPN
- SSL
- IPsec
- Cifrado/Descifrado
- Hash
- Redundancia
- Reserva Activa

## Datos en proceso

### Formas de procesamiento y computo de datos

Esta categoria de datos se refiere a los datos durante la entrada, la modificacion, el computo o el resultado.
La proteccion de la integridad __comienza cuando los datos son obtenidos__ mediante alguna de las vias como resultados de sensores, ingreso manual de datos, etc.. Cada uno de estos metodos representa potenciales problemas a nivel de seguridad de la integridad de datos. Un ejemplo de estos daños a datos, incluye errores en la entrada de datos o sensores del sistema desconectados, con funcionamiento incorrecto o inoperables. Otros ejemplos pueden incluir formatos de datos identificacion erronea, incorrectos o no coincidentes.
La __modificacion__ de los datos se refiere a cualquier cambio de los datos originales, como procesamiento por programa, cambio manual, fallas en el equipo, etc.. Procesos como la encriptacion y desencriptacion, codificacion y decodificacion y cifrado y descifrado son ejemplos de cambios en los datos orginales. El codigo malicioso tambien provoca daños en la informacion.
El daño a datos tambien puede suceder durante el proceso de __salida de datos__. La salida de datos se refiere a los datos que salen de dispositivos especializados como por ej. Impresoras o monitores. El que estos datos sean correctos y que no hayan sufrido un cambio no deseado es esencial para que procesos que sean llevados a cabo con esos datos no se vean nublados, estos procesos pueden ser: Aplicacion de otros procesos, tomas de decisiones, etc.. Ejemplos de daños a los datos incluyen el uso incorrecto de delimitadores de datos, configuraciones incorrectas de comunicación e impresoras configuradas incorrectamente.

### Desafios en la proteccion de datos en proceso

La proteccion contra la modificacion de los datos no validos durante el proceso puede tener un efecto adverso. Los errores en sistemas pueden llevar a verdaderos desastres. Ejemplos de esto son descuentos en tiendas de forma initencional, errores en dispositivos esenciales como por ej: los termotanques NEST de google.
La protección de los datos durante el proceso requiere sistemas bien diseñados. Los profesionales de ciberseguridad diseñan políticas y procedimientos que requieren pruebas, mantenimientos y actualización de sistemas para mantenerlos en funcionamiento con la menor cantidad de errores.
Algunas contramedidas son:
- Control de acceso
- Validacion de los datos
- Duplicacion de los datos

## Tecnologias

### Medidas de proteccion tecnologicas con base en software

Las medidas de proteccion de software incluyen programas y servicios que protegen los sistemas operativos, las bases de datos y otros servicios que operan en las estaciones de trabajo, dispositivos portatiles y servidores. Los administradores aplican las contramedidas o protecciones basadas en software en los hosts individuales o los servidores. Algunas de estas tecnologias son:
- __Los firewalls de software__: Controlan el acceso remoto a un sistema. Los SO generalmente incluyen uno o un usuario puede adquirir o descargar un software de terceros
- __Los escaners de redes y puertos__: Detectan y supervisan puertos abiertos en un host o server.
- __Los analizadores de protocolos o analizadores de firmas__: Dispositivos que recopilan y analizan trafico de red. Identifican problemas de rendimientos, configuraciones incorrectas, identifican apps que funcionan de forma incorrecta, establecen una linea de base y patrones de trafico normal y depuran los problemas de comunicacion.
- __Los escaners de vulnerabilidades__: Son programas informaticos diseñados para evaluar las debilidades en las computadoras o redes.
- __Los sistemas de deteccion de intrusiones (IDS)__: Son sistemas basados en host que se encargan de examinar la actividad. Un IDS genera archivos de registro y mensajes de alarma cuando detecta actividad inusual. Un sistema que almacena datos confidenciales o que proporciona servicios criticos es un candidato para el IDS basado en host.

### Medidas de proteccion tecnologicas con base en hardware

Varias tecnologias basadas en hardware utilizadas para proteger activos de la organizacion:
- Los __dispositivos de firewall__ bloquean el trafico no deseado. Los firewalls contienen reglas que definen el trafico permitido dentro y fuera de la red.
- __Los sistemas de deteccion de intrusiones (IDS)__: detectan signos de ataques o de trafico inusual en una red y envia una alerta.
- __Los sistemas de prevencion de intrusiones (IPS)__: Detectan signos de ataques o de trafico inusual en una red, generar una alerta y toman acciones correctivas.
- __Los sistemas de filtrado de contenido__: Controlan el acceso y la transmision de contenido inaceptable u ofensivo.

### Medidas de proteccion tecnologicas con base en la red

Varias tecnologias, entre estas:
-   __La red privada virtual (VPN)__: Es una red virtual segura que utiliza la red publica. La seguridad de una VPN reside en el cifrado del contenido de los paquetes entre los terminales que definen la VPN
-   __Control de acceso a la red (NAC)__: Requiere un conjunto de verificaciones antes de permitir que un dispositivo se conecte a una red. Algunas verificaciones comunes incluyen la instalacion de actualizaciones de software antivirus o de sistema operativo.
-   __Seguridad de punto de acceso inalambrico__: Incluye la implementacion de la autenticacion y encriptacion.

### Medidas de proteccion tecnologicas con base en la nube

Estas medidas cambian el componente de tecnologia de la organizacion al proovedor de la nube. Los tres servicios principales de computacion en la nube incluyen:
-   __Software como servicio (SaaS)__: Permite que los usuarios tengan acceso al software y las bases de datos de la aplicacion. Los provedores administran la infraestructura. Los usuarios almacenan los datos en los servidores del proovedor en la nube.
-   __Infraestructura como servicio (IaaS)__: Proporciona recursos informaticos virtualizados a traves de internet. El proovedor es el host del hardware, del software, de los servidores y de los componentes de almacenamiento.
-   __Plataforma como servicio (PaaS)__: Proporciona acceso a las herramientas de desarrollo y a los servicios utilizados para proporcionar las apps.
Los proovedores tambien han ampliado su servicio a __IT como servicio (ITaaS)__ que brinda soporte IT a las soluciones previamente enumeradas.
Los proovedores de servicio en la nube utilizan dispositivos de seguridad virtual que se ejecutan en un entorno virtual con un sistema operativo preempaquetado y reforzado que se ejecuta en un hardware virtualizado.

## Formacion, Conocimiento y Capacitacion

### Como implementar la capacitacion y formacion en ciberseguridad

Invertir mucho en tecnologia no variara el resultado si las personas son el eslabon mas debil en el area de la seguridad. Esto debido a que un empleado puede llevar a cabo una accion maliciosa sin siquiera tener intenciones. Algunas de las formas de capacitar son:
-   Hacer de la capacitación en el conocimiento de la seguridad una parte del proceso de incorporación de los empleados
-   Vincular el conocimiento de la seguridad con los requisitos o las evaluaciones de rendimiento
-   Realizar sesiones de capacitación en persona
-   Completar los cursos en línea
El reconocimiento de la seguridad debe ser un proceso continuo dada la evolucion de la tecnologia.

### Establecimiento de una cultura de conocimiento de la ciberseguridad

Los miembros de una organizacion deben tener en cuenta las politicas de seguridad y tener el conocimiento para hacer de la seguridad algo cotidiano.
Un programa de reconocimiento de seguridad depende de:
- El entorno de la organizacion
- El nivel de amenaza
La creación de una cultura de conocimiento de la ciberseguridad es un esfuerzo continuo que requiere el liderazgo de la administración superior y el compromiso de todos los usuarios y empleados. La modificación de la cultura de la ciberseguridad de una organización comienza con el establecimiento de políticas y procedimientos por parte de la administración. Por ejemplo, muchas organizaciones tienen días de concientización sobre la ciberseguridad. Las organizaciones también pueden publicar mensajes y señalizaciones para aumentar el conocimiento general sobre ciberseguridad. La creación de talleres y seminarios de orientación en ciberseguridad ayudan a aumentar la conciencia.

## Politicas y procedimientos de ciberseguridad

### Politicas

Una politica de seguridad es un conjunto de objetivos de seguridad para una empresa que incluye la regla de comportamiento para los usuarios y administradores y especificar los requisitos del sistema.
Una politica de seguridad completa logra varias tareas:
- Demuestra el compromiso de la organizacion con la seguridad.
- Establece las reglas para el comportamiento esperado.
- Garantiza la uniformidad en las operaciones del sistema, el software y la adquisicion y uso de hardware, y el mantenimiento.
- Define las consecuencias legales de violaciones.
- Brinda al personal de seguridad el respaldo de la administracion.
Las politicas se encargan de informar a todo aquel atado a estas de los requisitos para proteger la tecnologia y activos de informacion. Una politica tambien especifica los mecanismos para cumplir con la seguridad.
Una politica generalmente incluye:
- __Politicas de autenticacion e identificacion__: Determina las personas autorizadas para acceder a recursos de la red y describen los procedimientos de verificacion.
- __Politicas de contraseña___: Garantiza que las contraseñas cumplan con requisitos minimos y se cambien periodicamente.
- __Politicas de uso aceptable__: Identifican los recursos y el uso de red aceptables para la organizacion. Tambien pueden identificar las consecuencias de las violaciones de la politica.
- __Politicas de acceso remoto__: Identifican como los usuarios remotos pueden obtener acceso a la red y cual es accesible.
- __Politicas de mantenimiento de red__: Especifican SO de los dispositivos de la red y los procedimientos de actualizacion de software de los usuarios finales.
- __Politicas de manejo de incidentes__: Describen como se manejan los incidentes de seguridad.
Uno de los componentes mas comunes en una politica de seguridad es una politica de uso aceptable (AUP). Este componente define que pueden y no pueden hacer los usuarios con los componentes del sistema. El AUP debe ser redactado de la forma mas explicita posible para evitar malinterpretaciones. Un ejemplo es un AUP que explicite las paginas web, grupos informativos o aplicaciones de uso intensivo de banda ancha prohibidos en el espacio laboral.

### Estandares

Los estandares ayudan al personal de IT a mantener la uniformidad en el funcionamiento de la red. Los documentos sobre estandares proporcionan las tecnologias que los usuarios o programas necesitan, ademas de requisitos o criterios del programa que una organizacion debe seguir. Esto permite mejorar la eficiencia y simplicidad en el diseño, mantenimiento y resolucion de problemas para el personal IT.

### Pautas

Las pautas son una lista de sugerencias sobre como hacer las cosas de forma mas eficaz y segura. Son similares a los estandares pero normalmente son mas flexibles y no obligatorias. Las pautas definen como se desarrollan los estandares y garantizan el cumplimiento de las politicas de seguridad general.
Algunas de las pautas mas utiles conforman las mejores practicas de una organizacion. Ademas de las mejores practicas que define la organizacion, las pautas tambien estan disponible a partir de lo siguiente:
- Insitituto Nacional de Normas y Tecnologia (NIST), Centro de recursos de Seguridad Informatica.
- Departamento de Seguridad Nacional (NSA), Guias para las configuraciones de seguridad.
- El estandar de criterios comunes.

### Procedimientos

Los documentos de procedimiento son mas detallados que los de estandares y las pautas. Los procedimientos incluyen detalles de implementacion que contienen generalmente instrucciones paso a paso y graficos.

## El modelo de ciberseguridad de ISO

### Descripcion general del modelo

Es un modelo para guiar a un especialista en ciberseguridad en sus tareas. El modelo ISO es para un especialista en ciberseguridad lo que el OSI es para un Ingeniero en redes. Ambos proporcionan un marco para comprender y abordad tareas complejas.

### Dominios de la ciberseguridad

La norma ISO/IEC 27000 es un estandar de seguridad informatica publicado en 2005 y revisado en 2013. Este estandar no es obligatorio pero es empleado por la mayoria de paises cuando se refiere a ciberseguridad.
Estos estandares describen la implementacion de un sistema de administracion de la seguridad de la informacion (ISMS) completo. Un ISMS incluye todos los controles administrativos, tecnicos y operativos para mantener la informacion segura dentro de una organizacion. Doce dominios representan los componentes del estandar ISO 27000. Estos doce dominios sirven como base comun para desarrollar estandares de seguridad organizativa y practicas eficaces de administracion de la seguridad. Ademas, facilitan la comunicacion entre organizaciones. Estos doce dominios son:
- Evaluacion de riesgos.
- Politica de seguridad.
- Organizacion de la seguridad informatica. 
- Gestion de activos.
- Seguridad de los recursos humanos.
- Seguridad fisica y medioambiental.
- Administracion de operaciones y comunicaciones.
- Adquisicion, desarrollo y mantenimiento de sistemas informaticos.
- Control de acceso.
- Administracion de incidentes de seguridad informatica.
- Administracion de la continuidad empresarial.
- Cumplimiento.

### Objetivos de control

Los doce dominios constan de objetivos de control definidos en la parte 27001 del estandar. Los objetivos de control definen los requisitos de alto nivel para implementar un ISM completo. El ISO 27001 es utilizado para definir las politicas de seguridad de una empresa. Estos objetivos proporicionan una lista de comprobaciones para utilizar durante las auditorias de administracion de seguridad. Muchas organizaciones tienen que aprobar una auditoria ISMS para obtener una designacion de cumplimiento del estandar ISO 27001.
La certificacion y el cumplimiento proporcionan confianza para dos organizaciones que deben confiar sus datos y las operaciones confidenciales de c/u. Las auditorias de cumplimiento y de seguridad demuestran que las organizaciones aumentan continuamente su sistema de administracion de seguridad.

### Controles

El estandar ISO/IEC 27002 define los controles del sistema de administracion de seguridad informatica. Los controles son mas detallados que los objetivos. Los objetivos de control indican a la organizacion lo que debe hacer. Los controles definen como alcanzar el objetivo.
Según el objetivo de control, para controlar el acceso a las redes mediante los mecanismos de autenticación adecuados para los usuarios y los equipos, el control sería el siguiente:
___Utilice contraseñas seguras. Una contraseña segura consta de al menos ocho caracteres que son una combinación de letras, números y símbolos (@, #, $, %, etc.) si están permitidos. Las contraseñas distinguen entre mayúsculas y minúsculas, de modo que una contraseña segura contiene letras en mayúsculas y minúsculas.___
Los profesionales de ciberseguridad reconocen lo siguiente:
- Los controles no son obligatorios, sino que estan ampliamente aceptados y adoptados
- Los controles deben mantener la neutralidad del proovedor para evitar la imagen de que respalda a un producto o empresa especifica.
- Los controles son como las pautas. Esto significa que puede haber mas de una manera de cumplir con el objetivo.

## Uso del modelo de ciberseguridad de ISO

### El modelo de ciberseguridad de ISO y la triada de CID

La norma ISO 27000 es un marco de trabajo universal para cada organizacion. Para utilizar este marco de manera eficaz, una organizaciones debe restringir dominios, objetivos de control, y los controles que aplican a su entorno y sus operaciones.
Los objetivos de control del ISO 27001 funcionan como una lista de verificacion. El primer paso que una organizacion toma es para ver si se cumplen o no. La mayoria de organizaciones generan un documento llamado Declaracion de aplicabilidad (SOA). La SOA define los objetivos de control que la organizacion necesita usar.
Las distintas organizaciones dan mas importancia a la confidencialidad, integridad y disponibilidad segun el tipo de empresa. Google, por ejemplo, da mas importancia a la integridad y a la disponibilidad, mientras que Amazon pone todo su capital en la disponibilidad, por nombrar un caso.
Una organizacion adapta su uso de los objetivos de control y los controles disponibles a lo que mejor se adapta a sus intereses con respecto a la triada CID.

### El modelo de ciberseguridad de ISO y los estados de los datos

Los diferentes grupos dentro de una misma organizacion son responsables por los datos en cada uno de estos estados. Los controles de ISO abordan especificamente los objetivos de seguridad de los datos en cada uno de los tres estados.

### El modelo y los mecanismos de proteccion de la Ciberseguridad de ISO

Los objetivos de control de ISO 27001 se relacionan directamente con las politicas, los procedimientos y las pautas de ciberseguridad de la organizacion que la administracion superior determina. Los controles de ISO 27002 proporcionan direccion tecnica. 