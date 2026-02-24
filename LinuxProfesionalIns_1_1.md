# Linux Profesional Institute

## 1.2 Principales aplicaciones de código abierto

Para buscar paquetes en distros Debian usaremos ```apt-cache search
package_name``` o ```apt search package_name```.
 
Si lo que queremos es borrar algun paquete usaremos 
```apt-get remove package_name``` o ```apt remove package_name``` para paquetes DEB 

*Recuerda usar el Tab (tabulador) para ver las opciones y echar un ojo al comando con ```man```
o ```tldr``` o incluso la ayuda ```comando --help```*

Hay diferencias entre "remove" y "purge". **Remove** solo elimina el programa pero NO los archivos de configuración y con **purge** eliminamos todos los archivos.

### Preguntas y ejercicios del tema 1.2

**1.-Para cada uno de los siguientes comandos, identifique si está asociado con el sistema de
empaquetado Debian (Debian packaging system) o con el sistema de empaquetado Red Hat (Red
Hat packaging system) :**

_dpkg y apt-get están asociados con el sistema de empaquetado Debian, mientras que rpm, yum y dnf están asociados con el sistema de empaquetado Red Hat._

**2.-¿Qué comando se puede usar para instalar Blender en Ubuntu? Después de la instalación,
¿cómo se puede ejecutar el programa?**

Lo primero siempre debes actualizar los repos con ```apt-get update```para luego proceder a instalarlo con ```apt-get install blender```. Para ejecutarlo solo ```blender```

## 1.3 Software de Código Abierto y las licencias

### Preguntas y ejercicios del tema 1.3

**1.-¿Cuáles son, en pocas palabras, las "cuatro libertades" definidas por Richard Stallman y la Free
Software Foundation?**

Las "cuatro libertades" definidas por Richard Stallman y la Free Software Foundation (Fundación para el Software Libre) son los principios fundamentales del software libre. Estas libertades son:

1. Libertad de usar el software: La libertad de usar el software para cualquier propósito, sin restricciones.

2. Libertad de estudiar el software: La libertad de acceder al código fuente del software y estudiar cómo funciona, permitiendo comprender su funcionamiento interno.

3. Libertad de distribuir el software: La libertad de compartir y distribuir copias del software a otros, lo que implica la posibilidad de ayudar a los demás ofreciendo programas de software libre.

4. Libertad de modificar el software: La libertad de modificar y adaptar el software para satisfacer tus necesidades, lo que implica la posibilidad de hacer mejoras, correcciones o agregar nuevas características.

En resumen, estas cuatro libertades defienden el derecho de los usuarios de software a utilizar, estudiar, compartir y modificar el software que utilizan. El objetivo es garantizar la libertad y el control de los usuarios sobre el software que utilizan, fomentando la transparencia, la colaboración y el beneficio colectivo.

**2.-¿Qué significa la abreviatura FLOSS?**

La abreviatura FLOSS significa "Free/Libre and Open Source Software" en inglés.

**3.-Ha desarrollado software libre y desea asegurar el software en sí, pero que también todos los
trabajos futuros basados en este permanezcan libres. ¿Qué licencia eliges?**

CC BY
GPL version 3
2-Clause BSD License
LGPL

En este caso nos decantamos por GPL version 3.

GPL versión 3 (GNU General Public License): Es una licencia de software libre copyleft que garantiza las cuatro libertades fundamentales del software libre. Además de permitir el uso, estudio, distribución y modificación del software, la GPL versión 3 también requiere que cualquier trabajo derivado o modificado se distribuya bajo los mismos términos de la GPL. Esto garantiza que cualquier trabajo basado en tu software también sea software libre.

**4.-A cuál de las siguientes licencias llamaría permisiva, cuál llamaría copyleft?***
 -Simplified BSD License
 -GPL version 3
 -CC BY
 -CC BY-SA

 De las licencias mencionadas, se podría clasificar de la siguiente manera:

Permisiva:
- **Simplified BSD License**: Esta licencia se considera permisiva porque permite el uso, modificación y redistribución del software, tanto en proyectos comerciales como no comerciales, sin imponer muchas restricciones adicionales. Solo requiere la inclusión del aviso de copyright y renuncia a responsabilidades en la redistribución del software.

Copyleft:
- **GPL version 3 (GNU General Public License)**: La GPL versión 3 se considera copyleft porque exige que cualquier trabajo derivado o modificado del software también se distribuya bajo los mismos términos de la GPL. Esto significa que los trabajos derivados también deben ser software libre y mantener las libertades del software original.

- **CC BY-SA (Creative Commons Attribution-ShareAlike)**: Aunque CC BY-SA no es una licencia específicamente copyleft, se asemeja a esta categoría porque requiere que los trabajos derivados se distribuyan bajo la misma licencia o una similar. Esto significa que los trabajos derivados también deben permitir la libre distribución y modificación.

Es importante tener en cuenta que estas clasificaciones son generales y cada licencia tiene sus propias características y requisitos específicos. Es recomendable revisar detenidamente los términos y condiciones de cada licencia antes de elegir la más adecuada para tu proyecto.

