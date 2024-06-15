## Firewalls

### Tipos de firewall

Un firewall es una medida de seguridad empleada para controlar o filtrar la entrada y/o salida de comunicaciones de un dispositivo o una red. Un firewall se puede instalar en una unica computadora con el fin de protegerla (firewall ejecutado en un host) o puede ser un dispositivo de red independiente que protege toda una red de computadoras y todos los disposititvos host de esa red (firewall basado en la red).

Debido a la sofisticacion de los ataques a las computadoras y a las redes, se han desarrollado distintos tipos de firewalls que atienden a diversas necesidades en la proteccion de la red. Algunos de los mas comunes son:
- __Firewall de capa de red__: Filtrado basado en las direcciones IP de origen y destino.
- __Firewall de capa de transporte__: Filtrado basado en puertos de origen y datos de destino y filtrado basado en el estado de la conexion.
- __Firewall de capa de aplicacion__: Filtrado basado en la aplicacion, el programa o servicio.
- __Firewall de aplicacion consciente del contexto__: Filtrado basado en el usuario, el dispositivo, la funcion, el tipo de aplicacion y el perfil de amenazas.
- __Servidor proxy__: Filtrado de solicitudes de contenido web, como URL, dominios, medios, etcetera.
- __Servidor proxy inverso__: Ubicados frente a los servidores web, estos proxies protegen, ocultan, descargan y distribuyen el acceso a los servidores web.
- __Firewall de traduccion de direcciones de red (NAT)__: Ocultan o enmascaran las direcciones privadas de los hosts de red. 
- __Firewall basado en host__: Filtrado de puertos y llamadas de servicio del sistema en el SO de una computadora.

### Escaneo de puertos

El escaneo de puertos es un proceso de comprobacion de una computadora, servidor o host de red para conocer los puertos abiertos. En redes, a cada aplicacion que se ejecuta se le asigna un identificador llamado numero de puerto. Este numero se utiliza de ambos extremos de la comunicacion para asegurarse que la informacion esta llegando a la aplicacion correcta. El escaneo de puertos puede ser utilizado con fines maliciosos como una herramienta de reconocimiento, para identificar el SO y los servicios de la computadora o host, o inofensivamente por parte de un administrador de red para verificar las politicas de seguridad en la red.

Con el proposito de evaluar el firewall de la red de computadoras y la seguridad de los puertos, se puede utilizar una herramienta llamada "Nmap", herramienta la cual es utilizada con el fin de obtener los puertos abiertos de un dispositivo. El escaneo de puertos puede ser considerado como un precursor a un ataque a la red, por lo tanto, no debe ser intentado contra servidores publicos o redes privadas de empresas sin el permiso de estas.

Para ejecutar un escaneo de puertos con esta herramienta debe: 
- Proporcionar la direccion IP del host que desee escanear
- Elegir el perfil de escaneo que desee
- Enviar el comando para iniciar el test o agregar parametros adicionales como por ej.: -Pn, -n, --min-rate, -oN, -oG, etc.
Con estos pasos usted podra enviar un escaneo de puertos, a lo que la herramienta reportara los puertos segun su estado:
- Abierto: El host respondio e indico que un servicio se encuentra corriendo en ese puerto.
- Cerrado, denegado o no escucha: El host respondio e indico que se denegaran las conexiones en el puerto.
- Filtrado, caido o bloqueado: No hubo respuesta del host.

Para ejecutar escaneo del puerto desde fuera de la red, debera iniciar el escaneo desde fuera de la red. Esto implica iniciar el escaneo con la ip publica del router, IP la cual puede ser obtenida de paginas como __cualesmiip__.

### Dispositivos de seguridad

Debido a la gran variedad de dispositivos de seguridad disponibles y herramientas que deben implementarse, es importante que trabajen en conjunto. Los dispositivos de seguridad son mas efectivos cuando forman parte de un sistema.

