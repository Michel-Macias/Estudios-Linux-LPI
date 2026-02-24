# Tema 1: Encontrando el camino en un sistema Linux

### 1.4 Destrezas TIC y el trabajo con Linux

#### **RESUMEN**

* El terminal es una forma poderosa de interactuar con el sistema, y hay muchas herramientas
útiles y muy maduras para usar en este tipo de entorno. Puede llegar al terminal buscando uno
gráfico en el menú del entorno de su escritorio o presionando Ctrl + Alt + F# .
Linux se usa en gran medida en la industria tecnológica para ofrecer servicios IaaS, PaaS y SaaS.
Hay tres hipervisores principales que juegan un papel importante en el soporte de esos: Xen, KVM
y Virtualbox.
* El navegador es una pieza esencial de software en la informática hoy en día, pero es necesario
entender algunas cosas para usarlo con seguridad. DNT es sólo una manera de decirle al sitio web
que usted no quiere ser rastreado, pero no hay ninguna garantía en eso.Las ventanas privadas son
privadas solo para el equipo que está utilizando, pero esto puede permitirle escapar del
seguimiento de cookies exactamente por eso.
* TLS puede cifrar su comunicación en Internet, pero debe poder reconocer cuándo está en uso. El
uso de contraseñas seguras también es muy importante para mantenerlo a salvo, por lo que la
mejor idea es delegar esa responsabilidad en un administrador de contraseñas y permitir que el
software cree contraseñas aleatorias en cada sitio en el que inicie sesión.
* Otra forma de asegurar tu comunicación es firmar y encriptar tus carpetas de archivos y correos
electrónicos con GnuPG. dm-crypt y EncFS son dos alternativas para encriptar discos enteros o
particiones que utilizan respectivamente métodos de encriptación por bloques y por pilas.
* Finalmente, LibreOffice Impress es una alternativa de código abierto muy completa a Microsoft
Powerpoint, pero existen otras opciones como Beamer y RevealJS si prefieres crear presentaciones
usando código en lugar de GUI. ProjectLibre y GanttProject pueden ser la opción correcta si
necesita un reemplazo de Microsoft Project.

#### **Ejercicios y preguntas

##### 1. Debe usar una “ventana privada” en su navegador si desea:

- Para navegar completamente anónimo en Internet
- Para no dejar rastro en la computadora que está utilizando
- Para activar TLS y evitar el seguimiento de cookies
- Para usar DNT
- Para utilizar la criptografía durante la transmisión de datos

**RESPUESTA**:

> La opción correcta es: "Para navegar completamente anónimo en Internet" y "Para no dejar rastro en la computadora que está utilizando".

- Una "ventana privada" en un navegador, también conocida como "navegación privada" o "modo incógnito", proporciona ciertas características de privacidad que ayudan a proteger tu identidad y a no dejar rastros en la computadora que estás utilizando. Al abrir una ventana privada, el navegador no guarda el historial de navegación, las cookies ni otra información relacionada con la sesión de navegación actual. Esto significa que cuando cierras la ventana privada, no quedan registros de los sitios web visitados ni de las acciones realizadas durante esa sesión.

- Sin embargo, es importante tener en cuenta que utilizar una ventana privada no garantiza un anonimato completo en Internet. Aunque no se guarden registros localmente en la computadora, tu actividad aún puede ser rastreada por otros medios, como los proveedores de servicios de Internet (ISP) o los sitios web que visitas. Para una privacidad y anonimato más completos, se recomienda utilizar herramientas adicionales, como redes privadas virtuales (VPN), proxies o navegadores especializados en privacidad, que brindan capas adicionales de protección y anonimato en línea.

##### 2. ¿Qué es OpenStack?
- Un proyecto que permite la creación de IaaS privadas
- Un proyecto que permite la creación de PaaS privadas
- Un proyecto que permite la creación de SaaS privadas
- Un hipervisor
- Un administrador de contraseñas de código abierto

**RESPUESTA**

> La opción correcta es: "Un proyecto que permite la creación de IaaS privadas".

