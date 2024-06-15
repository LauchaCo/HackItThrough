## Proteja sus dispositivos y su red

### Proteja sus dispositivos informaticos

Sus dispositivos almacenan sus datos y son el portal hacia su vida en linea. La siguiente lista son paso a seguir para proteger sus dispositivos informaticos contra intrusiones:
- __Mantenga el firewall encendido__: El firewall debe siempre esta activado y actualizado para evitar para que atacantes accedan a datos personales y empresariales.
- __Utilice un antivirus y un antispyware__: Este software esta diseñado para analizar sus dispositivos y correos electronicos entrantes para asi detectar viruses y eliminarlos. A veces el software antivirus tambien provee Antispyware. Mantenga el software de sus dispositivos actualizado para estar protegido de software malicioso reciente.
- __Administre su SO y su navegador__: Para proteger su computadora y sus datos, establezca los parametros de seguridad en su computadora y navegador en medio/alto. Y, al igual que en el punto anterior, se aconseja firmemente que el SO y el navegador se encuentren actualizados para tener los ultimos parches y actualizaciones en lo referente a la seguridad. 
- __Proteja todos sus dispositivos__: Todos sus dispositivos deben estar cubiertos con contraseña para asi evitar acceso no deseado. La informacion que estos albergan debe estar cifrada y aun mas en casos de datos sensibles o confidenciales. En los dispositivos moviles, almacene solamente informacion necesaria en caso de robo o perdida cuando esta fuera de su hogar. Si alguno de sus dispositivos se ve comprometido, los atacantes pueden acceder a los datos a traves del proveedor de servicios de almacenamiento en la nube, como iCloud o Google Drive

Los dispositivos IoT representan un riesgo aun mayor a cualquier otro dispositivo informatico, esto es debido a que, a diferencia de moviles o computadores, los dispositivos de esta naturaleza pocas veces reciben actualizaciones al firmware para aplicar parches de seguridad. Es por esto, que si alguna vulnerabilidad es encontrada en un dispositivo asi, es probable que se mantenga vulnerable. Para empeorar el problema, los dispositivos IoT estan diseñados para conectarse con los servidores del proveedor (Call Home) y solicitar acceso a internet. Para este proposito, los dispositivos utilizan la red local del usuario. El resultado es que, al verse muy propensos a ser vulnerados, los dispositivos IoT pueden ser una puerta de entrada para la red local de los clientes y sus datos. La mejor manera de protegerse es crear una red aislada la cual sea solo para dispositivos IoT. Un ejemplo de buscadores de dispositivos IoT puede ser __Shodan__.

### Use las redes inalambricas de forma segura

El medio por el cual se conectan los dispositivos habilitados con Wi-Fi es un identificador conocido como Identificador de conjunto de servicios (SSID). Para evitar que alguien ingrese sin autorizacion el SSID predeterminado y la contraseña predeterminada para la interfaz de administracion en el navegador web deben cambiarse. Los hackers son conscientes de estas credenciales predeterminadas. Opcionalmente, una medida de seguridad seria que el router no divulge el SSID, añadiendo asi una capa mas de seguridad para la deteccion de la red. Sin embargo, esta no debe ser considerada una medida de seguridad adecuada para una red. Ademas, debe encriptar la comunicacion inalambrica habilitando la seguridad inalambrica y la funcion de encriptado WPA2 en el router. Incluso con este encriptado la red aun puede ser vulnerable.

En octubre del 2017 se descubrio una falla en el protoclo WPA2 la cual permitia descifrar la encriptacion entre el router inalambrico y el cliente inalambrico, permitiendo asi, que el atacante obtenga acceso al trafico de la red y lo manipule. Esta vulnerabilidad es atacada usando el Ataque de reinstalacion de clave (KRACK, Key Reinstallation Attack). Afecta a todas las redes Wi-Fi protegidas, modernas. Para mitigar este ataque se debe tan solo aplicar un parche de seguridad en los dispositivos. Si su dispositivo no tiene un parche que mitigue esta vulnerabilidad o se quiere asegurar de no padecerla al 100%, otra alternativa es el uso de conexion por cable ethernet. Ademas, otra medida de seguridad que podria aplacar este problema seria el uso de VPNs para prevenir el acceso no autorizado a los datos mientras se utiliza una red inalambrica.

