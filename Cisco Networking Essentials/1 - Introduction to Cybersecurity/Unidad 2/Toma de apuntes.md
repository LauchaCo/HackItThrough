## Conceptos
- __Vulnerabilidad__: Defecto en un hardware o software
- __Ataque__: Termino que se utiliza para referirse al acto de utilizar un programa escrito para aprovecharse de una vulnerabilidad conocida. Su objetivo es acceder a un sistema, los datos que aloja o a un recurso
- __Buffers__: Los buffers son areas de memoria asignadas para una aplicacion en especifico
- __Malware__: El malware o "Malicious Software" es cualquier codigo que pueda utilizarse para el robo de datos, la evasion de controles de acceso, ocasionar daños o comprometer un sistema.
- __Botnet__: Una Botnet es una red de ordenadores infectados por un malware los cuales cumplen el unico proposito de llevar a cabo una accion que el dueño del malware les dicte. Usualmente estas botnets son de miles de dispositivos y pasan desapercibidas hasta que el hacker decida tomar alguna accion como por ej. llevar a cabo un __DDoS__

### Vulnerabilidades de software
Las vulnerabilidades de software se generan normalmente por errores en el sistema operativo o el codigo de la aplicacion. Estas vulnerabilidades son encontradas casi a diario, generando asi que grandes compañias tengan que sacar actualizaciones casi diarias para arreglar estos errores.

Un conocido equipo de busqueda de vulnerabilidades de software es el conocido como __Project Zero__, este grupo de analistas de aplicaciones fue creado por Google con el unico proposito de encontra zero-days en aplicaciones del mercado

#### Ejemplos
- __SYNful__: Fue una vulnerabilidad descubierta en 2015 para sistemas operativos Cisco. Esta vulnerabilidad genero que los atacantes pudieran tomar el control de decenas, sino miles de Routers, posibilitando asi el monitoreo de las comunicaciones y la capacidad de infectar otros dispositivos en la red. La vulnerabilidad fue introducida debido a un cambio en la version del IOS. La forma manual de verificar esta vulnerabilidad es verificando la integridad de la imagen del IOS y limitar el acceso fisico al equipo solo a personal autorizado

### Actualizaciones
El principal objetivos de estas es el de mantener el propio software actualizado, pero ademas, tiene otro objetivo que es el de mitigar vulnerabilidades

### Vulnerabilidades de hardware
Estas vulnerabilidades son dadas por un defecto a nivel de hardware que causa comportamientos no deseados, generando asi, que los atacantes puedan tomar provecho de esto para beneficio propio. Las vulnerabilidades de hardware tienen una peculiardidad. Esta peculiaridad es que es altamente raro que se encuentre la vulnerabilidad por error, siendo esto un factor clave para fijar el target de los ataques mediante vulnerabilidades de hardware a objetivos de alto calibre. Es por esto ultimo que una proteccion frente a malware y la seguridad fisica son medidas mas que efectivas para un usuario comun.

#### Ejemplos
- Rowhammer: Fue una vulnerabilidad en las memorias RAM que genero que, mediante la reescritura repetida de memoria en las misma direcciones, se pudiese obtener datos de celdas de memoria cercanas a la que estaba recibiendo la sobrecarga, incluso si estas celdas contiguas estaban protegidas.

### Categorias de las vulnerabilidades en seguridad del software
- __Desbordamiento del buffer__: Esta vulnerabilidad se hace presente cuando se escriben datos mas alla de los limites de un buffer. Cuando esto ocurre, la aplicacion accede a memoria asignada a otros procesos. Estos tipos de vulnerabilidades pueden llegar a un bloqueo del sistema, comprometer los datos o hasta llegar a llevar a cabo una escalada de privilegios
- __Entrada no validada__: Esta vulnerabilidad se centra en la falta de verificaciones por parte de la aplicacion al cargar datos en alguna de sus entradas. Este comportamiento puede llegar a causar que la aplicacion tenga comportamientos no deseados si es que se ingresa contenido malicioso. __Ej.__: Si una aplicacion que recibe fotos de un determinado peso es suministrada con una imagen de un peso mayor el buffer se vera afectado, generando asi, una caida de la aplicacion por falta de memoria.
- __Condiciones de carrera__: Esta vulnerabilidad aparece cuando el resultado de un evento es decidido por resultados ordenados o temporizados. Este comportamiento puede ser una fuente de vulnerabilidades si los eventos no se producen en un orden correcto o al tiempo adecuado.
- __Debilidades en las practicas de seguridad:__ Los datos pueden ser protegidos con una gran variedad de tecnicas, entre estas: autenticacion, autorizacion, encriptacion, etc.. Debido a esto, es recomendable que los desarrolladores no creen sus propios algoritmos de seguridad que puede acarrear vulnerabilidades, sino que utilicen librerias ya creadas, aprobadas y verificadas.
- __Problemas de control de acceso__: El control de acceso es controlar quien hace que y va desde la administracion del acceso fisico hasta quien tiene acceso a determinado recurso. Muchas vulnerabilidades aparecen debido a un control de acceso incorrecto o insuficiente.

