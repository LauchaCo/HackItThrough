## Tipos de malware

### Que es el malware?

Es software malicioso diseñado para interrumpir las operaciones de la computadora u obtener acceso a los sitemas informaticos. Mas informacion de malware [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]]
Tipos de malware:
- Virus: Es un codigo malicioso ejecutable asociado a otro archivo ejectuable, como un programa legitimo. Los mayoria de los virus requieren la inicializacion del usuario y pueden activarse en un momento determinado. Los virus se propagan de una de tres maneras: desde medios extraibles; desde descargas de internet y desde archivos adjuntos del correo. Los virus pueden ser inofensivos o destructivos. Para evitar la deteccion un virus se transforma. Una vez que el virus este activo generalmente este atacara otros programas y/o otros dispositivos de la red. 
- Gusanos: Son codigos maliciosos que se auto-replican al explotar de manera automatizada vulnerabilidades en las redes. Los gusanos por lo general, realentizan las redes. Este tipo de malware, a diferencia del virus, se ejecuta por si mismo. A excepcion de la infeccion inicial, ya no requieren de interaccion del usuario. Los gusanos comparten un patron. Todos tienen una vulnerabilidad de activacion, una manera de propagarse y contienen una carga util.
- Troyano: Es un malware que ejecuta operaciones maliciosas bajo la apariencia de una operacion deseada. Este codigo ataca los privilegios de usuario que lo ejecutan. Un troyano se diferencia de un virus en que este se centra en archivos no ejecutables, como imagenes, audios o juegos. 

### Bomba logica

Es un programa malicioso que utiliza un activador para reactivar el codigo malicioso. Algunos ejemplos son: Horas especificas, Borrado de una cuenta, otros programas en ejecucion, etc.. La bomba logica permanece activa hasta que se da el evento activador. Una vez activada, una bomba logica implementa un codigo malicioso que causa daños en una computadora. Una bomba logica puede: sabotear registros de bases de datos, borrar los archivos y atacar los sistemas operativos o aplicaciones. Recientemente tambien fueron descubiertas bombas logicas que causaban daños a componentes de la maquina victima como pueden ser el CPU, las memorias RAM, la fuente de alimentacion, etc. mediante el sobrecalientamiento de estas hasta un punto de fallo. 

### Ransomware

Cubierto en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]].

### Puertas traseras y rootkits

Son programas o codigos que genera un delincuente una vez comprometido un sistema. Una puerta trasera omite la autenticacion normal. Algunos programas conocidos de puertas traseras son __Netbus__ y __Back Orifice__, que permiten el acceso remoto a usuarios no autorizados al sistema. El proposito de una puerta trasera es otorgar a los delincuentes el acceso futuro al sistema. Los delincuentes, luego de la ejecucion de un troyano, instalan este tipo de malware para asi poder ingresar en el futuro.
Un rootkit modifica el SO para crear una puerta trasera. La mayoria de los rootkits explotan vulnerabilidades para escalar privilegios y modificar los archivos del sistema. Tambien es comun que los rootkits modifiquen la informatica forense del sistema y las herramientas de supervision, por lo que es muy dificil detectarlos. A menudo el usuario debe limpiar y reinstalar el SO de una computadora infectada con un rootkit.

### Defensa contra malware

Algunos pasos simples pueden ayudar a brindar proteccion contra todas las formas de malware son:
- Programa antivirus. [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 3/Toma de apuntes|Toma de apuntes]]. Debido a que todos los dias salen nuevas amenazas a diario es necesario mantener las firmas actualizadas. Una firma es como una huella. Identifica las caracteristicas de un codigo malicioso
- Software de actualizacion. [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 3/Toma de apuntes|Toma de apuntes]]. Es necesario actualizar tanto el SO como las aplicaciones, las cuales son actualmente la principal forma de ataque de un sistema. Ultimamente los desarrolladores de SO estan mas receptivos a nivel de vulnerabilidades nuevas, a diferencia de los desarrolladores de aplicaciones.

## Ataques a correos electronicos y navegadores

### Correo electronico no deseado

