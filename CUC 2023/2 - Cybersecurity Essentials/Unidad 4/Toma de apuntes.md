## Descripción general

### Que es la criptografía?

La criptografía es la ciencia de generar y descifrar códigos secretos. La criptografía es un método para almacenar y transmitir datos de modo que el receptor destinado pueda leerlos o procesarlos. La criptografía moderna utiliza algoritmos seguros a nivel informático para asegurarse de que los delincuentes cibernéticos no puedan poner en peligro fácilmente información protegida.
La confidencialidad de los datos garantiza la privacidad de modo que solo el receptor previsto pueda leer el mensaje. Las partes logran esto mediante la encriptación. La encriptación es el proceso de codificar datos de modo que una parte no autorizada no pueda leerlos fácilmente.
Al activar la encriptación el texto pasa de ser de texto claro a ser un texto completamente ilegible. El descifrado, por su parte, es el proceso inverso a este. La encriptación requiere una clave, clave la cual, desempeña un rol importante en la encriptación y desencriptación del mensaje. Las personas que posean la clave pueden descifrar el texto cifrado a texto simple.

### Creación del texto cifrado

Cada método de encriptación utiliza un algoritmo especifico, llamado código, para cifrar y descifrar los mensajes. Existen varios metodos para crear un texto cifrado:
- Transposicion: las letras cambian.
- Sustitucion: las letras se reemplazan.
- Libreta de un solo uso: texto no cifrado combinado con una clave secreta que crea un nuevo caracter, que luego se combina con el texto simple para producir el texto cifrado.
Actualmente, debido a la ingenieria inversa y la tecnologia moderna, la seguridad de una encriptacion no se basa en la privacidad del algoritmo sino que reside en la privacidad de las claves. En la practica, tomando en cuenta lo dicho antes, los ataques a sistemas criptograficos no son a la encriptacion en si sino al sistema de administracion de claves. 

### Dos tipos de encriptacion

Existen dos tipos de enfoques para garantizar la seguridad de los datos. La primera es proteger el algoritmo. Si la seguridad del algoritmo depende del secreto de este, el aspecto mas importante es proteger el algoritmo a toda costa. Este enfoque normalmente no es el mas indicado debido a que si se filtran los detalles de esto ambas partes deben cambiarlo, es por esto que casi siempre se procede a el segundo enfoque. El segundo es el de proteger las llaves. En este enfoque se usan algoritmos publicos con claves privadas que garantizan la privacidad de los datos.
Existen dos clases de algoritmos de encriptación:
- __Algoritmos simétricos__: Estos algoritmos utilizan la misma clave pre-compartida, a veces llamada un par de clave secreta, para cifrar y descifrar los datos. El emisor y receptor conocen la clave antes de empezar la comunicación cifrada. Los algoritmos con una clave común son mas simples y necesitan menos capacidad informatica.
- __Algoritmos asimétricos__: Estos algoritmos usan una clave para cifrar los datos y una clave diferente para descifrarlos. Una clave es publica y la otra es privada. En un sistema de cifrado de clave publica, cualquier persona puede cifrar un mensaje con la clave publica del receptor, y el receptor es el único que puede descifrarlo mediante su clave privada. Las partes intercambian mensajes sin la necesidad de una clave pre-compartida. Este tipo de algoritmos son mas complejos y requieren mas recursos para ser implementados, además de ser mas lentos que su contraparte.

## Encriptación de clave privada

### Proceso de encriptación simétrica

Los algoritmos simétricos como se dijo previamente utilizan una misma clave pre-compartida para encriptar y desencriptar.
Si una persona desea hablar con varias personas al mismo tiempo, debe manejar una gran cantidad de claves, esto es debido a que estas son pre-compartidas y exclusivas para una comunicación en particular.

### Tipos de criptografía

