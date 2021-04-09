/ calculo /
*//Uma loja necessita de um programa que facilite o cálculo de venda de seus produtos.  As áreas dos produtos são definidas como: 
1) Informática  
2) Jogos
3) Eletrônicos  Os produtos de Informática têm 5% de desconto na compra, os jogos têm 8% e os produtos eletrônicos, 10%. 
*//

#include <stdio.h> //Biblioteca

int main(void)
 {

//Variáveis

   char prod [30], continuar ='s';

   float valor, classe, qtd , total, desc, valor_total;

//Comeco do programa


while( continuar != 'n')
{

//Classificação
   printf( "Classificacao \n [1] - Informatica \n [2] - Jogos \n [3] - Eletronicos \n Insira o codigo correspondente ao tipo de opcao:  ");

   scanf("%f", &classe);


   printf("Insira o nome do produto: ");

   scanf("%s", &prod);


   printf("Insira o valor do produto: ");

   scanf("%f", &valor);


   printf("Insira a quantidade de unidades a serem compradas: ");

   scanf("%f", &qtd);

//Opções:
   if (classe == 1)
    {

   valor_total=valor * qtd;

   desc=valor*0.5;

   total=valor_total- desc;


   printf("O valor do(s) seu(s) produto(s) com desconto é de: %.2f", total);

   }else

   if(classe==2){

    valor_total=valor * qtd;

   desc=valor *0.8;

   total=valor_total- desc;


   printf("O valor do(s) seu(s) produto(s) com desconto é de: %.2f", total);

   }else

   if(classe==3){

   valor_total= valor * qtd;

   desc=valor *0.1;

   total=valor_total- desc;

   printf("O valor do(s) seu(s) produto(s) com desconto é de: %.2f", total);

   }

//Detalhes
   printf("\nO nome do produto: %s",prod);
   printf("\nA quantidade do produto foi de: %.0f ", qtd);
   printf("\nO valor unitário do produto foi de: %.2f", valor);
   printf("\nO valor base do produto foi de: %.2f", valor_total);
   printf("\nO valor do desconto foi de : %.2f", desc);

//opcao para continuar ou não:
  printf("\nDeseja continuar, informe s para sim ou n para abandonar o programa: ");
            scanf("%s",&continuar);

return 0; //fim da aplicação

 }
 }
