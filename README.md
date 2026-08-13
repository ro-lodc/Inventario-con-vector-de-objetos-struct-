# Inventario-con-vector-de-objetos-struct-
# Implementar un programa de inventario con vector de objetos (struct) en C++

Este programa, escrito en C++, refactoriza el manejo del inventario de
una tienda: en lugar de usar dos vectores paralelos, cada producto se
agrupa en un `struct Producto` (con los campos `nombre` y `precio`), y
todo el inventario se maneja con un único `vector<Producto>`.

El programa se controla mediante un menú interactivo que permite
listar los productos, agregar uno nuevo, modificar el precio de un
producto por índice, calcular el precio promedio del inventario y
consultar un producto por posición de forma segura.

## Estructura del programa

* **Struct `Producto`**: agrupa el nombre (`string`) y el precio
  (`float`) de cada producto en un solo objeto.
* **Vector de objetos**: `vector<Producto> inventario` almacena cada
  producto completo, en lugar de usar dos vectores separados.
* **Agregar (`push_back()`)**: se crea un objeto `Producto`, se le
  asignan sus datos y se inserta al final del vector.
* **Recorrido (`for (Producto p : inventario)`)**: se recorre el
  vector accediendo a `p.nombre` y `p.precio` para listar, calcular el
  promedio o mostrar la información de cada producto.
* **Modificar por índice**: se accede directamente a
  `inventario[i].precio` para actualizar el precio de un producto sin
  recorrer todo el vector.
* **Validación (`at()`)**: al consultar un producto por posición, se
  usa `at()` dentro de un `try/catch`, de modo que si la posición no
  existe se muestra un mensaje de error en lugar de cerrar el
  programa.

## Cómo compilar y ejecutar
```bash
g++ -o inventario_struct inventario_struct.cpp
./inventario_struct
```
![Image Alt](https://github.com/ro-lodc/Inventario-con-vector-de-objetos-struct-/blob/cfafd67a0cf462d7e9e47f7222bef12e856e91d9/Captura%20de%20pantalla%202026-08-12%20203254.png)
![Image Alt](https://github.com/ro-lodc/Inventario-con-vector-de-objetos-struct-/blob/e6cf31f146655ebcd649648e8e68d2b1ff5feeea/Captura%20de%20pantalla%202026-08-12%20203323.png)
![Image Alt](https://github.com/ro-lodc/Inventario-con-vector-de-objetos-struct-/blob/e7fd4607b8ab49ff575728c40da4285211332b03/Captura%20de%20pantalla%202026-08-12%20203346.png)
![Image Alt](https://github.com/ro-lodc/Inventario-con-vector-de-objetos-struct-/blob/068c05905f452258214da1a73a3fa516b2e2c633/Captura%20de%20pantalla%202026-08-12%20203456.png)