Los dispositivos de seguridad pueden ser dispositivos independientes, como un router o un firewall, y tambien pueden ser herramientas que se ejecutan en un dispositivo de red. Los dispositivos de seguridad se dividen en las siguientes categorias generales:
- __Routers__: Los routers de servicio integrado (ISR) tienen muchas capacidades similares a las de un firewall ademas de las funciones de ruteo, entre ellas, el filtrado de trafico, la capacidad de ejecutar un sistema de prevencion de intrusiones (IPS), el cifrado y las capacidades de VPN para las conexiones de cifrado seguro.
- __Firewalls__: Los firewalls de nueva generacion tienen todas las capacidades de un router ISR ademas del analisis y administracion de redes avanzadas. Algunos dispositivos de este estilo son llamados dispositivo de seguridad adaptable (ASA), un ejemplo son los Firewalls de Cisco.
- __IPS__: Son dispositivos dedicados a la prevencion de intrusiones.
- __VPN__: Son dispositivos diseñados para tener conexiones de cifrado seguro.
- __Malware/Antivirus__: Son antivirus instalados dentro de los dispositivos anteriormente nombrados. Un ejemplo de esto son los prouctos de Cisco, los cuales vienen con Cisco Advanced Malware Protection (AMP) desde Routers hasta Firewalls y dispositivos IPS
- __Otros dispositivos de seguridad__: Esta categoria incluye dispositivos de seguridad web y correo electronico, dispositivos de cifrado, servidores de control de acceso del cliente y sistemas de administracion de seguridad.

### Deteccion de ataques en tiempo real

Cuando un atacante explota una vulnerabilidad antes de que el creador pueda parchearlo, es considerado un ataque de dia cero o "Zero day". Debido a la complejidad de estos ataques actualmente no es extraño que los ataques tengan exito y ahora el exito, en cuanto a la defensa, se mida en la capacidad de detectarlo y mitigarlo lo mas rapido posible. La capacidad de detectar ataques mientras suceden en tiempo real, asi como de detenerlos inmediatamente o en cuestion de minutos, es el objetivo ideal. Sin embargo, a dia de hoy hay empresas que todavia les puede tomar dias o incluso meses detectar un ataque.

- Analisis en tiempo real de pricipio a fin: Detectar ataques en tiempo real requiere el analisis activo mediante el firewall y los dispositivos de red IPS/IDS. Tambien debe usarse la deteccion de malware Cliente/Servidor de nueva generacion con conexiones a los centros de amenaza globales en linea. En la actualidad el software y los dispositivos de analisis activo deben detectar anomalias mediante la deteccion de comportamientos y el analisis basado en comportamientos.
- Ataques DDoS y respuesta en tiempo real: El ataque __DDoS__ es una de las mayores amenazas que requiere la deteccion y respuesta en tiempo real. Es complicado el mitigar ataques de esta naturaleza debido a que se utilizan hosts zombies de alrededor de todo el mundo y hacen que parezca que es trafico legitimo. Para una gran cantidad de empresas los ataques DDoS son cosas regulares y paralizan los servidores de internet y la disponibilidad de la red. La capacidad de detectar y responder a ataques DDoS en tiempo real es crucial.

### Proteccion contra el malware

La forma de llevar a cabo una proteccion efectiva contra Zero-days y APTs o amenazas persistentes avanzadas es utilizar una aplicacion de deteccion de malware avanzada de nivel empresarial, esta ofrece como su principal caracteristica, la deteccion de malware en tiempo real.

Los administradores de red deben siempre estar monitorizando la red para advertir la presencia de un posible Malware o APT en la red interna. Un ejemplo de una solucion de seguridad brindada por Cisco es Advanced Malware Protection (AMP) Threat Grid, que analiza millones de archivos y los correlaciona con cientos de millones de otros objetos de malware analizados. Esto brinda a los clientes una vista global de las campañas, la distribución y los ataques de malware. AMP es un software de Cliente/Servidor implementado en terminales de host, como servidor independiente, o en otros dispositivos de seguridad de la red.

