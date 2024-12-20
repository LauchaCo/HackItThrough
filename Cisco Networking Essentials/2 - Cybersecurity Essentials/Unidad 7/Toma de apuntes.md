## Protección del host

### Seguridad del sistema operativo

Un administrador protege un sistema operativo mediante la modificación de la configuración predeterminada para que sea más seguro frente a las amenazas externas. Este proceso incluye la eliminación de servicios y programas innecesarios. Otro requisito crítico de la protección de los sistemas operativos es la aplicación de actualizaciones y parches de seguridad.

Una organización debe tener un enfoque sistemático vigente para abordar las actualizaciones de sistemas mediante:
-   El establecimiento de procedimientos para monitorear la información relacionada con la seguridad.
-   La evaluación de las actualizaciones respecto de su aplicabilidad.
-   La planificación de la instalación de actualizaciones y parches en las aplicaciones.
-   La instalación de actualizaciones mediante un plan documentado.

Otro requisito fundamental para proteger los sistemas operativos es identificar posibles vulnerabilidades. Esto puede lograrse mediante el establecimiento de una línea de base. Establecer una línea de base permite al administrador hacer una comparación de cómo funciona un sistema frente a las expectativas de la línea de base.

El analizador de seguridad de la línea de base de Microsoft (MBSA) evalúa los errores de configuración y las actualizaciones de seguridad que faltan en Microsoft Windows. El MBSA comprueba las contraseñas en blanco, simples o inexistentes, la configuración del firewall, el estado de las cuentas de usuario temporal, los detalles de la cuenta de administrador, la auditoría de eventos de seguridad, los servicios innecesarios, los intercambios de red y las configuraciones de registros. Después de reforzar el sistema operativo, el administrador crea políticas y procedimientos para mantener un alto nivel de seguridad.

### Protección contra malware

Es importante proteger las computadoras y los dispositivos móviles usando ⁪software de antimalware de confianza. Los siguientes tipos de software de antimalware se encuentran disponibles:
-   Protección antivirus: El programa monitorea continuamente en busca de virus. Cuando detecta un virus, el programa advierte al usuario e intenta poner en cuarentena o eliminar el virus.
-   Protección contra adware: El programa busca continuamente programas que muestren anuncios publicitarios en la computadora.
-   Protección contra la suplantación de identidad: El programa bloquea las direcciones IP de sitios web conocidos que realizan la suplantación de identidad y avisa al usuario acerca de los sitios sospechosos.
-   Protección contra spyware: El programa busca registradores de teclado y otro tipo de spyware.
-   Fuentes confiables y no confiables: el programa advierte al usuario sobre programas inseguros que intentan instalarse o sitios web inseguros antes de que un usuario los visite.

Es posible que deban utilizarse varios programas distintos y múltiples análisis para eliminar todo el software malicioso por completo. Ejecute solo un programa de protección contra malware a la vez.

Varias organizaciones con experiencia en seguridad, como McAfee, Symantec y Kaspersky, ofrecen protección contra malware integral para computadoras y dispositivos móviles.

### Administración de parches

Los parches son actualizaciones de códigos que proporcionan los fabricantes para evitar que un virus o gusano recientemente descubierto logre atacar con éxito. Periódicamente, los fabricantes combinan parches y actualizaciones en una aplicación de actualización integral denominada paquete de servicios. Numerosos ataques de virus devastadores podrían haber sido mucho menos graves si más usuarios hubieran descargado e instalado el último paquete de servicios.

Windows verifica sistemáticamente el sitio web de Windows Update en busca de actualizaciones de alta prioridad que ayuden a proteger una computadora de las amenazas de seguridad más recientes.

Es posible que algunas organizaciones quieran probar un parche antes de implementarlo en la organización. La organización utilizará un servicio para administrar los parches localmente en lugar de usar el servicio de actualización en línea del proveedor. Los beneficios de utilizar un servicio de actualización de parches automatizado incluyen lo siguiente:
-   Los administradores pueden aprobar o rechazar las actualizaciones.
-   Los administradores pueden imponer la actualización de los sistemas para una fecha específica.
-   Los administradores pueden obtener informes sobre la actualización necesaria para cada sistema.
-   No es necesario conectar todas las computadoras al servicio del proveedor para descargar parches; un sistema obtiene la actualización de un servidor local.
-   Los usuarios no pueden desactivar ni eludir las actualizaciones.

El servicio de parches automatizado proporciona a los administradores una configuración más controlada.

### Firewalls basados en el host y sistemas de detección de intrusiones

Una solución basada en el host es una aplicación de software que se ejecuta en una computadora host local para protegerla. El software funciona con el sistema operativo para prevenir ataques.

- **Firewalls basados en el host**: Un firewall de software es un programa que se ejecuta en una computadora para permitir o impedir el tráfico entre la computadora y otras computadoras conectadas. El firewall de software aplica un conjunto de reglas a las transmisiones de datos mediante la inspección y el filtrado de paquetes de datos. El firewall de Windows es un ejemplo de firewall de software. El sistema operativo Windows lo instala de manera predeterminada en la instalación.
	El usuario puede controlar el tipo de datos enviados hacia y desde la computadora abriendo o bloqueando los puertos seleccionados. Los firewalls bloquean las conexiones de red entrantes y salientes, a menos que se definan excepciones para abrir y cerrar los puertos que necesita un programa.
- **Sistemas de detección de intrusiones basado en el host**: Un sistema de detección de intrusiones basado en el host (HIDS) es un software que se ejecuta en una computadora host para monitorear la actividad sospechosa. El HIDS monitorea las llamadas del sistema y el acceso al sistema de archivos para asegurarse de que las solicitudes no sean el resultado de actividades maliciosas. También controla los parámetros de registro del sistema. El registro conserva la información de la configuración de la computadora.
	El HIDS almacena todos los datos de registro localmente. El rendimiento del sistema puede verse afectado debido a su uso intensivo de los recursos. Un sistema de detección de intrusiones basado en el host no puede supervisar el tráfico de red que no alcanza el sistema host, pero puede monitorear los procesos del sistema crítico y el sistema operativo específicos del host.

### Comunicaciones seguras

Al conectarse a la red local y compartir archivos, la comunicación entre las computadoras permanece dentro de la red. Los datos permanecen seguros porque están fuera de otras redes e Internet. Para comunicar y compartir recursos por una red que no es segura, los usuarios emplean una ⁪red privada virtual (VPN).

La VPN utiliza conexiones seguras dedicadas enrutadas a través de Internet desde la red privada corporativa hasta el usuario remoto. Al conectarse a la red privada corporativa, los usuarios se convierten en parte de dicha red y tienen acceso a todos los servicios y recursos, como si estuvieran físicamente conectados a la LAN corporativa.

El software de cliente de VPN cifra los datos antes de enviarlos al gateway de VPN de la red privada corporativa a través de Internet. Los gateways de VPN establecen, administran y controlan las conexiones de VPN, también denominadas túneles de VPN.