Los tipos mas comunes de criptografía son cifrados por bloques y cifrados de flujo. Cada uno se diferencia en la forma de agrupar bits de datos para cifrarlo.
- __Cifrado por bloques__: Los cifrados de este tipo transforman un bloque de texto simple, de longitud fija en un bloque común de texto cifrado de 64 o 128 bits. El tamaño del bloque es la cantidad de datos cifrados en cualquier momento. Para descifrar utilice la misma transformación inversa al bloque de texto cifrado, utilizando la misma clave secreta. 
	Los cifrados por bloques generalmente producen una cantidad mayor de datos de salida que los datos de entrada. Esto es debido a que, como se toman bloques de datos, si un bloque se encuentra incompleto se lo completa de manera artificial. Un ejemplo de este cifrado es el algoritmo __DES__
- __Cifrado de flujo__: Estos cifrados cifran de a un byte por vez. Esto se puede pensar como el cifrado por bloques con bloques de un bit. Debido a que estos "bloques" son de un bit no se produce un aumento artificial en el tamaño del texto y es de mayor velocidad que el otro tipo de cifrado. Ejemplos de este cifrado son A5 que es utilizado en servicios de voz y DES con tamaño de bloque de uno. 
Ambos cifrados pueden ser utilizados en un mismo proceso.

### Algoritmos de encriptacion simetrica

Algunos de los mas comunes son:
- __3DES (DES triple)__: el Estandar de encriptacion digital (DES) es un cifrado de bloques simetrico con un tamaño de bloques de 64 y un tamaño de llave de 56 bits. Entra un bloque de 64 bits y se genera un bloque de salida de 64 bits. En su algoritmo son usadas las tecnicas de permutacion y sustitucion. 
	El 3DES se encarga de cifrar tres veces y utilizar una clave diferente para al menos una de esas veces, proporcionando un tamaño de clave acumulativo de 112 a 168 bits. El 3DES es resistente a ataques, pero mas lento que el DES.
	El ciclo de encriptacion de 3DES es:
	1) Datos cifrados por el primer DES
	2) Datos descifrados por el segundo DES
	3) Datos vueltos a cifrar por el tercer DES
	El proceso inverso descifra el texto
- __IDEA__: el Algoritmo internacional de cifrado de datos (IDEA) utiliza bloques de 64 bits y claves de 128 bits. IDEA realiza 8 rondas de las transformaciones en cada uno de los 16 bloques que se producen al dividir cada bloque de 64 bits. IDEA fue el remplazo de DES y ahora la PGP (Pretty Good Privacy) la utiliza. El PGP es un programa que proporciona privacidad y autenticación en la comunicación. Su alternativa gratuita es GNU (GPG).
- __AES__: el Estándar de encriptación avanzada (AES) tiene un tamaño fijo de 128 bits con un tamaño de clave de 128, 192 o 256 bits. El NIST aprobó este algoritmo y es utilizado por el gobierno de los Estados Unidos para proteger información clasificada.
	Este algoritmo es de los mas solidos y utiliza claves de mayor longitud. Este es mas rápido que los vistos anteriormente por lo cual brinda soluciones para las aplicaciones y el uso de hardware en firewalls y los routers.
Algunos otros cifrados pueden ser Skipjack (Desarrollado por la NSA), Blowfish y Twofish.

## Encriptación de clave publica

### El proceso de encriptación asimétrica

Este proceso utiliza una clave para la encriptación (Clave publica de la persona destino) y utiliza una distinta para la desencriptación (Clave privada de la persona destino). Una persona no puede calcular una clave a partir de la otra. 

### Algoritmo de encriptacion asimetrica

La seguridad de estos algoritmos reside en el par de claves no relacionadas. Los algoritmos asimetricos incluyen:
- __RSA (Rivest-Shamir-Adleman)__: Utiliza el producto de dos numeros primos muy grandes con una longitud igual entre 100 y 200 digitos. Este algoritmo es usado por los navegadores para establecer una conexion segura.
- __Diffie-Hellman__: Proporciona un medio de intercambio electronico para intercambiar la clave privada. Protocolos como SSL, SSH, TLS e IPsec utilizan este algoritmo.
- __ElGamal__: Utiliza el estandar del gobierno de EE.UU. para las firmas digitales.
- __Criptografia de curva eliptica (ECC)__: En EE.UU. la NSA utiliza este algoritmo para la generacion de firma digital y el intercambio de claves.

## Encriptacion simetrica frente a asimetrica