**5.-¿Bajo qué licencia (incluida la versión) están disponibles las siguientes aplicaciones?
-Apache HTTP Server
-MySQL Community Server
-Wikipedia articles
-Mozilla Firefox
-GIMP**

Las siguientes aplicaciones están disponibles bajo las siguientes licencias:

1. **Apache HTTP Server**: Está disponible bajo la licencia Apache License 2.0.

2. **MySQL Community Server**: Está disponible bajo una doble licencia. La versión comunitaria de MySQL, también conocida como MySQL Community Edition, está disponible bajo la licencia GNU General Public License (GPL) versión 2. Sin embargo, también se puede obtener una licencia comercial para MySQL a través de Oracle, lo que permite el uso en situaciones que no cumplen con los términos de la GPL.

3. **Wikipedia articles**: Los artículos de Wikipedia están disponibles bajo la licencia Creative Commons Attribution-ShareAlike 3.0 Unported License (CC BY-SA 3.0). Esto significa que puedes utilizar, compartir y modificar los artículos de Wikipedia, siempre y cuando se atribuya la autoría original y cualquier trabajo derivado se comparta bajo una licencia similar.

4. **Mozilla Firefox**: Mozilla Firefox está disponible bajo la licencia Mozilla Public License (MPL) versión 2.0. Esta licencia es una licencia de código abierto que permite el uso, modificación y distribución del software de Firefox, tanto para uso personal como comercial, siempre y cuando se cumplan los términos de la licencia.

5. **GIMP**: GIMP (GNU Image Manipulation Program) está disponible bajo la licencia GNU General Public License (GPL) versión 3. Esto significa que puedes utilizar, modificar y distribuir el software de GIMP, incluyendo cualquier modificación que realices, siempre y cuando se cumplan los términos de la GPL.

Recuerda que las licencias pueden estar sujetas a cambios, por lo que es importante consultar la documentación oficial de cada aplicación para obtener información actualizada sobre las licencias utilizadas.

##6.-Desea lanzar su software bajo la GNU GPL v3. ¿Qué pasos debes seguir?**

Si deseas lanzar tu software bajo la Licencia Pública General de GNU (GNU General Public License o GPL) versión 3, debes seguir estos pasos:

1. **Revisa la licencia**: Lee detenidamente la GNU GPL versión 3 para asegurarte de comprender todos los términos y condiciones. Familiarízate con las obligaciones y derechos que implica esta licencia.

2. **Asegúrate de que tu software cumple con la GPL v3**: Verifica que tu software cumple con los requisitos de la GPL versión 3. Esto incluye que tu software sea un trabajo derivado o contenga componentes que sean compatibles con la GPL v3.

3. **Agrega el texto de la licencia**: Asegúrate de incluir una copia del texto completo de la GPL v3 junto con tu software. Esto puede ser un archivo separado de texto o puedes incluirlo en la documentación del software.

4. **Indica claramente que tu software está bajo la GPL v3**: Debes proporcionar una declaración clara y visible indicando que tu software está licenciado bajo la GPL versión 3. Puede ser en forma de un aviso en la interfaz del programa, en la documentación o en el sitio web oficial del proyecto.

5. **Distribuye el código fuente**: La GPL v3 requiere que, al distribuir tu software, también distribuyas el código fuente correspondiente. Asegúrate de incluir el código fuente o proporcionar una forma accesible para que los usuarios puedan obtenerlo.

6. **Proporciona instrucciones para la licencia**: Junto con tu software, proporciona instrucciones claras sobre cómo los usuarios pueden aceptar y cumplir con los términos de la GPL v3. Esto puede incluir información sobre cómo obtener el código fuente, cómo realizar modificaciones y cómo distribuir versiones modificadas.

Recuerda que la GPL v3 es una licencia legalmente vinculante, por lo que es recomendable obtener asesoramiento legal si tienes alguna pregunta o preocupación específica relacionada con la licencia y su aplicación a tu software.

Además de estos pasos, también es importante comprender y respetar las obligaciones y derechos que la GPL v3 otorga tanto a ti como al usuario final del software.

**7.-Usted ha un escrito software propietario y desea combinarlo con software libre bajo GPL versión 3. ¿Se le permite hacer esto o qué debe considerar?**

Si tienes un software propietario y deseas combinarlo con software libre licenciado bajo la GPL versión 3, existen algunas consideraciones importantes que debes tener en cuenta:

1. **Compatibilidad de licencias**: La GPL versión 3 es una licencia copyleft que impone ciertas restricciones y obligaciones. Una de las condiciones principales de la GPL v3 es que cualquier trabajo derivado o combinado con software licenciado bajo la GPL v3 también debe ser distribuido bajo los términos de la GPL v3. Esto significa que si combinas tu software propietario con software bajo la GPL v3, deberás liberar el código fuente de tu software combinado y distribuirlo bajo la GPL v3.

