# Tasca-S2.03.-Estructura-de-dades---MongoDB // niveles 1, 2 y 3


OPTICA

Contenido de la colección: Gafas
{
	"_id" : ObjectId("64a02d023388789a0aa27a6d"),
	"proveedor" : "Proveedor 1",
	"marca" : "Marca 1",
	"graduacion" : "2.0",
	"tipo_montura" : "flotante",
	"color_montura" : "negro",
	"color_vidrio" : "transparente",
	"precio" : 100.5
}
------------------------------------
Contenido de la colección: clientes
{
	"_id" : ObjectId("64a02e453388789a0aa27a6e"),
	"nombre" : "Nombre del cliente",
	"direccion_postal" : "Direccion del cliente",
	"telefono" : "Telefono del cliente",
	"email" : "Email del cliente",
	"fecha_de_registro" : ISODate("2023-07-01T00:00:00Z"),
	"cliente_recomendador" : "Cliente que lo recomendo",
	"empleado_venta" : "Empleado que vendio las gafas"
}
------------------------------------
Contenido de la colección: proveedores
{
	"_id" : ObjectId("64a02c7e3388789a0aa27a6c"),
	"nombre" : "Proveedor 1",
	"direccion" : {
		"calle" : "Calle 1",
		"numero" : 123,
		"piso" : "1A",
		"puerta" : "B",
		"ciudad" : "Ciudad 1",
		"codigo_postal" : "12345",
		"pais" : "País 1"
	},
	"telefono" : "123456789",
	"fax" : "987654321",
	"nif" : "12345678A"
}
------------------------------------



PIZZERIA

