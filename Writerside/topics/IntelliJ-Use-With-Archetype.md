# Uso de IntelliJ

**Para abrir el proyecto recién creado con IntelliJ IDEA.**

1. Desde el IntelliJ elegir la opción <shortcut>Open</shortcut> para abrir un nuevo proyecto

![intellij-archetype-1.png](intellij-archetype-1.png)

2. Desde el explorador de archivos emergente elegir el **pom.xml del directorio raíz del proyecto**.

En este ejemplo es <code>sample-project/pom.xml</code>

3. Elegir <shortcut>Open as Project</shortcut>

![intellij-archetype-2.png](intellij-archetype-2.png)

4. Desde el menú de <shortcut>Maven</shortcut> puede ejecutar los comandos <code>mvn clean</code> y
<code>mvn package</code> sin recurrir a la terminal

![intellij-archetype-3.png](intellij-archetype-3.png)

<tip>

Recordar de siempre seleccionar el módulo parent
(en este ejemplo <code>sample-project-parent</code>)

</tip>

## Solución de Problemas

<tip>

En el caso de que **el IDE no reconozca archivos que se generaron con el proyecto** recomendamos intentar
las siguientes opciones desde el menú contextual (click derecho) sobre el archivo **pom.xml del módulo padre**:

1. **Generate Sources and Update Folders**

2. **Sync Project**

![intellij-archetype-4.png](intellij-archetype-4.png)

</tip>