### Administracion de claves

La administración de claves incluye generacion, intercambio, almacenamiento, uso y reemplazo de claves utilizadas en un algoritmo de encriptacion.
Dos terminos para referirse a las claves son:
- __Longitud de claves__: Tambien denominado tamaño de la clave, es la medida en bits.
- __Espacio de clave__: Es la cantidad de intentos que una longitud de clave especifica puede generar.
A medida que aumenta la longitud de la clave, aumenta el espacio de la clave de manera exponencial.

### Aplicaciones

La industria de pago electronico utiliza 3DES. Los SO utilizan DES para proteger los archivos de los usuarios y datos del sistema como contraseñas. La mayoria de sistemas de archivos de cifrado, como NTFS, utilizan AES.
Cuatro algoritmos utilizan algoritmos de claves asimetrica:
- Intercambio de claves por internet (IKE), que es un componente fundamental para las VPN de IPsec.
- Secure Sockets Layer (SSL), un medio para implementar la encriptación en un navegador web.
- Shell Seguro (SSH), un protocolo que proporciona una conexion de acceso remoto seguro a un dispositivo de la red.
- Pretty Good Privacy (PGP), un programa informático que proporciona privacidad y autenticación criptográfica para mejorar la seguridad de las comunicaciones por correo electrónico.
Las VPN utilizan IPsec. IPsec es un conjunto de protocolos desarrollado para lograr servicios seguros en las redes. Los servicios de IPSec permiten la autenticación, la integridad, el control de acceso y la confidencialidad. Con IPsec, los sitios remotos pueden intercambiar información cifrada y verificada.

## Tipos de control de accesos

### Controles de acceso fisico

Son obstaculos reales puestos para que una persona no autorizada no pueda acceder a las instalaciones, el equipo y otros activos de la empresa.
Ejemplos de estos controles pueden ser:
-   Las protecciones supervisan las instalaciones
-   Las cercas protegen el perímetro
-   Los detectores de movimiento detectan objetos móviles
-   Los bloqueos de las PC portátiles protegen los equipos portátiles
-   Las puertas bloqueadas evitan el acceso no autorizado
-   Las tarjetas de deslizamiento permiten el acceso a las áreas restringidas
-   Los perros guardianes protegen las instalaciones
-   Las videocámaras supervisan las instalaciones al recopilar y registrar las imágenes
-   Las trampas permiten el acceso al área segura después de que la puerta 1 se cierra
-   Las alarmas detectan intrusiones

### Controles de acceso lógico

Estas son soluciones de hardware y software que se utilizan para administrar el acceso a recursos y sistemas. Estas soluciones incluyen herramientas y protocolos que los sistemas informáticos utilizan para la identificación, autenticación, autorización y responsabilidad.
Algunos controles de acceso lógico pueden ser:
-   La __encriptación__ es el proceso de tomar el texto simple y crear el texto cifrado
-   Las __tarjetas inteligentes__ tienen un microchip integrado
-   Las __contraseñas__ constan de una cadena de caracteres protegida
-   La __biométrica__ consta de las características físicas de los usuarios
-   Las __listas de control de acceso (ACL)__ definen el tipo de tráfico permitido en una red
-   Los __protocolos__ son un conjunto de reglas que rigen el intercambio de datos entre dispositivos
-   Los __firewalls__ evitan el tráfico de red no deseado
-   Los __routers__ conectan al menos dos redes
-   Los __sistemas de detección de intrusiones__ supervisan una red para detectar actividades sospechosas
-   Los __niveles de recorte__ son determinados umbrales permitidos para detectar errores antes de activar una indicador rojo

### Controles de acceso administrativo

Son políticas y procedimientos que se definen para implementar y hacer cumplir todos los aspectos del control de acceso no autorizado. Estos controles se enfocan en las practicas de personal y las practicas empresariales. Estos controles son: 
-   Las políticas son declaraciones de intenciones
-   Los procedimientos son los pasos detallados necesarios para realizar una actividad
-   Las prácticas de contratación comprende los pasos que una organización sigue para encontrar empleados calificados
-   Las comprobaciones de antecedentes son un evaluación del empleo que incluye la información de la última verificación de empleo, historial de crédito y antecedentes penales
-   La clasificación de datos califica los datos según su sensibilidad
-   La capacitación de seguridad capacita a los empleados sobre las políticas de seguridad en una organización
-   Las revisiones evalúan el rendimiento laboral de un empleado