El correo no deseado se puede utilizar para enviar enlaces nocivos, malware o contenido engañoso. El objetivo final es obtener informacion confidencial, como informacion de un numero de seguro social o de una cuenta bancaria. La mayor parte del correo no deseado proviene de varias computadoras en redes infectadas por un virus o gusano. 
Incluso despues de implementar diversas medidas para mejorar la seguridad en los correos electronicos, aun pueden llegar algunos de los email. A pesar de esto, hay algunos indicadores mas comunes de correos no deseados los cuales son los siguientes:
- El correo electronico no tiene asunto.
- El correo electronico solicita la actualizacion de una cuenta.
- El texto del correo electronico tiene palabras mal escritas o puntuacion extraña.
- Los enlaces del correo electronico son largos o cripticos.
- Un correo electronico se parece a una correspondencia de una empresa legitima.
- El correo electronico solicita que el usuario abra un archivo adjunto.
Si un usuario recibe algun correo electronico con alguno de estos indicadores no es recomendable abrir el correo electronico ni los archivos adjuntos. Es muy comun que sea politica de la empresa que al recibir un email de estas caracteristicas el empleado se lo reporte al equipo de ciberseguridad. A pesar de que los proveedores filtran estos correos electronicos todavia ocupan una parte del ancho de banda y el servidor todavia debe procesar el correo.

### Spyware, adware y scareware

Explicado en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]].
Resumido:
- Spyware es un software que permite a un delincuente obtener informacion sobre las actividades informaticas del usuario. El spyware incluye a menudo rastreadores de actividades, recopilación de pulsaciones de teclas y captura de datos.
- Adware muestra generalmente los elementos emergentes molestos para generar ingresos para sus autores.
- Scareware convence al usuario a realizar acciones especificas segun el temor meidante ventanas emergentes que se asemejan a las del SO.

### Falsificacion de identidad

Este es un tipo de fraude. Los delincuentes utilizan los medios sociales para intentar recopilar informacion personal como credenciales o informacion de una cuenta disfrazandose como una entidad o persona de confianza. La suplantacion de identidad ocurre cuando un ciberdelincuente se disfraza de alguien de confianza para llegar a su fin generalmente relacionado con el malware o robo de informacion personal. 
La suplantacion de identidad focalizada es un ataque de falsificacion de identidad altamente dirigido. Si bien ambos ataques son similares, en la suplantacion de identidad focalizada el email o la forma de contactar a la victima es mucho mas elaborada y personalizada para aumentar la probabilidad de que la persona caiga en el engaño. Para realizar esto el delincuente realiza un proceso de reconocimiento a fondo para obtener los intereses y puntos debiles de la persona. 

### Vishing, Smishing, Pharming y Whaling

El vishing es una practica de suplantacion de identidad mediante el uso de la tecnologia de comunicacion de voz. El atacante puede realizar llamadas de suplantacion de fuentes legitimas mediante la tecnologia de voz sobre IP (VoIP). Mediante este ataque se busca obtener datos personales como tarjetas de credito u informacion de la victima. Este ataque se basa en que la mayoria de las personas estan sujetas al uso de las redes moviles.
El Smishing es la suplantacion de identidad mediante el uso de mensajes de texto de los telefonos. Lo que se busca, al igual que con los otros ataques, es instalar malware en el sistema de la victima o robar informacion mediante un enlace a un sitio web fraudulento.
El Pharming es la suplantacion de un sitio web legitimo en un esfuerzo por engañar a los usuarios a ingresar sus credenciales. En esta modalidad los usuarios ingresan sus credenciales en el sitio fake pensando que lo estan haciendo en el sitio web legitimo.
El Whaling es un ataque de suplantacion de identidad que apunta a objetivos de alto nivel en una organizacion.

### Complementos y envenenamiento del navegador

Un delincuente puede hackear el archivo ejecutable de un navegador, los componentes de este o sus complementos. Todo esto es realizado para instalar algun tipo de malware o por otros fines de beneficio propio.
- Complementos: Los complementos, como flash y shockwave de adobe, muestran contenido animado e interesantemente grafico mediante el software adecuado.
	A pesar de que era pensado que flash era notablemente seguro, los hackers se dedicaron a intentar explotar estos complementos hasta que encontraron vulnerabilidades que podian provocar la caida de todo el sistema o permitir que el atacante tome control completo del sistema afectado. A medida que los potenciales atacantes o hackers siguen intentando buscar vulnerabilidades en estos complementos se puede esperar una creciente perdida de datos confidenciales