Los sistemas operativos incluyen un cliente de VPN que el usuario configura para una conexión de VPN.

## Protección de dispositivos móviles e inalámbricos

### WEP

La privacidad equivalente por cable (WEP) es uno de los primeros y más utilizados estándares de seguridad Wi-Fi. El estándar de WEP brinda protecciones de encriptación y autenticación. Los estándares de WEP son obsoletos, pero muchos dispositivos aún admiten la WEP para la compatibilidad retrospectiva. El estándar de WEP se convirtió en un estándar de seguridad Wi-Fi en 1999 cuando las comunicaciones inalámbricas comenzaban a hacerse populares. A pesar de las revisiones al estándar y el incremento del tamaño de la clave, la WEP sufrió numerosas debilidades de seguridad. Los ciberdelincuentes podían descifrar las contraseñas de WEP en minutos con el software gratuito disponible. Pese a las mejoras, la WEP sigue siendo muy vulnerable y los usuarios deben actualizar los sistemas que dependen de la WEP.

### WPA/WPA2

La siguiente mejora importante a la seguridad inalámbrica fue la introducción del WPA y WPA2. El acceso protegido a Wi-Fi (WPA) fue la respuesta del sector informático a las debilidades del estándar de WEP. La configuración más común del WPA es WPA-PSK (clave precompartida). Las claves utilizadas por el WPA son de 256 bits, un aumento significativo respecto de las claves de 64 y 128 bits empleadas por el sistema de WEP.

El estándar de WPA proporcionó varias mejoras de seguridad. Primero, el WPA proporcionó controles de integridad de mensajes (MIC) que podían detectar si un atacante había capturado y alterado los datos que pasaban entre el punto de acceso inalámbrico y un cliente inalámbrico. Otro avance de la seguridad de las claves fue el protocolo de integridad de la clave temporal (TKIP). El estándar de TKIP mejoró la capacidad para manejar, proteger y modificar las claves de cifrado. La ⁪norma de cifrado avanzado (AES) reemplazó el TKIP para una mejor protección de la administración y cifrado de claves.

El WPA, como su predecesor WEP, incluyó varias vulnerabilidades ampliamente reconocidas. Como resultado, el lanzamiento del estándar de acceso protegido a Wi-Fi II (WPA2) tuvo lugar en el año 2006. Una de las mejoras más importantes en la seguridad del WPA al WPA2 fue el uso obligatorio de los algoritmos de la AES y la introducción del modo de cifrado inverso con protocolo de código de autenticación de mensajes encadenados en bloques (CCM) como reemplazo del TKIP.

### Autenticación mutua

Una de las grandes vulnerabilidades de las redes inalámbricas es el uso de puntos de acceso falsos. Los puntos de acceso son dispositivos que se comunican con los dispositivos inalámbricos y se conectan a la red cableada. Todo dispositivo que tenga un transmisor inalámbrico y una interfaz cableada a una red pueden actuar potencialmente como puntos de acceso no autorizados o falsos. El punto de acceso falso puede imitar un punto de acceso autorizado. El resultado es que los dispositivos inalámbricos de la red inalámbrica se comunican con el punto de acceso falso en lugar del punto de acceso autorizado. 

El impostor puede recibir solicitudes de conexión, copiar los datos de la solicitud y transmitir los datos al punto de acceso a la red autorizado. Este tipo de ataque de intermediarios es muy difícil de detectar y puede generar el robo de las credenciales de inicio de sesión y los datos transmitidos. Para evitar los puntos de acceso falsos, el sector informático desarrolló la autenticación mutua. La autenticación mutua, también llamada autenticación de dos vías, es un proceso o una tecnología donde ambas entidades en un enlace de comunicación se autentican unas a otras. En un entorno de red inalámbrica, el cliente autentica el punto de acceso y el punto de acceso autentica el cliente. Esta mejora permitió a los clientes detectar puntos de acceso falsos antes de conectarse al dispositivo no autorizado.

## Protección de datos del host

### Control de acceso a los archivos

Los permisos son las reglas configuradas para limitar el acceso a una carpeta o un archivo a una persona o un grupo de usuarios.

- **Principio de privilegios mínimos**: Debe limitarse el acceso de los usuarios únicamente a los recursos que necesitan de un sistema informático o una red. Por ejemplo, no deberían poder acceder a todos los archivos en un servidor si solo necesitan acceso a una carpeta. Limitar el acceso a los recursos también permite evitar el acceso de programas malintencionados a dichos recursos en caso de que se infecte la computadora del usuario.
- **Restricción de los permisos de usuario**: Si un administrador deniega los permisos a un intercambio de red para una persona o un grupo, esta denegación anula cualquier otra configuración de permisos. Por ejemplo, si un administrador le niega el permiso de acceso a un intercambio de red a una persona, el usuario no podrá acceder a este intercambio aunque sea el administrador o forme parte del grupo de administradores. La política de seguridad local debe describir los recursos a los que puede acceder cada usuario y cada grupo y el tipo de acceso para cada uno.

Además, la ubicación de los datos y la acción realizada en los datos determinan la propagación de los permisos:
-   Los datos que se transmiten al mismo volumen mantienen los permisos originales.
-   Los datos que se copian en el mismo volumen heredan los nuevos permisos.
-   Los datos que se transfieren a otro volumen heredan los nuevos permisos.
-   Los datos que se copian en otro volumen heredan los nuevos permisos.

### Encriptación de archivos

La encriptación es una herramienta que se usa para proteger datos. La encriptación transforma los datos con un algoritmo complicado para que no puedan leerse. Una clave especial transforma la información ilegible en información legible. Los programas de software cifran archivos, carpetas e incluso unidades enteras.

El sistema de cifrado de archivos (EFS) es una característica de Windows que permite cifrar datos. La implementación de Windows del EFS se conecta directamente con la cuenta de un usuario específico. Solo el usuario que cifró los datos podrá acceder a las carpetas o los archivos cifrados.

Un usuario también puede elegir cifrar una unidad de disco duro completa en Windows con una función denominada BitLocker. Para utilizar BitLocker, se debe contar con dos volúmenes como mínimo en un disco duro.

Antes de utilizar BitLocker, el usuario debe habilitar el módulo de plataforma confiable (TPM) en el BIOS. El TPM es un chip especializado que se instala en la placa madre. El TPM almacena información específica del sistema host, como claves de cifrado, certificados digitales y contraseñas. Las aplicaciones, como BitLocker, que utilizan cifrado pueden aprovechar el chip del TPM. Haga clic en Administración del TPM para ver los detalles del TPM, como se muestra en la figura.

BitLocker To Go cifra unidades extraíbles. BitLocker To Go no utiliza un chip del TPM, pero aún proporciona cifrado para datos y requiere una contraseña.

### Sistema y copias de respaldo de datos

