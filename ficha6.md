Ficha 6 · Reto 6: el mensaje en otro alfabeto (hexadecimal)
Enunciado. Decodifica la cadena hexadecimal 4b6572636b686f666673 y envía flag{palabra}.

1. Tipo de reto: ☐ Hash ☐ Codificación ☐ Cifrado ☐ Combinado
Codificación.

---

2. Concepto. ¿Qué es el hexadecimal? ¿Qué caracteres puede contener? ¿Cuántos caracteres hexadecimales hacen falta para representar un byte? ¿Protege la información o solo la representa?

 - Es un sistema de numeración en base 16.
 - 2 caracteres hexadecimales para representar un bits.
 - Solo la representa.
 - numeros de la a a la f
---
3. Procedimiento. Comando o herramienta y explicación:

|Herramienta|	Qué hace|
| --- | --- |
| convertextream | pasa de hexadecimal a texto |

---

4. Por qué lo hacemos así. ¿Cómo supisteis que estaba en hexadecimal? La cadena tiene 20 caracteres: ¿cuántas letras esperáis obtener y por qué? Relacionadlo con el caso guiado 4.

Para investigar. La palabra que obtenéis es el apellido de una persona que enunció un principio muy importante en criptografía. ¿Quién era y qué dice ese principio?
Sabemos que es hexadecimal debido a que tiene letras que van de la a a la f y del 0 al 9.
Lo que hace hexadecimal será pasar el texto a un lenguaje mas próximo al binario por lo que su longitud dependerá de la longitud de la palabra o el texto.
Kerckhoffs fue un criptógrafo holandés que fue el primero en realizar ensayos de criptografía militar. Su principio fue Establecer que todo sistema criptográfico debe ser seguro incluso si todo el sistema, excepto la clave, es de conocimiento público "Lo único que debe permanecer oculto es la clave".


---

5. Uso de la IA

Pregunta que le hicimos	Qué aprendimos	¿Se equivocó? ¿Cómo lo comprobamos?
No sea utilizado la IA

---

6. Flag: flag{Kerckhoffs}

---
7. Verificación
Lo verificaremos debido a que al pasar el código por distintos decodificadores y la terminal y todos dan el mismo resultado.

---
