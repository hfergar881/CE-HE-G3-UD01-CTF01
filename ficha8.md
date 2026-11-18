1. Tipo de reto: ☐ Hash ☐ Codificación ☐ Cifrado ☐ Combinado
Cifrado

¿Por qué esto sí es un cifrado y Base64 no lo era? ¿Cuál es la clave?
Base64 lo que hace es cambiar la representacion de un texto, mientras que rod13 cambia el mensaje directamente siguiendo un sistema.
SeguridadPorOscuridadNoFunciona.

---
2. Concepto. ¿Qué es el cifrado César? ¿Qué es ROT13? ¿Por qué aplicar ROT13 dos veces devuelve el texto original? ¿Qué relación tiene el 13 con un alfabeto de 26 letras?
 - Es uno de los métodos de criptografía mas antiguos es un cifrado por sustitución donde cada letra del texto original se remplaza por otra letra que se encuentra un numero fijo de posiciones mas adelante en el alfabeto.
 - Como cesar es un cifrado de sustitución con lo cual mueve la letra 13 posiciones mas adelante.
 - Porque desplaza cada letra 13 posiciones en el alfabeto y el albeto ingles tiene 26 letras.

---
3. Procedimiento. Comando o herramienta y explicación:

Parte del comando o paso	Qué hace

---

4. Por qué lo hacemos así. ¿Por qué el cifrado César es inseguro?  
Al tener pocas claves posibles, es vulnerable a ataques de fuerza bruta.
Otro problema es la frecuencia de las letras, por ejemplo en el lenguaje español se repiten las letras "a" y "e".
Analizando un texto largo, podemos observar qué letras aparecen más veces y deducir cuáles podrían corresponder a las letras originales.
¿Cuántas claves posibles tiene?
Si se usa el alfabeto inglés solamente existen 25 desplazamientos posibles (sin contar el desplazamiento 0, esto significa que no hemos desplazado ninguna letra)
Por ejemplo desplazamiento 1 es A -> B.

¿Cómo lo romperíais si no supierais que el desplazamiento es 13?
1. Analizar el texto.
2. Probar todos los desplazamientos posibles.
3. Usar análisis de frecuencia.
4. Automatizar con python.

Para investigar. El texto descifrado está relacionado con el reto 6. ¿Qué relación tiene con el principio de Kerckhoffs?
Ambos retos demuestran que si el método es público y no existe una clave secreta, la seguridad es nula. El principio de Kerckhoffs exige separar el algoritmo de la clave, al fallar en esto, tanto el Reto 6 como el Reto 8 se rompen en cuanto se reconoce el sistema.

---

5. Uso de la IA

Pregunta que le hicimos	Qué aprendimos	¿Se equivocó? ¿Cómo lo comprobamos?
- ¿Por qué el c.cesar es considerado inseguro en la actualidad?
- Como podriamos romper el cifrado si no sabemos que es rot13.
No se equivoco en ninguna pregunta debido a que revisamos las respuesta por internet.
---
6. Flag: flag{...}

---

7. Verificación. Volved a aplicar ROT13 al resultado. ¿Qué obtenéis?

---