Gran cantidad de estas tecnicas pueden ser bypasseadas por el simple hecho de hacer el ataque de forma fisica, esto debido a que hay menos seguridad y cosas como la autenticacion para solicitar un archivo son inutiles ante el robo de un HDD por poner un ejemplo. Tecnicas efectivas contra esto pueden ser algunas como la encriptacion del disco para asi prevenir robo o daño al disco

### Categorias del malware
- __Spyware__: Es un malware diseñado para el rastreo y espionaje de usuarios. Algunas funcionalidades comunes de los Spywares son: Rastreo de actividad, recopilamiento de pulsaciones de teclas y captura de datos. Comunmente cuando un spyware desea superar medidas de seguridad lo unico que se limita a hacer es a modificar configuraciones de seguridad. Normalmente el spyware es agrupado junto con software legitimo o con troyanos
- __Adware__: Es software de publicidad que se instala en la maquina de la victima. Este tipo de malware normalmente viene acompañado de Spyware
- __Bot__: Es un malware diseñado para llevar a cabo acciones automaticamente. Usualmente los bots eran inofensivos, sin embargo, ultimamente se les esta dando un uso especifico que son las BotNets
- __Ransomware__: Como su nombre lo indica (Ransom o rescate) este tipo de malware es utilizado normalmente para encriptar todos los datos de un ordenador hasta la recepcion de un pago por parte de la victima. Los ransomwares son esparcidos como un archivo descargado o alguna vulnerabilidad de un software
- __Scareware__: Es un malware el cual se caracteriza por persuadir al usuario a tomar ciertas acciones que podrian perjudicar la integridad o confidencialidad del equipo en funcion del temor que le pase algo a este. Esto es logrado mediante ventanas emergentes semejantes a ventanas del sistema pidiendole al usuario que realice cierta accion para mantener la seguridad de su sistema
- __Rootkit__: Es un tipo de malware muy poderoso, el cual es utilizado como puerta trasera para posibles ataques siguientes. Este tipo de malware se encarga de explotar vulnerabilidades conocidas para realizar un escalamiento de privilegios. Una vez el programa esta asentado y tiene maximos privilegios, se encarga de realizar cambios en los sistemas de deteccion de malware para que este pase desapercibido y sea visto como un simple software. Lo recomendable una vez que un sistema esta infectado con este tipo de malware es limpiar el pc y reinstalar todo por defecto.
- __Virus__: Es un codigo ejectuable malintencionado que viene adjunto a otros archivos, generalmente legitimos. La mayoria de estos malwares requiere la activacion por parte del usuario y puede activarse en una fecha o momento especifico. Este malware puede ser tanto inofensivo, mostrar una foto o ejecutar un sonido, o pueden llegar a ser muy destructivos, eliminar o modificar archivos del dispositivo. La principal caracterisitica de estos ejecutables es que tienen la capacidad de mutar para asi escaparse de sistemas de deteccion de intrusion automatizados.
- __Troyano__: Un troyano es un malware que ejecuta acciones maliciosas bajo la apariencia de operaciones deseadas. Los troyanos normalmente se encuentran adjuntos a imagenes, audios o juegos. Se diferencian de los virus en que estos, a diferencia de los virus, no se adjuntan a un archivo ejecutable.
- __Gusanos__: Los gusanos son codigos maliciosos que tienen la caracteristica de autoreplicarse. Esto lo logran mediante la explotacion automatica de vulnerabilidades especificadas en su codigo. Por lo general un sintoma de la infeccion de un malware de tipo gusano es la realentizacion de las redes en las cuales se encuentra accionando. A diferencia de los virus, este tipo de malware no requiere la participacion activa del usuario, esto es debido a que tienen la capacidad de autoejectuarse, ademas de la de autoreplicacion. Todos los gusanos poseen 3 patrones similares: tienen una vulnerabilidad de activacion, una manera de propagacion y una carga util. Un claro ejemplo de este tipo de infecciones podria ser el gusano "Codigo Rojo". Este gusano infecto a 658 servidores, elevandose rapidamente hasta 300.000 servidores en un lapso de tan solo 19 horas
- __Hombre en el medio (MitM)__: Este tipo de malware posibilita al atacante el control del dispositivo de la victima sin el conocimiento de este ultimo. Gracias a esto el ciberdelincuente puede interceptar y capturar informacion acerca del usuario antes de que este la retransmita al destino. La variedad de formas de ataques MitM es inmensa, sin embargo, el objetivo normalmente es el mismo, "datos financieros".
- __Hombre en el movil (MitMo)__: Es una variacion del ultimo ataque mencionado. En este ataque el atacante toma el control del movil de la victima. Al igual que el ataque previamente nombrado, este ataque puede exfiltrar informacion confidencial del usuario y enviarsela al atacante. Un ejemplo de este tipo de ataques es "ZeuS". Este ataque permitia que los atacantes consigan silenciosamente un SMS de verificacion de 2 pasos enviado a los usuarios.

