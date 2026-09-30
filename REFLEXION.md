# Reflexión del equipo

**Instrucciones:** respondan **solo las 4 preguntas de su versión** (A o B), con **sus propias palabras** (3–5 líneas cada una)
y **citando nombres de métodos o líneas de SU código**. Las respuestas genéricas o iguales a las de otro grupo se califican en 0.
Escriban debajo de cada pregunta. (Se evalúa después; el autograde no califica este archivo.)

---

## VERSIÓN A

**A1.** `aplicarFactor` modifica el arreglo original, pero `copiaEscalada` no. Expliquen por qué, y qué es lo que
realmente se copia cuando le pasan un arreglo a un método.

> _Respuesta: La diferencia es que 'aplicarFactor´ cambia directamente el arreglo que recibe, mientras 'copiaEscalada' hace una copia nueva y trabaja sobre esa. Esto pasa porque cuando pasamos un arreglo a un metodo, se esta trabajando sobre el mismo arreglo original, Por eso si uso 'aplicarFactor', los valores originales cambian, pero con 'copaEscalada' se mantiene igual.

**A2.** ¿Por qué Java no permite tener `double calcularCosto(double kwh)` y `int calcularCosto(double kwh)` en la misma clase?
¿Qué versión de `calcularCosto` elige Java para la llamada `calcularCosto(5, 2.5, 0.1)` y por qué?

> _Respuesta: Java permite tener varios métodos con el mismo nombre siempre que sus parámetros sean diferentes. En nuestro caso usamos tres métodos llamados 'calcularCosto', pero cada uno recibe diferentes datos. Por ejemplo cuando usamos tres argumentos (5, 2.5, 0.1), java sabe que debe usar el método que recibe 'int dias', 'double kwhPorDia' y 'double tarfia'.

**A3.** En `Medidor`, ¿para qué sirve `this(id, 0)` en el constructor de un solo parámetro? ¿Qué ventaja tiene frente a copiar y pegar el código del otro constructor?

> _Respuesta: 'this(id, 0)' sirve para llamar al otro constructor de la misma clase. En este caso, cuando solamente damos el 'id', automáticamente se usa '0' como lectura inicial. Me parece útil porque así no tenemos que volver a escribir toda la lógica del otro constructor y evitamos repetir código.

**A4.** ¿Por qué los atributos de `Medidor` son `private`? ¿Qué protege `registrarLectura` y qué podría pasar si `lecturaActual` fuera público?

> _Respuesta: Los atributos de 'Medidor' están como 'private' para que no cualquier parte del programa pueda cambiarlos directamente. Por ejemplo, la lectura no puede simplemente modificarse a un valor menor, porque eso afectaría el cálculo del consumo. Por eso usamos 'registrarLectura', que se encarga de revisar primero si la nueva lectura es válida.

---

## VERSIÓN B

**B1.** Dibujen con texto (cajas y flechas) qué pasa en la memoria —variable `datos`, el arreglo y el parámetro del método—
cuando se ejecuta `aplicarFactor(datos, 2)`. ¿Por qué el arreglo original queda modificado?

> _Respuesta:_

**B2.** `imprimirEncabezado` es `void` y `clasificarConsumo` devuelve `String`. ¿Qué error da el compilador si olvidan un `return`
en alguna rama de `clasificarConsumo`? Expliquen con un caso de su código.

> _Respuesta:_

**B3.** ¿Por qué `sumaRecursiva` necesita un caso base? ¿Qué error aparece en Java si se omite y por qué ocurre?

> _Respuesta:_

**B4.** Si `Medidor` tuviera un atributo `double[] historial` y un getter que lo devolviera directamente, ¿qué riesgo hay para el
encapsulamiento? ¿Cómo se soluciona (idea de *copia defensiva*)?

> _Respuesta:_
