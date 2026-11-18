# Ficha 7 · Reto 7: Base… ¿cuál? (Base32)
    Enunciado. Decodifica la cadena en Base32 MRSWMZLOONQV6ZLOL5YHE33GOVXGI2LEMFSA==== y envía flag{texto}.

## 1. Tipo de reto.
Codificación

## 2. Concepto. ¿En qué se diferencia Base32 de Base64? Comparad el alfabeto y el relleno con =.
|  | Base64 | Base32 |
| --- | --- | --- |
| **Caracteres que usa** | Alfabeto de 64: Mayúsculas, minúsculas, dígitos, "+" y "/" | Alfabeto de 32: Solo mayúsculas y dígitos 2-7 |
| **Relleno** | Hasta 2 | Hasta 6 |
| **¿Usa minúsculas?** | Sí | No |

## 3. Procedimiento. Comando exacto y explicación de cada parte
| Parte del comando	| Qué hace |
| --- | --- |
| echo -n "cadena de texto"| Toma la palabra que queremos decodificar|
| base32 -d | Sirve para decodificar |

## 4. Por qué lo hacemos así.
**¿Qué os hizo sospechar que no era Base64? ¿Qué pasa si intentáis decodificarla con base64 -d?**  
**Para investigar. El texto obtenido es un principio de seguridad. ¿Qué significa? Poned un ejemplo aplicado a un instituto.**  
 - Todas las letras eran mayúsculas y tenia más de 2 "=" de relleno.
 - Nos dará un archivo corrupto o datos sin sentido.
 - Principio de defensa en profundidad. Consiste en utilizar múltiples mecanismos de seguridad para proteger los activos de la organización. Ejemplo: Aparte de firewalls y filtros poner seguridad perimetral en los dispositivos.

## 5. Uso de la IA
| Pregunta que le hicimos	| Qué aprendimos	| ¿Se equivocó? ¿Cómo lo comprobamos? |
| ¿Como diferenciar Base32 de Base64? | Diferencias clave entre ambos métodos de codificación | No. Lo comprobamos comparando las dos cadenas de texto y viendo que todo se cumplía. |

## 6. Flag:  
flag{defensa_en_profundidad}

## 7. Verificación
No dio error y además se comprobó con distintos decodificadores en línea.

