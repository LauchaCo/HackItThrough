- Tipos de atacantes - Cubierto en [Toma de apuntes](</Cisco Networking Essentials/1 - Introduction to Cybersecurity/Unidad 1/Toma de apuntes>)

## Tipos de hackers

- __Script kiddies__: Se refiere a hackers adolescentes o inexpertos que ejecutan scripts, herramientas y ataques que pueden generar daños.
- __Agentes de vulnerabilidad__: Son generalmente hackers de sombrero gris que intentan descubrir ataques e informarlos a los proovedores a cambio de recompensas o premios.
- __Patrocinados por el estado__: Son atacantes que roban secretos de gobierno, recopilan inteligencia y sabotean redes. Sus objetivos son gobiernos, grupos terroristas y corporaciones extranjeras.
- __Hacktivistas__: Son hackers de sombrero gris que protestan contra ideas politicas y sociales. Los hacktivistas protestan en publico contra las organizaciones o los gobiernos mediante la publicacion de articulos, videos, filtracion de archivos confidenciales y la ejecucion de ataques de denegacion de servicio. 
- __Ciberdelincuentes__: Son hackers de sombrero negro que independientes o que trabajan para organizaciones de delito cibernetico. Cada año los delincuentes ciberneticos son responsable de perdidas millonarias de empresas e individuales.

## Por que la ciberseguridad?

- __Alta posibilidad de ganancias__ debido a el nivel de habilidad requerido para ser eficiente en esta profesion
- __Carrera dificil__ debido a la naturaleza dinamica de la tecnologia.
- __Carrera sumamente portatil__ debido a la gran cantidad de trabajos alrededor de todo el mundo
- __Servicio al publico__ debido a el nivel de servicio que aportan los especialistas en ciberseguridad a organizaciones, paises y empresas.

## Como frustrar a los ciberdelincuentes?

Acciones coordinadas de organizaciones y gobiernos en pos de detener los ataques:
- __Bases de datos de vulnerabilidades__: La creacion de bases de datos completas con firmas conocidas de vulnerabilidades y ataques del sistema (una disposicion unica de la informacion para detectar un atacante que intenta explotar una vulnerabilidad conocida). Las organizaciones comparten estas bases de datos en pos de la seguridad a nivel global en lo referente a vulnerabilidades conocidas. Un ejemplo podria ser la base de datos CVE (Common Vulnerabilities and Exposures)
- __Sistemas de advertencia temprana__: Establecimiento de sensores de advertencia temprana y redes de alerta. Debido al costo y la imposibilidad de supervisar cada red, las organizaciones supervisan los objetivos de alto perfil o crean impostores que se parecen a los objetivos de alto valor. Debido a que estos objetivos son mas propensos a recibir ataques, advierten a los otros de ataques potenciales. Un ejemplo es el proyecto HoneyNet
- __Compartir inteligencia cibernetica__: Las empresas y gobiernos se comparten informacion sobre ataques a objetivos de alto calibre para evitar que sucedan ataques similares en otros entes. Muchos paises han establecido servicios de inteligencia cibernetica para colaborar en este proceso alrededor del mundo. Un ejemplo de esta practica podria ser InfraGard, una asociacion entre el FBI y el sector privado.
- __Estandares ISM__: Establecimiento de estandares de administracion de seguridad de la info entre organizaciones nacionales e internacionales. ISO/IEC 27000 es un ejemplo de estos estandares.
- __Nuevas Leyes__: Promulgacion de nuevas leyes para desalentar los ataques ciberneticos y las violaciones de datos. Estas leyes tienen multas severas para los ciberdelincuentes que las infringan.

## Tipos de registros personales
- Revisar en [Apuntes unidad 1](<Cisco Networking Essentials/1 - Introduction to Cybersecurity/Unidad 1/Toma de apuntes>).

Sus datos:
- Datos sobre sus dispositivos informaticos
- Datos medicos
- Ocupacion
- Informacion en linea
- Su identidad
- Datos de educacion
- Datos financieros

## Amenazas a los servicios

Los servicios que necesitan las redes para funcionar incluyen routing, asignacion de direcciones, designacion de nombres y administracion de bases de datos. Debido a su gran importancia en la infraestructura son un principal objetivo para los atacantes y ciberdelincuentes. Las formas que tienen los hackers de lograr comprometer estos servicios son varias como por ej:
- Usar herramientas de analisis de paquetes para capturar flujos de datos en una red. Significando una perdida de confidencialidad en datos de usuarios.
- Implantar puntos de acceso fraudulentos, generando asi que sea robada toda la informacion que sea enviada a traves de estos.
- Suplantacion de identidad DNS (o envenenamiento de cache DNS) introduciendo datos en la cache de resolucion de DNS. Estos ataques atacan una debilidad en el software DNS que hace que los DNS redirijan el trafico de un dominio especifico a la computadora del delincuente.
- Falsificar paquetes (o inyectar paquetes) interfiriendo en una comunicacion establecida haciendose pasar por uno de los 2 usuarios en los extremos. Este tipo de ataques son denominados MitM o Man in the middle.