Al estar lejos de casa los puntos publicos de acceso inalambrico permiten acceder a internet. Sin embargo, no es recomendable enviar informacion confidencial ni sensible a traves de estos. Ademas, debe verificar, en caso de usar una computadora, que esta este configurada para no compartir archivos ni medios digitales, y en caso de compartirlos, requiera la autenticacion de un usuario con encriptacion. Pese a todas estas medidas es recomendable usar algun servicio como tuneles VPN y servicios encriptados para asi mitigar ataques de "eavesdropping" o interceptacion de informacion. El servicio VPN ofrece acceso seguro a internet a traves de un tunel cifrado entre la PC y el servidor VPN del proovedor de servicios. Con un tunel de este tipo aunque se intercepte una transmision de datos, no podra descifrarse.

Pasando al protocolo Bluetooth, este es un tipo de funcionalidad que se recomienda se mantenga desactivada en caso de no ser usada. Esta ultima recomendacion es debido a que puede ser un foco de ataque para hackers que quieren realizar ataques del tipo de espionaje de dispositivos, establecer controles del acceso remoto, distribuir malware y consumir bateria.

### Utilice contaseñas unicas para cada cuenta en linea

Es de buena practica que cada cuenta que tengamos en paginas web tenga una contraseña distinta, esto es con el fin de que, en caso de ser vicitmas de un ataque, no sean comprometidas todas nuestras cuentas sino que, tan solo sea comprometida la cuenta que tuvo la brecha de seguridad. Un ejemplo de un ataque que podria "leakear" nuestra contraseña seria un ataque de suplantacion de identidad.

Al usar tantas contraseñas se hace imposible recordarlas a todas, es por eso que existe una herramienta que puede facilitarnos esta tarea, gozando ademas de una seguridad añadida como son las encriptaciones. Esta herramienta es un gestor de contraseñas. Este gestor se encarga de almacenar y a su vez encriptar las contraseñas que se le guardan en su interior. Ademas, este gestor puede ayudar a iniciar sesion automaticamente en sus distintas cuentas, facilitandole asi gran parte del logueo. Lo unico necesario para el uso de esta herramienta es el acordarse de la contraseña maestra para acceder a todas las que se encuentran en su interior.

#### Consejos para la eleccion de una buena contraseña

- No use palabras del diccionario o nombres en ningun idioma.
- No use errores ortograficos comunes de palabras del diccionario.
- No use nombre de equipos o cuentas.
- De ser posible use caracteres especiales
- Utilice una contraseña con 10 o mas caracteres.

### Use una frase en lugar de una palabra como contraseña

Para evitar el acceso no autorizado a sus cuentas es recomendable usar frases en lugar de palabras debido a que su longitud es mayor, dificultando asi que puedan ser obtenidas mediante ataques de fuerza bruta o diccionario. Ademas, una frase es mas facil de recordar en caso de que tenga que ser cambiada con regularidad. 

#### Sugerencias para elegir una buena frase

- Elegir una oracion que signifique algo para usted
- Agregue caracteres especiales
- Mientras mas larga mejor
- Evite usar oraciones comunes o famosas, como por ejemplo, la letra de una cancion

Recientemente el Instituto Nacional de Normas y Tecnologia (NIST) de los Estados Unidos publico requisitos de contraseña mejorados. Pese a que estos estan orientados a aplicaciones del gobierno, tambien pueden servir para usuarios normales. Estas pautas tienen como objetivo proporcionar la mejor experiencia al usuario y poner la responsabilidad de comprobacion del user en los proovedores.

#### Resumen de las nuevas pautas

- Longitud minima de 8 maxima de 64
- No utilice contraseñas comunes ni que se adivinen con facilidad
- No hay reglas de composicion 
- Mejore la precision de escritura permitiendo que el usuario vea la contraseña mientras la escribe
- Se permiten todos los caracteres de impresion y los espacios
- Sin pistas de contraseña
- Sin fecha de caducidad periodica o arbitraria de la contraseña
- Sin autenticacion basada en conocimientos

## Mantenimiento de datos

### Encripte sus datos

Sus datos siempre deben estar encriptados. A pesar de que crea que sus datos no son para nada importantes es necesario encriptar sus datos porque para un tercero pueden si ser de utilidad.

Formas de ver esto serian: Esta listo para que extraños vean sus documentos e imagenes?, Le mostraria todos sus datos financieros almacenados en sus dispositivos a sus amigos?, Desea divulgar sus contraseñas y correos electronicos al publico general?

