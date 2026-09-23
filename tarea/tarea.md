# Tarea: Mi prompt profesional

## Funcionalidad elegida

Diseño e implementación de un **CRUD de Productos** en consola utilizando el lenguaje Java para la gestión de inventario básico (Crear, Leer, Actualizar y Eliminar).

## Version 1: prompt basico

```text
Hazme un codigo en Java para un CRUD de productos.
```

**Qué cambió / Qué mejoró:** Es la versión inicial. La respuesta de la IA es excesivamente genérica, utiliza estructuras complejas, mezcla bases de datos o frameworks externos y no organiza el código en un formato fácil de leer.

## Version 2

```text
Actua como desarrollador Java experto. Crea un sistema CRUD de productos en consola. El programa debe permitir registrar, listar, actualizar y eliminar productos utilizando una lista en memoria (ArrayList).
```

**Qué mejoro:** Se añadió un **Rol** y se especificó el **Contexto** técnico (consola y simulación en memoria con ArrayList). La respuesta mejoró drásticamente porque el código ya no incluye bases de datos complejas, pero el formato de salida y el control de errores siguen siendo inconsistentes.

## Version 3: prompt final

```text
Actua como desarrollador Java experto. Diseña un sistema CRUD de productos (id, nombre, precio, stock) interactivo por consola mediante un menú de opciones utilizando programación orientada a objetos. RESTRICCIÓN: No utilices librerías externas ni bases de datos, gestiona todo en memoria mediante ArrayList. Como EJEMPLO de buenas prácticas, encapsula las variables y maneja excepciones básicas (InputMismatchException) si el usuario ingresa texto en lugar de números en el precio. FORMATO: Presenta el código limpio y comentado estructurado en dos clases bien definidas (Producto y SistemaCRUD), seguido de una breve guía de uso de 3 viñetas.
```

**Qué mejoro:** Se incorporaron todos los componentes esenciales: restricciones claras, manejo de errores específico como ejemplo y un formato de entrega estricto en dos clases. El código resultante es modular, seguro, compila de forma inmediata y cumple los requisitos de producción académica.

## Componentes del prompt final

| Componente      | Texto de mi prompt                                                                                                                                               |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Rol**         | Actua como desarrollador Java experto.                                                                                                                           |
| **Instruccion** | Diseña un sistema CRUD de productos interactivo por consola mediante un menú de opciones utilizando programación orientada a objetos con control de excepciones. |
| **Contexto**    | Gestión de productos (id, nombre, precio, stock) en memoria mediante ArrayList.                                                                                  |
| **Restricción** | No utilices librerías externas ni bases de datos.                                                                                                                |
| **Ejemplo**     | Encapsula las variables y maneja excepciones básicas (InputMismatchException) si el usuario ingresa texto en lugar de números.                                   |
| **Formato**     | Presenta el código limpio estructurado en dos clases (Producto y SistemaCRUD), seguido de una guía de uso de 3 viñetas.                                          |

## Evaluacion del resultado

| Criterio de Calidad                                          | Cumple (Sí / No) |
| ------------------------------------------------------------ | ---------------- |
| ¿El sistema es interactivo por consola con menú?             | Sí               |
| ¿Cumple con la restricción de no usar librerías externas?    | Sí               |
| ¿Implementa la separación en las dos clases solicitadas?     | Sí               |
| ¿Evita errores de ejecución manejando excepciones numéricas? | Sí               |

## Errores que evite

**Ser demasiado general:** En la V1 el pedido era tan ambiguo que la IA podía dar código web o de escritorio. Se evitó definiendo que se requería una aplicación nativa de consola.

**No indicar el formato:** En los primeros intentos el código venía mezclado en un solo archivo plano difícil de leer. Se solucionó exigiendo explícitamente la división modular en las clases Producto y SistemaCRUD.
