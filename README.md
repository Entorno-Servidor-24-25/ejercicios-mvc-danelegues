
# Arquitectura MVC

### Pregunta 1: ¿Qué camino sigue el código cuando el usuario accede por primera vez a `index.php`?
**Descripción**: Explica qué ocurre desde que el usuario carga `index.php` hasta que se muestra algo en pantalla. Incluye cómo intervienen el controlador, las vistas y el modelo, si es necesario.

-Una vez que se carga index.php llama a los controlers "UserController.php". Una vez que entra a este controlador llama a views "userForm.php" para cargar la vista (que seria lo que ve el usuario al entrar al index.php), en una funcion.

### Pregunta 2: ¿Qué camino sigue el código cuando el usuario introduce datos en el formulario?
**Descripción**: Detalla el proceso desde que el usuario envía el formulario hasta que se guarda la información y se muestra una respuesta en pantalla.

-De la misma manera  que la anterior pregunta lo primero lalma a los controlers en este caso "UserController.php". Una vez que entra al controlador llama a archivo que crea la base de datos, y con ello hace una funcion para que se puedan guardar los users en la que se llama a el modelo de "user.php" para crear el usuario, dentro de esta funcion, en el caso de que se cree un nuevo user llama a la view "userSucces.php"

### Ejercicio 1: Mostrar Todos los Usuarios
**Descripción**: Extiende la funcionalidad de la aplicación para que se muestre una lista de todos los usuarios que están en la base de datos.
- Añadir un nuevo método en el controlador `UserController` llamado `getAllUsers()`.
- Crear una nueva vista `showUsers.php` para mostrar una tabla con los nombres de los usuarios.
> **Nota:** Al crear nuevas vistas, añade alguna forma de navegar entre ellas de modo que el usuario pueda acceder a todas las vistas sin tener que modificar la URL directamente.
> 
### Ejercicio 2: Eliminar Usuario
**Descripción**: Implementa la funcionalidad para eliminar un usuario de la base de datos.
- Crear un método `deleteUser()` en `UserController`.
- Crear una acción en `showUsers.php` que permita eliminar usuarios, mostrando un botón "Eliminar" al lado de cada nombre en la lista de usuarios.
> **Nota:** Al crear nuevas vistas, añade alguna forma de navegar entre ellas de modo que el usuario pueda acceder a todas las vistas sin tener que modificar la URL directamente.