## Estrategias de control de acceso

### Control de acceso obligatorio

El control de acceso obligatorio (MAC) restringe las acciones que un sujeto puede realizar en un objeto.
Las organizaciones utilizan MAC donde se encuentran diferentes niveles de clasificaciones de seguridad. Cada objeto tiene una etiqueta y cada sujeto tiene un espacio libre. Un sistema MAC restringe un sujeto según la clasificación de seguridad del objeto y la etiqueta anexada del usuario.
Ejemplo de esto seria un archivo que tiene de etiqueta "Maxima confidencialidad" solo puede ser accesibles por personas con permiso de "Maxima confidencialidad". 

### Control de acceso discrecional

El propietario de un objeto determina si permite o no el acceso a un objeto con control de acceso discrecional (DAC). Esto se puede inferir por su nombre, el propietario transmite o no los permisos a usuarios que el propietario quiera. 
En controles de este tipo el dueño del objeto permite o no el acceso a su archivo y especifica que permisos quiere brindar.

### Control de acceso basado en roles

El control de acceso basado en roles (RBAC) depende del rol del sujeto. Los roles son las funciones de trabajo en una organización. Los roles específicos requieren permisos para realizar determinadas operaciones.
El RBAC puede trabajar junto con el DAC o MAC al hacer cumplir las políticas de cualquiera de ellos. El RBAC ayuda a implementar la administración de permisos en grandes organizaciones. 

### Control de acceso basado en reglas

El control de acceso basado en reglas utiliza listas de control de acceso (ACL) para ayudar a determinar si se otorga acceso o no. Una serie de reglas se incluyen en la ACL. Estas pueden ser:
- Hora del día
- Pertenencia a grupos
- Necesidad de conocimiento
- Propiedades del objeto
- Clasificación del sujeto
Como ocurre con el MAC, los usuarios no pueden cambiar las reglas de acceso. Al igual que con el RBAC este tipo de control también puede ser combinado con otros controles.

## Identificación

### Que es la identificación?

La identificacion aplican las reglas establecidas por la politica de autorizacion: el usuario solicita acceso y si sus permisos se lo permiten se le brinda acceso. Por ejemplo, la politica de autorizacion determina que actividades puede realizar un usuario en un recurso.
Un identificador unico garantiza la correcta asociacion entre actividades y usuarios. Un nombre de usuario es el metodo mas comun de identificacion. Este puede tambien ser un PIN, una tarjeta inteligente o metodo biometrico.
Un identificador unico garantiza que un sistema pueda identificar a un usuario particular de manera individual; permitiendo asi, que un usuario autorizado realice las acciones adecuadas en un recurso particular.

### Controles de identificacion

Las politicas de ciberseguridad determinan que controles de identidad deben utilizarse. La sensibilidad de la informacion y los sistemas de informacion determinan cuan rigurosos son esos controles. 

## Metodos de autenticacion

### Que es lo que sabe

Contraseñas o PIN son ejemplos de esta seccion. Si esta cadena de caracteres se relaciona con el usuario, sera mas facil para un ciberdelincuente adivinar la contraseña del usuario.
Varias publicaciones recomiendan que las contraseñas sean tan largas como se puedan y que contengan letras mayusculas, minuscular, numeros y simbolos especiales.
Los usuarios, ademas, deben utilizar diferentes contraseñas para los distintos sistemas, esto es debido a que si las credenciales son crackeadas una vez se pueden reutilizar en todos los sistemas. 

### Que es lo que tiene

