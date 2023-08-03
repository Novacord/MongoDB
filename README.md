# Base de datos "db_campus_alquiler" Con MongoDB

Esta base de datos "db_campus_alquiler" contiene varias colecciones que se utilizan para administrar información sobre clientes, automóviles, alquileres, reservas, empleados, sucursales y registros de entrega y devolución en una empresa de alquiler de automóviles.

## Colecciones

1. **Cliente:** Contiene información sobre los clientes que alquilan los automóviles.
   - Campos: id_, Nombre, Apellido, DNI, Direccion, Telefono, Email.
2. **Automovil:** Almacena detalles de los automóviles disponibles para alquilar.
   - Campos: id_, Marca, Modelo, Anio, Tipo, Capacidad, Precio_Diario.
3. **Alquiler:** Registra los alquileres de automóviles realizados por los clientes.
   - Campos: id_, ID_Automovil, ID_Cliente, Fecha_Inicio, Fecha_Fin, Costo_Total, Estado.
4. **Reserva:** Contiene información sobre las reservas realizadas por los clientes para futuros alquileres.
   - Campos: id_, ID_Cliente, ID_Automovil, Fecha_Reserva, Fecha_Inicio, Fecha_Fin, Estado.
5. **Sucursal:** Almacena información sobre las sucursales de la empresa de alquiler de automóviles.
   - Campos: id_, Nombre, Direccion, Telefono.
6. **Sucursal_Automovil:** Es una colección de enlace para mapear los automóviles disponibles en cada sucursal.
   - Campos: id_, ID_Automovil, Direccion.
7. **Empleado:** Contiene información sobre los empleados de la empresa de alquiler de automóviles.
   - Campos: id_, Nombre, Apellido, DNI, Direccion, Telefono, Cargo.
8. **Registro_Entrega:** Registra la información de entrega de un automóvil alquilado.
   - Campos: id_, ID_Alquiler, ID_Empleado, Fecha_Entrega, Combustible_Entregado, Kilometraje_Entregado.
9. **Registro_Devolucion:** Registra la información de devolución de un automóvil alquilado.
   - Campos: id_, ID_Alquiler, ID_Empleado, Fecha_Devolucion, Combustible_Devuelto, Kilometraje_Devuelto, Monto_Adicional.

## Instrucciones de Uso

1. Clonar el repositorio e iniciar el servidor del Sistema de Alquiler de Automóviles.
2. Conectarse a la base de datos MongoDB usando el cliente adecuado.
3. Ejecutar las consultas proporcionadas a continuación para obtener la información deseada.

