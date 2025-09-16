# 🚌 Ordenação com Bubble Sort em C 

Este projeto tem como objetivo ordenar 10 tempos de chegada de ônibus em ordem crescente e decrescente utilizando o algoritmo Bubble Sort.

## 📌 Descrição

O programa:

Recebe 10 tempos de chegada de ônibus (em minutos ou outro formato definido).

Aplica o algoritmo Bubble Sort para organizar os valores:

Ordem crescente (do menor para o maior tempo).

Ordem decrescente (do maior para o menor tempo).

Exibe os resultados de forma clara para o usuário.

## ⚙️ Tecnologias Utilizadas

Linguagem: C (pode adaptar caso use outra linguagem).

IDE recomendada: Visual Studio Code ou qualquer compilador de C.

# 💻 Código em C

```c
#include <stdio.h>

void crescente(int v[], int tamanho) {
    int i, j, aux;
    for(i = 0; i < tamanho - 1; i++) {
        for(j = 0; j < tamanho - 1 - i; j++) {
            if(v[j] > v[j+1]) {
                aux = v[j];
                v[j] = v[j+1];
                v[j+1] = aux;
            }
        }
    }
}

void decrescente(int v[], int tamanho) {
    int i, j, aux;
    for(i = 0; i < tamanho - 1; i++) {
        for(j = 0; j < tamanho - 1 - i; j++) {
            if(v[j] < v[j+1]) {
                aux = v[j];
                v[j] = v[j+1];
                v[j+1] = aux;
            }
        }
    }
}

int main() {
    int vet[10];
    int i;

    printf("Digite 10 tempos de chegada de onibus (em minutos):\n");
    for(i = 0; i < 10; i++) {
        scanf("%d", &vet[i]);
    }

    printf("Tempos de chegada digitados:\n");
    for (i = 0; i < 10; i++) {
        printf("%d ", vet[i]);
    }
    printf("\n");

    crescente(vet, 10);
    printf("Tempos em ordem crescente:\n");
    for (i = 0; i < 10; i++) {
        printf("%d ", vet[i]);
    }
    printf("\n");

    decrescente(vet, 10);
    printf("Tempos em ordem decrescente:\n");
    for (i = 0; i < 10; i++) {
        printf("%d ", vet[i]);
    }
    printf("\n");

    return 0;
}
```

## Exemplo de Saida:

```bash
Digite 10 tempos de chegada de onibus (em minutos):
15 8 23 5 42 19 3 30 12 27

Tempos de chegada digitados:
15 8 23 5 42 19 3 30 12 27

Tempos em ordem crescente:
3 5 8 12 15 19 23 27 30 42

Tempos em ordem decrescente:
42 30 27 23 19 15 12 8 5 3
```