Tarjetas inteligentes y llaveros de seguridad son claros ejemplos de cosas que un usuario tiene.
- __Seguridad de una tarjeta inteligente__: una tarjeta inteligente es una pequeña tarjeta de plástico con un pequeño chip incorporado en ella. El chip es un portador de datos inteligente, capaz de procesar, almacenar, y de proteger los datos. Las tarjetas inteligentes almacenan información privada, como números de cuenta bancaria, identificación personal, historias clínicas y firmas digitales.
- **Llaveros de seguridad**: es un dispositivo que es lo suficientemente pequeño como para llevarlo en un llavero. Primero, el usuario ingresa un número de identificación personal (PIN). Si está ingresado correctamente, el llavero de seguridad mostrará un número. Éste es el segundo factor que el usuario debe ingresar para iniciar sesión en el dispositivo o la red.

### Quien es

Una característica física única que identifica a un usuario específico se denomina biométrica. La seguridad biométrica compara características físicas con perfiles almacenados para autenticar usuarios. Un perfil es un archivo de datos que contiene características conocidas de una persona. El sistema otorga acceso de usuario si sus características coinciden con configuraciones guardadas.
Existen dos tipos de identificadores biométricos:
- **Características fisiológicas**: incluyen huellas digitales, ADN, características de rostro, manos, retina oído
- **Características de comportamiento**: incluye patrones de comportamiento, como gestos, voz, ritmo de escritura o la manera de caminar de un usuario
La implementación de datos biométricos utiliza un dispositivo de escaneo o lectura, un software que convierte la información escaneada en formato digital y una base de datos que almacena datos biométricos para su comparación.

### Autenticacion de varios factores

La autenticación de varios factores utiliza al menos dos métodos de verificación. Un llavero con clave de seguridad es un buen ejemplo Los dos factores son algo que usted sabe, como una contraseña, y algo que posee, como un transmisor de seguridad. 

## Autorización 

### Que es la autorización?

La autorización controla lo que el usuario puede hacer o no en la red después de una autenticación satisfactoria: Después de que un usuario prueba su identidad, el sistema verifica a qué recursos de red puede acceder el usuario y qué pueden hacer los usuarios con los recursos. La autorización responde si el usuario tiene o no uno o varios de los siguientes permisos:
- Lectura
- Copia
- Crear
- Eliminar
La autorización utiliza un conjunto de atributos que describe el acceso del usuario a la red.
La autorización es automática y no requiere que los usuarios tomen medidas adicionales después de la autenticación. Implemente la autorización inmediatamente después de que el usuario realice la autenticación.

### Uso de la autorización

La autorización es automática y no requiere que los usuarios tomen medidas adicionales después de la autenticación. Implemente la autorización inmediatamente después de que el usuario realice la autenticación.
Una política de pertenencia a grupos define la autorización según la pertenencia a un grupo determinado. 
Una política de autoridad define los permisos de acceso según la posición de un empleado dentro de la organización. Por ejemplo, solo los empleados de nivel sénior en un departamento de TI pueden tener acceso a la sala de servidores.

## Responsabilidad

### Que es la responsabilidad?

La responsabilidad rastrea una acción hasta una persona o un proceso y realiza el cambio a un sistema, recopila esta información e informa los datos de uso.La organización puede utilizar estos datos para fines como auditorías o facturación. Los datos recopilados pueden incluir el tiempo de inicio de sesión de un usuario, si el inicio de sesión fue un éxito o una falla o los recursos de red a los que el usuario tenía acceso. Esto permite que una organización localice acciones y errores durante una auditoría o una investigación.

### Implementación de la responsabilidad

La implementación de responsabilidad consta de tecnologías, políticas procedimientos y formación. Un ejemplo seria, una organización que puede ver el registro de los inicios de sesión fallidos y correctos. Las políticas y los procedimientos de la organización explican qué medidas deben registrarse y cómo se generan, se revisan y almacenan los archivos de registro.
La retención de datos, la eliminación de medios y los requisitos de cumplimiento proporcionan la responsabilidad. Muchas leyes requiere la implementación de medidas para proteger diferentes tipos de datos. Estas leyes guían a una organización de forma correcta para administrar, almacenar y desechar datos.

## Tipos de control de seguridad

### Controles preventivos

Los controles de acceso preventivo evitan que ocurran actividades no deseadas o no autorizadas. Para un usuario autorizado, un control de acceso preventivo significa restricciones. La asignación de privilegios específicos a un usuario en un sistema es un ejemplo de control preventivo. Un firewall que bloquea el acceso a un puerto o servicio también se considera un tipo de control preventivo.

