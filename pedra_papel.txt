#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
  int numeroAleatorio = rand()%3+1;

    int jogador, pc;
    printf ("--- Pedra, Papel, Tesoura ---\n");
    printf ("1. Pedra\n");
    printf ("2. Papel\n");
    printf ("3. Tesoura\n");
    scanf ("%d", &jogador);

  
    srand(time(NULL));

    pc = numeroAleatorio; //gera um numero aleatorio
    switch(pc)
    {
        case 1:
         printf ("Computador jogou Pedra\n");
        switch (jogador){
          case 1: 
          printf("Jogador jogou Pedra\n");
          printf("Teve um empate\n");
          break;
          case 2:
          printf("Jogador jogou Papel\n");
          printf("Jogador ganhou: Papel embrulha Pedra\n");
          break;
          case 3:
          printf("Jogador jogou Tesoura \n");
          printf("Computador ganhou: Tesoura quebra Pedra \n");
          break;
          default: 
        printf("Jogador, digite um número válido");
        }
        break;
        case 2: printf ("Computador jogou Papel\n"); 
        switch (jogador){
        case 1: 
          printf("Jogador jogou Pedra\n");
          printf("Computador ganhou: Papel embrulha Pedra\n");
          break;
          case 2:
          printf("Jogador jogou Papel\n");
          printf("Ocorreu empate \n");
          break;
          case 3:
          printf("Jogador jogou Tesoura \n");
          printf("Jogador ganhou: Tesoura corta Papel \n");
          break;
          default: 
          printf("Jogador, digite um número válido");
        }
        break;
        case 3: 
        printf ("Computador jogou Tesoura\n");
        switch (jogador){
      case 1: 
          printf("Jogador jogou Pedra\n");
          printf("Jogador ganhou: Pedra quebra Tesoura\n");
          break;
          case 2:
          printf("Jogador jogou Papel\n");
          printf("Computador ganhou: : Tesoura corta Papel \n");
          break;
          case 3:
          printf("Jogador jogou Tesoura \n");
          printf("Ocorreu empate \n");
          break;
           default: 
        printf("Jogador, digite um número válido");
        }
        break;
    }
        return 0;
}