### Buenas practicas de seguridad

La siguiente es una lista de buenas practicas de seguridad:
- __Realizar una evaluacion de riesgos__: Conocer el valor de lo que se protege ayuda a justificar los gastos de seguridad.
- __Crear una politica de seguridad__: Cree una politica que delinee claramente las reglas de la empresa, tareas y expectativas
- __Medidas de seguridad fisica__: Restringen el acceso a los centros de datos, a las ubicaciones de los servidores y a los extintores.
- __Medidas de seguridad de recursos humanos__: Los empleados deben ser correctamente investigados con comprobaciones de antecedentes.
- __Efectuar y probar las copias de respaldo__: Realice copias de respaldo periodicas y pruebe los datos recuperados de las copias.
- __Mantener parches y actualizaciones de seguridad__: Actualice periodicamente los servidores, computadoras, programas y sistemas operativos de los dispositivos de la red.
- __Implementar controles de acceso__: Configure los roles de usuario y los niveles de privilegio, asi como una autenticacion de usuario solida.
- __Revisar periodicamente la respuesta ante incidentes__: Utilice un equipo de respuesta ante incidentes y pruebe los escenarios de respuesta ante emergencias.
- __Implementar una herramienta de administracion, analisis y supervision de red__: Seleccione una solucion de monitoreo de seguridad que se integre con otras tecnologias.
- __Implementar dispositivos de seguridad en la red__: Utilice routes de nueva generacion, firewalls y otros dispositivos de seguridad.
- __Implementar una solucion de seguridad integral para terminales__: Utilice software antivirus y antimalware de nivel empresarial.
- __Informar a los usuarios__: Educar a los usuarios y empleados sobre los procedimientos seguros.
- __Cifrar los datos__: Cifrar todos los datos confidenciales de la empresa, incluido el correo electronico.

Algunas de las pautas mas utiles se encuentran en los depositos organizacionales, como por ej.: el NIST.

Ademas, una de las organizaciones mas conocidas y respetadas para la capacitacion en ciberseguridad es el SANS Institute.

## Comportamiento a seguir en la ciberseguridad

### Botnet

Un botnet es un grupo de bots conectados a traves de internet con la capacidad de ser controlados por un atacante o grupo malicioso. Una computadora bot generalmente se infecta por visitar un sitio web, abrir un elemento adjunto de correo electronico o abrir un archivo de medios infectado.

Un botnet puede tener decenas de miles o incluso cientos de miles de bots. Estos bots se pueden utilizar para distribuir malware, lanzar ataques DDoS, distribuir correo electronico no deseado o ejecutar ataques de fuerza bruta a contraseñas. Las botnets generalmente son controladas mediante servidores de comando y control (o Command & Control).

Los ciberdelincuentes normalmente alquilan una botnet a proovedores para fines delictivos.

### Cadena de eliminacion o proceso de ataque (Kill Chain) en la ciberdefensa

Esta es la cadena que representa las etapas de un ataque a los sistemas de informacion. Este proceso fue desarrolado por Lockheed Martin como marco para la respuesta y la deteccion de incidentes, esta cadena consta de los siguientes pasos:
- __Etapa 1. Reconocimiento__: El atacante recopila informacion del dispositivo
- __Etapa 2.  Armamentizacion__: El atacante crea un ataque y contenido malicioso para enviar al objetivo.
- __Etapa 3. Entrega__: El atacante envia el ataque y la carga maliciosa al objetivo por correo electronico u otros metodos.
- __Etapa 4. Explotacion__: Se ejecuta el ataque.
- __Etapa 5. Instalacion__: El malware y las puertas traseras son instaladas en el objetivo.
- __Etapa 6. Mando y control__: Se obtiene el control remoto del objetivo mediante un servidor o un canal de comando y control.
- __Etapa 7. Accion__: El atacante realiza acciones maliciosas, como el robo de informacion, o ejecuta ataques adicionales contra otros dispositivos dentro de la red a traves de las etapas de la cadena de eliminacion nuevamente.