### Sintomas frecuentes de una infeccion por malware
Independientemente del tipo de malware con el cual un dispositivo es infectado, los sintomas frecuentes de estos son:
- Aumento del uso de la CPU.
- Disminucion de la velocidad de la PC.
- La computadora se congela o falla con frecuencia.
- Hay una disminucion en la velocidad de navegacion web.
- Existen problemas en la conexion de red.
- Se modifican los archivos
- Se eliminan archivos
- Presencia de archivos, programas e iconos de escritorio desconocidos
- Se ejecutan procesos desconocidos
- Los programas se cierran o reconfiguran solos
- Se envian email sin el consentimiento ni conocimiento del usuario

## Metodos de infiltracion

### Ingenieria Social

#### Que es?
La ingenieria social es un ataque de acceso que intenta manipular a las personas para que realicen acciones o divulgen informacion confidencial. Los ingenieros sociales normalmente dependen de la disposicion de las personas a ayudar, sin embargo, a veces se aprovechan de sus vulnerabilidades. Un ejemplo podria ser un atacante requiriendo acceso inmediato a la red y hablando con un empleado autorizado. El atacante puede atraer la vanidad o la codicia del empleado o invocar la autoridad mediante tecnicas de nombres.

#### Algunos de los ataques
Hay diversos tipos de ataques, sin embargo, algunos de estos son:
- __Pretexto__: El atacante llama a la persona y miente en el intento de obtener acceso a datos privilegiados. Un ejemplo seria un atacante que pretende necesitar datos personales o financieros para confirmar la identidad de un objetivo
- __Seguimiento__: Esto es cuando un atacante persigue rapidamente a una persona autorizada a un lugar seguro.
- __Algo por algo (quid pro quo)__: Esto es cuando un atacante solicita informacion personal de una parte a cambio de algo, por ejemplo, un obsequio.

### Decodificacion de contraseñas Wi-Fi

La decodificacion es el proceso de deteccion de la contraseña utilizada para proteger la red inalambrica. Algunas de las tecnicas de decodificacion de contraseñas son:
- __Ingenieria Social__: El atacante manipula a una persona que conoce la contraseña para que se la proporcione.
- __Ataques por fuerza bruta__: El atacante prueba diversas contraseñas en el intento de adivinar las credenciales correctas. Si, por ejemplo, la contraseña es de 4 digitos, esta operacion tomaria 10000 intentos. Normalmente lo ataques por fuerza bruta son realizados usando un archivo de texto con una lista de palabras con palabras tomadas del diccionario. Debido a su naturaleza de azar las contraseñas complejas llevan mucho mas tiempo en ser decifradas. Algunas de las herramientas para llevar a cabo estos ataques pueden ser: Ophcrack, L0phtCrack, THC Hydra, RainbowCrack y Medusa.
- __Monitoreo de la red__: Mediante la escucha y la captura de paquetes enviados por la red, un atacante puede descubrir la pass si esta es enviada sin cifrar. Si esta esta cifrada, el atacante aun puede revelarla mediante una aplicacion de decodificacion de contraseñas.