### Controles disuasivos

Los profesionales y las empresas de seguridad cibernética utilizan obstáculos para limitar o para mitigar una acción o un comportamiento. Los obstáculos del control de acceso desalientan a los delincuentes cibernéticos a obtener acceso no autorizado a los sistemas de información o a datos confidenciales. 
Los obstáculos hacen que los delincuentes cibernéticos potenciales piensen dos veces antes de cometer un delito. Algunos obstáculos comunes son:
- Bloqueos
- Cercas
- Tarjetas de identificación
- Protecciones
- Trampas
- Camaras
- Alarmas de intrusion
- Separación de tareas
- Capacitación sobre conocimiento
- Encriptación
- Auditoria
- Firewalls

### Controles de detección

Las detecciones de control de acceso identifican diferentes tipos de actividad no autorizada. Los sistemas de detección pueden ser muy simples, como un detector de movimiento o un guardia de seguridad. También pueden ser más complejos, como un sistema de detección de intrusiones. Todos los sistemas de detección tienen muchas cosas en común; buscan la actividad inusual o prohibida. Los controles de detección no impiden que algo suceda; más bien son medidas que se toman después de que se realiza el hecho.
Algunos ejemplos de estos controles de detección son:
- Rotación de trabajo
- Vacaciones obligatorias
- Registros de auditoria
- Sistema de detección de intrusiones
- Señuelos
- Revision de los eventos de la camara de seguridad
- Detectores de movimiento
- Perros guardianes
- Guardias de seguridad

### Controles correctivos

Los controles correctivos contrarrestan algo que no es deseable. Las organizaciones establecen controles de acceso correctivos después de que un sistema experimenta una amenaza. Los controles correctivos restauran el sistema a un estado de confidencialidad, integridad y disponibilidad. También pueden restaurar los sistemas a la normalidad luego de que se produzca una actividad no autorizada.

### Controles de recuperación

Los controles de acceso de recuperación restauran recursos, funciones y capacidades después de una violación de la política de seguridad. Los controles de recuperación pueden reparar el daño, además de detener cualquier otro daño. Estos controles tienen capacidades más avanzadas sobre los controles de acceso correctivos.
Algunos ejemplos son:
- Operaciones de respaldo/restauración
- Sistemas de activación de tolerancia a fallas
- Agrupación de servidores
- Seguimiento de bases de datos
- Software antivirus

### Controles compensativos

Los controles de acceso compensativos ofrecen opciones a otros controles para fomentar el cumplimiento en respaldo de la política de seguridad.
Un control compensativo también puede ser una sustitución utilizada en lugar del control que no es posible en determinadas circunstancias. Por ejemplo, una organización puede no tener un perro guardián, entonces implementa un detector de movimiento con un reflector y un sonido de ladridos.
Otros ejemplos pueden ser:
- Politica de seguridad
- Supervision del personal
- Monitoreo
- Procedimientos de la tarea de trabajo

## Enmascaramiento de datos

### Que es el enmascaramiento de datos?

Es una tecnología que protege los datos al reemplazar la información confidencial por una versión no confidencial. Esto significa que un proceso comercial puede usar los datos no confidenciales y no es necesario cambiar las aplicaciones de respaldo o las instalaciones de almacenamiento de datos. El enmascaramiento limita la propagación de datos confidenciales dentro de los sistemas de TI al distribuir los conjuntos de datos sustitutos para la prueba y el análisis. La información puede estar enmascarada dinámicamente si el sistema o la aplicación determina que una solicitud de información confidencial del usuario es arriesgada.

### Técnicas de enmascaramiento de datos

Existen varias técnicas de enmascaramiento de datos que pueden garantizar que los datos sigan siendo importantes pero se cambien lo suficiente para protegerlos:
- La sustitución reemplaza los datos por valores que parecen auténticos para aplicar el anonimato a los registros de datos.
- El desplazamiento deriva un conjunto de sustitución de la misma columna de datos que un usuario desea enmascarar. Esta técnica funciona bien para la información financiera en una base de datos de prueba, por ejemplo.
- La anulación aplica un valor nulo a un campo específico, lo cual evita completamente la visibilidad de los datos.

