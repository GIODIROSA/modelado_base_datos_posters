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

