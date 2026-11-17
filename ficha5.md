# Ficha 5 · Reto 5: otra huella distinta (SHA-1)
    Enunciado. La contraseña es HashingIsOneWay2026. Calcula su hash SHA-1 y envía flag{sha1}.

## 1. Tipo de reto.  
Hash

## 2. Concepto.  
**¿En qué se diferencia SHA-1 de MD5 en longitud de salida? ¿Se considera seguro SHA-1 hoy? ¿Por qué?**
SHA-1 genera una salida de 160 bits con una longitud de 40 caracteres, más larga que los 128 bits con 32 caracteres de MD5.  
No se considera seguro hoy en día para datos que requieran una seguridad avanzada. Esto se debe a que se encontraron algoritmos para generar colisiones de hashes; es decir, que dos archivos con contenidos distintos tengan el mismo exacto hash.


## 3. Procedimiento. Comando exacto y explicación de cada parte:
|Parte del comando|	Qué hace|
| --- | --- |
| echo | Imprimi texto |
| -n | Indica que no se agregue un salto de línea |
| "HashingIsOneway2026" | Es el texto o cadena de caracteres exacta que se va a procesar. |
| Sha1sum | Es la herramienta encargada de calcular el hash utilizando el algoritmo SHA-1 |

## 4. Por qué lo hacemos así.  
**¿Por qué el guion y los espacios de la salida no forman parte de la flag? Calculad también el MD5 de la misma contraseña y comparad las dos salidas.**
Los espacios son solo separadores y el guión informa que se ha leido desde la entrada estándar en lugar de un archivo.

**Comparación SHA-1/MD5**  
| Algoritmo |	Hash obtenido |	Nº de caracteres |	Bits |
| --- | --- | --- | --- |
| MD5	|	1374cfc99a0de192a72ea8f627304d52 | 32 | 128 |
| SHA-1	|	98666584dca50be8bfc35461f4eabe0e31b887ad | 40 | 160 |		

**Conclusión:**  
SHA-1 es más seguro ya que tiene más caracteres de longitud que MD5 (aunque ambos estan obsoletos).

## 5. Uso de la IA
| Pregunta que le hicimos |	Qué aprendimos	| ¿Se equivocó? ¿Cómo lo comprobamos? |
| --- | --- | --- |
| ¿Por que SHA-1 ya no es seguro? | Vulnerabilidades críticas en el diseño del algoritmo | No, lo contrastamos en internet |

## 6. Flag:  
flag{98666584dca50be8bfc35461f4eabe0e31b887ad}

## 7. Verificación  
Hemos verificado que las longitudes de los hashes coinciden con las investigadas. (32 en MD5 y 40 en SHA-1)

