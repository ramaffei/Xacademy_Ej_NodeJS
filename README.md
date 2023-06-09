## Ejercicio de entrega de NodeJs

### Enunciado

Se requiere una API REST que permita manejar librerías y los libros asociados a cada una de
las librerías. Utilizar Node.Js Express, Sequelize y Passport como la infraestructura para crear
el servicio.

### Entidades
#### Libreria:
  ● Descripción: 
      Una librería puede tener desde 0 a muchos libros.
  ● Ruta: /library
  ● Acciones:
      ○ Crear librería (AUTH)
      ○ Obtener una librería
      *Debe traer también todos los libros*
      ○ Obtener todas las librerías
      ○ Modificar una librería (AUTH)
      ○ Eliminar una librería (**) (AUTH)
      ○ Agregar un libro nuevo (*) (AUTH)
      
● Entidad

  * **id:** *Int* (El identificador de la librería)
  * **name:** *String* (Nombre de la librería. Eg: El Librote)
  * **location:** *String* (Dirección física de la librería. Eg: Av. Libertador 1460)
  * **telefono:** *String* (Número de teléfono. Eg: 3514563344)

### Libro:
  ● Descripción: 
      Un libro tiene todos los datos del mismo, puede pertenecer a una librería
      o no y representan la instancia (copia) de un libro. Puede haber más de un libro con los
      mismos datos, excepto el id que es único para esa instancia.
  ● Ruta: /book
  ● Acciones:
      ○ Crear libro (AUTH): Para crear un libro, pueden hacerlo de las dos formas:
            ● Haciendo que la librería tenga un método para agregar un libro nuevo
            ● Crear un libro directamente con /book y enviar el id de la librería
      ○ Obtener un libro en particular
      ○ Obtener todos los libros
      ○ Modificar un libro (AUTH)     
      ○ Eliminar un libro (AUTH): El borrado, siempre de forma lógica. Esto quiere decir que no borramos de la base de
datos si no que marcamos que fué borrado
● Entidad