## Amenazas a los sectores

Los ultimos años fue demostrado como atacantes mediante la explotacion de vulnerabilidades pueden causar grandes perdidas y la caida de infraestructuras criticas. Un gran ejemplo de los ultimos años puede ser StuxNet con su ataque a las centrales nucleares generando una perdida millonaria al gobierno. Este ataque se centro en atacar el sistema de control de supervicion y adquisicion de datos (SCADA) encargado de controlar y supervisar procesos industriales.
A la luz de la historia moderna, un simple ataque puede generar cortes en sectores muy importantes de un pais. Es por esto que se necesita estar al pendiente de posibles vulnerabilidades que podrian dejar expuestos grandes sectores y/o servicios.

## Amenazas internas y externas
- Reviar en [Toma de apuntes](<Cisco Networking Essentials/1 - Introduction to Cybersecurity/Unidad 1/Toma de apuntes>) Atacantes internos, externos y datos tradicionales.

## Las vulnerabilidades de los dispositivos moviles

Este tema es una cuestion que escapa de las manos de los administradores de sistemas. Con la creciente tendencia de BYOD (Bring your own devices) se complica la tarea de mantener los dispositivos de los empleados actualizados para asi mantener la seguridad e integridad de la red, posibilitando asi que los atacantes tengan mas vectores de ataque en contra de las organizaciones.

## Surgimiento del internet de las cosas (IoT)

El internet de las cosas (IoT) es el conjunto de tecnologias que permiten la conexion de varios dispositivos a Internet. Estas tecnologias permiten la conexion de miles de millones de dispositivos a las redes. Este crecimiento y adicion de los dispositivos a internet generaron una gran cantidad de datos que requieren de una proteccion activa. Los usuarios, a su vez, acceden a estos dispositivos de forma remota, lo que genera ademas, que aumente la cantidad de redes que requieren proteccion. Esta expansion de datos y redes que requieren proteccion genero una nueva area de interes en la tecnologia y los negocios denominada "datos masivos".

## El impacto de los datos masivos

Los __datos masivos__ son el resultado de los conjuntos de datos que son grandes y complejos, lo que hace que las aplicaciones tradicionales de procesamiento de datos sean inadecuadas. Los datos masivos presentan desafios y oportunidades:
- El volumen o la cantidad de datos.
- La velocidad de los datos.
- La variedad o el rango de los tipos y fuentes de datos.
Existen muchos ejemplos de amenazas de gran envergadura en las noticias. Empresas grandes como Paypal, Home depot, etc. son objetivos de ataques muy promocionados. Como resultado, los sistemas empresariales deben realizar cambios drasticos en cuanto a la seguridad y actualizaciones importantes a tecnologias y practicas. Ademas, los gobiernos y las industrias estan haciendo mas regulaciones y obligaciones que requieren una mejor proteccion de los datos y controles de seguridad para ayudar a proteger los datos masivos.

## Uso de instrumentos avanzados

- Vulnerabilidades actuales tienen como base los errores de programacion, las vulnerabilidades de protocolo o las configuraciones erroneas del sistema.
- Actualmente, se percibe una creciente sofisticacion en los ataques. Con las sofisticadas APT cubiertas en [Toma de apuntes](<Cisco Networking Essentials/1 - Introduction to Cybersecurity/Unidad 2/Toma de apuntes>).
- Ataques a algoritmos para asi poder romper alguna de las partes de la triada CIA
- Por ultimo, la nueva generacion de ataques involucran la seleccion inteligente de las victimas para asi pasar desapercibidos la mayor cantidad de tiempo posible sin llamar la atencion de un administrador de sistemas.

## Un alcance mas amplio y el efecto cascada

La administracion de identidades federada se refiere al permitir que los usuarios puedan ingresar a una red de empresas con los mismos datos. Esto generaria que, ante un posible ataque, caigan todas las empresas con una cantidad abrumadora de datos.
Una identidad federada conecta la identidad electronica de un sujeto mediante sistemas de administracion de identidades separados. Un ejemplo seria iniciar sesion en Yahoo con credenciales de Google.
Es imprecindible que las organizaciones escudriñen la informacion de identificacion compartida por los partners. Si esta informacion cae en las manos de un ladron, este podria perpetrar un ataque de suplantacion de la identidad con todas las consecuencias que esto conlleva.

