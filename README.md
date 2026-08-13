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
![Image Alt]()