Esto puede incluso ir mas alla si una aplicacion maliciosa o malware toma control de todos sus datos personales e inicia ataques del tipo de robo de identidad, fraude o rescates. Los ciberdelincuentes pueden simplemente encriptar sus datos y hacer que sean inutilizables hasta que la extorsion se liquide.

#### Que es la encriptacion?

La encriptacion es un proceso de conversion de la informacion a un formato que una parte no autorizada no puede leer. Solo la persona autorizada con la contraseña o clave secreta puede descifrar los datos y acceder a ellos en su formato original. La encriptacion en si no impide que una persona pueda interceptar los datos. La encriptacion solamente se asegura de que la persona que intercepto esos datos no los pueda ver o acceder.

Windows viene con un sistema de encriptacion llamado EFS o Encrypting File System como caracteristica. El EFS esta directamente vinculado con una cuenta de usuario determinada. Solo el usuario que encripto los datos puede acceder a estos luego de ser encriptados. Para usar este sistema siga los siguientes pasos:
- Paso 1: Seleccione uno o mas archivos o carpetas
- Paso 2: Haga click derecho en los datos seleccionados y seleccione "Propiedades"
- Paso 3: Haga click en "Opciones Avanzadas"
- Paso 4: Seleccione la casilla "Encriptar contenido para proteger datos"
- Paso 5: Los archivos y carpetas encriptadas se mostraran en verde

### Realice un respaldo de sus datos

Tener un respaldo puede evitar la perdida de datos importantes ante eventuales eventos inesperados como la falla de un disco duro, el extravio o robo de un telefono o errores personales como la incorrecta eliminacion de un archivo importante. Para hacer un respaldo necesitara una ubicacion de almacenamiento adicional para los datos y debera copiar los datos a dicha ubicacion periodica y automaticamente.

Usted puede decidir donde sera la copia de seguridad, ya sea en la nube, en su red domestica o en una ubicacion secundaria. Cada una de estas opciones tiene sus propias ventajas, como por ej., en local tiene completo control de los archivos. Esto lo puede hacer copiando todos los datos en un dispositivo de almacenamiento conectado a la red (NAS), un disco duro externo simple o puede seleccionar solo algunas carpetas y enviarlas a un dispositivo como un CD/DVD, un pendrive, etc.. En este escenario usted es el propietario y es enteramente responsable del mantenimiento y el costo, como asi tambien de los datos. Si contrata a un servicio de almacenamiento, el costo depende del espacio que decida contratar. Con un servicio de respaldo de datos en la nube, como AWS, tendra acceso a sus datos siempre que tenga acceso a la cuenta. Cuando contrata un servicio de esta naturaleza, normalmente, es necesario que sea mas selectivo con los datos que desee almacenar debido al costo que viene apareado al almacenamiento, ademas de las constantes transferencias de datos en linea. Uno de los beneficios de guardar un respaldo en una ubicacion alternativa es que este no es suceptible a eventos que sucedan en el lugar donde trabaja el dispositivo principal.

### Eliminacion de datos de manera permanente

Una vez que un archivo es eliminado de forma "permanente" de la papelera de reciclaje no puede ser accedido por el SO, sin embargo, este archivo todavia puede ser obtenido por cualquier persona con herramientas forenses adecuadas debido al rastro magnetico que dejo la presencia de este archivo en el disco duro.

Para borrar datos de forma que estos no puedan ser recuperados, los datos deben ser sobreescritos varias veces por unos y ceros. Para llevar a cabo esta accion es necesario el uso de herramientas dedicadas. Ejemplos de estos programas pueden ser: SDelete para Windows, Shred para linux y Secure Empty Trash para Mac OSX.

La unica forma de estar seguros de que los datos no son accesibles es la destruccion del disco duro o dispositivo de almacenamiento.

Ademas del paso anterior tambien debe asegurarse de que sus datos no estan presentes en la nube. En caso de estar presentes tambien deber ser destruidos. Es por esto que cuando se eliminan datos uno se debe preguntar, He protegido los datos para evitar que caigan en las manos incorrectas?

## Autenticacion Solida

### Autenticacion en dos factores

