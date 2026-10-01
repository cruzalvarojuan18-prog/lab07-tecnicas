## Ejercicio 7: Tarea Práctica - Optimización de Prompts y Descomposición de Tareas
## Ejercicio 7: Tarea Práctica - Optimización de Prompts y Descomposición de Tareas

En esta sección se aplican las técnicas de Prompt Engineering avanzadas (Role Prompting, Few-Shot Prompting, Chain-of-Thought y Decomposición de Tareas) para resolver un caso de uso práctico.

### 1. Caso de Uso Elegido
* **Dominio:** Desarrollo de Software / Inteligencia Artificial aplicada a la educación.
* **Problema:** Un estudiante necesita comprender el concepto de *Recursividad* en programación, pero los ejemplos teóricos le resultan confusos. Requiere explicaciones progresivas, analógicas y un paso a paso claro del flujo de ejecución en memoria.

---

### 2. Descomposición de la Tarea (Task Decomposition)
Para lograr una respuesta precisa y estructurada, el proceso se divide en 4 sub-tareas consecutivas:

1. **Sub-tarea 1 (Explicación conceptual con analogía):** Explicar la recursividad utilizando una analogía de la vida real sin términos técnicos complejos.
2. **Sub-tarea 2 (Estructura y caso base):** Identificar las dos partes clave de cualquier función recursiva (Caso Base y Caso Recursivo).
3. **Sub-tarea 3 (Traza de ejecución en pila):** Mostrar la ejecución paso a paso (Call Stack) de un ejemplo clásico (Factorial o Fibonacci).
4. **Sub-tarea 4 (Buenas prácticas y prevención de errores):** Indicar los errores comunes (Stack Overflow) y cuándo usar bucles iterativos en lugar de recursividad.

---

### 3. Prompt Maestro Integrado (System Prompt + Chain-of-Thought + Few-Shot)

```text
[ROL]
Actúa como un Profesor Experto en Ciencias de la Computación y MENTOR de programación estructurada.

[TAREA]
Tu objetivo es enseñar el concepto de "Recursividad" a un alumno principiante siguiendo un proceso claro y paso a paso.

[INSTRUCCIONES Y RESTRICCIONES]
1. Piensa paso a paso antes de dar la respuesta final.
2. Usa un lenguaje claro, accesible y formal pero empático.
3. Proporciona ejemplos en pseudocódigo o Python limpios.

[EJEMPLOS (FEW-SHOT)]
Ejemplo de analogía clara:
- Concepto: Pila de platos (LIFO).
- Explicación: El último plato que pones es el primero que quitas.

[PROCESO DE PENSAMIENTO (CHAIN-OF-THOUGHT)]
Paso 1: Inicia con la analogía del "Muñeco Matrioshka" o la "Fila en el cine".
Paso 2: Define el Caso Base y la Llamada Recursiva.
Paso 3: Muestra el código para calcular el factorial de N.
Paso 4: Muestra el comportamiento de la memoria (Stack) paso a paso para factorial(3).
Paso 5: Concluye con el riesgo del Stack Overflow.
