# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Tokens y ventana de contexto

| Texto                              | Caracteres | Tokens |
| ---------------------------------- | ---------- | ------ |
| Los estudiantes programan en Java. | 7          | 35     |
| The students program in Java.      | 6          | 30     |
| desafortunadamente                 | 4          | 18     |

En el paso 4, la IA recuerda los datos porque se encuentran activos dentro de su ventana de contexto actual. Por otro lado en el paso 5, al abrir un chat nuevo, no hay una ventana de contexto, por lo que la IA no tiene acceso al contexto anterior.

## Ejercicio 3: Temperatura

| Temperatura | % de BiblioTec | Nombres en los 5 intentos                                 |
| ----------- | -------------- | --------------------------------------------------------- |
| 0           | 100.0%         | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec     |
| 0.5         | 65.3%          | BiblioTec, LectoGo, BiblioTec, BiblioTec, BiblioTec       |
| 1           | 44.5%          | BiblioTec, BiblioTec, LibroYa, BiblioTec, BiblioTec       |
| 1.8         | 32.2%          | BiblioTec, PrestaLibro, BiblioTec, BiblioTec, PrestaLibro |

Al subir la temperatura, las probabilidades se distribuyen de forma más equitativa, haciendo que el modelo elija opciones menos frecuentes.

## Ejercicio 4: Prompt vago vs estructurado

| Criterio                            | Prompt vago   | Prompt estructurado |
| ----------------------------------- | ------------- | ------------------- |
| Menciona el objetivo del sistema    | No / A medias | Si                  |
| Menciona a los usuarios principales | No            | Si                  |
| Tiene exactamente 3 funcionalidades | No            | Si                  |
| Esta en 3 parrafos                  | No            | Si                  |
| Lo usaria en un informe real        | No            | Si                  |

## Ejercicio 5: Anatomia de un prompt

| Componente  | Texto de mi prompt                                                                                   |
| ----------- | ---------------------------------------------------------------------------------------------------- |
| Rol         | Actua como desarrollador Java.                                                                       |
| Instruccion | Crea un programa en Java usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto    | Para gestionar los productos de una tienda.                                                          |
| Ejemplo     | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio).                             |
| Formato     | Explica primero la estructura de la clase y luego presenta el codigo Java.                           |

En el nivel 1 la IA fue libre y genérica, mientras que al añadir el rol, contexto, instrucciones minuciosas, ejemplos y el formato, el codigo generado fue mas limpio, preciso y entendible.

## Ejercicio 6: Del prompt basico al profesional

| Qué revisar                                            | Cumple (Sí / No) |
| ------------------------------------------------------ | ---------------- |
| ¿Está escrito en Java y usa Swing?                     | Si               |
| ¿Pide correo y contraseña?                             | Si               |
| ¿Explica el funcionamiento antes o después del código? | Si               |
| ¿El código está organizado en clases?                  | Si               |
| ¿Valida los datos que ingresa el usuario?              | No               |

```text
Actua como desarrollador Java. Crea un ejemplo de login para una
aplicacion de escritorio utilizando Swing. El usuario debe ingresar
correo y contrasena. Explica brevemente el funcionamiento y presenta
el codigo organizado por clases.

Mejora el codigo anterior con estas restricciones: no uses librerias
externas, valida que el correo contenga @ y que la contrasena tenga
al menos 8 caracteres, y muestra los mensajes con JOptionPane.
```
