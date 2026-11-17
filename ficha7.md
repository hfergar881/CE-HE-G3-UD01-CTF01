1. Tipo de reto: ☐ Hash ☐ Codificación ☐ Cifrado ☐ Combinado
Codificación
---
2. Concepto. ¿En qué se diferencia Base32 de Base64? Comparad el alfabeto y el relleno con =.
| |Base64|Base32|
|...|...|...|
|Caracteres que usa|64 caracteres|32 caracteres|
|Relleno| Es mas compacto| tiene mas relleno|
|¿Usa minúsculas?|Si usa | No usa |

---

3. Procedimiento. Comando exacto y explicación de cada parte:
| Parte del comando	|Qué hace|
|...|...|
|eco -n "cadena de texto |"| Toma la palabra que queremos decodificar|
| base32 -d | Sirve para decodificar |

---

4. Por qué lo hacemos así. ¿Qué os hizo sospechar que no era Base64? ¿Qué pasa si intentáis decodificarla con base64 -d?

Para investigar. El texto obtenido es un principio de seguridad. ¿Qué significa? Poned un ejemplo aplicado a un instituto.

 - Todo era en mayúsculas y tenia mas relleno.
 - Nos dará un archivo corrupto o datos sin sentido.
 - Principio de defensa en profundidad consiste en utilizar múltiples mecanismos de seguridad para proteger los activos de la organización. Ejemplo: Aparte de firewalls y filtros poner seguridad perimetral en los dispositivos.

---
5. Uso de la IA

Pregunta que le hicimos	Qué aprendimos	¿Se equivocó? ¿Cómo lo comprobamos?
¿Como diferencial la Base32 de la 64?
No se equivoco y lo comprobamos comparando las dos cadenas de texto.

---

6. Flag: flag{defensa_en_profundidad}

---

7. Verificación
No dio error y ademas se comprobo con distintos decodificadores en linea.

---
