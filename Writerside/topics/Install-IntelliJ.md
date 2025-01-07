# Instalación de IntelliJ IDEA

En este tutorial se cubre la instalación del IDE IntelliJ IDEA y la utilización del kit de desarrollo
para Java (JDK) ya instalado.

## Registro y Licencia

**IntelliJ IDEA Ultimate** requiere una licencia. Los alumnos pueden registrarse en
<a href="https://www.jetbrains.com/shop/eform/students">**Productos JetBrains para el aprendizaje**</a>
con su mail **@itba.edu.ar** y así obtener una **licencia gratuita** para utilizar IntelliJ IDEA Ultimate y demás aplicaciones
de JetBrains de forma gratuita.

<tip>
También puede descargar la versión 
<b>gratuita</b> denominada
<b>IntelliJ IDEA Community Edition</b>
que no requiere licencia.
</tip>

## Instalación de IntelliJ IDEA usando ToolBox App

Para instalar **IntelliJ IDEA** recomendamos utilizar **Toolbox App**.

Puede consultar el siguiente tutorial:

<a href="https://www.jetbrains.com/help/idea/installation-guide.html#toolbox">Install using the Toolbox App</a>.

## Primer proyecto y utilización del JDK instalado

Una vez instalado **IntelliJ IDEA** necesita indicar la ubicación del Java Development Kit (JDK).
Podrá hacerlo en la ventana de creación de un nuevo proyecto.

Abrir **IntelliJ IDEA** y elegir
<shortcut>New Project</shortcut>.

<img src="intellij-1.png" alt="IntelliJ 1" width="600"/>

En la ventana debe completar el nombre del proyecto y elegir una carpeta.
En **Language** elegir **Java**. En **Build system** elegir **IntelliJ**.

<img src="intellij-2.png" alt="IntelliJ 2" width="600"/>

Ahora es momento de indicar el JDK. En **JDK** abrir el menú contextual.
Elegir la versión de JDK que instaló, en este caso **Oracle OpenJDK 23.0.1**.

<img src="intellij-3.png" alt="IntelliJ-3" width="600"/>

De no listar opciones en Registered JDKs ni en Detected JDKs puede utilizar la opción
Add JDK from Disk... y desde el explorador de archivos buscar el directorio de instalación del JDK.

De vuelta en la ventana de **New Project**, elegir el JDK descargado
y presionar
<shortcut>Create</shortcut>.

<note>
    <p>
        Listo! Ya cuenta con IntelliJ IDEA y Java instalado correctamente.
    </p>
</note>

<tip>Para más información consultar:
<a href="https://www.jetbrains.com/help/idea/run-for-the-first-time.html">
Run IntelliJ IDEA for the first time</a>.
</tip>