Para la defensa de cada una de estas etapas hay medidas diseñadas. Algunas preguntas para hacerse en cuanto a la cadena de eliminacion de una empresa pueden ser:
- Cuales son los indicadores de ataque en cada una de las etapas de la cadena de eliminacion?
- Que herramientas de seguridad son necesarias para la deteccion de los indicadores de ataque en c/u de las etapas?
- Hay brechas en la capacidad de la empresa para detectar un ataque?

Segun Lockheed Martin, comprender a fondo estas etapas permite tomar acciones mas efectivas en cuanto a como llevar a cabo la seguridad de una empresa, como poner obstaculos defensivos, demorar el ataque y evitar la perdida de datos. Cada etapa de la cadena eliminacion es mas costosa y requiere mas esfuerzo para el impedimento y correcion de ataques, siendo la etapa 1 la mas barata de todas.

### Seguridad basada en el comportamiento

Este tipo de seguridad es una que se basa en el contexto informatico a la hora de detectar anomalias en la red, a diferencia de la seguridad tradicional la cual depende de las firmas malintencionadas. Este tipo de deteccion implica la captura y el analisis del flujo de comunicacion entre un usuario de la red local y un destino local o remoto. Estas comunicaciones, una vez analizadas, revelan contexto y patrones de comportamiento utiles para la deteccion de anomalias. Esta deteccion puede llegar a detectar una anomalia mediante un cambio en un comportamiento normal.

- __Honeypot__: Es una herramienta de deteccion basada en el comportamiento que primero atrae al atacante apelando al patron previsto de comportamiento malicioso; una vez dentro del honeypot, un administrador de red puede capturar, registrar y analizar todas las acciones de un atacante. Esto le permite a un administrador ganar mas conocimiento sobre posibles formas de acceso a un sistema.

- __Arquitectura de Cyber Threat Defense Solution de CISCO__: Es una arquitectura de seguridad de Cisco que utiliza deteccion basada en comportamiento e indicadores para mas visibilidad, contexto y control. El objetivo es obtener toda la informacion posible sobre un ataque. Esta arquitectura usa muchas soluciones de seguridad para lograr su cometido.

### Netflow

Se utiliza para recopilar informacion sobre los datos que transitan la red. Muestra quien y que dispositivos estan en la red, asi como tambien, como y cuando los usuarios o dispositivos ingresaron a la red. NetFlow es un importante componente para el analisis y la deteccion basada en comportamientos. Switches, Firewalls y Routers con esta tecnologia puede enviar informes sobre datos que son transportados por la red. Gracias a estos datos, NetFlow puede establecer comportamientos de linea base en mas de 90 atributos diferentes.

## Enfoque de Cisco para la seguridad

### CSIRT

Es un Equipo de respuesta a incidentes de seguridad informatica (CSIRT), comunmente presente en todas las empresas grandes, el cual se encarga de recibir, revisar y responder a informes de incidentes de todo lo relacionado a la seguridad. La funcion principal de estos equipos es la de ayudar a proteger la empresa y la preservacion de datos realizando investigaciones integrales de los incidentes de seguirdad informatica. Para evitar incidentes, el CSIRT debe realizar evaluaciones de amenazas proactivas, planificaciones de mitigaciones, analisis de tendencias de incidentes, y revision de la arquitectura de seguridad. 

Hay organizaciones de CSIRT tanto nacionales y publicas, como por ej. la division CERT, la cual esta dispuesta a ayudar a las organizaciones, y a los CSIRT nacionales, a desarrolar, utilizar y mejorar sus capacidades de administracion de incidentes.

### Libro de estrategias de ciberseguridad