La realización de copias de respaldo de datos es uno de los métodos más eficaces para evitar la pérdida de estos. Si el hardware de la computadora falla, el usuario puede restaurar los datos de la copia de respaldo una vez que el sistema sea funcional.

La política de seguridad de la organización debe incluir copias de respaldo de datos. Los usuarios deben realizar copias de respaldo de datos con regularidad. Las copias de respaldo de datos suelen almacenarse externamente para proteger los medios de copia de respaldo en caso de que ocurra algo en la instalación principal.

Las siguientes son algunas consideraciones para las copias de respaldo de datos:
-   Frecuencia: La realización de copias de respaldo puede llevar mucho tiempo. En ocasiones, es más sencillo realizar una copia de respaldo completa mensual o semanalmente y luego realizar copias de respaldo parciales de los datos que se hayan modificado desde la última copia de respaldo completa. No obstante, tener muchas copias de respaldo parciales incrementa el tiempo necesario para restaurar los datos.
-   Almacenamiento: Para mayor seguridad, las copias de respaldo se deben trasladar a una ubicación de almacenamiento externa diariamente, semanalmente o mensualmente, según lo exija la política de seguridad.
-   Seguridad: proteja las copias de respaldo con contraseñas. El operador debe ingresar la contraseña antes de restaurar los datos de los medios de copia de respaldo.
-   Validación: Siempre deben validarse las copias de respaldo para garantizar la integridad de los datos.

## Control de contenido e imágenes

### Bloqueo y filtración de contenido

El software de control de contenido puede bloquear los sitios que contienen ciertos tipos de materiales, como pornografía o contenido político o religioso controversial. Un padre puede implementar el software de control de contenido en la computadora utilizada por un niño. Las bibliotecas y las escuelas también implementan el software para evitar el acceso a contenido considerado censurable.

Un administrador puede implementar los siguientes tipos de filtros:
-   Filtros basados en el navegador mediante una extensión de navegador de terceros.
-   Filtros de correo electrónico mediante un filtro basado en el servidor o cliente.
-   Filtros del lado del cliente instalados en una computadora específica.
-   Filtros de contenido basados en el router que bloquean el ingreso de tráfico en la red.
-   Filtros de contenido basados en dispositivos similares a los basados en el router.
-   Filtros de contenido basados en la nube.

### Congelamiento y clonación de discos

La clonación de discos copia el contenido del disco duro de la computadora en un archivo de imagen. Por ejemplo, un administrador crea las particiones requeridas en un sistema, formatea la partición y luego instala el sistema operativo. Instala todo el software de aplicación requerido y configura todo el hardware. El administrador utiliza el software de clonación de discos para crear el archivo de imagen. El administrador puede utilizar la imagen clonada de la siguiente manera:
-   Para limpiar automáticamente un sistema y restaurar la imagen principal limpia.
-   Para implementar nuevas computadoras dentro de la organización.
-   Para proporcionar una copia de respaldo del sistema completa.

La congelación bloquea la partición de la unidad de disco duro. Cuando un usuario reinicia un sistema, el sistema se revierte a la configuración congelada. El sistema no guarda ningún cambio del usuario, por lo que cualquier aplicación instalada o archivo guardado se pierden cuando el sistema se reinicia.

Si el administrador necesita cambiar la configuración del sistema, primero debe reanudar la partición protegida desactivando la congelación. Después de realizar los cambios, debe volver a activar el programa. El administrador puede configurar la congelación para que se reinicie después de que un usuario cierra sesión, después del apagado tras un período de inactividad o en un horario programado.

Estos productos no ofrecen protección en tiempo real. Un sistema sigue siendo vulnerable hasta que el usuario o un evento programado reinicien el sistema. Sin embargo, un sistema infectado con código malicioso obtiene un nuevo comienzo ni bien se reinicia el sistema.

## Protección física de las estaciones de trabajo

### Cerraduras y cables de seguridad

Existen varios métodos para proteger físicamente los equipos informáticos:
-   Utilizar seguros de cables en los equipos.
-   Mantener cerradas las salas de telecomunicaciones.
-   Utilizar jaulas de seguridad alrededor de los equipos.

### Temporizadores de cierre de sesión

Un empleado se levanta y deja su computadora para tomar un descanso. Si el empleado no adopta ninguna medida para proteger su estación de trabajo, cualquier información en el sistema es vulnerable ante un usuario no autorizado. Una organización puede adoptar las siguientes medidas para impedir el acceso no autorizado:
- **Tiempo de espera de inactividad y bloqueo de pantalla**: Los empleados pueden o no cerrar sesión de sus computadoras cuando dejan el lugar de trabajo. Por lo tanto, es una de las mejores prácticas de seguridad configurar un temporizador de inactividad que desactive automáticamente al usuario y bloquee la pantalla después de un período determinado. El usuario debe volver a iniciar sesión para desbloquear la pantalla.
- **Horario de inicio de sesión**: En algunas situaciones, una organización puede desear que los empleados inicien sesión durante horas específicas, como de 7 a. m. a 6 p. m. El sistema bloquea los inicios de sesión en el horario fuera de las horas de inicio de sesión permitidas.

### Seguimiento por GPS

El sistema de posicionamiento global (GPS) utiliza satélites y computadoras para determinar la ubicación de un dispositivo. La tecnología del GPS es una característica estándar en los smartphones que proporciona seguimiento de la posición en tiempo real. El seguimiento por GPS puede identificar una ubicación en el rango de 100 metros. Esta tecnología está disponible para seguir a los hijos, los adultos mayores, las mascotas y los vehículos. Utilizar el GPS para localizar un teléfono celular sin el permiso del usuario es una invasión a la privacidad y es ilegal.

Muchas aplicaciones de telefonía celular utilizan el seguimiento del GPS para rastrear la ubicación de un teléfono. Por ejemplo, Facebook permite a los usuarios registrar una ubicación, que es visible para las personas en sus redes.

### Inventario y etiquetas de RFID

La identificación por radiofrecuencia (RFID) utiliza ondas de radio para identificar y rastrear objetos. Los sistemas de inventario de RFID usan etiquetas adjuntas a todos los elementos que una organización desea rastrear. Las etiquetas contienen un circuito integrado que se conecta a una antena. Las etiquetas de RFID son pequeñas y requieren muy poca energía, por lo que no necesitan batería para almacenar información para intercambiar con un lector. La RFID puede ayudar a automatizar el seguimiento de los activos o bloquear, desbloquear o configurar inalámbricamente los dispositivos electrónicos.

Los sistemas de RFID operan dentro de distintas frecuencias. Los sistemas de baja frecuencia tienen un rango de lectura más corto y tasas de lectura de datos más bajas, pero no son tan sensibles a las interferencias de las ondas de radio ocasionadas por los líquidos y metales presentes. Las frecuencias más altas tienen una velocidad de transferencia de datos más rápida y mayores rangos de lectura, pero son más sensibles a las interferencias de las ondas de radio.

