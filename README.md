# Matriz5x5

Programa em C que gera uma Matriz5x5 e realiza o cálculo das somas dos valores das linhas e o total das linhas somadas.
```
#include<stdio.h>
#include<stdlib.h>
#include<time.h>

//global
int matriz[5][5];
int linha, coluna;
int soma = 0;
int somaLinhas[5];
void *geraMatriz(){ // Funcao Matriz 5x5
	srand(time(NULL)); // gerador de numeros aleatorios
	for(linha=0; linha<5; linha++){
		for(coluna=0;coluna<5;coluna++){
			matriz[linha][coluna]=rand()%100; //aloca os numeros aleatorios
			soma += matriz[linha][coluna]; //soma do total
			somaLinhas[linha] += matriz[linha][coluna]; //soma de cada linha
			printf("%d\t",matriz[linha][coluna]);
		}
		printf("\n");
	}
}
void *somatorio(){
	for (int linha = 0; linha < 5; linha++){
		printf("\nA soma da linha %d = %d", linha+1, somaLinhas[linha]);
	}
	printf("\nA soma total = %d", soma);
}
int main() {
	printf("\n\t MATRIZ 5X5\n\n");
	geraMatriz();
	somatorio();
}
```
