# Posters

## Listado de Entidades:

### posters (ED)

    poster_id (PK)
    poster_nombre
    poster_descripcion
    poster_precio
    poster_stock

### tamannos_posters

    tamanno_id (PK)
    tamanno_descripcion

### usuarios (ED)

    usuario_id (PK)
    usuario_nombre
    usuario_apellido
    usuario_direccion
    usuario_email
    usuario_contrasenna

### roles (EC)

    rol_id (PK)
    rol_nombre

### usuarios_roles (EP)

    usuario_id (PK)
    rol_id (FK)

### categorias (EC)

    categoria_id (PK)
    categoria_nombre

### carrito_compras (ED) - (ET)

    carrito_compra_id (PK)
    usuario_id (FK)
    fecha_creacion

### detalle_carrito (EP)

    detalle_carrito_id (PK)
    carrito_compra_id (FK)
    poster_id (FK)
    detalle_carrito_cantidad

### pedido (ED)

    pedido_id (PK)
    usuario_id (FK)
    pedido_fecha
    estadoPedido_id (FK)

### detalle_pedido (EP)

    detalle_pedido_id (PK)
    pedido_id (FK)
    poster_id (FK)
    detalle_cantidad
    detalle_precio_unitario

### estado_pedido (EC)

    estado_id (PK)
    estado_descripcion

## Relaciones

1. Un _usuario_ puede tener varios _carrito compras_ (1 a m)
2. Un _carrito compras_ pertenece a un _usuario_ (m a 1)
3. Un _carrito compras_ puede tener muchos _posters_ (m a m a través de la entidad "detalle_carrito")
4. Un _poster_ puede pertenecer a varias categorías (m a m)
5. Un _detalle carrito_ pertenece a un _carrito compras_ y a un poster (1 a 1 a m)
6. Un _pedido_ pertenece a un usuario (m a 1)
7. Un _pedido_ puede contener varios productos (m a m a través de la entidad "detalle_pedido")
