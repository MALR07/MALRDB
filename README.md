# MALRDB

Entidad: Cliente
Atributos:
ID_cliente: Identificador único del cliente.

Nombre: Nombre del cliente.

Teléfono: Número de teléfono del cliente.

Email: Dirección de correo electrónico del cliente.

Relación:
Un cliente puede hacer varias ventas (relación 1 a N). Es decir, un cliente puede realizar múltiples compras a lo largo del tiempo.

Entidad: Venta
Atributos:
ID_Venta: Identificador único de la venta.

Id_cliente: Clave foránea que hace referencia al cliente que realizó la venta.

Fecha: Fecha en que se realizó la venta.

Total: total de la venta.

Relación:
Cada venta está asociada a un cliente (relación N a 1). Un cliente puede realizar varias ventas, pero cada venta pertenece a un único cliente.
Una venta puede incluir varios productos (en este caso, varios videojuegos) a través de la entidad Detalleventa.

Entidad: DetalleVenta
Atributos:
ID_detalle: Identificador único del detalle de la venta.

cantidad: Cantidad de productos (videojuegos) comprados en esa venta.

precio_unitario: Precio unitario de cada videojuego en esa venta.

Id_videojuego: Clave foránea que hace referencia al videojuego comprado.

Id_venta: Clave foránea que hace referencia a la venta en la que se incluye este detalle.

Relación:
Cada detalle de venta está asociado a una venta (relación N a 1).

Cada detalle de venta está asociado a un videojuego específico (relación N a 1). Una venta puede incluir múltiples videojuegos, por lo que hay una relación de muchos a uno entre Detalleventa y Videojuegos.

Entidad: Videojuegos
Atributos:
ID_videojuego: Identificador único del videojuego.

Nombre: Nombre del videojuego.

categoria: Categoría del videojuego (por ejemplo, acción, aventura, deporte, etc.).

precio: Precio unitario del videojuego.

stock: Cantidad disponible en inventario.

Relación:
Un videojuego puede aparecer en varias ventas (relación 1 a N). Esto es porque un videojuego puede ser comprado por varios clientes en distintas ventas, lo cual se representa a través de la entidad Detalleventa.
