
# Tarea: Mi prompt profesional

## Funcionalidad elegida

He elegido desarrollar un programa en Java que permita registrar las notas de un estudiante, calcular su promedio final y determinar si aprobo o desaprobo el curso.

Elegí esta funcionalidad porque es sencilla de entender y me permite comprobar cómo un prompt puede mejorar cuando agregamos instrucciones más específicas, contexto, ejemplos y un formato de respuesta.

## Version 1: prompt basico

### Prompt utilizado

```text
Crea un programa en Java para calcular notas de estudiantes.
```

### Analisis de la version 1

**Que cambie:** Esta es mi primera version, por lo que todavia no realice modificaciones.

**Por que:** Quise comprobar que programa generaba ChatGPT utilizando una instruccion sencilla y sin muchos detalles.

**Resultado obtenido:** ChatGPT creo un programa llamado CalculadoraNotas que registra tres notas, calcula el promedio y determina si el estudiante aprobo o desaprobo.

**Que mejoro:** Todavia no existe una version anterior para comparar, pero obtuve un programa funcional como punto de partida.

**Que falta mejorar:** No especifique la cantidad de notas, la nota minima aprobatoria ni el formato de presentacion. ChatGPT decidio esos detalles por su cuenta.

## Version 2

### Prompt utilizado

```text
Actua como desarrollador Java. Crea un programa de consola para registrar el nombre de un estudiante y sus tres notas, utilizando una escala de 0 a 20. Calcula el promedio de las tres notas y determina si el estudiante esta APROBADO cuando su promedio es mayor o igual a 11, o DESAPROBADO cuando es menor a 11. Valida que las notas ingresadas esten entre 0 y 20.
```

### Analisis de la version 2

**Que cambie:** Agregue el rol de desarrollador Java e indique la cantidad de notas, la escala de calificacion, la nota minima aprobatoria y las validaciones necesarias.

**Por que:** Queria evitar que ChatGPT decidiera por su cuenta los requisitos del programa.

**Que mejoro:** ChatGPT genero un programa llamado RegistroNotas, que cumple las condiciones indicadas. Ademas, incorporo una validacion para evitar que el usuario ingrese letras u otros valores no numericos.

**Resultado obtenido:** El programa solicita el nombre y las tres notas, calcula el promedio con dos decimales y muestra si el estudiante esta APROBADO o DESAPROBADO.

## Version 3: prompt final

### Prompt utilizado

```text
Actua como desarrollador Java especializado en aplicaciones educativas.

Crea un programa de consola en Java llamado RegistroNotas para registrar el nombre de un estudiante y sus tres notas.

Contexto: El programa sera utilizado en una institucion educativa peruana. Las notas van de 0 a 20 y el promedio se calcula sumando las tres notas y dividiendo entre 3. Si el promedio es mayor o igual a 11, el estudiante esta APROBADO; en caso contrario, esta DESAPROBADO. Valida que las notas sean numericas y esten dentro del rango permitido.

Ejemplo: Si un estudiante llamado Carlos obtiene 15, 12 y 14, el resultado debe mostrar un promedio de 13.67 y el estado APROBADO.

Formato de respuesta:
1. Explica brevemente como funciona el programa.
2. Presenta el codigo Java completo.
3. Muestra un ejemplo de ejecucion.
4. Explica las validaciones realizadas.

Restriccion: No utilices librerias externas. Usa solamente las clases incluidas en Java estandar.
```

### Analisis de la version 3

**Que cambie:** Agregue un contexto educativo mas detallado, un ejemplo concreto de calificaciones, el formato de respuesta y la restriccion de utilizar solamente Java estandar.

**Por que:** Queria obtener una respuesta mejor organizada, con requisitos claros y un ejemplo que me permitiera comprobar si el calculo era correcto.

**Que mejoro:** ChatGPT explico el funcionamiento antes del codigo, incluyo validaciones adicionales y presento un ejemplo de ejecucion. Tambien utilizo un metodo llamado leerNota() para validar las calificaciones.

**Resultado obtenido:** La IA genero un programa RegistroNotas que, segun el codigo presentado, cumple los requisitos solicitados. En el ejemplo de Carlos, con notas de 15, 12 y 14, calculo un promedio de 13.67 y mostro el estado APROBADO.

## Componentes del prompt final

### Identificacion de los componentes

| Componente | Texto de mi prompt final |
|------------|--------------------------|
| Rol | Actua como desarrollador Java especializado en aplicaciones educativas. |
| Instruccion | Crea un programa de consola en Java llamado RegistroNotas para registrar el nombre de un estudiante y sus tres notas. |
| Contexto | El programa sera utilizado en una institucion educativa peruana. Las notas van de 0 a 20 y el promedio se calcula sumando las tres notas y dividiendo entre 3. Si el promedio es mayor o igual a 11, el estudiante esta APROBADO; en caso contrario, esta DESAPROBADO. Valida que las notas sean numericas y esten dentro del rango permitido. |
| Ejemplos | Si un estudiante llamado Carlos obtiene 15, 12 y 14, el resultado debe mostrar un promedio de 13.67 y el estado APROBADO. |
| Formato | Explica brevemente como funciona el programa. Presenta el codigo Java completo. Muestra un ejemplo de ejecucion. Explica las validaciones realizadas. |
| Restriccion adicional | No utilices librerias externas. Usa solamente las clases incluidas en Java estandar. |

## Evaluacion del resultado

### Evaluacion del prompt profesional

| Criterio | Cumple (Si/No) |
|----------|----------------|
| Registra el nombre del estudiante y sus tres notas | Si |
| Calcula el promedio de las tres notas | Si |
| Determina si el estudiante aprobo o desaprobo | Si |
| Valida notas fuera del rango de 0 a 20 | Si |
| Utiliza solamente clases de Java estandar | Si |
| Presenta la explicacion, el codigo, el ejemplo y las validaciones en el orden solicitado | Si |

### Analisis de la evaluacion

El prompt profesional cumplio con los seis criterios revisados en la respuesta de ChatGPT. En comparacion con las versiones anteriores, consegui una respuesta mas organizada, con validaciones adicionales y un ejemplo concreto para comprobar el calculo del promedio.

Esta evaluacion se basa en el codigo y las explicaciones generadas por ChatGPT. Todavia no se ha comprobado su ejecucion real en Java.


### Errores frecuentes que evite

**1. Utilizar un prompt demasiado general**

En la primera version solamente pedi crear un programa para calcular notas. ChatGPT genero una solucion, pero decidio por su cuenta cuantos datos utilizar y cual seria la nota aprobatoria. Para evitar este problema, en las siguientes versiones especifique las tres notas, la escala de 0 a 20 y el promedio minimo de 11 para aprobar.

**2. No indicar el formato de la respuesta**

En las primeras versiones no estableci un orden especifico para presentar la informacion. En la version final indique que primero explicara el funcionamiento, despues mostrara el codigo, luego un ejemplo de ejecucion y finalmente las validaciones. Esto me permitio obtener una respuesta mas organizada y facil de comprender.
