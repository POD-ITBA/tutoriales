# Instalación de Java en Windows

## Descarga de OpenJDK

Ir al sitio de 
<a href="https://jdk.java.net/23/"><b>OpenJDK</b></a>
y descargar el .zip correspondiente a Windows.

En este caso corresponde a la versión 23.

Elegir la opción **Windows/x64**

Luego de finalizada la descarga ubicar el archivo correspondiente. En este caso

<shortcut>openjdk-23.0.1_windows-x64_bin</shortcut> 

En el explorador de archivos, usando el menú contextual sobre la descarga elegir la opción **Extraer todo...**

Elegir un path donde deseemos instalar Java. En este caso utilizaremos 

<shortcut>C:\Java</shortcut> 

Se creará la carpeta necesaria.

<img src="windows-java-0.png" alt="Windows 0" width="600"/>

## Variables de entorno

Abrir **Configuración**. Luego en **Sistema**, elegir el botón **Información**

En la sección **Especificaciones del dispositivo** elegir la opción **Configuración avanzada del sistema**

En la ventana elegir la opción **Variables de entorno..** que se encuentra en la esquina inferior derecha.

En la sección **Variables del sistema** debe agregar una nueva variable de sistema presionando el botón **Nueva..**

En el popup completamos con <shortcut>JAVA_HOME</shortcut> como **Nombre de la variable**. 
En **Valor de la variable** lo completamos con la opción **Examinar directorio...**

Elegir el path donde se instaló Java, en este caso, <shortcut>C:\Java\jdk-23.0.1</shortcut>

<img src="windows-java-1.png" alt="Windows 1" width="600"/>

Por último vamos a modificar la variable de sistema **Path** para que incluya a la recién definida

Seleccionar la variable de sistema Path y luego **Editar...**

En la ventana elegir la opción **Nuevo** y luego **Examinar**

Ubicar el directorio donde se instaló Java pero ahora indicando la carpeta **bin/** correspondiente

<img src="windows-java-2.png" alt="Windows 2" width="600"/>

Aceptar los cambios en todas las ventanas.

## Consultar la versión instalada

Consulte la versión de Java instalada
abriendo una terminal usando Símbolo de Sistema
y ejecutando el siguiente comando

<code-block lang="console">java -version</code-block>

Debería ver una salida similar a la siguiente

<code-block lang="plain text">
C:\Users\foo>java -version    
openjdk version "23.0.1" 2024-10-15
OpenJDK Runtime Environment (build 23.0.1+11-39)
OpenJDK 64-Bit Server VM (build 23.0.1+11-39, mixed mode, sharing)
</code-block>

Identifique en la salida una versión
<shortcut>23</shortcut> o superior, en este ejemplo es la <code>23.0.1</code>

<note>
    <p>
        Listo! Ya cuenta con Java instalado correctamente.
    </p>
</note>