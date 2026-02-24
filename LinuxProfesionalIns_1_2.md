# Linux Profesional Institute

## 1.4 Destrezas TIC y el trabajo con Linux

**Áreas de conocimiento clave**
*    Destrezas en el escritorio
*    Iniciación a la línea de comandos
*    Usos de Linux en la Industria, Cloud Computing y Virtualización

**Lista parcial de archivos, términos y utilidades**
*    Uso del navegador, preocupaciones en torno a la privacidad, opciones de configuración,
búsquedas en la web y almacenamiento de contenido
*    La terminal y la consola
*    Problemas relacionados con las contraseñas
*    Problemas y herramientas relacionadas con la privacidad
*    Uso de aplicaciones de código abierto comunes en presentaciones y proyectos


### Cifrado de archivos y correo electrónico con GnuPG

GNU Privacy Guard.
See gpg2 for GNU Privacy Guard 2. Most operating systems symlink gpg to gpg2
More information: https://gnupg.org.

 - Create a GPG public and private key interactively:
  ```gpg --full-generate-key```

 - Sign doc.txt without encryption (writes output to doc.txt.asc): 
  ```gpg --clearsign doc.txt```
 - Encrypt and sign doc.txt for alice@example.com and bob@example.com (outpu 
  ```gpg --encrypt --sign --recipient alice@example.com --recipient bob@exampl```
 - Encrypt doc.txt with only a passphrase (output to doc.txt.gpg):
  ```gpg --symmetric doc.txt```
 - Decrypt doc.txt.gpg (output to stdout):
  ```gpg --decrypt doc.txt.gpg```
 - Import a public key:
  ```gpg --import public.gpg```
 - Export public key for alice@example.com (output to stdout):
  ```gpg --export --armor alice@example.com```
 - Export private key for alice@example.com (output to stdout):
```gpg --export-secret-keys --armor alice@example.com```

#### ¿Qué es OpenStack?

OpenStack es una plataforma de computación en la nube de código abierto que permite la creación y gestión de infraestructuras de nube pública y privada. Proporciona un conjunto de servicios para virtualizar y administrar recursos de hardware, como servidores, almacenamiento y redes, de manera eficiente y escalable.

OpenStack se compone de varios proyectos interrelacionados, cada uno de los cuales se enfoca en una función específica de la infraestructura de la nube. Estos proyectos incluyen:

1. **Nova**: Se encarga de la gestión de instancias de máquinas virtuales (VM) y controla la asignación de recursos de computación.

2. **Swift**: Proporciona almacenamiento de objetos distribuido y escalable, ideal para el almacenamiento y recuperación de grandes cantidades de datos no estructurados.

3. **Cinder**: Ofrece almacenamiento en bloques para VM y permite la creación y administración de volúmenes de almacenamiento.

4. **Neutron**: Gestiona la red y la conectividad en la infraestructura de la nube, permitiendo la configuración de redes virtuales y la asignación de direcciones IP.

5. **Horizon**: Es la interfaz de usuario basada en web de OpenStack, que permite a los usuarios administrar y utilizar los recursos de la nube a través de un panel de control gráfico.

Estos son solo algunos ejemplos de los proyectos de OpenStack, pero hay muchos otros componentes y servicios disponibles, incluidos proyectos adicionales para el monitoreo, la orquestación y la administración de identidad.

OpenStack es altamente modular y flexible, lo que permite a las organizaciones construir y personalizar sus propias soluciones de nube de acuerdo con sus necesidades específicas. Además, al ser de código abierto, la comunidad de desarrolladores y usuarios puede colaborar, mejorar y compartir nuevas funcionalidades y mejoras en la plataforma.

En resumen, OpenStack es una plataforma de nube de código abierto que brinda la infraestructura necesaria para implementar y gestionar servicios de computación en la nube, almacenamiento y redes de manera escalable y flexible.

#### Debe usar una “ventana privada” en su navegador si desea:

Si deseas mantener cierta privacidad mientras navegas por Internet, puedes considerar utilizar una "ventana privada" en tu navegador. A continuación, te menciono algunas situaciones en las que sería recomendable utilizar una ventana privada:

1. **Navegación anónima**: Cuando deseas navegar sin dejar rastros en el historial de navegación, cookies o archivos temporales en tu dispositivo. Una ventana privada no guarda información localmente, lo que significa que al cerrarla, se eliminarán automáticamente los datos asociados a esa sesión.

2. **Acceso a cuentas personales en dispositivos públicos**: Si necesitas acceder a tus cuentas personales, como correo electrónico o redes sociales, desde un dispositivo compartido o público, una ventana privada puede proporcionar una capa adicional de seguridad al no guardar tus credenciales de inicio de sesión ni otros datos personales.

3. **Compras en línea**: Al utilizar una ventana privada para realizar compras en línea, reduces la posibilidad de que tus datos personales y de pago se almacenen en el dispositivo o sean accesibles por terceros.

4. **Investigación sensible**: Si estás realizando investigaciones o recopilando información sensible en línea, una ventana privada puede ayudar a prevenir que los datos sean almacenados en el dispositivo y a proteger tu privacidad.

5. **Pruebas y desarrollo web**: Los desarrolladores web a menudo utilizan ventanas privadas para probar y depurar sitios web sin la interferencia de las cookies o datos almacenados en el caché del navegador.

Recuerda que si bien una ventana privada puede proporcionar cierto nivel de privacidad, no garantiza un anonimato total en Internet. Tu proveedor de servicios de Internet y otros pueden seguir rastreando tu actividad en línea. Si necesitas un nivel más alto de privacidad y seguridad, considera el uso de herramientas adicionales, como redes privadas virtuales (VPN) y navegadores especializados en privacidad.

#### ¿Cuál de las siguientes opciones son softwares válidos de cifrado de disco ?
* RevealJS, EncFS y dm-crypt
* dm-crypt y KeePass
* EncFS y Bitwarden
* EncFS y dm-crypt
* TLS y dm-crypt

Las opciones válidas de softwares de cifrado de disco son:

- dm-crypt: Es una opción válida de cifrado de disco que se utiliza en sistemas Linux para encriptar particiones y volúmenes.
- EncFS: Es otra opción válida de cifrado de disco que proporciona un sistema de archivos encriptado de forma transparente para los usuarios en sistemas Linux.
- EncFS y dm-crypt: Ambas opciones, EncFS y dm-crypt, son softwares válidos de cifrado de disco y se utilizan en sistemas Linux para proteger datos almacenados en particiones o sistemas de archivos.

Por lo tanto, la opción correcta es "EncFS y dm-crypt".

#### 4. Seleccione verdadero o falso para el cifrado de dispositivo dm-crypt:

- Los archivos se cifran antes de escribirse en el disco
- Todo el sistema de archivos es un blob cifrado
- Solo los archivos y directorios están encriptados, no los enlaces simbólicos
- No requiere acceso root
- Es un cifrado de dispositivo de bloque

Las afirmaciones sobre el cifrado de dispositivo dm-crypt son las siguientes:

- Verdadero: Los archivos se cifran antes de escribirse en el disco. dm-crypt cifra los datos en el nivel del bloque antes de escribirlos en el dispositivo de almacenamiento.

- Verdadero: Todo el sistema de archivos es un blob cifrado. dm-crypt encripta el dispositivo de almacenamiento completo, lo que significa que todos los datos, incluidos los archivos y metadatos, están protegidos y cifrados.

- Verdadero: Solo los archivos y directorios están encriptados, no los enlaces simbólicos. dm-crypt encripta los archivos y directorios, pero no afecta a los enlaces simbólicos, que se mantienen sin cambios y no están cifrados.

- Falso: Requiere acceso root. Para utilizar dm-crypt y configurar el cifrado de dispositivo, generalmente se requiere acceso de administrador (root) en Linux.

- Verdadero: Es un cifrado de dispositivo de bloque. dm-crypt es un cifrado de dispositivo de bloque que encripta y descifra los bloques de datos en tiempo real a medida que se leen y escriben en el disco.

#### Beamer es:

Beamer es una clase de documento de LaTeX diseñada específicamente para crear presentaciones profesionales. LaTeX es un sistema de composición de documentos de alta calidad que se utiliza ampliamente en la comunidad académica y científica. Beamer proporciona un conjunto de estilos y opciones que permiten crear diapositivas con contenido estructurado, ecuaciones matemáticas, imágenes, gráficos y animaciones.

Con Beamer, los usuarios pueden crear presentaciones de aspecto profesional con una amplia gama de características y personalizaciones. Permite organizar el contenido en diapositivas individuales, agregar transiciones entre diapositivas, utilizar temas y plantillas predefinidos, y personalizar el diseño y los estilos según las necesidades del usuario. Además, Beamer es altamente flexible y extensible, lo que permite a los usuarios personalizar aún más su presentación según sus requisitos específicos.

En resumen, Beamer es una clase de documento de LaTeX que se utiliza para crear presentaciones profesionales de alta calidad con un amplio conjunto de características y opciones de personalización.

### EJERCICIOS EXPLORATORIOS

#### Exercise 1
La mayoría de las distribuciones vienen con Firefox instalado por defecto (si el tuyo no, tendrás
que instalarlo primero).Vamos a instalar una extensión de Firefox llamada Lightbeam.Puede
hacerlo pulsando Ctrl + Shift + A y buscando “Lightbeam” en el campo de búsqueda que se
mostrará en la pestaña abierta, o visitando la página de extensión con Firefox y haciendo clic
en el botón “Instalar”: https://addons.mozilla.org/en-GB/firefox/addon/lightbeam-3-0/ Después
de hacer esto, inicie la extensión haciendo clic en su icono y comience a visitar algunas páginas
web en otras pestañas para ver qué sucede.

- Os dejo un enlace del gran Txema Alonso sobre esta extensión.

https://www.youtube.com/watch?v=D0nmfudY1-M

#### Exercise 2

**¿Qué es lo más importante cuando se usa un administrador de contraseñas?**

Cuando se utiliza un administrador de contraseñas, lo más importante es garantizar la seguridad de tus contraseñas y la protección de tus cuentas en línea. Aquí hay algunos aspectos clave a tener en cuenta:

1. **Seguridad de las contraseñas**: El administrador de contraseñas debe generar contraseñas seguras y únicas para cada cuenta, evitando el uso de contraseñas débiles o repetidas. Además, debe proporcionar una forma segura de almacenar y cifrar las contraseñas para protegerlas de posibles ataques.

2. **Cifrado y protección de datos**: Es fundamental que el administrador de contraseñas utilice técnicas de cifrado sólidas para proteger tus datos confidenciales. Asegúrate de que el administrador de contraseñas cifre tus contraseñas y otra información almacenada antes de almacenarla o sincronizarla en la nube.

3. **Acceso seguro**: El administrador de contraseñas debe requerir una contraseña maestra o un factor de autenticación adicional para acceder a tus contraseñas. Asegúrate de establecer una contraseña maestra fuerte y no compartirla con nadie más.

4. **Sincronización y respaldo**: Es beneficioso utilizar un administrador de contraseñas que ofrezca opciones de sincronización y respaldo en la nube. Esto te permite acceder a tus contraseñas desde múltiples dispositivos y asegurarte de que tus datos estén respaldados en caso de pérdida o daño del dispositivo.

5. **Actualizaciones y seguridad**: Mantén tu administrador de contraseñas actualizado con las últimas versiones y parches de seguridad. Esto asegura que se aborden posibles vulnerabilidades y se mejore la seguridad general del software.

6. **Confianza y reputación del proveedor**: Investiga y elige un administrador de contraseñas de confianza, con una buena reputación en cuanto a seguridad y protección de datos. Revisa las opiniones de otros usuarios y la política de privacidad del proveedor.

Recuerda también que el uso de un administrador de contraseñas no debe ser la única medida de seguridad que implementes. Es importante seguir buenas prácticas de seguridad, como utilizar autenticación de dos factores, actualizar regularmente tus contraseñas y estar atento a posibles intentos de phishing o ataques cibernéticos.

#### Exercise 3

Use su navegador web para navegar a https://haveibeenpwned.com/. Descubra el propósito del
sitio web y verifique si su dirección de correo electrónico se incluyó en algunas filtraciones de
datos.

#### Exercise 4