- Envenenamiento SEO: Puede verlo en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]]
- Secuestrador de navegadores: Es el malware que cambia la configuracion de los navegadores para redirigir al usuario a sitios webs que pagan los clientes de los ciberdelincuentes. Estos programas normalmente son instalados junto con software legitimo, al igual que lo puede hacer un virus.

### Como defenderse de los ataques a correos electronicos y navegadores

Los principales metodos incluyen el filtrado del mail entrante, la formacion del usuario y el uso de filtrados de host y de servidor.
Es dificil filtrar todo el correo no deseado, sin embargo, hay una gran variedad de aplicaciones para lograr este cometido, asi como tambien los ISP normalmente tambien filtran los mails de forma automatizada.
Las organizaciones normalmente imparten capacitaciones sobre los servicios de correo electronico. Una de estas principales medidas es el nunca abrir archivos adjuntos, por mas que estos provengan de contactos conocidos, debido a que puede ser un gusano intentando auto-reproducirse.
El grupo de trabajo contra la suplantacion de identidad (APWG) se encarga de reducir estos ataques yendo a por las ocurrencias de estos.

## El arte de uso de trucos

### Ingenieria social

Cubierto en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]]

### Tacticas de ingenieria social

Las tacticas de ingenieria social son las siguientes:
- Autoridad: Es mas probable que las personas cumplan cuando reciben una orden de una "autoridad"
- Intimidacion: Los delincuentes hostigan a una victima para que tome acciones
- Consenso/Prueba Social: Las personas tomaran medidas si sienten que a otras personas les gusta tambien
- Escasez: Las personas tomaran medidas cuando sientan que existe una cantidad limitada.
- Urgencia: Las personas tomaran medidas cuando sientan que existe un tiempo limitado.
- Familiaridad/Agrado: Los delincuentes desarrollan una buena relacion con la victima para establecer una relacion y confianza
- Confianza: Los delincuentes crean una relacion de confianza con una victima la cual puede tomar mas tiempo para establecerse.

## Tipos de trucos

### Espiar por encima del hombro y hurgar en la basura

Un delincuente observa para asi obtener credenciales como un PIN, un patron, etc. que le de acceso a alguna informacion privada. Un ejemplo de contramedida de esta tecnica son los angulos desde los que se puede ver en un cajero automatico.
La tecnica de buscar en la basura puede llevar a obtener informacion que desecha una organizacion. Cualquier informacion confidencial debe ser desechada de manera correcta para hacerla irrecuperable.

### Simulacion de identidad y engaños

Las simulacion de identidad fue previamente cubierta. Un ejemplo seria una persona haciendose pasar por el AFIP y pidiendo el pago urgente de una deuda para no tomar medidas legales.
Un engaño es el intento de embaucar a alguien a que realice algo o crea algo que no es cierto.

### Piggybacking y Tailgating

El piggybacking se centra en seguir a alguna persona a todos lados para asi poder obtener ingreso a zonas seguras o a un area restringida. Algunos metodos pueden ser:
- Dan la apariencia de estar acompañados por una persona autorizada
- Se unen a una multitud grande y fingen ser un miembro
- Apuntan a una victima descuidada con respecto a las reglas de las instalaciones.
El tailgating es otro termino que refiere a la misma tecnica
Una trampa que puede evitar esta tecnica es el usar una puerta doble. Primero debe entrar por la puerta exterior y cerrarla para luego entrar por la puerta interior.

### Trucos en linea y por correo electronico

Si en un lugar de trabajo se reenvian correos engañosos, y otras bromas, peliculas, etc. pueden ser tomadas medidas disciplinarias en contra de la persona.

### Como defenderse contra el uso de trucos

Las organizaciones deben tomar cartas en el asunto y concientizar a sus empleados de las distintas tecnicas de ingenieria social existentes para que asi estos no sean victimas. Ademas, deben enseñar las medidas de prevencion, las cuales son:
- Nunca proporcione informacion confidencial o credenciales por correo electronico, sesiones de chat, en persona o por telefono a desconocidos.
- Resista el impulso de hacer clic en correos electronicos y enlaces de sitios web atractivos
- Preste atencion a las descargas no iniciadas o automaticas
- Establezca politicas y brinde formacion a los empleados sobre esas politicas
- Cuando se trate de seguridad, ofrezca a los empleados un sentido de la propiedad
- No se siente presionado por personas desconocidas