### Suplantacion de identidad (Phishing)

Esta metodologia de ataque es cuando una persona maliciosa envia un correo electronico fraudulento disfrazado de una fuente legitima y confiable. El objetivo es engañar a la victima para que instale malware o comparta informacion personal o financiera. Un ejemplo seria el de un mail que adjunta un link el cual lleva a una pagina falsa en la cual se piden datos personales o incluso se descarga automaticamente un malware.
Luego tambien esta la __Suplantacion de identidad focalizada (Spear Phishing)__. Este tipo de ataques se diferencian de el phishing normal en que, normalmente, son ataques a personas mas importantes o a un blanco en especifico, es por esto, que lo correos contienen mas referencias a datos personales y son hechos con el objetivo de que se sientan mas personalizados para esa persona en particular.

### Aprovechamiento de vulnerabilidades

El aprovechamiento de vulnerabilidades es un metodo comun de infiltracion el cual se centra en la obtencion de informacion acerca de un equipo y la posterior explotacion de una vulnerabilidad conocida que este presente en una version del software o hardware.
Un metodo comun para el aprovechamiento de vulenrabilidades es el siguiente:
- Paso 1. Recopilacion de informacion sobre el sistema destino. Esto se puede hacer de diversas formas, sin embargo, las mas conocidas son la ingenieria social y el escaneo de puertos. El objetivo es aprender la mayor cantidad posible de cosas acerca del sistema destino.
- Paso 2. Parte de la informacion previamente recogida puede ser del SO, la version y los servicios que se encuentran corriendo
- Paso 3. Buscar vulnerabilidades conocidas para el SO en cuestion o para los servicios que se encuentran corriendo en esa Maquina.
- Paso 4. Una vez encontrada una vulnerabilidad se puede buscar correr un ataque creado anteriormente. Si no se encuentra ningun ataque previo, el atacante puede considerar crear uno.
Ejemplos de herramientas para llevar a cabo este tipo de ataques pueden ser __Nmap__ y __WhoIs__

#### APT o Amenazas persistentes avanzadas

Es una forma de infiltracion. Estas amenazas consisten en una operacion cautelosa y avanzada en varias fases a largo plazo contra un objetivo especifico. Debido a la complejidad y el nivel de habilidad requeridos, las APT generalmente estan bien financiadas. Las APT apuntan a organizacion o naciones por motivos politicos o comerciales.
Generalmente relacionadas con el espionaje, el proposito de las APT es implementar malware personalizado en uno o varios sistemas de destino y pasar desapercibidas. Con multiples bases de operacion y varios tipos personalizados de malware que afectan a distintos dispositvos y cumplen funciones especificas, un atacante individual generalmente carece de las habilidades, recursos o la perseverancia para llevar a cabo un APT

## Denegacion de servicio

### DoS

Los ataques de denegacion de servicio o DoS son un tipo de ataque a la red. El resultado de un DoS es la interrupcion del servicio de red a los usuarios, los dispositivos o las aplicaciones. Existen 2 tipos de DoS:
- __Cantidad abrumadora de datos__: Esto ocurre cuando se envia una gran cantidad de datos a una red, un host o una aplicacion a una velocidad que no se pueden administrar. Esto ocasiona una disminucion de la velocidad de transmision o respuesta o una falla en un dispositivo o servicio.
- __Paquetes maliciosos formados__: Esto sucede cuando es enviado un paquete malicoso formateado y la aplicacion no puede manejarlo. Por ej.: Un atacante envia paquetes a una aplicacion con errores que esta no puede identificar o reenvia paquetes incorrectamente formateados. Esto hace que el dispositivo receptor se realentice o se detenga.

Los ataques DoS se consideran de un riesgo importante debido a que pueden ser llevados a cabo pero alguien inexperto y aun asi causar una perdida de tiempo y dinero. Esto es debido a que estos ataque causan una facil interrupcion en la comunicacion.

### DDoS

Este tipo de ataque es similar a un DoS, sin embargo, la principal diferencia radica en que estos ataques son hechos de multiples fuentes coordinadas. Un ejemplo de un ataque DDoS es cuando un atacante crea una red de hosts infectados, una botnet. Los infectados se denominan "Zombies". Estos son controlados por sistemas manipuladores. 
Las computadoras zombies constantemente analizan e infectan mas hosts. Cuando esta listo, un atacante proporciona la informacion de ataque y da la orden a la botnet a traves de los sistemas manipuladores (Command and Control) 

