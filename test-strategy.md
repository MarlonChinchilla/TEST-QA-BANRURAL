
**Errores Encontrados y Soluciones**

**1. Error en la Generación del Número Aleatorio**
- **Descripción:** El número aleatorio generado para el juego no estaba en el rango correcto. El código `Math.random() * 10` producía números decimales entre 0 y 10, en lugar de números enteros entre 1 y 100.
- **Solución:** Modificado el código para generar un número entero entre 1 y 100 usando `Math.floor(Math.random() * 100) + 1`.

**2. Error en el Método de Eventos**
- **Descripción:** El método para agregar un evento estaba mal escrito como `addeventListener`.
- **Solución:** Corregido el nombre del método a `addEventListener`.

**3. Validación de Entrada Incorrecta**
- **Descripción:** El código no validaba correctamente que el número ingresado fuera un entero dentro del rango permitido (1-100). Esto podía llevar a que entradas inválidas no fueran manejadas adecuadamente.
- **Solución:** Se añadió validación para asegurar que el número ingresado sea un entero entre 1 y 100. Si la entrada no es válida, se muestra una alerta y no se incrementa el contador de intentos.

**4. Mensajes y Colores de Resultados Inconsistentes**
- **Descripción:** Los mensajes y colores mostrados para los resultados no coincidían con los requisitos especificados. Los mensajes de mayor o menor se mostraban incorrectamente, y los colores para los mensajes de éxito y fallo no eran correctos.
- **Solución:** Ajustes de los mensajes y colores de los resultados:
  - Mensaje verde para la victoria.
  - Mensaje negro para la indicación de número mayor o menor.
  - Mensaje rojo para el caso en que se pierden todos los intentos.

 **5. Contador de Intentos Incorrecto**
- **Descripción:** El contador de intentos se incrementaba incluso si la entrada no era válida, lo cual no seguía el requisito de no contar intentos para entradas inválidas.
- **Solución:** El contador de intentos ahora solo se incrementa si la entrada es válida. La validación de entradas evita el incremento en caso de datos inválidos.