## Esteganografía 

### Que es la esteganografía?

La esteganografía oculta datos (el mensaje) en otro archivo, como un archivo de texto gráfico, de audio u otro archivo de texto. La ventaja respecto a la criptografía es que el mensaje secreto no atrae ninguna atención especial. Nadie sabría nunca que una imagen contenía realmente un mensaje secreto al ver el archivo en formato electrónico o impreso.
Existen varios componentes involucrados en el ocultamiento de datos: Primero, existen los datos integrados, que es el mensaje secreto. El texto cubierto (imagen cubierta o audio cubierto) oculta los datos integrados y genera un estegotexto (o una estegoimagen o estegoaudio). Una estegoclave controla el proceso de ocultamiento.

### Técnicas de esteganografía

El enfoque utilizado para integrar los datos en una imagen cubierta utiliza los bits menos significativos (LSB). Este método utiliza bits de cada píxel en la imagen. Tres bytes de datos especifican el color de un píxel (un byte para cada color). El sistema de colores de 24 bits utiliza los tres bytes. LSB utiliza un bit de cada uno de los componentes rojo, verde y azul. Cada píxel puede ahorrar 3 bits. 
La figura muestra tres píxeles de una imagen de 24 bits. Una de las letras del mensaje secreto es la letra T y la inserción del caracter T solo cambia dos bits del color. El ojo humano no puede reconocer los cambios realizados a los bits menos significativos. El resultado es un carácter oculto.

### Laboratorio
Comando:
`steghide embed -cf keyboard.jpg -ef secret.odt` - -cf para especificar una imagen y -ef para especificar el texto a guardar o la información a guardar en la imagen
Comando:
`steghide info archivo` - Usado para verificar si hay alguna información oculta en ese archivo mediante el uso de la herramienta y una contraseña. 
Comando:
`steghide extract -sf archivo` - Usado para extraer la información del archivo previamente chequeado.

### Esteganografía social

La esteganografía social oculta información a plena vista al crear un mensaje que algunos pueden leer de determinada manera para recibir el mensaje. Otras personas que lo ven de manera normal, no verán el mensaje. Por ejemplo, la frase «vamos al cine» puede significar «vamos a la playa».
Las personas en los países que censuran los medios también utilizan la esteganografía social para mandar sus mensajes al deletrear las palabras de manera incorrecta a propósito o hacer referencias imprecisas. En efecto, se comunican con diferentes audiencias de manera simultánea.

### Detección

El estegoanálisis es el descubrimiento de que existe información oculta. El objetivo del estegoanálisis es detectar información oculta.
Los patrones de la estegoimagen generan sospecha. Por ejemplo, un disco puede tener áreas sin utilizar que ocultan información. Las utilidades de análisis de disco pueden informar sobre la información oculta en clústeres sin utilizar de dispositivos de almacenamiento. Los filtros pueden capturar los paquetes de datos que contienen información oculta en los encabezados de paquete. Ambos métodos usan las firmas de esteganografía.
Al comparar una imagen original con la estegoimagen, un analista puede recoger patrones repetitivos de manera visual.

## Ofuscación de datos

### Ofuscación

La ofuscación de datos es el uso y la práctica de las técnicas de esteganografía y enmascaramiento de los datos en el área de ciberseguridad y la profesión de inteligencia cibernética: La ofuscación es el arte de hacer que el mensaje sea confuso, ambiguo o más difícil comprender.

### Aplicaciones

La marca el agua de software protege al software del acceso o la modificación no autorizada. La marca de agua de software inserta un mensaje secreto en el programa como prueba de propiedad. El mensaje secreto es la marca de agua del software. Si alguien intenta eliminar la marca de agua, el resultado es un código no funcional.
La ofuscación de software traduce el software a una versión equivalente a la original, pero a una solución que es más difícil de analizar para los atacantes. Si se intenta revertir la ingeniería del software esto puede brindar resultados incomprensibles de un software que todavía funciona.