## Tipos de ciberataques

### Denegacion de servicio

Cubierto en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]].

### Analisis

La tecnica de analisis es similar al escuchar a escondidas a alguien. Ocurre cuando un atacante examina todo el trafico de la red a medida que pasa por la NIC, independientemente del destinatario. Los delincuentes pueden hacer un analisis de trafico mediante un software, hardware o una combinacion. 
La seguridad fisica es necesaria para que no se instale un analizador de protocolos dentro de la red interna.

### Falsificacion de identidad (Spoofing)

La falsificacion de identidad es un ataque que aprovecha la relacion de confianza entre dos sistemas. Si dos sistemas aceptan la autenticacion lograda por cada uno, es posible que una persona registrada en un sistema no pase denuevo por un proceso de autenticacion. Un atacante puede aprovechar esto al enviar un paquete a un sistema que parece provenir de un sistema confiable. Dado que existe esta relacion de confianza, el sistema objetivo puede llevar a cabo una accion sin la autenticacion.
Existen varios ataques de suplantacion de identidad:
- La falsificación de direcciones MAC se produce cuando una computadora acepta los paquetes de datos según la dirección MAC de la otra computadora.
- La falsificación de direcciones IP envía paquetes IP de una dirección de origen falsificada para disfrazarse.
- El protocolo de resolución de direcciones (ARP) es un protocolo que corrige las direcciones IP a direcciones MAC para transmitir los datos. La suplantación de ARP envía mensajes ARP falsos a traves de la LAN para conectar la dirección MAC del delincuente a la dirección IP de un miembro autorizado de la red.
- El Sistema de nombres de dominios (DNS) asigna nombres de dominios en direcciones IP. La suplantación de identidad de servidor DNS modifica el servidor DNS para redirigir un nombre de dominio especifico a una dirección IP diferente, controlada por el ciberdelincuente. 

### Ataque man-in-the-middle

Un delincuente realiza un ataque man-in-the-middle (MitM) al interceptar las comunicaciones entre las computadoras para robar la información que transita por la red. El delincuente también puede modificar el mensaje en transito debido a que ninguna de las dos partes saben que el mensaje sufrió un cambio. El ataque MitM permite que el delincuente tome el control del dispositivo sin el conocimiento del usuario.
Man-in-the-mobile (MitMo): Cubierto [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes|Toma de apuntes]].

### Ataques de día cero (Zero-days)

Este es un tipo de ataque que es desconocido o no revelado por el proveedor del software, por lo cual no hay parches de seguridad como contramedida. Cubierto en [[CUC 2023/1 - Introduction to Cybersecurity/Unidad 4/Toma de apuntes|Toma de apuntes]].

### Registro del teclado

Es un programa de software que registra las teclas de los usuarios del sistema. Los delincuentes pueden implementar registros de teclas mediante software instalado en un sistema informático o a traves de hardware conectado físicamente a una computadora. El delincuente configura el software para enviar por correo electrónico el archivo de registro.
Estas aplicación pueden ser detectadas y eliminadas por software anti-spyware. Si bien el software de registro de claves es legal, el uso dado por los ciberdelincuentes no lo es. 

### Como defenderse de los ataques

Una organización puede realizar una gran cantidad de cosas para defenderse de ataques. Configure firewalls para descartar cualquier paquete fuera de la red que tenga direcciones que indiquen que se originaron dentro de la red. Esto normalmente no sucede y normalmente representa que un atacante esta realizando un ataque de suplantacion de identidad.
Para evitar DoS y DDoS asegúrese de tener todo actualizado, distribuya la carga de trabajo en todos los servidores y bloquee los paquetes de Protocolo de mensajería de control de Internet (ICMP) en la frontera. Los dispositivos de red utilizan paquetes ICMP para verificar que un dispositivo pueda comunicarse con otro en la red.
Los sistemas pueden evitar ser victimas de un ataque de repetición al cifrar el trafico, proporcionar autenticación criptográfica e incluir una marca de tiempo con cada parte del mensaje.

## Ataques a los dispositivos mobiles o inalámbricos

### Grayware y SMiShing

Grayware son aplicaciones que se comportan de manera molesta o no deseada. Esto puede representar un riesgo para el usuario. Un ejemplo de las funcionalidades del grayware es el de rastrear la ubicación del usuario.
SMiShing es la suplantación de identidad de SMS. Esta técnica se basa en el envio de mensajes de texto falsos con el fin de incitar al usuario de entrar a un sitio web falso o llamar a un teléfono fraudulento.

