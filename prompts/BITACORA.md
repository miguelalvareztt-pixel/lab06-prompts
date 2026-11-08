# Bitacora de prompts

Laboratorio 06: Fundamentos de Ingenieria de Prompts.

Herramienta de IA usada: ChatGPT

## Ejercicio 2: Tokens y ventana de contexto

| Texto | Caracteres | Tokens |
|-------|------------|--------|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |


### Observaciones sobre la ventana de contexto

1. En el primer chat, ChatGPT recordó correctamente que mi aplicación se llamaba TiendaTec y utilizaba Java Swing, porque le había proporcionado esa información anteriormente.
2. En un chat nuevo, ChatGPT también respondió correctamente, aunque no le proporcioné nuevamente esos datos. Esto podría deberse a la función de memoria de ChatGPT, que permite recuperar información de conversaciones anteriores.

## Ejercicio 3: Temperatura

### Resultados del simulador

| Temperatura | % de BiblioTec | Nombres en los 5 intentos |
|-------------|----------------|---------------------------|
| 0 | 100 % | BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 0.5 | 65.3 % | LibroYa, BiblioTec, BiblioTec, BiblioTec, BiblioTec |
| 1 | 44.5 % | BiblioTec, PrestaLibro, PaginaLibre, LibroYa, PaginaLibre |
| 1.8 | 32.2 % | PaginaLibre, PrestaLibro, PrestaLibro, PrestaLibro, NubeDeTinta |

### Observaciones

1. Al aumentar la temperatura, las probabilidades se distribuyen entre más opciones y los nombres generados presentan mayor variedad.
2. El simulador nunca inventa nombres nuevos porque solamente puede seleccionar los seis nombres que están definidos en el código.

## Ejercicio 4: Prompt vago vs estructurado


### Comparación de los prompts

| Criterio | Prompt vago | Prompt estructurado |
|----------|-------------|---------------------|
| Menciona el objetivo del sistema | Sí | Sí |
| Menciona a los usuarios principales | Sí | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Está en 3 párrafos | No | Sí |
| Lo usaría en un informe real | Sí | Sí |

### Observación

El prompt vago produjo una respuesta útil, pero incluyó más funcionalidades y párrafos de los necesarios. En cambio, con el prompt estructurado obtuve una descripción más precisa y organizada, que cumplió las indicaciones sobre los usuarios, las tres funcionalidades y el formato solicitado.

## Ejercicio 5: Anatomia de un prompt


### Componentes de mi prompt final

| Componente | Texto de mi prompt |
|------------|--------------------|
| Rol | Actua como desarrollador Java. |
| Instruccion | Crea un programa en Java. / usando una clase Producto con los atributos codigo, nombre, precio y stock. |
| Contexto | para gestionar los productos de una tienda |
| Ejemplos | Usa este estilo para los metodos: getPrecio(), setPrecio(double precio). |
| Formato | Explica primero la estructura de la clase y luego presenta el codigo Java. |


### Comparacion de los cinco niveles

1. **Nivel 1:** Al pedir solamente un programa en Java, ChatGPT genero una calculadora porque no especifique que tipo de aplicacion necesitaba.
2. **Nivel 2:** Al agregar el rol de desarrollador Java, la IA tambien creo una calculadora, pero incluyo un menu numerico, un ejemplo de ejecucion y explicaciones.
3. **Nivel 3:** Al agregar el contexto de una tienda, ChatGPT dejo de generar calculadoras y creo un sistema para gestionar productos utilizando Java Swing.
4. **Nivel 4:** Al especificar la clase Producto y sus cuatro atributos, la IA organizo mejor el programa y creo las clases Producto y Tienda.
5. **Nivel 5:** Al indicar el formato, ChatGPT explico primero la estructura de la clase Producto y despues presento el codigo Java, respetando el orden solicitado.