2. **Separación de componentes**: Si deseas mantener tu software propietario y no liberar su código fuente, debes asegurarte de que los componentes bajo la GPL v3 y tu software propietario estén claramente separados y no se mezclen o dependan directamente entre sí. De esta manera, puedes distribuir tu software propietario sin afectar los términos de la GPL v3 para los componentes de software libre.

3. **Interfaz y comunicación**: Si el software propietario y el software libre interactúan o se comunican entre sí, debes tener cuidado de definir claramente una interfaz bien definida y no derivada del software libre. Esto significa que la comunicación entre los componentes propietarios y los componentes GPL v3 debe ser a través de interfaces claramente definidas y no debe implicar una fusión o dependencia directa que pueda considerarse una creación de un trabajo derivado.

4. **Consultar a un experto legal**: Debido a la naturaleza compleja de las licencias y las implicaciones legales, es altamente recomendable buscar asesoramiento legal especializado si planeas combinar software propietario con software licenciado bajo la GPL v3. Un abogado especializado en derecho de software podrá ayudarte a evaluar las implicaciones específicas de tu situación y brindarte orientación adecuada.

En resumen, combinar software propietario con software libre licenciado bajo la GPL v3 puede ser desafiante y requerir medidas cuidadosas para cumplir con los términos de la licencia. Es importante comprender las implicaciones legales y buscar asesoramiento legal para garantizar el cumplimiento de las licencias y proteger tus derechos y los derechos de los usuarios del software.

**8.-¿Por qué la Free Software Foundation lanzó la GNU Affero General Public License (GNU AGPL)
como complemento a la GNU GPL?**

La Free Software Foundation (FSF) lanzó la GNU Affero General Public License (GNU AGPL) como complemento a la GNU GPL para abordar un aspecto específico relacionado con el software que se ejecuta en servidores de red.

La GNU GPL, en sus versiones anteriores, se enfocaba principalmente en el software distribuido y modificado. Estas licencias requerían que cualquier modificación o distribución del software se realizara bajo los términos de la GPL y que el código fuente estuviera disponible para los usuarios.

Sin embargo, con el advenimiento de las aplicaciones web y los servicios en línea, surgió la preocupación de que el software libre se ejecutara en servidores de red sin necesariamente ser distribuido o modificado. Esto significaba que los usuarios podían interactuar con el software a través de una interfaz web, pero no tenían acceso al código fuente y, por lo tanto, no podían beneficiarse de las libertades del software libre.

La GNU AGPL fue creada para abordar esta brecha. Esta licencia extiende los términos de la GNU GPL al software que se ejecuta en servidores de red y se proporciona a los usuarios a través de una red. Requiere que, si un usuario interactúa con el software a través de una red, también se le debe proporcionar acceso al código fuente del software, permitiendo así que los usuarios ejerzan las libertades asociadas al software libre.

En resumen, la FSF lanzó la GNU AGPL como una respuesta a la necesidad de asegurar que el software libre se mantenga libre incluso cuando se ejecuta en servidores de red y se proporciona a los usuarios a través de una interfaz web. Con esta licencia, se busca garantizar que los usuarios puedan acceder al código fuente y beneficiarse plenamente de las libertades del software libre, incluso en entornos en línea.

**9.-Nombre tres ejemplos de software libre, que también se ofrecen como “Business Edition”, es
decir, en una versión de pago.**

Aquí tienes tres ejemplos de software libre que también se ofrecen en una versión de pago conocida como "Business Edition":

1. **MySQL**: MySQL es un sistema de gestión de bases de datos relacional de código abierto ampliamente utilizado. La comunidad de MySQL ofrece una versión gratuita y de código abierto llamada "MySQL Community Edition", que es adecuada para la mayoría de los casos de uso. Sin embargo, también existe una versión comercial llamada "MySQL Enterprise Edition" que ofrece características adicionales, soporte técnico y herramientas avanzadas para empresas que requieren un nivel de servicio más alto.

2. **Red Hat Enterprise Linux**: Red Hat Enterprise Linux (RHEL) es una distribución de Linux empresarial basada en software libre. La versión de código abierto de RHEL, llamada "Fedora", está disponible de forma gratuita para uso general. Sin embargo, Red Hat también ofrece una versión comercial llamada "Red Hat Enterprise Linux" que proporciona características adicionales, soporte técnico y servicios empresariales para satisfacer las necesidades de organizaciones y entornos de producción.

3. **GitLab**: GitLab es una plataforma de desarrollo de software basada en web que admite la gestión de repositorios de código fuente y colaboración en proyectos. La versión de código abierto de GitLab, conocida como "GitLab Community Edition", está disponible de forma gratuita y puede instalarse en servidores propios. Sin embargo, GitLab también ofrece una versión comercial llamada "GitLab Enterprise Edition" que brinda características adicionales, seguridad avanzada, soporte técnico y opciones de implementación empresarial.

Estos son solo tres ejemplos de software libre que ofrecen una versión comercial para empresas que buscan características y servicios adicionales. Es importante tener en cuenta que, si bien la versión de pago puede tener beneficios adicionales, la versión de código abierto sigue siendo libre y puede ser utilizada de manera gratuita según los términos de sus respectivas licencias.