Contenido de la colección: categoria
{ "_id" : ObjectId("64a082df8efe07d3a219e8c1"), "nombre" : "marguerita" }
------------------------------------
Contenido de la colección: clientes
{
	"_id" : ObjectId("64a0410a8efe07d3a219e8b9"),
	"nombre" : "David",
	"apellidos" : "Parra Garcia",
	"direccion" : "Paseo de la Castellana 2, Madrid",
	"codigo_postal" : "030032",
	"localidad" : ObjectId("64a0410a8efe07d3a219e8b7"),
	"provincia" : ObjectId("64a0410a8efe07d3a219e8b8"),
	"telefono" : "687999888"
}
{
	"_id" : ObjectId("64a282114fe50bdccd01ed43"),
	"nombre" : "Pablo",
	"apellidos" : "Fernandez Lopez",
	"direccion" : "av del mar 18, Murcia",
	"codigo_postal" : 67832,
	"localidad" : "Barranco del Lobo",
	"provincia" : "Murcia",
	"telefono" : "645333213"
}
{
	"_id" : ObjectId("64a282114fe50bdccd01ed44"),
	"nombre" : "Pepe",
	"apellidos" : "Perez Muñoz",
	"direccion" : "calle 2 de mayo, 24; 3o 5a",
	"codigo_postal" : 42336,
	"localidad" : "Sevilla",
	"provincia" : "Sevilla",
	"telefono" : "644533124"
}
------------------------------------
Contenido de la colección: empleado
{
	"_id" : ObjectId("64a0894b8efe07d3a219e8c8"),
	"nombre" : "David",
	"apellidos" : "Lopez Garcia",
	"nif" : "23434567A",
	"telefono" : "967666555",
	"cocinero" : true,
	"repartidor" : false
}
{
	"_id" : ObjectId("64a2836c4fe50bdccd01ed45"),
	"nombre" : "Juan",
	"apellidos" : "Gallego Herrera",
	"nif" : "67887689F",
	"telefono" : "644567542",
	"cocinero" : false,
	"repartidor" : true
}
{
	"_id" : ObjectId("64a2836c4fe50bdccd01ed46"),
	"nombre" : "Francisco",
	"apellidos" : "Lopez Faba",
	"nif" : "55566643E",
	"telefono" : "698784033",
	"cocinero" : false,
	"repartidor" : true
}
------------------------------------
Contenido de la colección: localidad
{ "_id" : ObjectId("64a07e6d8efe07d3a219e8ba"), "nom" : "Madrid" }
{ "_id" : ObjectId("64a283f04fe50bdccd01ed47"), "nombre" : "Barcelona" }
{ "_id" : ObjectId("64a283f04fe50bdccd01ed48"), "nombre" : "Sevilla" }
------------------------------------
Contenido de la colección: pedido
{
	"_id" : ObjectId("64a081c18efe07d3a219e8bc"),
	"fecha_hora" : ISODate("2023-07-01T10:00:00Z"),
	"repartido" : true,
	"cantidad_productos" : {
		"pizza" : 2,
		"bebida" : 3
	},
	"precio_total" : 35.5,
	"cliente" : ObjectId("64a081c18efe07d3a219e8bd"),
	"tienda" : ObjectId("64a088cc8efe07d3a219e8c5"),
	"repartidor" : ObjectId("64a081c18efe07d3a219e8bf"),
	"fecha_hora_llevar" : ISODate("2023-07-01T11:30:00Z")
}
{
	"_id" : ObjectId("64a285964fe50bdccd01ed49"),
	"fecha_hora" : ISODate("2023-07-01T10:00:00Z"),
	"repartido" : false,
	"cantidad_productos" : {
		"pizza" : 1,
		"bebida" : 1
	},
	"precio_total" : 19.99,
	"cliente" : "64a282114fe50bdccd01ed43",
	"tienda" : "64a088cc8efe07d3a219e8c5",
	"repartidor" : "64a2836c4fe50bdccd01ed45",
	"fecha_hora_llevar" : ISODate("2023-07-01T11:30:00Z")
}
{
	"_id" : ObjectId("64a285964fe50bdccd01ed4a"),
	"fecha_hora" : ISODate("2023-07-01T10:00:00Z"),
	"repartido" : false,
	"cantidad_productos" : {
		"pizza" : 1,
		"bebida" : 1
	},
	"precio_total" : 19.99,
	"cliente" : "64a282114fe50bdccd01ed43",
	"tienda" : "64a088cc8efe07d3a219e8c5",
	"repartidor" : "64a2836c4fe50bdccd01ed45",
	"fecha_hora_llevar" : ISODate("2023-07-01T11:30:00Z")
}
------------------------------------
Contenido de la colección: pizza
{
	"_id" : ObjectId("64a088238efe07d3a219e8c3"),
	"nombre" : "marguerita",
	"descripcion" : "tomate, mozzarella y albahaca",
	"imagen" : "url",
	"precio" : "7.99",
	"categoria" : ObjectId("64a082df8efe07d3a219e8c1")
}
------------------------------------
Contenido de la colección: producto
------------------------------------
Contenido de la colección: productos
{
	"_id" : ObjectId("64a082708efe07d3a219e8c0"),
	"nombre" : "pizza",
	"descripcion" : "tomate, mozarella, albahaca y aceite picante",
	"imagen" : "url",
	"precio" : 7.99
}
------------------------------------
Contenido de la colección: provincia
{ "_id" : ObjectId("64a07ed48efe07d3a219e8bb"), "nombre" : "Madrid" }
{ "_id" : ObjectId("64a2860d4fe50bdccd01ed4b"), "nombre" : "Barcelona" }
{ "_id" : ObjectId("64a2860d4fe50bdccd01ed4c"), "nombre" : "Sevilla" }
------------------------------------
Contenido de la colección: tienda
{
	"_id" : ObjectId("64a088cc8efe07d3a219e8c5"),
	"direccion" : "calle xx, 2. 032233, Madrid",
	"codigo_postal" : "032233",
	"localidad" : ObjectId("64a07e6d8efe07d3a219e8ba"),
	"provincia" : ObjectId("64a07ed48efe07d3a219e8bb")
}
{
	"_id" : ObjectId("64a288584fe50bdccd01ed4d"),
	"direccion" : "calle xx 23, 3o 2a",
	"codigo_postal" : "41623",
	"localidad_id" : "64a283f04fe50bdccd01ed48",
	"provincia_id" : "64a2860d4fe50bdccd01ed4c"
}
{
	"_id" : ObjectId("64a288584fe50bdccd01ed4e"),
	"direccion" : "calle xx, 12",
	"codigo_postal" : "56443",
	"localidad_id" : "64a283f04fe50bdccd01ed47",
	"provincia_id" : "64a2860d4fe50bdccd01ed4b"
}
------------------------------------