### Puntos de acceso no autorizado

Un punto de acceso de esta naturaleza es un punto de acceso inalámbrico instalado en una red segura sin autorización explicita. Hay dos formas de que suceda esto. O un empleado bienintencionado lo instalo para ser util en la facilitación de la conexión de dispositivos móviles, o un atacante se escabullo en la organización y lo hizo de forma malintencionada. Dado que ambas son no autorizadas, presentan riesgos para la organización. 
Un punto de acceso dudoso también puede referirse al punto de acceso de un delincuente. En este caso el delincuente aplica una técnica de MitM para captar información sensible de los usuarios.
Un ataque con AP de red intrusa utiliza el punto de acceso de delictiva gracias a una mayor potencia y antenas mas altas de ganancias de ser una mejor opción para los usuarios. Una vez que los usuarios se conectan se lleva a cabo el ataque MitM y se analiza el trafico.

### Interferencia de RF

Las señales inalámbricas son susceptibles a la interferencia electromagnética (EMI), a la interferencia de radiofrecuencia (RFI) e incluso pueden ser vulnerables a rayos o ruidos de luces fluorescentes. Las señales también son vulnerables a interferencia deliberada. La interferencia de RF interrumpe la trasmisión y no posibilita que la señal llegue a la estación receptora.

La frecuencia, la modulación y el poder del que realiza la interferencia de RF debe ser idéntica a la de la transmisión que se quiere interrumpir.

### Bluejacking y Bluesnarfing

El bluetooth es un protocolo de corto alcance y baja energía. Este servicio transmite datos en una red de area personal, o PAN, y puede incluir dispositivos como teléfonos, laptops, impresoras, etc.. La configuración de bluetooth es sencilla utilizando el emparejamiento para establecer una conexión entre dos dispositivos. Al establecer el emparejamiento, ambos dispositivos utilizan la misma clave de acceso.
Las principales vulnerabilidades bluetooth son:
- El Bluejacking: Se utiliza para enviar mensajes no autorizados a otro dispositivo bluetooth. Una variación de esto es enviar una imagen impactante a otro dispositivo.
- El Bluesnarfing: Ocurre cuando el atacante copia la información de la victima de su dispositivo. Esta información puede incluir correos electrónicos y listas de contactos.

### Ataques a los protocolos WEP y WPA

Privacidad equivalente por cable (WEP): es un protocolo de seguridad que intento proporcionar una red de area local inalámbrica (WLAN) con el mismo nivel de seguridad que el de una red LAN cableada. El protocolo WEP pretendía el proteger los datos enviados mediante una WLAN con encriptación.
El protocolo WEP utiliza una clave para la encriptación, por lo cual, la cantidad de personas con la clave iba creciendo continuamente. Dado el uso de la misma clave, el delincuente tiene acceso a una gran cantidad de datos para los ataques analíticos.
El WEP tiene varios problemas con el vector de inicialización (IV) que es uno de los componentes del sistema criptográfico:
- Es un campo de 24bits, lo cual es demasiado pequeño.
- Es un texto no cifrado, por lo tanto, es legible.
- Es estático, por lo que los flujos de claves idénticas se repetirán en una red ocupada.
El protocolo de acceso protegido (WPA) y luego el WPA2 salieron como protocolos mejorados para reemplazar el WEP. El protocolo WPA2 no tiene los mismos problemas porque la clave no puede ser obtenida de tan solo revisar el trafico. El protocolo WPA2 es suceptible porque los atacantes pueden analizar los paquetes que se envian entre el punto de acceso y el usuario legitimo. Los delincuentes utilizan un analizador de protocolos de paquetes y luego ejecutan los ataques sin conexion en la contraseña.

### Defensa contra los ataques a dispositivos moviles e inalambricos

Existen varios métodos de defensa. El mas básico es el de cambiar las configuraciones por defecto en su red WLAN para activar características de seguridad de sus productos.
Restrinja la ubicación del punto de acceso con la red al colocar estos dispositivos fuera del firewall o dentro de una zona perimetral (DMZ) que contenga otros dispositivos no confiables.
Las herramientas de WLAN como NetStumbler pueden detectar puntos de acceso dudosos o estaciones no autorizadas. Desarrolle una política de invitado para abordar la necesidad cuando invitados legítimos necesiten conectarse a internet. Para empleados autorizados, utilice una VPN de acceso remoto para el acceso a la WLAN.

