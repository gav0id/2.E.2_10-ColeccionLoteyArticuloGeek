Ejercicio 2.E.2 10 - Colección Lote y Artículo Geek

Lógica del programa
Para resolver el último ejercicio de esta etapa, trabajé con el modelado de relaciones de asociación y agregación simple entre objetos. 

Primero, tomé la clase `ArticuloGeek` del primer ejercicio y la redefiní aplicando encapsulamiento: declaré sus atributos `nombre` y `precioBase` como privados y creé los métodos *getters* para permitir su lectura de forma segura.

Luego, diseñé la clase `ColeccionLote`. Esta clase actúa como un agrupador, por lo que le definí un atributo `descripcion` (String) y dos atributos de referencia que apuntan directamente a objetos externos: `articuloPrincipal` y `articuloSecundario` (ambos de tipo `ArticuloGeek`).

Para el comportamiento de la colección, implementé dos métodos que interactúan con estos objetos internos:
1. `calcularValorLote()`: Se comunica con ambos artículos invocando a sus métodos `getPrecioBase()`, suma ambos valores y retorna el `double` total.
2. `mostrarDetalleLote()`: Accede a los nombres y precios de los objetos agrupados a través de sus *getters* para imprimir un desglose por consola.

Dentro de la clase `Main`, desarrollé la siguiente lógica de prueba:
1. Instancié dos objetos `ArticuloGeek` totalmente independientes ("Figura de Miku" y "Tomo de manga").
2. Instancié un objeto `ColeccionLote`, pasándole su descripción y las referencias de los dos artículos previamente creados a través del constructor, logrando así la agregación.
3. Invoqué los métodos `calcularValorLote()` y `mostrarDetalleLote()` de la colección, comprobando por consola que el lote es capaz de leer y operar con los datos de los objetos que contiene.

Ejecución en consola
<img width="1366" height="721" alt="{0FFB5C82-0111-4395-A588-3458AD64BA02}" src="https://github.com/user-attachments/assets/bdc8d4f8-410f-46f5-8ab6-beefcf06ef8b" />