## Acceso remoto seguro

### Administración del acceso remoto

El acceso remoto se refiere a cualquier combinación de hardware y software que permite a los usuarios acceder a una red interna local de manera remota.

Al habilitar esta función, se abre el puerto 3389, lo que puede ocasionar una vulnerabilidad si un usuario no necesita este servicio.

### Telnet, SSH y SCP

El shell seguro (SSH) es un protocolo que proporciona una conexión de administración segura (cifrada) a un dispositivo remoto. El SSH debe reemplazar a Telnet para las conexiones de administración. Telnet es un protocolo más antiguo que usa la transmisión no segura de texto no cifrado de la autenticación de inicio de sesión (nombre de usuario y contraseña) y de los datos transmitidos entre los dispositivos que se comunican. El SSH proporciona seguridad para las conexiones remotas mediante el cifrado seguro cuando se autentica un dispositivo (nombre de usuario y contraseña) y para los datos transmitidos entre los dispositivos de comunicación. El SSH utiliza el puerto TCP 22. Telnet utiliza el puerto TCP 23.

El protocolo de copia segura (SCP) transfiere de forma segura los archivos informáticos entre dos sistemas remotos. El SCP usa el SSH para la transferencia de datos (incluido el elemento de autenticación), por lo que el SCP garantiza la autenticidad y la confidencialidad de los datos en tránsito.

## Medidas administrativas

### Protección de puertos y servicios

Los ciberdelincuentes atacan los servicios que se ejecutan en un sistema porque saben que la mayoría de los dispositivos ejecuta más servicios o programas que los necesarios. Un administrador debe observar cada servicio para comprobar su necesidad y evaluar el riesgo. Elimine cualquier servicio innecesario.

Un método simple que muchos administradores usan para contribuir a la seguridad de la red ante accesos no autorizados es la inhabilitación de todos los puertos del switch que no se utilizan. Por ejemplo, si un switch tiene 24 puertos y hay tres conexiones Fast Ethernet en uso, es aconsejable inhabilitar los 21 puertos que no se utilizan.

El proceso de habilitación e inhabilitación de puertos puede llevar mucho tiempo, pero mejora la seguridad de la red y vale la pena el esfuerzo.

### Cuentas privilegiadas

Los ciberdelincuentes atacan las cuentas privilegiadas porque son las más poderosas dentro de la organización. Las cuentas privilegiadas tienen credenciales para acceder a los sistemas y brindan acceso elevado sin restricción. Los administradores usan estas cuentas para implementar y administrar los sistemas operativos, las aplicaciones y los dispositivo de red. Los distintos tipos de cuentas privilegiadas son:
- Cuentas administrativas locales
- Cuentas de usuario con privilegios
- Cuentas administrativas de dominio
- Cuentas de emergencia
- Cuentas de servicio
- Cuentas de aplicaciones

La organización debe adoptar las siguientes mejores prácticas para proteger las cuentas privilegiadas:
-   Identificar y reducir la cantidad de cuentas privilegiadas.
-   Aplicar el principio de privilegios mínimos.
-   Establecer un proceso para la revocación de derechos cuando los empleados dejan o cambian de trabajo.
-   Eliminar las cuentas compartidas con contraseñas que no caducan.
-   Proteger el almacenamiento de contraseñas.
-   Eliminar las credenciales compartidas entre varios administradores.
-   Cambiar automáticamente las contraseñas de la cuenta privilegiada cada 30 o 60 días.
-   Registrar las sesiones privilegiadas.
-   Implementar un proceso para cambiar las contraseñas integradas para los scripts y las cuentas de servicio.
-   Registrar toda la actividad del usuario.
-   Generar las alertas para comportamientos inusuales.
-   Deshabilitar las cuentas privilegiadas inactivas.
-   Usar la autenticación de varios factores para todo el acceso administrativo.
-   Implementar un gateway entre el usuario final y los activos confidenciales para limitar la exposición de la red al malware.

Bloquear las cuentas privilegiadas es fundamental para la seguridad de la organización. Proteger estas cuentas debe ser un proceso continuo. Una organización debe evaluar el proceso de realización de todos los ajustes necesarios para mejorar la seguridad.

### Políticas de grupo

En la mayoría de las redes que usan computadoras Windows, un administrador configura Active Directory con dominios en Windows Server. Las computadoras con Windows son miembros de un dominio. El administrador configura una directiva de seguridad de dominio que se aplica a todas las computadoras que se unan. Las directivas de cuenta se configuran automáticamente cuando un usuario inicia sesión en Windows.

Cuando una computadora no es parte de un dominio de Active Directory, el usuario configura las políticas a través de la política de seguridad local de Windows. En todas las versiones de Windows, excepto la edición doméstica, ingrese **secpol.msc** en Ejecutar comando para abrir la herramienta de política de seguridad local.

Un administrador configura las políticas de cuenta de usuario, como políticas de contraseña y políticas de bloqueo, expandiendo Políticas de cuentas > Políticas de contraseñas. Con las configuraciones los usuarios deben cambiar sus contraseñas cada 90 días y utilizar la nueva contraseña al menos un (1) día, entre otras cosas. Las contraseñas deben contener ocho (8) caracteres y tres de las siguientes cuatro categorías: letras mayúsculas, letras minúsculas, números y símbolos. Por último, el usuario puede reutilizar la contraseña después de 24 contraseñas únicas. Esos son ejemplos de políticas que se pueden poner a funcionar desde la pestaña de políticas de windows.

Una política de bloqueo de cuentas bloquea una computadora durante un tiempo determinado cuando ocurren demasiados intentos de acceso incorrecto al sistema. Por ejemplo, una política permite que el usuario introduzca un nombre de usuario o una contraseña incorrectos cinco veces. Después de cinco intentos, la cuenta queda bloqueada por 30 minutos. Después de 30 minutos, la cantidad de intentos se restablece a cero y el usuario puede intentar iniciar sesión nuevamente.

Hay más configuraciones de seguridad disponibles ampliando la carpeta **Políticas locales**. Una política de auditoría crea un archivo de registro de seguridad que se utiliza para rastrear los eventos.

### Habilitación de registros y alertas

Un registro registra todos los eventos a medida que ocurren. Las entradas de registro conforman el archivo de registro y contienen toda la información relacionada con un evento específico. Los registros relacionados con la seguridad informática han crecido en importancia.

Por ejemplo, un registro de auditoría sigue los intentos de autenticación del usuario y un registro de acceso proporciona todos los datos de solicitudes de archivos específicos en un sistema. Monitorear los registros del sistema puede determinar cómo se produjo un ataque y si las defensas implementadas se realizaron correctamente.

Con el aumento de la gran cantidad de archivos de registro generados para fines de seguridad informática, una organización debe considerar el proceso de administración de registros. La administración de registros determina el proceso para generar, transmitir, almacenar, analizar y eliminar datos de registro de seguridad informática.

