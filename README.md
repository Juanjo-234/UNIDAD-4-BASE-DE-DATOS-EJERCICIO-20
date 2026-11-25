# UNIDAD-4-BASE-DE-DATOS-EJERCICIO-20
1. Entidades Principales y Miembros
miembro

Almacena la información de los usuarios registrados que utilizan el coworking.

Atributos: dni (clave primaria), nombre, apellido, empresa, correo y num_identificador_tarjeta.

espacio_trabajo

Contiene el catálogo de salas, escritorios y oficinas disponibles para la renta.

Atributos: id_espacio (clave primaria), nombre, capacidad_maxima, tarifa_hora y tipo_espacio.

2. Control de Operaciones y Servicios
control_acceso

Registra los fichajes e ingresos de las personas mediante tarjetas identificatorias RFID.

Atributos: id_acceso (clave primaria), fecha_fichaje, hora_fichaje, tarjeta_rfid y dni_miembro_validado (clave foránea hacia miembro).

reserva

Administra la programación y el uso de los diferentes espacios de trabajo.

Atributos: id_reserva (clave primaria), fecha, hora_inicio, hora_fin, estado, dni (clave foránea al miembro) e id_espacio (clave foránea al espacio de trabajo).

consumo_adicional

Controla los gastos o servicios extras consumidos por los usuarios dentro de las instalaciones.

Atributos: id_consumo (clave primaria), fecha, hora, descripcion, cantidad, costo y dni (clave foránea al miembro).

IMAGEN DE EJEMPLO DE CONSULTA:
<img width="1122" height="338" alt="image" src="https://github.com/user-attachments/assets/6fe5d0e2-c506-47f8-8a0e-a8af10e0ca73" />


3. Restricciones e Integridad Referencial
El script configura reglas estrictas de validación mediante claves primarias y foráneas que aseguran la consistencia relacional del sistema, vinculando los accesos, consumos y reservas directamente con los miembros e interconectando las reservas con los espacios de trabajo correspondientes.