- OpenStack es un proyecto de código abierto que proporciona una plataforma de computación en la nube para la creación y gestión de infraestructuras como servicio (IaaS). Permite a las organizaciones construir y administrar su propia infraestructura en la nube de forma privada.

- Mediante OpenStack, es posible crear y gestionar máquinas virtuales, redes, almacenamiento y otros recursos de infraestructura de manera flexible y escalable. Proporciona una interfaz unificada y herramientas para el aprovisionamiento y el control de recursos en la nube. Además, OpenStack es altamente modular y permite la integración con diferentes componentes y tecnologías para adaptarse a las necesidades específicas de cada organización.

- OpenStack no se limita a la creación de IaaS privadas, también se puede utilizar para construir y gestionar infraestructuras en la nube de tipo público e híbrido. Sin embargo, su enfoque principal es brindar a las organizaciones la capacidad de implementar y administrar sus propias nubes privadas de manera eficiente y personalizada.

##### 3. ¿Cuál de las siguientes opciones son softwares válidos de cifrado de disco ?
- RevealJS, EncFS y dm-crypt
- dm-crypt y KeePass
- EncFS y Bitwarden
- EncFS y dm-crypt 
- TLS y dm-crypt

**RESPUESTA**

> La opción correcta es: "dm-crypt y EncFS".

- dm-crypt: Es una herramienta de cifrado de disco que se utiliza en sistemas Linux. Permite cifrar particiones, volúmenes lógicos o dispositivos de almacenamiento completos. dm-crypt utiliza el mapeo de dispositivos (device-mapper) del kernel de Linux para proporcionar cifrado a nivel de bloque, lo que significa que cifra y descifra los datos a medida que se leen o escriben en el disco.

- EncFS: Es un software de cifrado en tiempo real que se utiliza para crear directorios cifrados en sistemas Linux. EncFS proporciona un sistema de archivos virtual encriptado en el que los datos se cifran automáticamente a medida que se escriben en el directorio cifrado. Los archivos individuales dentro del directorio cifrado también están encriptados de forma independiente.

> Ambas opciones, dm-crypt y EncFS, son softwares válidos de cifrado de disco en sistemas Linux. Mientras que dm-crypt se enfoca en el cifrado a nivel de bloque para particiones o dispositivos completos, EncFS se utiliza para crear directorios cifrados en tiempo real.

##### 4. Seleccione verdadero o falso para el cifrado de dispositivo dm-crypt:

- Los archivos se cifran antes de escribirse en el disco
- Todo el sistema de archivos es un blob cifrado 
- Solo los archivos y directorios están encriptados, no los enlaces simbólicos
- No requiere acceso root 
- Es un cifrado de dispositivo de bloque

**RESPUESTA**

Aquí tienes la clasificación verdadero/falso para las afirmaciones relacionadas con el cifrado de dispositivo dm-crypt:

- *Verdadero*: Todo el sistema de archivos es un blob cifrado. dm-crypt cifra todo el contenido del dispositivo de almacenamiento en el nivel de bloque, por lo que todo el sistema de archivos se trata como un único blob cifrado.

- *Falso*: Los archivos se cifran antes de escribirse en el disco. dm-crypt realiza el cifrado a nivel de bloque mientras los datos se escriben en el disco, no cifra los archivos antes de escribirlos.

- *Falso*: Solo los archivos y directorios están encriptados, no los enlaces simbólicos. dm-crypt cifra todo el contenido del sistema de archivos, incluyendo archivos, directorios y enlaces simbólicos.

- *Falso*: Requiere acceso root. Para configurar y utilizar dm-crypt, generalmente se requiere acceso de administrador (root) en el sistema.

- *Verdadero*: Es un cifrado de dispositivo de bloque. dm-crypt proporciona cifrado a nivel de bloque para dispositivos de almacenamiento, como particiones, volúmenes lógicos o dispositivos completos.

> Recuerda que dm-crypt es una herramienta de cifrado de disco en sistemas Linux y se utiliza para cifrar y descifrar datos sobre la marcha mientras se accede a ellos.