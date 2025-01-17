# Nuevo proyecto desde IntelliJ

Otra opción para crear un proyecto usando el arquetipo consiste en **indicarle a IntelliJ
qué arquetipo queremos usar.**

1. Desde el IntelliJ elegir la opción <shortcut>New Project</shortcut> para crear un nuevo proyecto

![intellij-archetype-1.png](intellij-archetype-1.png)

2. En la sección izquierda de <shortcut>Generators</shortcut>
   elegir <shortcut>Maven Archetype</shortcut>

3. Antes de completar los campos para crear el proyecto dirigirse a la opción
<shortcut>Manage catalogs...</shortcut>

![intellij-archetype-wizard-1.png](intellij-archetype-wizard-1.png)

4. En la ventana emergente de
<shortcut>Manage Catalog</shortcut> 
hacer click en el botón 
<shortcut>+</shortcut> 
para agregar un nuevo catálogo

![intellij-archetype-wizard-2.png](intellij-archetype-wizard-2.png)

5. En la ventana emergente de
<shortcut>Add Catalog</shortcut> 
hacer click en la carpeta y navegar hasta el archivo 
<code>archetype-catalog.xml</code>

Según el sistema operativo, asumiendo un nombre de usuario **Foo**, el archivo se encuentra ubicado en:

<tabs>
    <tab id="macos-catalog" title="macOS">
        <code-block lang="console">
            /Users/Foo/.m2/archetype-catalog.xml
        </code-block>
    </tab>
    <tab id="linux-catalog" title="Linux">
        <code-block lang="console">
            /home/Foo/snap/strictly-maven/common/repository/archetype-catalog.xml
        </code-block>
    </tab>
    <tab id="windows-catalog" title="Windows">
        <code-block lang="console">
            C:/Users/Foo/.m2/archetype-catalog.xml
            C:/Usuarios/Foo/.m2/archetype-catalog.xml
        </code-block>
    </tab>
</tabs>

![Screenshot 2025-01-17 at 14.35.41.png](intellij-archetype-wizard-3.png)

Guardar los cambios con
<shortcut>Add</shortcut>.

6. De vuelta en la ventana de
<shortcut>Manage Catalog</shortcut> 
debería ver algo similar a lo siguiente:

![intellij-archetype-wizard-4.png](intellij-archetype-wizard-4.png)

Guardar los cambios con
<shortcut>OK</shortcut>.

7. De vuelta en la ventana de
<shortcut>New Project</shortcut> elegir en 
<shortcut>Catalog</shortcut> 
la opción recién creada

8. En
<shortcut>Archetype</shortcut> 
elegir la opción 
<code>ar.edu.itba.pod:pod-mp-grpc-archetype</code>

9. Completar los demás campos de la ventana de
<shortcut>New Project</shortcut> (en este ejemplo crearemos un archivo llamado <code>my-project</code>)
y presionar <shortcut>Create</shortcut>

![intellij-archetype-wizard-5.png](intellij-archetype-wizard-5.png)