Tipos de registros:
- **Registros del sistema operativo**: Los registros del sistema operativo registran eventos que ocurren por acciones operativas realizadas por el sistema operativo. Los eventos del sistema incluyen lo siguiente:
	-   Las solicitudes de clientes y las respuestas de servidores, como autenticaciones de usuario exitosas.
	-   Información de uso que contiene la cantidad y el tamaño de las transacciones en un período determinado.
- **Registros de aplicación de seguridad**: Las organizaciones utilizan software de seguridad basado en la red o el sistema para detectar actividades maliciosas. Este software genera un registro de seguridad para proporcionar datos de seguridad informática. Los registros son útiles para realizar el análisis de auditoría e identificar las tendencias y los problemas a largo plazo. Los registros además permiten que una organización proporcione documentación que evidencie el cumplimiento de las leyes y los requisitos normativos.

## Proteccion fisica de los servidores

### Alimentación

Un aspecto crítico de la protección de los sistemas de información son los sistemas y las consideraciones de energía eléctrica. El suministro constante de electricidad es fundamental en las actuales instalaciones de almacenamiento de datos y servidores masivos. Estas son algunas reglas generales en el desarrollo de sistemas de suministro eléctrico eficaces:
-   Los centros de datos deben estar en una fuente de alimentación distinta al resto del edificio.
-   Fuentes de alimentación redundantes: dos o más fuentes que provienen de dos o más subestaciones eléctricas.
-   Acondicionamiento de la energía.
-   Con frecuencia se requieren sistemas energéticos de respaldo.
-   Debe contarse con un UPS para apagar satisfactoriamente los sistemas.
Una organización debe protegerse contra varios problemas al diseñar sus sistemas de fuente de alimentación eléctrica:
- **Exceso de energía**: 
	-   Sobre voltaje: Alto voltaje momentáneo.
	-   Explosión: Alto voltaje prolongado.
- **Pérdida de energía**:
	-   Falla: Pérdida de energía momentánea.
	-   Apagón: Pérdida de energía completa.
- **Degradación de energía**:
	-   Holgura/caída: Bajo voltaje momentáneo.
	-   Apagón: Bajo voltaje prolongado.
	-   Corriente de irrupción: sobre voltaje inicial de energía.

### Calefacción, ventilación y aire acondicionado (HVAC)

Los sistemas de HVAC son fundamentales para la seguridad de las personas y los sistemas de información en las instalaciones de la organización. Al diseñar instalaciones de TI modernas, estos sistemas juegan un papel importante en la seguridad general. Los sistemas de HVAC controlan el entorno ambiental (temperatura, humedad, flujo de aire y filtración de aire) y deben planificarse y operarse junto a otros componentes de centros de datos, como hardware informático, cableado, almacenamiento de datos, protección contra incendios, sistemas de seguridad física y energía. Casi todos los dispositivos de hardware informático físicos tienen requisitos ambientales que incluyen temperatura y rangos de humedad aceptables. Los requisitos ambientales aparecen en un documento de especificaciones del producto o en una guía de planificación física. Es fundamental mantener estos requisitos ambientales para evitar fallas del sistema y extender la vida útil de los sistemas de TI. Los sistemas de HVAC comerciales y otros sistemas de administración de edificios ahora se conectan a Internet para su supervisión y control. Eventos recientes han demostrado que dichos sistemas (a menudo denominados “sistemas inteligentes”) también aumentan las repercusiones de seguridad.

Uno de los riesgos asociados a los sistemas inteligentes es que las personas que acceden y administran el sistema trabajan para un contratista o un proveedor externo. Debido a que los técnicos de HVAC necesitan encontrar la información rápidamente, los datos cruciales tienden a almacenarse en muchos lugares diferentes, lo que los hace accesibles a muchas más personas. Tal situación permite que una amplia red de individuos, entre ellos, asociados de los contratistas, accedan a las credenciales del sistema de HVAC. La interrupción de estos sistemas puede representar un riesgo considerable para la seguridad informática de la organización.

### Supervisión de hardware

El monitoreo de hardware a menudo se encuentra en torres de servidores grandes. Una torre de servidores es una instalación que aloja cientos o miles de servidores de empresas. Google tiene muchas torres de servidores en todo el mundo para proporcionar servicios óptimos. Incluso las empresas más pequeñas construyen torres de servidores locales para alojar el creciente número de servidores necesarios para realizar los negocios. Los sistemas de control de hardware se utilizan para monitorear el estado de dichos sistemas y minimizar el tiempo de inactividad de la aplicación y el servidor. Los sistemas de control de hardware modernos utilizan los puertos de red y USB para transmitir la condición de temperatura de la CPU, el estado de la fuente de alimentación, la velocidad y la temperatura del ventilador, el estado de la memoria, el espacio en disco y el estado de la tarjeta de red. Los sistemas de control de hardware permiten a un técnico supervisar cientos o miles de sistemas desde un solo terminal. A medida que la cantidad de torres de servidores aumenta, los sistemas de control de hardware se han convertido en contramedidas esenciales para la seguridad.

## Protección de dispositivos de red

### Centros de operaciones

El Centro de Operaciones de Red (NOC) se compone de una o más ubicaciones que contienen las herramientas que proporcionan a los administradores un estado detallado de la red de una organización. El NOC es el punto cero de la solución de problemas, la supervisión del rendimiento, la distribución de software y actualizaciones, la administración de comunicaciones y la administración de dispositivos.

El Centro de Operaciones de Seguridad (SOC) es un sitio dedicado que supervisa, evalúa y protege los sistemas de información de la organización, como sitios web, aplicaciones, bases de datos, centros de datos, redes, servidores y sistemas de usuario. Un SOC es un equipo de expertos en seguridad que detectan, analizan, responden, informan y evitan incidentes de ciberseguridad.

Ambas entidades usan una estructura de nivel jerárquico para administrar los eventos. El primer nivel administra todos los eventos e incluye cualquier evento que no pueda administrarse en el segundo nivel. El personal del segundo nivel revisa el evento en detalle para intentar resolverlo. Si no pueden hacerlo, pasan el evento al tercer nivel, el de los expertos en la materia.

Para medir la eficacia general de un centro de operaciones, una organización impulsará ejercicios y prácticas realistas. Un ejercicio de simulación de tablero es un recorrido estructurado de un equipo para simular un evento y evaluar la eficacia del centro. Una medida más eficaz es simular una intrusión hecha y derecha sin advertencia. Esto supone el uso de un equipo rojo, un grupo independiente de personas que desafía los procesos en una organización para evaluar su eficacia. Por ejemplo, el equipo rojo debe atacar un sistema crítico, incluidos el reconocimiento y el ataque, el escalamiento de privilegios y el acceso remoto.

### Switches, routers y dispositivos de red

Los dispositivos de red se envían sin contraseñas o con contraseñas predeterminadas. Cambie las contraseñas predeterminadas antes de conectar un dispositivo a la red. Documente y registre los cambios en los dispositivos de red. Por último, examine todos los registros de configuración.