## Ataques a las aplicaciones

### Scripting entre sitios (XSS)

Es una vulnerabilidad que se encuentra en las webs. El XSS permite a los atacantes inyectar scripts en las paginas webs que ven los usuarios. Este script puede ser malicioso.
Los scripts tienen tres participantes: el atacante, la victima y el sitio web. El delincuente no apunta a la victima directamente. El delincuente aprovecha la vulnerabilidad en el sitio web. Los delincuentes introducen los scripts en la pagina que luego es visitada por los usuarios, los cuales, sin saber, ejecutan el script del hacker. Estos scripts pueden acceder a cookies, tokens de sesiones u otra información confidencial. Si los delincuentes obtienen estos datos pueden suplantar la identidad de ese usuario.

### Inyección de códigos

Una manera de almacenar datos es usar bases de datos. Es aquí donde surgen dos tipos de inyecciones debido a la falta de validación en las consultas a la base de datos. Estos tipos son:
- Inyección XML: Cuando se usa una base de datos de XML esta inyección puede dañar los datos. Cuando el sistema no inspecciona correctamente la entrada proporcionada por el usuario este puede tener acceso a la información de la base de datos.
	Todos los datos confidenciales  almacenados son accesibles para los delincuentes y pueden hacer cualquier cantidad de cambios en el sitio web. Un ataque de este estilo amenaza la seguridad del sitio web.
- Inyección SQL: El delincuente ataca la vulnerabilidad al insertar una declaración maliciosa de SQL en un campo. Nuevamente, el sistema no filtra correctamente los caracteres de entrada del usuario en una declaración de SQL. 
	Los delincuentes pueden suplantar la identidad, modificar datos existentes, destruir datos o convertirse en administradores de servidores de bases de datos. 

### Desbordamiento del buffer

Esto sucede cuando los datos van mas allá de los limites del buffer. Los buffers son areas de memoria asignadas a una aplicación. Al cambiar los datos mas allá de los limites del buffer, la aplicación accede a memoria asignada a otros procesos. Esto puede llevar a un bloqueo del sistema, comprometer los datos u ocasionar el escalamiento de privilegios.
El CERT/CC de la Universidad de Carnegie Mellon estima que casi la mitad de las vulnerabilidades surgieron de desbordamientos de buffers. La clasificación genérica de desbordamiento del buffer incluye muchas variantes, como rebasamiento de buffer estático, errores de indexación, errores de cadena de formato, incompatibilidades de tamaño del buffer ANSI y Unicode, y rebasamiento de pila.

### Ejecuciones remotas de códigos

Las vulnerabilidades de este estilo le permiten a un delincuente ejecutar cualquier comando en una maquina destino. Además, esto puede llevar a la ejecución de códigos y la toma de control del sistema con los privilegios del usuario que ejecuta la aplicación. Un ejemplo de explotación de esta vulnerabilidad es el modo de explotación de Metasploit con el Meterpreter.

### Controles ActiveX y Java

Los controles ActiveX y Java proporcionan la funcionalidad de un complemento a Internet Explorer. Los controles de ActiveX son piezas de software instaladas para otorgar funcionalidades extendidas. El principal problema de esto es que los terceros pueden escribir estos controles, y estos pueden ser maliciosos. 
Java por su parte funciona sobre un interprete, la Maquina virtual Java (JVM). La JVM habilita la funcionalidad del programa de Java. La JVM aísla el código no confiable del resto del SO. Existen algunas vulnerabilidades que posibiliten que el software sortee las restricciones impuestas por el sandbox. Tambien existen vulnerabilidades en la biblioteca de clase Java, que una aplicación utiliza para su seguridad. Java es la segunda vulnerabilidad mas grande despues del complemento Flash de Adobe. 

### Defensa de los ataques a las aplicaciones

La primera linea de defensa es escribir código solido. Independientemente del idioma o el origen de la entrada usado, la practica de programación prudente es tratar como hostil las entradas que estén fuera de la función. Valide todas las entradas como si fueran hostiles.
Mantenga actualizado todo el software.


