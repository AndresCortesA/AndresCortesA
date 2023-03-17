### Hi there 👋

<h1 align="center"> Estudiante en desarrollo de software </h1>

Interesado en data analytics y backend en java, actualmente me encuentro estudiando y practicando spring, java avanzado, MySQL, Go (golang).

## Lenguajes en desarrollo y conocimiento:

<img src ="https://user-images.githubusercontent.com/101019474/212137074-908d9360-73e9-4f55-bc7d-b9316d791266.png" width="1000" height="300" />

### JAVA
``` Java




public class Main {

    public static boolean existePalindromo(String oracion) {
        // Eliminar espacios y convertir a minúsculas
        String sinEspacios = oracion.replaceAll("\\s", "").toLowerCase();
        // Separar en palabras
        String[] palabras = sinEspacios.split("\\s+");
        // Iterar por cada palabra y verificar si es un palíndromo
        for (String palabra : palabras) {
            String reverso = new StringBuilder(palabra).reverse().toString();
            if (palabra.equals(reverso)) {
                return true;
            }
        }
        // Si no se encontró palíndromo, devolver false
        return false;
    }


    public static long f_sum(long n){
        long suma = 0;
        for (long i = -40; i <= 2*n; i++){
            for (long j = 40; j <= n*n; j++){
                suma += 2*i*j + 8*j;
            }
        }
        return suma;
    }

    public static long sol_sum(long n){
        long x = (n*n*(n*n+1)/2 - 780);
        long  parte1 = -40*41+2*n*(2*n + 1);
        long  parte2 = 8*(2*n + 41);
        return x *(parte1 + parte2);
    }



    public static void main(String[] args) {

        long[] arreglo = {10,20,40,60,80,100};

        String oracion = "Dabale arroz a la zorra el abad";

        String largoPalindromo = "";
        int sizePalindromo = 0;

        for (int i = 0; i < oracion.length(); i++){
            for(int j = i+1; j <= oracion.length(); j++ ){
                String subcadena = oracion.substring(i,j);
                boolean palindromo = existePalindromo(subcadena);
                if (palindromo && subcadena.length() > sizePalindromo){
                    largoPalindromo = subcadena;
                    sizePalindromo = subcadena.length();
                }
            }
        }
        System.out.println(largoPalindromo);

        System.out.println("************************************************* sumatoria");

        for(long valor:arreglo){
            System.out.println(valor+" "+f_sum(valor)+" "+sol_sum(valor));
        }

    }
}
``` 
### Golang
```Go
package main

import (
	"fmt"
	"strings"
)

/*
Quiero crear un programa que me detecte un palindromo, por lo que se
entonces:
Debo primero detectar la cadena de strings y recorrerla "I like 'racecar' that very fast"
ahí esta el palidromo, lo que deseo es obtener esa cadena como salida ya es la respuesta
entonces lo que debo omitir por ahora, es mayusculas y espacios
*/

//primero definamos una funcion que me ayude a leer una cadena y me indique si es un palindromo

func esPalindromo(s string) bool {
	//creo un for que me ayude a leer una cadena hasta la mitad y me indique si la otra mitad es igual
	for i := 0; i < len(s)/2; /*este me lee hasta la mitad*/ i++ {
		//entonces le defino que me lea la otra mitad de la cadena y me indique si no es igual
		if s[i] != s[len(s)-i-1 /*este me lee la otra mitad faltante*/] {
			return false
		}
	}

	return true
}

func main() {
	// entradaS := "racecar"
	entradaS := "I like racecar that very fast"
	entradaS = strings.ToLower(entradaS)
	//el -1 indica que los " " espaciados son eliminados
	entradaS = strings.Replace(entradaS, " ", "", -1)

	// fmt.Println(esPalindromo(entradaS))
	//ahora necesitamos almacenar el palindromo más largo

	largoPalindromo := ""
	sizePalindromo := 0

	for i := 0; i < len(entradaS); i++ {
		for j := i + 1; j <= len(entradaS); j++ {
			subcadenas := entradaS[i:j]
			/* lo que devuelve esta subcadena es lo siguite
			supongamos que recibe la palabra "hello"
			"h"
			"he"
			"hel"
			"hell"
			"hello"
			"e"
			"el"
			"ell"
			"ello"
			"l"
			"ll"
			"llo"
			"l"
			"lo"
			"o"
			esto es lo que devuelve por cada iteracion hasta recorrer la cadena
			para ser más claro supongamos que el i := 2 es dos empieza en "l" y termina en "llo"
			y asi sucesivamente para la cadena
			*/

			//hora vamos a definir el tamaño del palindromo y que realmente sea un palindromo

			if esPalindromo(subcadenas) && len(subcadenas) > sizePalindromo {
				largoPalindromo = subcadenas
				sizePalindromo = len(subcadenas)
			}
		}
	}

	fmt.Println(largoPalindromo)
}
```
[![AndresCortesA's GitHub stats](https://github-readme-stats.vercel.app/api?username=AndresCortesA)](https://github.com/AndresCortesA/github-readme-stats)

### Donde puedes encontrarme:


<a href="https://www.linkedin.com/in/andres-arias-792364229/" target="_blank">
<img src= https://user-images.githubusercontent.com/101019474/211182183-c9afd5c2-6c64-495c-9ca9-a275ddcbc7f3.png width= 150 height= 40 style="margin-bottom: 5px;" />
</a>
<a href="https://github.com/AndresCortesA" target="_blank">
<img src= https://user-images.githubusercontent.com/101019474/211182377-07f411bf-f0c9-40e4-b738-fae2a0ef366c.png width= 150 height= 40 style="margin-bottom: 5px;" />
</a>

<!--
**AndresCortesA/AndresCortesA** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