Una de las mejores maneras de prepararse para una violacion de seguridad es prevenirla. Se deben tomar pautas sobre como identificar el riesgo de la ciberseguridad en los sistemas, los activos, datos, funcionalidades, proteger los sistemas mediante la implementacion de protecciones y capacitaciones del personal, y detectar el evento de ciberseguridad lo mas rapido posible. Cuando se detecta una brecha se deben tomar todas las acciones para reducir riesgos e impacto. El plan de respuesta debe ser flexible con muchas opciones de accion. Una vez contenida la violacion y restaurados los sistemas y servicios, se debe ajustar la medidas de seguridad para contemplar lo aprendido en el ataque. 

Todo esto debe de ser recopilado en un libro de estrategias de seguridad. Un libro de estrategias es un conjunto de consultas repetidas (Informes) de fuentes de datos de eventos de seguridad que conducen a la deteccion y la respuesta ante los incidentes. Idealmente el libro debe cumplir con:
- Detectar equipos infectados con malware
- Detectar actividad de red sospechosa
- Detectar intentos de autenticacion irregulares
- Describir y entender el trafico entrante y saliente
- Proporcionar informacion de resumen que incluya tendencias, estadisticas y recuentos
- Proporcionar acceso rapido y utilizable a estadisticas y metricas
- Establecer una correspondencia de eventos en todas las fuentes de datos relevantes.

### Herramientas para prevencion y deteccion de incidentes

Algunas de las herramientas para detectar y evitar incidentes son:
- __SIEM__: Un sistema de administracion de informacion y eventos de seguridad (SIEM) es un software que recopila y analiza alertas de seguridad, los registros y otros datos historicos y en tiempo real de los dispositivos de seguridad de la red.
- __DLP__: Software Data Loss Prevention (DLP) es un sistema de hardware el cual se encarga de evitar el robo o fuga de datos confidenciales de la red. Este sistemas puede centrarse en la autorizacion de acceso a los archivos, el intercambio de datos, la copia de datos, la supervision de la actividad de usuario y mas. Los DLP estan diseñados para supervisar y proteger archivos en tres diferentes estados: en uso, en movimiento y datos almacenados. Datos en uso se centran en el cliente, en movimiento se refieren a datos mientras viajan por la red y almacenados refiere al almacenamiento de datos.
- __Cisco ISE y TrustSec__: Cisco Identify Sevices Engine (Cisco ISE) y Cisco TrustSec aplican el acceso a recursos de red mediante la creacion de politicas de control de acceso basado en roles que segmenta el acceso a la red (Usuarios moviles, Usuarios temporales, empleados) sin complejidad agregada. La clasificacion del trafico se basa en la identidad del usuario o el dispositivo.

### IDS e IPS

Un Sistema de deteccion de intrusiones o IDS es un dispositivo de red exclusivo, o una de varias herramientas en un servidor o firewall que analiza datos de una base de reglas o firmas de ataques, que busca trafico malicisoso. Si se detecta una coincidencia el IDS guardara la deteccion y le notificara al administrador de red. El IDS no adopta medidas cuando detecta una coincidencia, por lo que no evita ataques. El trabajo del IDS es solamente detectar, registrar y generar informes. 

El IDS normalmente realentiza la red, genera latencia. Es por esto que normalmente el IDS se configura en sin conexion separado del trafico de la red comun. Los datos se duplican o se copian mediante un switch y son enviados al IDS para la deteccion sin conexion. Tambien hay IDS que pueden ser instalados sobre un sistema operativo de un host, como Windows o Linux.

Un sistema de prevencion de intrusiones o IPS tiene la capacidad de bloquear o denegar trafico en funcion de las coincidencias positivas con la regla o la firma. Uno de los IDS/IPS mas conocidos es el "Snort" o Sourcefire de Cisco. Este dispositivo tiene la capacidad de realizar el analisis de trafico y de puerto en tiempo real, registrar, buscar y comparar contenido; puede detectar sondas, ataques y escaneos de puertos. Tambien se combina con otras herramientas para asi informar y analizar el rendimiento y los registros.