En las siguientes secciones se analizan varias medidas que un administrador puede adoptar para proteger diferentes dispositivos de red:
- **Switches**: son el corazón de la red de comunicación de datos moderna. Las principales amenazas para los switches de red son el robo, el hacking y el acceso remoto, los ataques contra los protocolos de red, como ARP/STP, o los ataques contra el rendimiento y la disponibilidad. Varias contramedidas y controles pueden proteger los switches de red, incluidas la seguridad física mejorada, la configuración avanzada y la implementación de actualizaciones y parches adecuados del sistema según sea necesario. Otro control eficaz es la implementación de la seguridad de los puertos. Un administrador debe proteger todos los puertos de switch (interfaces) antes de implementar el switch para fines de producción. Una forma de proteger los puertos es mediante la implementación de una característica denominada “seguridad de puertos”. La seguridad de puertos limita la cantidad de direcciones MAC válidas permitidas en el puerto. El switch permite el acceso a dispositivos con direcciones MAC legítimas y rechaza otras direcciones MAC.
- **VLAN**: ofrecen una forma de agrupar dispositivos dentro de una LAN y en switches individuales. Las VLAN usan conexiones lógicas en lugar de conexiones físicas. Los puertos individuales de switch pueden asignarse a una VLAN específica. Se pueden usar otros puertos para interconectar físicamente los switches y permitir el tráfico de varias VLAN entre los switches. Estos puertos se denominan enlaces troncales.
	Los dispositivos dentro de una VLAN funcionan como si estuvieran en su propia red independiente, aunque compartan una misma infraestructura con otras VLAN. Una VLAN puede separar los grupos que tienen datos confidenciales del resto de la red, lo que disminuye las posibilidades de violaciones de la información confidencial. Los enlaces troncales permiten que las personas en la VLAN de RR. HH. se conecten físicamente a varios switches.
	Existen varios tipos de vulnerabilidades y ataques de VLAN diferentes. Estos pueden incluir ataques a los protocolos de los enlaces troncales y la VLAN. Los hackers también pueden atacar el rendimiento y la disponibilidad de la VLAN. Las contramedidas comunes incluyen el monitoreo de los cambios y el rendimiento de la VLAN, las configuraciones avanzadas, y los parches y las actualizaciones regulares del sistema para el IOS.
- **Firewalls**
- **Routers**: Los routers forman la red troncal de Internet y las comunicaciones entre las diferentes redes. Los routers se comunican unos con otros para identificar la mejor ruta posible a fin de distribuir el tráfico a las diferentes redes. Los routers usan protocolos de routing para tomar decisiones de routing. Los routers también pueden integrar otros servicios, como las funcionalidades de switching y firewall. Estas operaciones hacen que los routers sean los principales objetivos. Las principales amenazas para los routers de red son el robo, el hacking y el acceso remoto, los ataques contra los protocolo de routing, como RIP/OSPF, o los ataques contra el rendimiento y la disponibilidad. Varias contramedidas y controles pueden proteger los routers de red, entre ellos, la seguridad física mejorada, la configuración avanzada, el uso de protocolos de routing seguros con autenticación, y la implementación de actualizaciones y parches adecuados del sistema según sea necesario.

## Dispositivos móviles e inalámbricos

Los dispositivos móviles e inalámbricos se han convertido en el tipo de dispositivo predominante en la mayoría de las redes modernas. Ofrecen movilidad y conveniencia, pero representan un conjunto de vulnerabilidades. Estas vulnerabilidades incluyen el robo, el hacking y el acceso remoto no autorizado, el espionaje, los ataques de intermediarios, y los ataques contra el rendimiento y la disponibilidad. La mejor manera de proteger una red inalámbrica es utilizar la autenticación y el cifrado. El estándar inalámbrico original (801.11) introdujo dos tipos de autenticación:
-   Autenticación del sistema abierto: Cualquier dispositivo inalámbrico puede conectarse a la red inalámbrica. Use este método en situaciones donde la seguridad no sea un problema.
-   Autenticación de clave compartida: Proporciona mecanismos para autenticar y cifrar datos entre el cliente inalámbrico y un AP o router inalámbrico.

Las tres técnicas de autenticación de clave compartida para las WLAN son las siguientes:
-   Privacidad equivalente por cable (WEP): era la especificación 802.11 original que protegía las WLAN. Sin embargo, la clave de cifrado nunca cambiaba al intercambiar paquetes, por lo que era fácil de descifrar.
-   Acceso protegido a Wi-Fi (WPA): este estándar utiliza la WEP, pero protege los datos con un algoritmo de cifrado del protocolo de integridad de clave temporal (TKIP), que es mucho más seguro. El TKIP cambia la clave para cada paquete, lo que hace que sea mucho más difícil de descifrar.
-   IEEE 802.11i/WPA2:: IEEE 802.11i es un estándar de la industria para proteger las WLAN. Tanto 802.11i como WPA2 usan la ⁪norma de cifrado avanzado (AES) para el cifrado, actualmente el protocolo de encriptación más sólido.

Desde 2006, cualquier dispositivo que tenga el logotipo de Certificado para Wi-Fi tiene la certificación WPA2. Por lo tanto, las WLAN modernas deben utilizar el estándar 802.11i/WPA2. Otras contramedidas incluyen la seguridad física mejorada y las actualizaciones y los parches regulares del sistema de los dispositivos.

### Servicios de routing y red

Los ciberdelincuentes usan servicios de red vulnerables para atacar un dispositivo o usarlo como parte del ataque. Para verificar si existen servicios de red inseguros, revise el dispositivo y busque puertos abiertos mediante un escáner de puertos. Proteger los servicios de red garantiza que solo los puertos necesarios estén expuestos y disponibles.

