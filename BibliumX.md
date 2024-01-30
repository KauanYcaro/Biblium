# PROJETO BIBLIUM
<span align="center">
<img src="https://github.com/KauanYcaro/Biblium/assets/132211801/d0b2a876-ce63-47e2-84f5-ddd97e5ccfdf" alt="logo" width="300">
</span>

#
### Gerencie sua loja , biblioteca e demais estruturas com essa simples , porém diversa , ferramenta de controle de inventário

# Tópicos
#
- <a href="#Autores">Autores</a> 
- <a href="#Principais Funções">Principais Funções</a>
- <a href="#Principais Janelas">Principais Janelas</a>
- <a href="#Ferramentas utilizadas">Ferramentas utilizadas</a>
- <a href="#Como executar">Como executar</a>
- <a href="#Codigo Aplicado">Codigo Aplicado</a>
#
#
## Autores
#
#
<img src="https://github.com/KauanYcaro/Biblium/assets/132211801/fbda170b-c9ab-40d5-916b-6bef6d9cc1a2" alt="Ycaro" width="70"/><img src="https://github.com/KauanYcaro/Biblium/assets/132211801/41313600-32b9-48cd-a020-8a2b0f6ddceb" alt="David" width="70"/><img src="https://github.com/KauanYcaro/Biblium/assets/132211801/35b79cba-b22c-4916-8c57-598202398fc8" alt="Fabricio" width="70"/><img src="https://github.com/KauanYcaro/Biblium/assets/132211801/35b79cba-b22c-4916-8c57-598202398fc8" alt="Riquelme" width="70"/>



#
#
## Principais Funções
- Adicionar livros à cesta virtual
- Alteração de preço
- Retornar preço equivalente a quantidade de produtos adicionados

#
#
 
## Principais Janelas 

- [x] Inicialização do sistema

