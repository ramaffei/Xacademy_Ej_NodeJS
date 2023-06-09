## Ejercicio de entrega de NodeJs

### Enunciado

Se requiere una API REST que permita manejar librerías y los libros asociados a cada una de
las librerías. Utilizar Node.Js Express, Sequelize y Passport como la infraestructura para crear
el servicio.

### Entidades
Libreria
  ● Descripción: Una librería puede tener desde 0 a muchos libros.
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