- **Protocolo de configuración dinámica de host (DHCP)**: El DHCP usa un servidor para asignar una dirección IP y otra información de configuración automáticamente a los dispositivos de red. En efecto, el dispositivo obtiene un formulario de permiso del servidor del DHCP para utilizar la red. Los atacantes pueden apuntar a los servidores del DHCP para denegar el acceso a los dispositivos en la red.
- **Sistema de nombres de dominio (DNS)**: El DNS resuelve una dirección de sitio web o URL de localizador de recursos uniforme [Cisco](http://www.cisco.com) para la dirección IP del sitio. Cuando los usuarios escriben una dirección web en la barra de direcciones, dependen de los servidores del DNS para resolver la dirección IP real del destino. Los atacantes apuntan a los servidores del DNS para denegar el acceso a los recursos de la red o redirigir el tráfico a sitios web falsos.
- **Protocolo de mensajes de control de Internet (ICMP)**: Los dispositivos de red usan ICMP para enviar mensajes de error, como un servicio solicitado que no está disponible o un host que no puede llegar a un router. El comando ping es una utilidad de red que emplea ICMP para probar la posibilidad de conexión de un host en una red. El ping envía mensajes de ICMP al host y espera una respuesta. Los ciberdelincuentes pueden alterar el uso de ICMP para los fines maliciosos. Los ataques de denegación de servicio usan ICMP. Muchas redes filtran ciertas solicitudes de ICMP para evitar estos ataques.
- **Protocolo de información de enrutamiento (RIP)**: El RIP limita la cantidad de saltos permitida en una ruta en una red desde el dispositivo de origen hasta el destino. La cantidad máxima de saltos permitida para el RIP es quince. El RIP es un protocolo de routing que se usa para intercambiar información de routing sobre qué redes alcanza cada router y el alcance de dichas redes. El RIP calcula la mejor ruta según el recuento de saltos. Los hackers pueden atacar los routers y el RIP. Los ataques a los servicios de routing pueden afectar el rendimiento y la disponibilidad. Algunos ataques incluso pueden dar como resultado el redireccionamiento del tráfico. Utilice los servicios seguros con autenticación e implemente parches y actualizaciones del sistema para proteger los servicios de routing, como el RIP.
- **Protocolo de tiempo de red (NTP)**: Es importante tener la hora correcta dentro de las redes. Las marcas de tiempo correctas hacen un seguimiento preciso de los eventos de red, por ejemplo, las violaciones de seguridad. Además, la sincronización de relojes es fundamental para la interpretación correcta de los eventos dentro de los archivos de datos syslog, así como para los certificados digitales.
	El protocolo de tiempo de red (NTP) es un protocolo que sincroniza los relojes de los sistemas informáticos sobre las redes de datos. El NTP permite que los dispositivos de red sincronicen la configuración de la hora con un servidor del NTP. Los ciberdelincuentes atacan los servidores de tiempo para interrumpir la comunicación segura que depende de certificados digitales y ocultar la información del ataque, como marcas de tiempo precisas.

## Equipos de voz y video

### Equipos de VoIP

La voz sobre IP (VoIP) utiliza redes, como Internet, para realizar y recibir llamadas telefónicas. El equipo requerido para VoIP incluye una conexión a Internet y un teléfono. Varias opciones están disponibles para los equipos de teléfono:
-   Un teléfono tradicional con un adaptador (el adaptador actúa como interfaz de hardware entre el teléfono analógico tradicional y la línea de VoIP digital).
-   Un teléfono habilitado para VoIP.
-   Software de VoIP instalado en una computadora.

La mayoría de los servicios de VoIP para consumidores utiliza Internet para las llamadas telefónicas. Muchas organizaciones, sin embargo, utilizan sus redes privadas debido a que proporcionan una seguridad más sólida y un servicio de calidad. La seguridad de VoIP es tan confiable como la seguridad de red subyacente. Los ciberdelincuentes apuntan a estos sistemas para obtener acceso para liberar servicios telefónicos, escuchar llamadas telefónicas o afectar el rendimiento y la disponibilidad.

Implemente las siguientes contramedidas para proteger la VoIP:
-   Cifre los paquetes de mensajes de voz para protegerlos de las infiltraciones.
-   Utilice el SSH para proteger los gateways y switches.
-   Cambie las contraseñas predeterminadas.
-   Utilice un sistema de detección de intrusiones para detectar ataques, como el envenenamiento del ARP.
-   Utilice la autenticación sólida para mitigar la suplantación de registros (los ciberdelincuentes enrutan todas las llamadas entrantes de la víctima hacia ellos), la suplantación del proxy (engaña a la víctima para que se comunique con un proxy falso establecido por los ciberdelincuentes) y la usurpación de llamadas (la llamada se intercepta y redirige a una ruta diferente antes de que llegue al destino).
-   Implemente firewalls que reconozcan la VoIP para monitorear las transmisiones y filtrar las señales anormales.

Cuando la red deja de funcionar, también lo hacen las comunicaciones de voz.

### Cámaras

Una cámara de Internet envía y recibe datos a través de una LAN o Internet. Un usuario puede ver de forma remota video en vivo con un explorador web en una amplia variedad de dispositivos, entre ellos, sistemas informáticos, PC portátiles, tablets y smartphones.

Las cámaras vienen en distintos formatos, incluidas las cámaras de seguridad tradicionales. Otras opciones incluyen cámaras de Internet discretamente ocultas en radiodespertadores, libros o reproductores de DVD.

Las cámaras de Internet transmiten video digital a través de una conexión de datos. La cámara se conecta directamente a la red y tiene todo lo necesario para transferir las imágenes sobre la red.

### Equipo de videoconferencia

La videoconferencia permite que dos o más ubicaciones se comuniquen de forma simultánea mediante tecnologías de telecomunicación. Estas tecnologías aprovechan los nuevos estándares de video de alta definición. 

El equipo de videoconferencia puede ser muy costoso y es un objetivo de alto valor para los ladrones y ciberdelincuentes. Los ciberdelincuentes apuntan a estos sistemas para infiltrarse en las videollamadas o afectar el rendimiento y la disponibilidad.

### Red y sensores de IdC

Uno de los sectores más rápidos de la tecnología de la información es el uso de sensores y dispositivos inteligentes. La industria informática lidera este sector como Internet de las cosas (IdC). Las empresas y los consumidores usan dispositivos de IdC para automatizar procesos, supervisar condiciones del entorno y alertar a los usuarios acerca de condiciones adversas. La mayoría de los dispositivos de IdC se conecta a una red a través de la tecnología inalámbrica e incluye cámaras, cerraduras de puertas, sensores de proximidad, luces y otros tipos de sensores utilizados para recopilar información acerca de un entorno o el estado de un dispositivo.

El sector de IdC representa un enorme desafío para los profesionales de seguridad de la información porque muchos dispositivos de IdC capturan y transmiten información confidencial. Los ciberdelincuentes apuntan a estos sistemas para interceptar los datos o afectar el rendimiento y la disponibilidad.

## Control de acceso fisico

### Cercas y barricadas

Las barreras físicas son lo primero que viene a la mente cuando se piensa en la seguridad física. Este es el nivel más remoto de seguridad y estas soluciones son las más visibles públicamente. Un sistema de seguridad perimetral generalmente consta de los siguientes componentes:
-   Un sistema de cerca perimetral.
-   Un sistema de puerta de seguridad.
-   Bolardos (pequeños postes utilizados para protegerse contra intrusiones de vehículos, como se muestra en la Figura 2).
-   Barreras de entrada de vehículos.
-   Refugios de protección.

Una cerca es una barrera que comprende áreas seguras y designa límites de la propiedad. Todas las barreras deben cumplir los requisitos de diseño específicos y las especificaciones de la estructura. Las áreas de alta seguridad a menudo requieren una “protección superior”, como un alambre de púas o concertina. Al diseñar el perímetro, los sistemas de cercado utilizan las siguientes reglas:
-   1 metro (3 a 4 pies) solo disuadirán a los intrusos casuales.
-   2 metros (6 a 7 pies) son muy altos para escalar para los intrusos casuales.
-   2,5 metros (8 pies) ofrecerán una demora limitada a un intruso determinado.
-   Las protecciones superiores proporcionan un impedimento adicional y pueden cortar gravemente al intruso; sin embargo, los atacantes pueden utilizar una manta o un colchón para mitigar esta amenaza.

Las normas locales pueden restringir el tipo de sistema de cercado que usa una organización.

Las cercas requieren un mantenimiento regular. Los animales pueden cavar debajo de la cerca o la tierra puede socavarse y dejar la cerca inestable, lo que proporcionará un acceso sencillo al intruso. Inspeccione los sistemas de cercado con regularidad. No aparque ningún vehículo junto a las cercas. Un vehículo aparcado en las inmediaciones de una cerca puede ayudar al intruso a escalar o dañar la cerca.

### Biometría

Los datos biométricos describen los métodos automatizados de reconocimiento de una persona en función de una característica fisiológica o conductual. Los sistemas de autenticación biométrica incluyen medidas del rostro, huellas digitales, geometría de la mano, iris, retina, firma y voz. Las tecnologías biométricas son la base de la identificación altamente segura y las soluciones de verificación personal. La popularidad y el uso de sistemas biométricos han aumentado debido a la mayor cantidad de infracciones a la seguridad y fraude de transacciones. Los datos biométricos proporcionan transacciones financieras confidenciales y privacidad de los datos personales.

Al comparar los sistemas biométricos, hay varios factores importantes que se deben considerar, entre ellos, la precisión, la tasa de velocidad o rendimiento, la aceptación de los usuarios, la singularidad de las acciones u órganos biométricos, la resistencia a la falsificación, la confiabilidad, los requisitos de almacenamiento de datos, el tiempo de inscripción y la impertinencia del análisis. El factor más importante es la precisión. La precisión se expresa en los índices y los tipos de errores.

El primer índice de error es el Error de tipo I o los falsos rechazos. El Error de tipo I rechaza a una persona que se registra y es un usuario autorizado. En el control de acceso, si el requisito es mantener a los malos afuera, el falso rechazo es el error menos grave.

La velocidad de aceptación se expone como porcentaje y es la velocidad con la que un sistema acepta a las personas no registradas o los impostores como usuarios auténticos. La falsa aceptación es un Error de tipo II. El Error de tipo II permite el ingreso de los delincuentes, por lo que normalmente se considera el error más importante para un sistema de control de acceso biométrico.

El método más ampliamente utilizado para medir la precisión de la autenticación biométrica es el índice de error de conexión cruzada (CER). El CER es la velocidad donde la velocidad de falso rechazo y la velocidad de aceptación falsa son equivalentes, como se muestra en la figura.

### Registros de acceso y tarjetas de identificación

La tarjeta de identificación de acceso permite que una persona obtenga acceso a un área con puntos de ingreso automatizados. Un punto de ingreso puede ser una puerta, un molinete, una entrada u otra barrera. Las tarjetas de identificación de acceso usan varias tecnologías, como una cinta magnética, un código de barras o la biometría.

Un lector de tarjetas lee un número contenido en la tarjeta de identificación de acceso. El sistema envía el número a una computadora que toma las decisiones de control de acceso en función de las credenciales provistas. El sistema registra la transacción para su posterior recuperación. Los informes revelan quién ingresó, el punto de ingreso y la hora.


## Vigilancia

### Guardias y escoltas

Todos los controles de acceso físico, incluidos los sistemas de disuasión y detección, dependen en última instancia del personal para intervenir y detener el ataque o la intrusión real. En las instalaciones de sistemas de información de alta seguridad, los guardias controlan el acceso a las áreas confidenciales de la organización. El beneficio de usar guardias es que pueden adaptarse más que los sistemas automatizados. Los guardias pueden descubrir y diferenciar varias condiciones y situaciones y tomar decisiones en el lugar. Los guardias de seguridad son la mejor solución para el control de acceso cuando la situación requiere una respuesta correcta e instantánea. Sin embargo, los guardias no son siempre la mejor solución. Existen numerosas desventajas en el uso de guardias de seguridad, como el costo y la capacidad para supervisar y registrar el tráfico de alto volumen. El uso de guardias también introduce el error humano en la combinación.

### Vigilancia por video y electrónica

La vigilancia por video y electrónica complementa o, en algunos casos, reemplaza a los guardias de seguridad. El beneficio del video y la vigilancia electrónica es la capacidad de supervisar las áreas cuando no hay guardias ni personal presente, la capacidad de registrar datos y videos de vigilancia durante largos períodos y la capacidad de incorporar la detección de movimiento y la notificación.

La vigilancia por video y electrónica también puede ser más precisa en la captura de eventos incluso después de que ocurran. Otra ventaja importante es que la vigilancia por video y electrónica ofrece puntos de vista que no se obtienen fácilmente con los guardias. También puede resultar mucho más económica que el uso de cámaras para supervisar el perímetro completo de una instalación. En un entorno altamente seguro, una organización debe colocar la vigilancia por video y electrónica en todas las entradas, las salidas, los compartimientos de carga, las escaleras y las áreas de recolección de basura. En la mayoría de los casos, la vigilancia por video y electrónica complementa a los guardias de seguridad.

### Vigilancia inalámbrica e RFID

Administrar y localizar activos de sistemas de información importantes constituyen un desafío clave para la mayoría de las organizaciones. El crecimiento en la cantidad de dispositivos móviles y dispositivos de IdC ha hecho que este trabajo sea incluso más difícil. El tiempo que insume buscar equipos críticos puede provocar costosas demoras o tiempo de inactividad. El uso de etiquetas de identificación de recursos de identificación por radiofrecuencia (RFID) puede ser de gran valor para el personal de seguridad. Una organización puede posicionar lectores de RFID en los marcos de las puertas de las áreas seguras de manera tal que no sean visibles para las personas.

El beneficio de las etiquetas de identificación de recursos de RFID es que pueden seguir cualquier activo que deje físicamente un área segura. Los nuevos sistemas de etiquetas de identificación de recursos de RFID pueden leer múltiples etiquetas en simultáneo. Los sistemas de RFID no requieren una línea de visión para analizar las etiquetas. Otra ventaja de la RFID es la capacidad para leer las etiquetas que no son visibles. A diferencia de los códigos de barras y las etiquetas legibles para los humanos que deben ubicarse físicamente y ser visibles para leer, las etiquetas de RFID no necesitan ser visibles para su análisis. Por ejemplo, etiquetar una PC debajo de un escritorio requiere que el personal se agache debajo el escritorio para ubicar y visualizar físicamente la etiqueta mediante un proceso de código de barras o manual. Una etiqueta de RFID permitirá al personal escanear la etiqueta sin siquiera verla.

