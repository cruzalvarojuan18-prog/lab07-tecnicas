# Bitacora de tecnicas avanzadas
Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: ChatGPT / Gemini

## Ejercicio 2: Zero-shot, one-shot y few-shot
| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|-----------------|-------------------------|------------------------------------|
| Zero-shot | 5 | Tabla con columnas (#, Comentario, Clasificación) y emojis | No |
| One-shot | 5 | Lista numerada con flecha (`1. Texto -> Etiqueta`) | No |
| Few-shot | 5 | Estricto ` "Texto" -> Etiqueta ` (sin numeración) | Si |
## Ejercicio 3: Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|--------|--------------------|---------------------------|------------------|
| Directo | 318.60 | No | Si |
| Paso a paso | S/ 318.60 (detallando descuento, IGV y multiplicación) | Si | Si |S
## Ejercicio 4: Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|---------|-------------------------------|-----------------------|----------------------|
| A. Sin rol | Tecnico estandar | Ejemplo sencillo en Java (`int edad = 18;`) | Estudiantes con nociones basicas |
| B. Rol docente | Sencillo y didactico | Ejemplo en JavaScript y la analogia de una "caja con etiqueta" | Principiantes sin experiencia previa |
| C. Rol senior | Tecnico avanzado | Diferencia tipos primitivos vs referencias a objetos en Java | Desarrolladores o companeros de equipo |
## Ejercicio 5: Descomposicion
## Ejercicio 5: Descomposición de Tareas

### Registro por pasos

* **Paso 1:** La IA entregó un esquema estructurado en 5 secciones principales para organizar el documento.
* **Paso 2:** La IA desarrolló el contenido detallado de cada una de las secciones según el esquema previo.
* **Paso 3:** La IA revisó el borrador, ajustó el tono profesional y aplicó formato Markdown con negritas y listas.

---

### Comparación con el pedido en una sola vez

Al descomponer la tarea en varios pasos se obtuvo una respuesta más profunda, ordenada y precisa, mientras que al solicitar todo de una sola vez la IA generó un resumen mucho más general y condensado.
## Ejercicio 6: Prompt estructurado y autocriticaS
| Qué revisar | Cumple (Sí / No) |
|-------------|------------------|
| ¿Tiene las 4 columnas pedidas? | si |
| ¿Incluye el bloqueo después de 3 intentos? | si |
| ¿Incluye casos con campos vacíos? | no |
| ¿Indica qué casos agregó en la autocrítica? | Si |
| ¿Hay algún caso repetido o que no tenga sentido? | Si |
PROMPT ESTRUCTURADO INICIAL:
<rol>Actua como analista de pruebas de software.</rol>
<contexto>Login web con correo y contrasena. La cuenta se bloquea despues de 3 intentos fallidos.</contexto>
<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>
<formato>Tabla con las columnas: ID, escenario, datos de entrada, resultado esperado.</formato>

MENSAJE DE AUTOCRÍTICA:
Revisa tu tabla: ¿faltan casos limite como campos vacios, correo sin @ o contrasena con espacios? Agrega los que falten e indica cuales agregaste.