Este tipo de autenticacion es una capa mas de seguridad utilizada por varios servicios en linea populares, entre los cuales se encuentran: Google, Facebook, Twitter, LinkedIn, Apple y Microsoft. Esta medida se encarga de agregar un segundo token a los medios de inicio de sesion mas basicos, usuario y contraseña, patron o PIN. Este segundo token puede ser:
- __Un objeto fisico__: una tarjeta de credito, una tarjeta de cajero automatico, un telefono o un control.
- __Escaneo biometrico__: huellas digitales, impresion de la palma o reconocimiento de voz o rostro.

Aun cuando esta presente la autenticacion en dos factores, los hackers todavia pueden llegar a saltarse estas medidas mediante ataques del tipo suplantacion de identidad, malware e ingenieria social. 

### OAuth 2.0

Open Authorization (OAuth) es un protocolo de estandar abierto que permite que las credenciales de los usuarios finales tengan acceso a aplicaciones de terceros sin exponer las contraseñas de los usuarios.  OAuth actua de intermediario para decidir si los usuarios pueden acceder a paginas de terceros. Suponiendo que se quiere acceder a la pagina XYZ pero no se tiene cuenta, lo que se puede hacer con este protocolo es utilizar la cuenta de una red social ABC para acceder a la pagina XYZ.

Para que esto funcione XYZ se registra con ABC y es una app aprobada. Cuando accede a XYZ usa sus credenciales de usuario para ABC. Luego XYZ solicita un token de acceso a ABC en su nombre. Ahora tiene acceso a XYZ sin haber brindado ningun dato sensible ni credenciales de usuario. El uso de tokens secretos impide que una aplicacion maliciosa obtenga su informacion y sus datos.

## Comparte demasiada informacion?

### No comparta demasiado en las redes sociales

Si desea mantener su privacidad, no comparta informacion sensible como e-mail, numero de telefono o fecha de nacimiento en las redes. La persona que necesite conocer su informacion personal probablemente ya la sepa. No complete su perfil de redes sociales en su totalidad, solo proporcione la informacion minima requerida. Ademas, configure la red social para solo personas que usted conozca vean sus actividades o participen en sus conversaciones.

Mientras mas informacion se provee, mas probable es que alguien lleve a cabo un ataque de suplantacion de identidad.

Si alguna vez ha olvidado su contraseña, seguramente se le ha presentado las preguntas personales para comprobar que es dueño de la cuenta. En caso de que no se hayan seguido las sugerencias anteriores, seguramente algun atacante podria responder esas preguntas con mucha facilidad. Es por esto que es siempre recomendable responder estas preguntas con algun tipo de informacion falsa o una respuesta que luego nos podamos acordad, esto con el objetivo de mantener las cuentas seguras de algun ataque llevado a cabo con OSINT.

### Privacidad del correo electronico y el navegador web

El correo electronico es en cierto modo similar a el mensaje de la tarjeta postal, esto debido a que se tranmite a plena vista de cualquier persona que pueda observarlo; el mensaje de correo electronico se transmite tambien en texto sin formato y es legible para cualquier persona que tenga acceso. Estas comunicaciones ademas pasan por una gran cantidad de servidores en la ruta hasta su destino. Ademas, incluso si borra los correos electronicos, estos son archivados en los servidores de correo durante algun tiempo.

Cualquier persona con acceso fisico a su computador o a su router puede acceder a su navegador y ver que sitios visito, el cache y posiblemente los archivos de registro. Este problema puede reducirse con el uso de la navegacion privada en su navegador. Algunos de los navegadores con navegacion privada pueden ser:
- Microsoft Internet Explorer: InPrivate
- Google Chrome: Incognito
- Mozilla Firefox: ventana privada/pestaña privada
- Safari: navegación privada

Al usar el modo privado, se deshabilitan las cookies y los archivos temporales y el historial de navegacion se eliminan una vez se cierra la ventana o el programa.

Ademas de como modo de seguridad el usar el modo de navegacion privada puede impedir parcialmente que otros recopilen informacion sobre sus actividades en linea y lo tienten a comprar algo con publicidad dirigida. Igualmente, las empresas desarrollaron diferentes maneras de, aun con la navegacion privada, poder identificar usuarios y recopilar informacion y seguir el comportamiento de estos. 

En ultima instancia, es su responsabilidad proteger sus datos, su identidad y sus dispositivos informaticos. Simplemente algunas precauciones pueden ahorrarte problemas en el futuro.
