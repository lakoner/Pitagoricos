#include <stdio.h>
#include <stdbool.h>
#include <stdlib.h>


void buscapareja1(int n, int *a, int *b);
void buscapareja2(int n, int a, int *b);
int pitagoricos (int h, int c1, int c2);

int pitagoricos (int h, int c1, int c2){
    return h*h==c1*c1+c2*c2;
}

void buscapareja2(int n, int a, int *b){
    bool encontrado;
    *b=1;
    encontrado=false;
    while (*b<n && !encontrado){
        encontrado=pitagoricos(n,a,*b);
        if (!encontrado==true){
            *b= *b+1;
        }
    }
}

void buscapareja1(int n, int *a, int *b){
    bool encontrado;
    *a=1;
    *b=1;
    encontrado=false;
    while (*a<n && !encontrado){
        buscapareja2 (n,*a,&*b);
        encontrado=pitagoricos(n,*a,*b);
        if (!encontrado==true){
            *a= *a+1;
        }
    }
}

int main (){
    int hipo, cmenor, cmayor;
    printf("Escribe un entero:");
    scanf ("%d", &hipo);
    while (hipo != 0) {
        buscapareja1(hipo, &cmenor, &cmayor);
        if (pitagoricos(hipo, cmenor, cmayor)){
            printf("Hipotenusa:" "%d \n", hipo);
            printf("Cateto mayor: " "%d \n", cmayor);
            printf("Cateto menor: " "%d \n", cmenor);
        }
        printf("Escribe otro entero: ");
        scanf ("%d", &hipo);
    }
    return 0;
}