### Envenenamiento de SEO

Este tipo de ataque consiste en aprovechar la optimizacion de motores de busqueda (SEO) realizando una gran cantidad de peticiones a una pagina fraudulenta para que asi esta sea posicionada mas arriba en motores de busqueda como Google por ej.. Todo esto es hecho con el objetivo de aumentar el trafico a sitios fraudulentos que puedan contar con malware o puedan ser utilizados para ingenieria social. Para que esta pagina aparezca mas arriba los atacantes abusan de los terminos de busqueda populares.

## Ataque combinado 

### Que es?

Un ataque combinado es un ataque el cual utiliza diversas tecnicas para comprometer a un objetivo. Mediante el uso de varias tecnicas de ataque simultaneas, los atacantes, tienen malware que combina gusanos, troyanos, spyware, keyloggers, spam y esquemas de suplantacion de identidad. Esta tendencia de ataques combinados revela malware mas complejo y pone datos en gran riesgo.

Los tipos mas comunes de este tipo de ataques utilizan mensajes de correo electronico no deseado, mensajes instantaneos o sitios web legitimos donde se esparce enlaces de descargas de malware o spyware. Otro ataque combinado puede ser DDoS con phising a traves de correos electronicos con suplantacion de identidad. Primero, se utiliza el DDoS para tumbar el sitio web y luego se envian correos electronicos con suplantacion de identidad para disculparse en nombre de la pagina y aprovechar el mail para insertar una falsa redireccion a un sitio web de emergencia fraudulento donde se busca el robar credenciales de inicio de sesion o datos personales.

Muchos de los gusanos mas perjudiciales se categorizan como ataques combinados. Algunos ejemplos son:
- Algunas variantes de __Nimbda__ que usaban los archivos adjuntos de correo electronico, descargas de archivos de un servidos web comprometido y uso compartido de archivos de Microsoft como medio de propagacion.
- Otras variantes de __Nimbda__ pueden modificar las cuentas de invitado del sistema para proporcionar al atacante o codigo malicioso los privilegios administrativos.

Los gusanos recientes Conficker y ZeuS/LICAT también son ataques combinados. Conficker utiliza todos los métodos de distribución tradicionales.

Algunos de los ejemplos mas importantes de cara a gusanos que se basan en ataques combinados pueden ser: Nimbda, CodeRed, BugBear, Klez y Slammer

## Que es la reduccion de impacto?

Partiendo de la base que no hay medidas de seguridad 100% efectivas para prevenir ciberataques y que es muy probable que existan violaciones de seguridad, si el premio es grande, las empresas deben estar preparadas para contener los daños.

Es importante comprender que una brecha de seguridad no se limita a las perdidas de datos, bases de datos dañadas o los daños a la propiedad intelectual; los daños tambien se extienden a la reputacion de la empresa. Responder a una infraccion de datos es un proceso muy dinamico.

Algunas de las medidas mas avaladas por expertos en ciberseguridad y que deben ser adoptadas ante una violacion de seguridad son:
- Comunicar el problema: Informar internamente a los empleados del problema y llamar a la accion. Infromar externamente a los clientes a traves de comunicacion directa y anuncios oficiales. La comunicacion genera transparencia que es vital para este tipo de situaciones.
- Ser sincero y responsable en caso de que sea error de la empresa.
- Proporcionar detalles: Explicar que y porque sucedio y que se vio afectado. Tambien se espera que la empresa se haga cargo de los costos de servicios de proteccion contra el robo de identidad para los clientes afectados.
- Comprender que causo y facilito la violacion de seguridad. De ser necesario contrate expertos en informatica forense para investigar y conocer los detalles.
- Aplicar los conocimientos del punto anterior para garantizar que no vuelva a ocurrir el mismo ataque o alguno similar en el futuro.
- Asegurese de que todos los sitemas esten limpios y que no hayan "backdoors" ni alguna otra cosa comprometida. Los atacantes frecuentemente intentan dejar puertas traseras para facilitar intrusiones futuras. Hay que asegurarse que esto no suceda.
- Capacitar empleados, partners y clientes acerca de como prevenir violaciones futuras.