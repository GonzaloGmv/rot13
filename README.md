# rot13

El link al repositorio es el siguiente: [github](https://github.com/GonzaloGmv/rot13)

Los participantes somos:
* Alexandre Muñoz
* Miguel González
* Gonzalo Martínez

Para este reto teníamos que descifrar un mensaje utilizando ROT13. Para ello hemos hecho un código en python.

Esta es la solución que nos ha dado nuestro programa:

![image](https://github.com/GonzaloGmv/rot13/assets/91721237/996c5445-5051-46e9-8b29-f397ed5914c5)

El código utilizado es el siguiente:
```
def rot13(texto):
    resultado = ''
    for caracter in texto:
        # Si el caracter es una letra del alfabeto, aplicamos el cifrado Rot13
        if 'a' <= caracter <= 'z':
            nueva_letra = chr(((ord(caracter) - ord('a') + 13) % 26) + ord('a'))
        elif 'A' <= caracter <= 'Z':
            nueva_letra = chr(((ord(caracter) - ord('A') + 13) % 26) + ord('A'))
        else:
            # Si no es una letra del alfabeto, lo dejamos sin cambios
            nueva_letra = caracter
        resultado += nueva_letra
    return resultado

# Ejemplo de texto cifrado con Rot13
texto_cifrado = "Yn fvthvragr vasbeznpvba rf pbasvqrapvny. Gr nlhqnen n cebfrthve ra yn vairfgvtnpvba. Ab gr pbasvrf, ab gbqnf ynf vasbeznpvbarf qr ynf dhr qvfcbarzbf fba gna snpvyrf pbzb rfgn ebgnpvba qr pnenpgrerf. Sveznqb: ha nzvtb.synt{rfgnzbf_rzcrmnaqb_n_pbabpre_nytb_qr_uvfgbevn}"
# Desciframos el texto
texto_descifrado = rot13(texto_cifrado)
print("Texto descifrado:", texto_descifrado)
```