## Implicaciones de seguridad

Los centros de 911 son suceptibles a varios ataques debido a que estan sobre servicios VoIP, la variedad de ataques que se podrian llevar a cabo son ataques del tipo DDoS, ataques TDoS (Ataque de denegacion de servicios telefonicos). Estos ultimos ataques generan un gran flujo hacia el numero deseado para que asi los llamados legitimos no lleguen a impactar en el numero deseado.

## Como abordar la escasez de especialistas en ciberseguridad

El Instituto Nacional de Normas y Tecnologias (NIST) creo un marco de trabajo para que asi las empresas y organizaciones que necesitan especialistas sepan que perfil buscar para cumplimentar con el rol de un especialista de este tipo en la empresa.

## Siete categorias en el area de la ciberseguridad

- __Operar y mantener__: Incluye proporcionar soporte tecnico, administracion y el mantenimiento necesario para garantizar el rendimiento y la seguridad de los sistemas IT.
- __Proteger y defender__: Incluye la identificacion, el analisis y la mitigacion de las amenazas a los sistemas internos y redes internas.
- __Investigar__: Incluye la investigacion de los eventos ciberneticos o los delitos informaticos que involucran a los recursos de IT.
- __Recopilar y operar__: Incluye operaciones especializadas de ataque y engaño, y la recopilacion de informacion sobre ciberseguridad.
- __Analizar__: Incluye la revision y evaluacion altamente especializada de la informacion entrante de ciberseguridad para determinar si es util para la inteligencia.
- __Supervision y desarrollo__: Establece el liderazgo, la administracion y la direccion para realizar el trabajo de ciberseguridad de manera eficaz.
- __Disponer de manera segura__: Incluye conceptualizacion, diseño y creacion de sistemas de IT seguros.

A su vez dentro de cada una de estas categorias existen a su vez distintas especializaciones y puestos de trabajo.

## Certificaciones del sector

- __CompTIA Security+__: Es un programa patrocinado por CompTIA que certifica la competencia en la seguridad de la informacion. Esta prueba abarca los fundamentos para proteger una red y administrar el riesgo, incluidas las inquietudes de la computacion en la nube.
- __Certified Ethical Hacker CICC (CEH)__: Esta certificacion de nivel intermedio certifica que los especialistas cuentan con las habilidades y el conocimiento para varias practicas de hacking. Estos especialistas usan las misma tecnicas y habilidades que los ciberdelincuentes para ingresar en un sistema e identificar vulnerabilidades y puntos de acceso al sistema.
- __SANS GIAC Security Essentials (GSEC)__: Es una buena credencial de nivel basico para especialistas que pueden demostrar que comprenden la terminologia y los conceptos de la seguridad, y tienen la habilidad y la experiencia necesarias para puestos "practicos" en seguridad. 
- __(ISC)^2 CISSP__: Es una certificacion neutral para especialistas con mucha experiencia tecnica y administrativa. Tambien esta aprobada formalmente por el Departamento de Defensa (DoD) de Estados Unidos y es una certificacion con reconocimiento a nivel global.
- __(CISM) de ISACA__: Se encarga de certificar que el especialista es capaz de administrar, desarrollar y supervisar sistemas de seguridad de informacion a nivel empresarial. Los titulares de esta certificacion poseen aptitudes avanzadas en la administracion de riesgos de seguridad.
- __CCNA de Cisco__: La certificación de Seguridad de CCNA ratifica que un especialista en ciberseguridad cuenta con el conocimiento y las habilidades necesarias para proteger las redes de Cisco.

## Como convertirse en un especialista
- **Estudie**: conozca los aspectos básicos al completar los cursos en TI. Sea un estudiante durante toda su vida. La ciberseguridad es un campo en constante cambio y los especialistas en ciberseguridad deben mantenerse actualizados.
- **Obtenga certificaciones**: las certificaciones patrocinadas por la empresa y el sector, de organizaciones como Microsoft y Cisco demuestran que uno posee los conocimientos necesarios para buscar empleo como especialista en ciberseguridad.
- **Busque pasantías**: la búsqueda de una pasantía en seguridad como estudiante puede traducirse en oportunidades en el futuro.
- **Únase a organizaciones profesionales**: únase a las organizaciones de seguridad informática, asista a reuniones y conferencias y participe en foros y blogs para obtener conocimiento de los expertos.

