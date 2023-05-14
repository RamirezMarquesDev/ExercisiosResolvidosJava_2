# Atividade Lógica de Programação Java
-----
##### *Ramirez Marques*
----
##### Parte 2: for


**01 - Ler um número inteiro N, daí mostrar na tela a tabuada de N para 1 a 10,
conforme exemplo.**
```
import java.util.Scanner;
public class For_1 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Informe qual tabuada deseja saber: ");
		int n = sc.nextInt();
		for (int i = 1; i <=10; i++) {
			int prod = n*i;
			System.out.printf("%d x %d = %d%n", n, i, prod);
		}
		sc.close();
	}
}
```
**02 - Leia 2 valores inteiros X e Y (em qualquer ordem). A seguir, calcule e mostre
a soma dos números impares entre eles.**
```
import java.util.Scanner;
public class For_2 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite 2 Numeros Inteiros: ");
		int x = sc.nextInt();
		int y = sc.nextInt();
		if (x > y) {
			int aux = x;
			x = y;
			y = aux;
		}
		int soma = 0;
		for (int i = x + 1; i < y; i++) {			
			if (i % 2 != 0) {
				soma += i;
			}
			System.out.println("Soma = "+ soma);	
		}		
		sc.close();
	}
}
```
**03 - Leia um valor inteiro X. Em seguida mostre os ímpares de 1 até X, um valor
por linha, inclusive o X, se for o caso.**
```
import java.util.Scanner;
public class For_3 {
	public static void main(String[] args) {		
		Scanner sc = new Scanner(System.in);
		System.out.println("Digite o Valor de x: ");
		int x = sc.nextInt();
		for (int i = 1; i <= x; i+=2) {
			if (i % 2 != 0) {
				System.out.println(i);
			}
		}
		sc.close();
	}
}
```
**04 - Leia um valor inteiro N. Este valor será a quantidade de valores inteiros X que
serão lidos em seguida. Mostre quantos destes valores X estão dentro do intervalo
[10,20] e quantos estão fora do intervalo.**
```
import java.util.Scanner;
public class For_4 {
	public static void main(String[] args) {		
		Scanner sc = new Scanner(System.in);
		System.out.println("Quantos números você vai giditar? ");
		int n = sc.nextInt();
		int dentro = 0;
		int fora = 0;
		for (int i = 1; i <= n; i++){
			System.out.println("Digite um Número: ");
			int x = sc.nextInt();
			if (x >=10 && x <= 20){
				dentro++;
		} else {
					 fora++;	
		} 	 	
		}
		System.out.println("Dentro :"+dentro);
		System.out.println("Fora :"+fora);
		sc.close();
	}
}
```
**05 - Leia um valor inteiro N. Este valor será a quantidade de números inteiros que
serão lidos em seguida. Para cada valor lido, mostre uma mensagem dizendo se
este valor lido é PAR ou IMPAR, e também se é POSITIVO ou NEGATIVO. No caso
de o valor ser igual a zero (0), seu programa deverá imprimir apenas NULO.**
```
import java.util.Scanner;
public class For_5 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Quantos numeros voce vai digitar? ");
		int n = sc.nextInt();
		for (int i = 0; i < n; i++) {
			System.out.println("Digite um Numero: ");
			int x = sc.nextInt();
			if (x % 2 != 0 && x < 0) {
				System.out.println("IMPAR NEGATIVO");				
			}else if (x % 2 == 0 && x < 0) {
				System.out.println("PAR NEGATIVO");
			}else if (x % 2 != 0 && x > 0) {
				System.out.println("IMPAR POSITIVO");
			}else if (x % 2 == 0 && x > 0) {
				System.out.println("PAR POSITIVO");
			}else {
				System.out.println("NULO");
			}
		}
		sc.close();
	}
}
```
**06 - Leia um valor inteiro N, que representa o número de casos de teste que vem a
seguir. Cada caso de teste consiste de 3 valores reais, para os quais você deverá
calcular e mostrar a média ponderada, sendo que o primeiro valor tem peso 2, o
segundo valor tem peso 3 e o terceiro valor tem peso 5. Vale lembrar que a média
ponderada é a soma de todos os valores multiplicados pelo seu respectivo peso,
dividida pela soma dos pesos.**
```
import java.util.Scanner;
public class For_6 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Quantos Casos voce vai digitar? ");
		int n = sc.nextInt();
		for (int i = 0; i < n; i++){
			System.out.println("Digite os tres Números: ");
			double a = sc.nextDouble();
			double b = sc.nextDouble();
			double c = sc.nextDouble();
			double media = (2 * a + 3 * b + 5 * c)/10;
			System.out.printf("MÉDIA = %.1f\n", media);
		}		
		sc.close();
	}
}
```
**07 - Escreva um algoritmo que leia dois números e imprima o resultado da divisão
do primeiro pelo segundo. Caso não for possível, mostre a mensagem “DIVISAO
IMPOSSIVEL”.**
```
import java.util.Scanner;
public class For_7 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Quantos Casos voce vai digitar? ");
		int n = sc.nextInt();
		for (int i = 0; i < n; i++) {
			System.out.println("Entre com o Numerador: ");
			int num = sc.nextInt();
			System.out.println("Entre com o Denominador: ");
			int den = sc.nextInt();
			if (num == 0 && den == 0){
				System.out.println("DIVISÃO IMPOSSÍVEL");
			}else if (den == 0) {
				System.out.println("DIVISÃO IMPOSSÍVEL");
			}else {
				double di = (double) num/den;
				System.out.println("Divisão = " + di);
			}			
		}				
		sc.close();
	}
}
```
**08 - Fazer um programa para ler um número natural N (valor máximo: 15), e depois
calcular e mostrar o fatorial de N.**
```
import java.util.Scanner;
public class For_8 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		int fat = 1;
		System.out.println("Digite o Valor de N: ");
		int n = sc.nextInt();
		if (n < 0 || n > 15) {
			System.out.println("Número inválido");
		}else {
			for (int i = n; i >= 1;i--) {
				fat = fat * i;				
			}System.out.println("O fatorial de é " + fat);
		}		
		sc.close();
	}
}
```
**09 - Maria acabou de iniciar seu curso de graduação na faculdade de medicina e
precisa de sua ajuda para organizar os experimentos de um laboratório o qual ela é
responsável. Ela quer saber no final do ano, quantas cobaias foram utilizadas no
laboratório e o percentual de cada tipo de cobaia utilizada. Este laboratório em
especial utiliza três tipos de cobaias: sapos, ratos e coelhos. Para obter estas
informações, ela sabe exatamente o número de experimentos que foram realizados,
o tipo de cobaia utilizada e a quantidade de cobaias utilizadas em cada experimento.
Faça um programa que leia um valor inteiro N que indica os vários casos de teste
que vem a seguir. Cada caso de teste contém um inteiro que representa a
quantidade de cobaias utilizadas e uma letra ('C', 'R' ou 'S'), indicando o tipo de
cobaia (R: Rato S: Sapo C: Coelho). Apresente o total de cobaias utilizadas, o total
de cada tipo de cobaia utilizada e o percentual de cada uma em relação ao total de
cobaias utilizadas, sendo que o percentual deve ser apresentado com dois dígitos
após o ponto.**
```
import java.util.Scanner;

public class For_9 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("Quantos casos de teste serao Digitados?");
		int n = sc.nextInt();
		int totalCobaias = 0;
		int totalRatos = 0;
		int totalSapos = 0;
		int totalCoelhos = 0;
		for (int i = 0; i < n; i++) {
			System.out.println("Quantidade de cobaias? ");
			int qtdCobaias = sc.nextInt();
			System.out.println("Tipo de Cobaias? ");
			char tipoCobaia = sc.next().charAt(0);
			totalCobaias += qtdCobaias;
			switch (tipoCobaia) {
			case 'R':
				totalRatos += qtdCobaias;
				break;
			case 'S':
				totalSapos += qtdCobaias;
				break;
			case 'C':
				totalCoelhos += qtdCobaias;
				break;
			}
		}
		System.out.println("Total: " + totalCobaias + " cobaias");
		System.out.println("Total de ratos: " + totalRatos);
		System.out.println("Total de sapos: " + totalSapos);
		System.out.println("Total de coelhos: " + totalCoelhos);
		System.out.printf("Percentual de ratos: %.2f %%\n", (double) totalRatos / totalCobaias * 100);
		sc.close();
	}
}
```
# Fim da Lista!








