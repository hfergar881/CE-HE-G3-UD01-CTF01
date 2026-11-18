Ficha 9 · Reto 9: capa sobre capa (combinado) ⭐
Enunciado. La cadena NTA2NTZlNzQ2NTczNzQ2OTZlNjc0NTc0Njk2MzZm está en Base64. Al decodificarla obtendrás hexadecimal; al decodificar este, una palabra. Calcula el MD5 de esa palabra y envía flag{md5}.

1. Tipo de reto: ☐ Hash ☐ Codificación ☐ Cifrado ☐ Combinado
¿Qué técnicas de los retos anteriores se combinan?
Combinado

Nos encontramos con base64, tras esta tenemos una cadena hexadecimal.
Tras decodificar la hex, obtenemos una palabra, a ésta le aplicamos un hash.

---

2. Concepto. ¿Por qué se usan varias capas de codificación? ¿Hace eso la información más segura?
Se utilizan varias capas de codificación para transformar la información varias veces, dificultando su identificación o interpretación a simple vista pero no significa necesariamente que lo hace más segura.
Codificar transforma la representación de los datos, pero no necesita una clave secreta.
Aunque visualmente el resultado pueda parecer muy complicado, un atacante puede revertir las transformaciones si conoce o identifica los métodos utilizados.

---

3. Procedimiento. Completad la tabla con cada capa:

| Capa |	Lo que tenéis |	Cómo reconocéis el formato|	Comando	| Resultado |
|---|---|---|---|---|
|1|	NTA2NTZlNzQ2NTczNzQ2OTZlNjc0NTc0Njk2MzZm | Formato alfanumérico largo que suele terminar con uno o dos caracteres de relleno = y utiliza letras mayúsculas, minúsculas y números. | echo -n "NTA2NTZlNzQ2NTczNzQ2OTZlNjc0NTc0Njk2MzZm" | base64 -d | 50656e74657374696e674574696e673663	|		
|2| 50656e74657374696e674574696e673663	| Cadena compuesta estrictamente por caracteres hexadecimales, con una longitud par.	|	echo "50656e74657374696e674574696e673663" xxd -r -p | PentestingEtico |	
|3| PentestingEticoPentestingEtico	| Una palabra en texto plano legible en formato ASCII.	| echo -n "PentestingEtico" md5sum | c784ae85751ffee70b053ec8ea30c92a |

---

4. Por qué lo hacemos así. ¿Cómo decidisteis el orden de las capas? ¿Qué pasaría si intentarais decodificar el hexadecimal antes que el Base64?
El orden de las capas se decidió siguiendo el proceso inverso al que se utilizó para transformar el mensaje.
Primero debemos decodificar Base64 porque es la capa más externa.

Si intentamos decodificar hexadecimal antes que Base64 podemos obtener un error o un resultado incorrecto.
Mensaje original -> hex -> base64.

La regla fundamental es que las capas de codificación deben eliminarse en orden inverso al que fueron aplicadas.

---

5. Uso de la IA

Pregunta que le hicimos	Qué aprendimos	¿Se equivocó? ¿Cómo lo comprobamos?
No nos ha hecho falta preguntarle a la IA.

---

6. Flag: flag{c784ae85751ffee70b053ec8ea30c92a}

---

7. Verificación
Funciona porque las codificaciones son operaciones reversibles y deterministas que simplemente cambian la representación de los datos de bytes a caracteres legibles. Al aplicar el proceso inverso exactamente en el orden contrario al que se cifró, logramos reconstruir la información original y calcular su huella digital de forma unívoca.
---