![](https://github.com/KauanYcaro/Biblium/assets/132211801/792b3d53-0a19-40ec-b95e-173e22bd63ad)
![](https://github.com/KauanYcaro/Biblium/assets/132211801/22c27122-954d-42a6-a951-8b06c5f62b59))

#
- [x] # Alternativas #

![](https://github.com/KauanYcaro/Biblium/assets/132211801/de380eee-525e-4bb2-b342-e2494822a0b4))
#

- [x] Manutenção 

![](https://github.com/KauanYcaro/Biblium/assets/132211801/72711881-98f5-461d-b8d0-d6fa8259eefd)
![](https://github.com/KauanYcaro/Biblium/assets/132211801/5679b794-4c50-402f-8b1c-7b047d6ac7ef)
#
#

- [x] Cesta virtual

![](https://github.com/KauanYcaro/Biblium/assets/132211801/0504f81b-f3ba-47a7-891c-fedb69bf46a7)
#
#

# Ferramentas utilizadas
1.  [CodeBlocks](https://www.codeblocks.org/#google_vignette)
2. [MinGW](https://sourceforge.net/projects/mingw-w64/)
#
#


# Codigo aplicado
#


``` c
#include <stdio.h>
#include "gconio.h"
#include <windows.h>
#include <time.h>
int main(){
//--------------------------------------------------------------------------------------------------------------
int MAX_COLUNAS=90;//verificar o total de colunas na sua tela
int MAX_LINHAS=25;//verificar o total de linhas na sua tela
int COR_FUNDO=LIGHTBLUE;
int COR_LETRA=WHITE;
int ALTERNATIVA;
int SENHA_administrador;
double Aladim_PRECO = 30;
double Pequeno_principe_PRECO = 20;
double Percy_jackson_PRECO = 10;
double Aladim_Quantidade;
double Pequeno_principe_Quantidade;
double Percy_jackson_Quantidade;
double resultados_das_vendas_Aladim;
double resultados_das_vendas_Pequeno_principe;
double resultados_das_vendas_Percy_jackson;
double resultados_Total;
textbackground(COR_FUNDO);
textcolor(COR_LETRA);
for(int linha=0;linha<MAX_LINHAS;linha++){
for(int coluna=0; coluna<MAX_COLUNAS;coluna++)
printf(" ");
printf("\n");
}
gotoxy(0,0);
printf("%c",201);
for(int coluna=1;coluna<MAX_COLUNAS-1;coluna++)
printf("%c",205);
printf("%c\n",187);
for(int linha=1;linha<MAX_LINHAS-1;linha++){
gotoxy(0,linha);printf("%c",186);
gotoxy(MAX_COLUNAS-1,linha);printf("%c",186);
}
printf("\n%c",200);
for(int coluna=1;coluna<MAX_COLUNAS-1;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(1, 7);printf(" _____ ");
gotoxy(1, 8);printf("/ ____| _____ ____ _____ _ _ ____ ___ _ ____ ___ ____
");
gotoxy(1, 9);printf("| | __ | ____|| _ \\ | ____| | \\ | | / ___| |_ _| / \\ | _ \\ / _ \\| _ \\ ");
gotoxy(1, 10);printf("| | |_ | | _| | |_) | | _| | \\| | | | | | / _ \\ | | || || ||| |_) | ");
gotoxy(1, 11);printf("| |__| | | |__ | _ < | |__ | |\ \\ | | |___ | | / ___ \\ | |_|| ||_||| _ < ");
gotoxy(1, 12);printf("|\______| |_____||_|\_\\_\\ |_____| |_| \\_| \\_____||___|/_/ \\_\\|____/
\\___/|_| \\_\\ ");
//-------------------------------------------------------------------------------------------------------------------------
--------
for (int coluna=35; coluna>=1; coluna--){
gotoxy(1,14);
printf(" ");
gotoxy(coluna,14);textbackground(WHITE);textcolor(BLUE);
printf("Monitore os seus Produtos com seguranca ");
printf(" {C} ");
Sleep(20);
textbackground(LIGHTBLUE);textcolor(WHITE);
}
gotoxy(12,15);printf("CARREGANDO ");textbackground(BLACK);printf(" ");
gotoxy(23,15);textbackground(GREEN);
for(int contador=1;contador<=5;contador++){
Sleep(1000);
printf(" ");
}
//-------------------------------------------------------------------------------------------------------------------------
--------
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("ESCOLHA UMA ALTERNATIVA: ");
gotoxy(13,18);printf("(1): Manutencao:");
gotoxy(13,19);printf("(2): Executar o sistema:");
gotoxy(13,21);printf("->");
scanf("%d",&ALTERNATIVA);
//Sleep(10000);
//-------------------------------------------------------------------------------------------------------------------------
--------
if (ALTERNATIVA==1) {
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("Executar como administrador");
gotoxy(13,17);printf("===========================");
gotoxy(13,19);printf("Senha:");
scanf("%d",&SENHA_administrador);
if (SENHA_administrador==123) {
double COD;
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf(" Alterar os precos dos livro |");
gotoxy(13,17);printf(" v ");
gotoxy(13,18);printf(" -> Aladim: COD(101)");
gotoxy(13,19);printf(" -> Pequeno principe: COD(110)");
gotoxy(13,20);printf(" -> Percy jackson: COD(100) ");
gotoxy(13,22);printf("Inserir codigo para alteracao: ");
scanf("%lf", &COD);
if (COD == 101) {
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("-> Aladim: COD(101)");
gotoxy(13,18);printf("-> valor antigo R$:R$%.2f\n",Aladim_PRECO);
gotoxy(13,20);printf("""-> Nova valor: ");
scanf("%lf", &Aladim_PRECO);
}
if (COD == 110) {
double Pequeno_principe_PRECO = 20;
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("-> Pequeno principe: COD(110)");
gotoxy(13,18);printf("-> valor antigo
R$:R$%.2f\n",Pequeno_principe_PRECO);
gotoxy(13,20);printf("""-> Nova valor: ");
scanf("%lf", &Pequeno_principe_PRECO);
}
if (COD == 100) {
textcolor(BLACK);
gotoxy(12,15);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=50;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(50,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<50;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("-> Percy jackson: COD(110)");
gotoxy(13,18);printf("-> valor antigo
R$:R$%.2f\n",Percy_jackson_PRECO);
gotoxy(13,20);printf("-> Nova valor: ");
scanf("%lf", &Percy_jackson_PRECO);
}
}
}
if (ALTERNATIVA==2) {
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,20);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=58;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(58,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",188);
for (int coluna=22; coluna>=14; coluna--){ //Parte 1
gotoxy(13,16);
printf(" ");
gotoxy(coluna,16);textbackground(WHITE);textcolor(BLUE);
printf(" __...--~~~-.__ _ _.-~~~--...__ ");
Sleep(10);
}
for (int coluna=15; coluna>=15; coluna--){ //Parte 2
gotoxy(13,17);
printf(" ");
gotoxy(coluna,17);textbackground(WHITE);textcolor(BLUE);
printf(" // \\\ // \\\\ ");
Sleep(10);
}
for (int coluna=22; coluna>=14; coluna--){ //Parte 3
gotoxy(13,18);
printf(" ");
gotoxy(coluna,18);textbackground(WHITE);textcolor(BLUE);
printf(" // \\\ // \\\\ ");
Sleep(10);
}
for (int coluna= 22; coluna>=14; coluna--){ //Parte 4
gotoxy(13,19);
printf(" ");
gotoxy(coluna,19);textbackground(WHITE);textcolor(BLUE);
printf(" //__...--~~~-.\\\ // __.-~~~~~~~\\\\ ");
Sleep(10);
}
for (int coluna=22; coluna>=14; coluna--){ //Parte 5
gotoxy(13,20);
printf(" ");
gotoxy(coluna,20);textbackground(WHITE);textcolor(BLUE);
printf(" //__...---~~~._\\_// ~~~~----..\\\\ ");
Sleep(10);
}
for (int coluna=22; coluna>=14; coluna--){ //Parte 6
gotoxy(13,21);
printf(" ");
gotoxy(coluna,21);textbackground(WHITE);textcolor(BLUE);
printf(" ================|_|=============== ");
Sleep(10);
}
for (int coluna=22; coluna>=14; coluna--){ //Parte 7
gotoxy(13,22);
printf(" ");
gotoxy(coluna,22);textbackground(WHITE);textcolor(BLUE);
printf(" ------------ Bem vindo ---------- ");
Sleep(10);
}
system("pause>NULL");//pausa até que uma tecla seja digitada
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,20);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=58;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(58,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",188);
}
gotoxy(13,16);printf("Insira a quantidade desejada para compra.\n");
gotoxy(13,17);printf("-> Aladim: valor:%.2f\n",Aladim_PRECO);
gotoxy(13,18);printf("Quant-> ");
scanf("%lf", &Aladim_Quantidade);
gotoxy(13,19);printf("-=-=-=-=-=-==-=-=-=-=-=-=-=-=-=\n");
gotoxy(13,20);printf("-> Pequeno principe::
valor:%.2f\n",Pequeno_principe_PRECO);
gotoxy(13,21);printf("Quant-> ");
scanf("%lf", &Pequeno_principe_Quantidade);
textbackground(WHITE);
textcolor(BLACK);
gotoxy(12,20);
for(int linha=15;linha<MAX_LINHAS;linha++){
for(int coluna=12; coluna<=58;coluna++)
printf(" ");
gotoxy(12,linha);
}
gotoxy(12,15);
printf("%c",201);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",187);
for(int linha=16;linha<MAX_LINHAS-1;linha++){
gotoxy(12,linha);printf("%c",186);
gotoxy(58,linha);printf("%c",186);
}
gotoxy(12,23);
printf("%c",200);
for(int coluna=13;coluna<58;coluna++)
printf("%c",205);
printf("%c",188);
gotoxy(13,16);printf("Insira a quantidade desejada para compra.\n");
gotoxy(13,17);printf("-> Percy jackson:
valor:%.2f\n",Percy_jackson_PRECO);
gotoxy(13,18);printf("Quant-> ");
scanf("%lf", &Percy_jackson_Quantidade);
if (Aladim_Quantidade >= 1) {
resultados_das_vendas_Aladim = (Aladim_Quantidade *
Aladim_PRECO);
}
if (Pequeno_principe_Quantidade >= 1){
resultados_das_vendas_Pequeno_principe = (
Pequeno_principe_Quantidade * Pequeno_principe_PRECO);
}
if (Percy_jackson_Quantidade >= 1){
resultados_das_vendas_Percy_jackson = ( Percy_jackson_Quantidade
* Percy_jackson_PRECO);
}
resultados_Total = (resultados_das_vendas_Aladim +
resultados_das_vendas_Pequeno_principe + resultados_das_vendas_Percy_jackson);
gotoxy(13,20);printf("-> Total a Pagar: valor:%.2f\n",resultados_Total);
Sleep(100000);
return 0;
}

```