YOUTUBE

Contenido de la colección: Canal
{
	"_id" : ObjectId("64a1232b0f75bcf5274768f7"),
	"nombre" : "Bases de Datos",
	"descripcion" : "programacion orientada a bases de datos",
	"fecha_creacion" : ISODate("2020-07-01T00:00:00Z")
}
------------------------------------
Contenido de la colección: Etiqueta
{ "_id" : ObjectId("64a1204d0f75bcf5274768f5"), "nombre" : "New" }
------------------------------------
Contenido de la colección: Like_Dislike
{
	"_id" : ObjectId("64a124c00f75bcf5274768f9"),
	"usuario_id" : "64a11f170f75bcf5274768f4",
	"video_id" : "64a122300f75bcf5274768f6",
	"tipo" : "like",
	"fecha_hora" : ISODate("2023-07-01T03:00:00Z")
}
------------------------------------
Contenido de la colección: Suscripcion
{
	"_id" : ObjectId("64a123df0f75bcf5274768f8"),
	"usuario_id" : "64a11f170f75bcf5274768f4",
	"canal_id" : "64a1232b0f75bcf5274768f7"
}
------------------------------------
Contenido de la colección: Usuario
{
	"_id" : ObjectId("64a11f170f75bcf5274768f4"),
	"email" : "dv@gmail.com",
	"password" : "xxxxx",
	"nombreUsuario" : "dv23002",
	"fecha_nacimiento" : ISODate("1990-01-02T00:00:00Z"),
	"sexo" : "femenino",
	"pais" : "Italia",
	"codigo_postal" : "41098"
}
------------------------------------
Contenido de la colección: Video
{
	"_id" : ObjectId("64a122300f75bcf5274768f6"),
	"titulo" : "Mongo db para principiantes",
	"descripcion" : "tutorial para aprender las bases de monogodb",
	"size" : "50 mb",
	"archivo_video" : "mongo_db.mp4",
	"duracion" : "2.50 min",
	"thumbnail" : "url",
	"reproducciones" : "5",
	"likes" : "2",
	"dislikes" : "0",
	"estado" : "publico",
	"etiqueta_id" : "64a1204d0f75bcf5274768f5",
	"usuario_id" : "64a11f170f75bcf5274768f4",
	"fecha_hora_publicacion" : ISODate("2023-07-01T12:00:00Z")
}
------------------------------------
Contenido de la colección: comentario
{
	"_id" : ObjectId("64a127680f75bcf5274768fb"),
	"texto" : "Gracias por este contenido",
	"fecha_hora" : ISODate("2023-07-01T01:30:00Z"),
	"video_id" : "64a122300f75bcf5274768f6",
	"usuario_id" : "64a11f170f75bcf5274768f4"
}
------------------------------------
Contenido de la colección: comentario_like_dislike
{
	"_id" : ObjectId("64a1285b0f75bcf5274768fc"),
	"usuario_id" : "64a11f170f75bcf5274768f4",
	"comentario_id" : "64a127680f75bcf5274768fb",
	"tipo" : "like",
	"fecha_hora" : ISODate("2023-07-01T01:42:00Z")
}
------------------------------------
Contenido de la colección: playlist
{
	"_id" : ObjectId("64a125ab0f75bcf5274768fa"),
	"nombre" : "playlist1",
	"fecha_creacion" : ISODate("2023-06-04T12:00:00Z"),
	"estado" : "publica",
	"video_id" : "64a122300f75bcf5274768f6"
}
------------------------------------

SPOTIFY

