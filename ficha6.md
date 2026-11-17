# Ficha 6 · Reto 6: el mensaje en otro alfabeto (hexadecimal)
    Enunciado. Decodifica la cadena hexadecimal 4b6572636b686f666673 y envía flag{palabra}.

## 1. Tipo de reto.  
Codificación; no encripta la información, solo cambia la forma de representarla

## 2. Concepto.  
**¿Qué es el hexadecimal? ¿Qué caracteres puede contener? ¿Cuántos caracteres hexadecimales hacen falta para representar un byte? ¿Protege la información o solo la representa?**  
 - Es un sistema de numeración en base 16.
 - Puede contener todos los dígitos (0-9) y las seis primeras letras del alfabeto (A-F). 
 - Usa 2 caracteres hexadecimales para representar un byte.
 - No protege la información de forma relevante ya que solo la representa en un formato distinto y cualquiera puede decodificarla fácilmente.

## 3. Procedimiento. Comando o herramienta y explicación.

|Herramienta|	Qué hace|
| --- | --- |
| convertstring.com | Decodifica cadenas hexadecimales a texto |

## 4. Por qué lo hacemos así
**¿Cómo supisteis que estaba en hexadecimal? La cadena tiene 20 caracteres: ¿cuántas letras esperáis obtener y por qué? Relacionadlo con el caso guiado 4.**  
**Para investigar. La palabra que obtenéis es el apellido de una persona que enunció un principio muy importante en criptografía. ¿Quién era y qué dice ese principio?**  
- Sabemos que es hexadecimal debido a que solo contiene letras de la a a la f y los números del 0 al 9. Se relaciona con el caso 4 porque también tratamos una codificación, en la que la longitud del resultado también se podía conocer antes de la conversión; aunque con una correspondencia distinta.
- La longitud del resultado debe ser la mitad de la longitud de la cadena hexadecimal, es decir, 10 caracteres, ya que cada caracter unicode se representa con 2 caracteres hexadecimales.
- Kerckhoffs fue un criptógrafo holandés que fue el primero en realizar ensayos de criptografía militar. Su principio fue establecer que todo sistema criptográfico debe ser seguro incluso si todo el sistema, excepto la clave, es de conocimiento público "Lo único que debe permanecer oculto es la clave".

## 5. Uso de la IA
No se ha utilizado la IA.

### 6. Flag:
flag{Kerckhoffs}

---
7. Verificación
Lo verificaremos debido a que al pasar el código por distintos decodificadores y la terminal y todos dan el mismo resultado.

---
