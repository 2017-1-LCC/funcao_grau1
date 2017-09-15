# funcao_grau1
algoritmo que calcula os zeros de uma função do 1º grau. A função tem o formato f(x) = ax + b

/*******************FUNÇÃO**********************
Faça um algoritmo que calcula os zeros
de uma função do 1º grau. A função tem o
formato f(x) = ax + b.

Lógica = Simplificando a função ax+b=0
ax=-b
x=-b/a
Criei uma função com o retorno do resultado em Fx para poder chamar na função main()


Autor: Jefferson Medeiros da Silva
Curso: Licenciatura em Ciências da Computação
***********************************************/

#include <stdio.h>
#include<stdlib.h>
#include<locale.h>
float Zero_Funcao (float a, float b);// Quando a função é declarada depois da função principal (main), tem de apontar ela
//antes do main também.

int main(){
setlocale(LC_ALL, "");
    float A, B, Fx;

    printf("Informe o valor de 'a': ");
    scanf("%f", &A);

    printf("Informe o valor de 'b': ");
    scanf("%f", &B);

    if (A!=0){
    Fx = Zero_Funcao(A, B);

    printf("O valor de X que faz com Fx seja igual a zero é: %.2f", Fx);
    }
    else {
        printf("Para ser função afim, 'a' tem de ser diferente de 0");
    }
    return 0;
}

float Zero_Funcao (float a, float b){
    float Fx;

    Fx = -b/a; // Para ficar mais fácil, simplificou-se a função para ax+b=0 ==> x=-b/a

    return(Fx);
}