Contenido de la colección: album
{
	"_id" : ObjectId("64a1550eeab85f44b89f0fda"),
	"titulo" : "album1",
	"agno_publicacion" : 2022,
	"portada" : "url",
	"artista_id" : "64a1534deab85f44b89f0fd7"
}
{
	"_id" : ObjectId("64a1550eeab85f44b89f0fdb"),
	"titulo" : "album2",
	"agno_publicacion" : 2023,
	"portada" : "url",
	"artista_id" : "64a1534deab85f44b89f0fd8"
}
{
	"_id" : ObjectId("64a1550eeab85f44b89f0fdc"),
	"titulo" : "album3",
	"agno_publicacion" : 2019,
	"portada" : "url",
	"artista_id" : "64a1534deab85f44b89f0fd9"
}
------------------------------------
Contenido de la colección: artista
{
	"_id" : ObjectId("64a1534deab85f44b89f0fd7"),
	"nombre" : "artista1",
	"imagen" : "url"
}
{
	"_id" : ObjectId("64a1534deab85f44b89f0fd8"),
	"nombre" : "artista2",
	"imagen" : "url"
}
{
	"_id" : ObjectId("64a1534deab85f44b89f0fd9"),
	"nombre" : "artista3",
	"imagen" : "url"
}
------------------------------------
Contenido de la colección: artistas_relacionados
{
	"_id" : ObjectId("64a1751ed84eff2a11a24e36"),
	"artista_id" : "64a1534deab85f44b89f0fd7",
	"relacionado" : "64a1534deab85f44b89f0fd8"
}
{
	"_id" : ObjectId("64a1751ed84eff2a11a24e37"),
	"artista_id" : "64a1534deab85f44b89f0fd8",
	"relacionado" : "64a1534deab85f44b89f0fd9"
}
------------------------------------
Contenido de la colección: cancion
{
	"_id" : ObjectId("64a1561eeab85f44b89f0fdd"),
	"titulo" : "cancion1",
	"duracion" : "03:45 min",
	"reproducciones" : 13555,
	"album_id" : "64a1550eeab85f44b89f0fda"
}
{
	"_id" : ObjectId("64a1561eeab85f44b89f0fde"),
	"titulo" : "cancion2",
	"duracion" : "02:27 min",
	"reproducciones" : 239789,
	"album_id" : "64a1550eeab85f44b89f0fdb"
}
{
	"_id" : ObjectId("64a1561eeab85f44b89f0fdf"),
	"titulo" : "cancion3",
	"duracion" : "03:10 min",
	"reproducciones" : 23654,
	"album_id" : "64a1550eeab85f44b89f0fdc"
}
------------------------------------
Contenido de la colección: canciones_playlist
{
	"_id" : ObjectId("64a1929dd84eff2a11a24e3d"),
	"playlist_id" : "64a151cdeab85f44b89f0fd4",
	"cancion_id" : "64a1561eeab85f44b89f0fdd",
	"usuario_id" : "64a142c9eab85f44b89f0fcc",
	"fecha_agregado" : ISODate("2023-01-01T00:00:00Z")
}
{
	"_id" : ObjectId("64a1929dd84eff2a11a24e3e"),
	"playlist_id" : "64a151cdeab85f44b89f0fd5",
	"cancion_id" : "64a1561eeab85f44b89f0fde",
	"usuario_id" : "64a142c9eab85f44b89f0fcd",
	"fecha_agregado" : ISODate("2022-01-01T00:00:00Z")
}
{
	"_id" : ObjectId("64a1929dd84eff2a11a24e3f"),
	"playlist_id" : "64a151cdeab85f44b89f0fd6",
	"cancion_id" : "64a1561eeab85f44b89f0fdf",
	"usuario_id" : "64a142c9eab85f44b89f0fce",
	"fecha_agregado" : ISODate("2021-01-01T00:00:00Z")
}
------------------------------------
Contenido de la colección: favoritos
{
	"_id" : ObjectId("64a1902bd84eff2a11a24e38"),
	"usuario_id" : "64a142c9eab85f44b89f0fcc",
	"album_id" : "64a1550eeab85f44b89f0fda",
	"cancion_id" : "64a1561eeab85f44b89f0fdd"
}
{
	"_id" : ObjectId("64a1902bd84eff2a11a24e39"),
	"usuario_id" : "64a142c9eab85f44b89f0fcd",
	"album_id" : "64a1550eeab85f44b89f0fdb",
	"cancion_id" : "64a1561eeab85f44b89f0fdf"
}
------------------------------------
Contenido de la colección: playlist
{
	"_id" : ObjectId("64a151cdeab85f44b89f0fd4"),
	"titulo" : "Favs",
	"numero_canciones" : 25,
	"fecha_creacion" : ISODate("2022-03-03T00:00:00Z"),
	"estado" : "activo"
}
{
	"_id" : ObjectId("64a151cdeab85f44b89f0fd5"),
	"titulo" : "Relax",
	"numero_canciones" : 100,
	"fecha_creacion" : ISODate("2019-03-15T00:00:00Z"),
	"estado" : "activo"
}
{
	"_id" : ObjectId("64a151cdeab85f44b89f0fd6"),
	"titulo" : "Fiesta",
	"numero_canciones" : 115,
	"fecha_creacion" : ISODate("2022-07-03T00:00:00Z"),
	"estado" : "activo"
}
------------------------------------
Contenido de la colección: suscripcion
{
	"_id" : ObjectId("64a14a51eab85f44b89f0fd0"),
	"usuario_id" : "64a142c9eab85f44b89f0fcc",
	"tipo" : "free",
	"fecha_inicio" : ISODate("2021-05-04T00:00:00Z")
}
{
	"_id" : ObjectId("64a14cdceab85f44b89f0fd2"),
	"usuario_id" : "64a142c9eab85f44b89f0fcd",
	"tipo" : "premium",
	"fecha_inicio" : ISODate("2022-05-07T00:00:00Z"),
	"fecha_renovacion" : ISODate("2024-05-07T00:00:00Z"),
	"forma_pago" : {
		"tipo" : "tarjeta",
		"numero" : "***********9876",
		"mes_caducidad" : 12,
		"agno_caducidad" : "2025",
		"codigo_seguridad" : "***"
	},
	"pagos" : [
		{
			"fecha" : ISODate("2022-06-01T00:00:00Z"),
			"numero_pago" : "ORD001",
			"precio_total" : "9.99"
		},
		{
			"fecha" : ISODate("2022-07-02T00:00:00Z"),
			"numero_pago" : "ORD001",
			"precio_total" : "9.99"
		},
		{
			"fecha" : ISODate("2022-06-01T00:00:00Z"),
			"numero_pago" : "ORD001",
			"precio_total" : "9.99"
		}
	]
}
{
	"_id" : ObjectId("64a14fe4eab85f44b89f0fd3"),
	"usuario_id" : "64a142c9eab85f44b89f0fce",
	"tipo" : "premium",
	"fecha_inicio" : ISODate("2020-01-01T00:00:00Z"),
	"fecha_renovacion" : ISODate("2024-01-01T00:00:00Z"),
	"forma_pago" : "paypal",
	"pagos" : [
		{
			"fecha" : ISODate("2021-01-01T00:00:00Z"),
			"numero_pago" : "ORD023",
			"precio_total" : 9.99
		},
		{
			"fecha" : ISODate("2022-01-01T00:00:00Z"),
			"numero_pago" : "ORD0023",
			"precio_total" : 9.99
		}
	]
}
------------------------------------
Contenido de la colección: usuario
{
	"_id" : ObjectId("64a142c9eab85f44b89f0fcc"),
	"email" : "sd1@gmail.com",
	"password" : "xxxx",
	"nombre_usuario" : "sd003",
	"fecha_nacimiento" : ISODate("1995-05-10T00:00:00Z"),
	"sexo" : "masculino",
	"pais" : "Espagna",
	"codigo_postal" : "08001"
}
{
	"_id" : ObjectId("64a142c9eab85f44b89f0fcd"),
	"email" : "fj11@gmail.com",
	"password" : "xxxxx",
	"nombre_usuario" : "fj1134",
	"fecha_nacimiento" : ISODate("1994-01-12T00:00:00Z"),
	"sexo" : "femenino",
	"pais" : "Italia",
	"codigo_postal" : "220988"
}
{
	"_id" : ObjectId("64a142c9eab85f44b89f0fce"),
	"email" : "ghj21@gmail.com",
	"password" : "xxxx",
	"nombre_usuario" : "ghj21",
	"fecha_nacimiento" : ISODate("1993-05-05T00:00:00Z"),
	"sexo" : "femenino",
	"pais" : "Espagna",
	"codigo_postal" : "08002"
}
------------------------------------
