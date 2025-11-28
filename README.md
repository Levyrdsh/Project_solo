#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <unistd.h>
#include <string.h>
#include <math.h>

int main() {
    setlocale(LC_ALL, "Portuguese");

    int menu = 1;
    int opcao;

    while (menu != 0) {
        system("clear");
        printf("\n");
        printf("++++++++++++++++++ CALCZILLA ++++++++++++++++++ \n");
        printf("Digite o código do calculo a ser executado: \n");

        printf("***********************************************\n");
        printf("\t01. Soma simples\n");
        printf("\t02. Produto simples\n");
        printf("\t03. Média I\n");
        printf("\t04. Média II\n");
        printf("\t05. Diferença\n");
        printf("\t06. Salário\n");
        printf("\t07. Salário com bônus\n");
        printf("\t08. Calculo simples\n");
        printf("\t09. Esfera\n");
        printf("\t10. Àrea\n");
        printf("\t11. O Maior\n");
        printf("\t12. Tempo de viagem\n");
        printf("\t13. Distancia entre dois pontos\n");
        printf("\t14. Distância\n");
        printf("\t15. Gasto de combustível\n");
        printf("\t16. Cédulas\n");
        printf("\t17. Conversão de tempo\n");
        printf("\t18. Equação do 1º grau\n");
        printf("\t19. Equação do 2º grau\n");
        printf("\t20. Calculo de IMC\n");
        printf("\t21. Conversor de temperatura\n");
        printf("\n");
        printf("\t0. Sair\n");
        printf("***********************************************\n");
        printf("Escolha uma opção: ");
        scanf("%d", &opcao);

        switch (opcao) {
            case 1:
                {
                system("clear");
                    printf("EXERCÍCIO 01\n");
                    int a, b, soma;
                    printf("Insira o 1º valor a ser somado: ");
                    scanf("%d", &a);
                    printf("Insira o 2º valor a ser somado: ");
                    scanf("%d", &b);
                    soma = a + b;
                    printf("\nSOMA = %d\n", soma);
                }
                break;
            case 2:
                {
                system("clear");
                    printf("EXERCÍCIO 02\n");
                    int a, b, prod;
                    printf("Insira o 1º valor: ");
                    scanf("%d", &a);
                    printf("Insira o 2º valor: ");
                    scanf("%d", &b);
                    prod = a * b;
                    printf("\nPROD = %d\n", prod);
                }
                break;
            case 3:
                {
                system("clear");
                    printf("EXERCÍCIO 03\n");
                    double a, b, soma, media;
                    do {
                        printf("Insira a 1ª nota: ");
                        scanf("%lf", &a);
                        printf("Insira a 2ª nota: ");
                        scanf("%lf", &b);
                        if (a < 0 || a > 10 || b < 0 || b > 10) {
                            printf("Notas inválidas! As notas devem estar entre 0 e 10.\n");
                        }
                    } while (a < 0 || a > 10 || b < 0 || b > 10);
                    
                    soma = a + b;
                    media = soma / 2;
                    printf("\nMÉDIA = %.5lf\n", media);
                }
                break;
            case 4:
                {
                system("clear");
                    printf("EXERCÍCIO 04\n");
                    double a, b, c, soma, media;
                    do {
                        printf("Insira a 1ª nota: ");
                        scanf("%lf", &a);
                        printf("Insira a 2ª nota: ");
                        scanf("%lf", &b);
                        printf("Insira a 3ª nota: ");
                        scanf("%lf", &c);
                        if (a < 0 || a > 10 || b < 0 || b > 10 || c < 0 || c > 10) {
                            printf("Notas inválidas! As notas devem estar entre 0 e 10.\n");
                        }
                    } while (a < 0 || a > 10 || b < 0 || b > 10 || c < 0 || c > 10);
                    
                    soma = (a * 2) + (b * 3) + (c * 5);
                    media = soma / 10;
                    printf("\nMÉDIA = %.1lf\n", media);
                }
                break;
            case 5:
                {
                system("clear");
                    printf("EXERCÍCIO 05\n");
                    printf("\n");
                    int a, b, c, d, total;
                    printf("Insira o 1º valor: ");
                    scanf("%d", &a);
                    printf("Insira o 2º valor: ");
                    scanf("%d", &b);
                    printf("Insira o 3º valor: ");
                    scanf("%d", &c);
                    printf("Insira o 4º valor: ");
                    scanf("%d", &d);
                    total = (a * b) - (c * d);
                    printf("DIFERENÇA = %d\n", total);
                }
                break;
            case 6:
                {
                system("clear");
                    printf("EXERCICIO 06\n");
                    printf("\n");
                    int num, h;
                    double valor_h, total;

                    printf("Insira o código do funcionário: ");
                    scanf("%d", &num);
                    printf("Insira as horas trabalhadas: ");
                    scanf("%d", &h);
                    printf("Insira o valor a receber por hora: (A casa decimal deve ser separada com ponto (.))");
                    scanf("%lf", &valor_h);

                    total = valor_h * h;

                    printf("NUMBER = %d", num);
                    printf("\n");
                    printf("SALARY = R$ %.2lf", total);
                }
                break;
            case 7:
                {
                system("clear");
                    printf("EXERCICIO 07\n");
                    printf("\n");
                    double salario, vendas, total, comissao;
                    char nome [20];

                    printf("Insira seu nome: ");
                    scanf("%s", nome);
                    printf("Insira o valor do salario: ");
                    scanf("%lf", &salario);
                    printf("Insira o valor do total das vendas: ");
                    scanf("%lf", &vendas);


                    comissao = vendas *0.15;
                    total = salario + comissao;

                    printf("TOTAL = R$ %.2lf", total);
                    printf("\n");
                }
                break;
            case 8:
                {
                system("clear");
                printf("EXERCICIO 08\n");
                printf("\n");

                int codigo1, codigo2, qtd1, qtd2;
                double valor1, valor2, soma1, soma2, total;

                printf("Sobre o 1º produto: \n");
                printf("Digite o código do produto, a quantidade e o valor nesta respectiva sequencia: \n");
                scanf("%d %d %lf", &codigo1, &qtd1, &valor1);

                printf("Sobre o 2º produto: \n");
                printf("Digite o código do produto, a quantidade e o valor nesta respectiva sequencia: \n");
                scanf("%d %d %lf", &codigo2, &qtd2, &valor2);

                soma1 = qtd1 * valor1;
                soma2 = qtd2 * valor2;
                total = soma1 + soma2;
                printf("VALOR A PAGAR: R$ %.2lf", total);
                printf("\n");
                }
                break;
            case 9:
                {
                system("clear");
                    printf("EXERCICIO 09\n");
                    printf("\n");
                    int raio;
                    double PI = 3.14159;
                    double volume;

                    printf("Insira o valor do RAIO: ");
                    scanf("%d", &raio);

                    volume = (4.0/3.0) * PI * (raio*raio*raio); // volume;

                    printf("VOLUME = %.3lf", volume);
                }
                break;
            case 10:
                {
                system("clear");
                printf("EXERCICIO 10\n");
                printf("\n");
                double a, b, c;
                double triangulo, circulo, trapezio, quadrado, retangulo;
                double PI = 3.14159;

                printf("Insira os respectivos valores de A, B e C. Conforme o exemplo abaixo:\nEx.: 3.0 4.0 5.2");
                printf("\n");
                scanf("%lf %lf %lf", &a, &b, &c);

                triangulo = (a * c) /2;
                circulo = PI * (c * c);
                trapezio = ((a + b) * c )/ 2;
                quadrado = b * b;
                retangulo = a * b;

                printf("TRIANGULO: %.3lf \n", triangulo);
                printf("CIRCULO: %.3lf \n", circulo);
                printf("TRAPEZIO: %.3lf \n", trapezio);
                printf("QUADRADO: %.3lf \n", quadrado);
                printf("RETANGULO: %.3lf \n", retangulo);
                }
                break;
            case 11:
                {
                system("clear");
                printf("EXERCICIO 11\n");
                printf("\n");
                int a, b, c, ab, abc;

                printf("Insira os valores de A, B e C: ");
                scanf("%d %d %d", &a, &b, &c);

                ab = (a + b + abs(a - b)) / 2;
                abc = (ab + c + abs(ab - c)) / 2;

                printf("%d eh o maior", abc);
                }
                break;
            case 12:
                {
                system("clear");
                printf("EXERCICIO 12\n");
                printf("\n");
                
                double km, velocidade, total;

                printf("Insira o valor do km a ser percorrido: ");
                scanf("%lf", &km);
                printf("Insira a velocidade média estabelecida: ");
                scanf("%lf", &velocidade);
                
                if(velocidade <=0){
                    printf("Velocidade inserida incorreta");
                }
                else{
                    total = km / velocidade;

                    printf("Tempo total de viagem: %.2lf horas", total);
                }
                }
                break;
            case 13:
                {
                system("clear");
                printf("EXERCICIO 13\n");
                printf("\n");


                }
                break;
            case 14:
                {
                system("clear");
                printf("EXERCICIO 14\n");
                printf("\n");

                int km, tempo;
                printf("Insira o valor do km percorrido: ");
                scanf("%d", &km);

                tempo = km * 2;

                printf("%d minutos\n", tempo);
                }
                break;
            case 15:
                {
                system("clear");
                printf("EXERCICIO 15\n");
                printf("\n");

                int tempo, velocidade;
                double distancia, litros;

                printf("Insira o tempo gasto de viagem: ");
                scanf("%d", &tempo);
                printf("Insira o valor do velocidade: ");
                scanf("%d", &velocidade);


                distancia = tempo * velocidade;
                litros = distancia / 12;

                printf("Serão necessários %.3lf litros para concluir a viagem.", litros);
                }
                break;
            case 16:
                {
                system("clear");
                printf("EXERCICIO 16\n");
                printf("\n");

                int N;
                int notas[7] = {100, 50, 20, 10, 5, 2, 1};
                printf("Insira o valor: ");
                scanf("%d", &N);

                printf("%d\n", N); // imprime o valor inicial

                for (int i = 0; i < 7; i++)
                    {
                    int qtd = N / notas[i];   // quantas notas dessa
                    printf("%d nota(s) de R$ %d,00\n", qtd, notas[i]);
                    N = N % notas[i];         // atualiza o resto
                    }
                }
                break;
            case 17:
                {
                system("clear");
                printf("EXERCICIO 17\n");
                printf("\n");
                int N;
                printf("Insira o tempo em segundos: ");
                scanf("%d", &N);

                int seg=0, min=0, horas=0;

                while (1)
                {
                    system ("cls");
                    if (seg == 59)
                    {
                        seg = 0;
                        min++;
                    }
                    if (min == 59)
                    {
                        min = 0;
                        horas ++;
                    }
                    seg++;

                    printf ("%.2d:%.2d:%.2d\n", horas, min, seg);

                    sleep(1);
                }


                }
                break;
            case 18:
                {
                system("clear");
                printf("\tEXERCICIO 18\n");
                printf("\n");
                
                float a, b, x;
                
                printf("\tEquação do 1º Grau\n");
                printf("\tInsira o Valor de A: ");
                scanf("%f", &a);
                printf("\tInsira o valor de B: ");
                scanf("%f", &b);                
                printf("\n");
                
                    x = -b / a;
                    printf("\tO valor de X: %.2f\n", x);

                break;
                }
            case 19:
                {
                system("clear");
                printf("EXERCICIO 19\n");
                printf("\n");
                int a, b, c;
                double x1, x2, delta;
                printf("\tEquação do 2º Grau\n");
                printf("\tInsira o Valor de Ax²: ");
                scanf("%d", &a);
                printf("\tInsira o valor de Bx: ");
                scanf("%d", &b);                
                printf("\tInsira o valor de C: ");
                scanf("%d", &c);
                printf("\n");
                
                delta = b*b - 4*a*c;
                
                if (delta < 0)
                {
                    printf("\tValor de Delta inválido!");
                    break;
                }
                else{
                x1 = (-b + sqrt(delta)) / (2 * a);
                x2 = (-b - sqrt(delta)) / (2 * a);

                printf("\tO valor de X1: %.2lf\n", x1);
                printf("\tO valor de x2: %.2lf\n", x2);

                }
                }
                break;
            case 20:
                {
                system("clear");
                printf("EXERCICIO 20\n");
                printf("\n");
                
                double imc, altura, peso;
                
                printf("Calculo de IMC");
                printf("\n");
                
                printf("Insira seu peso no formato (kg.g): ");
                scanf("%lf",  &peso);
                printf("Insira sua altura no formato (m.cm): ");
                scanf("%lf", &altura);
                printf("\n");
                
                imc = peso/(altura * altura);
                
                if (imc < 0){
                    printf("Dados invalidos!");
                }
                else if (imc >= 0 && imc < 18.5){
                    printf("Indice de massa corporal: MAGREZA!");
                }
                else if (imc >= 18.5 && imc <=24.9){
                    printf("Indice de massa corporal: NORMAL");
                }
                else if (imc >= 25 && imc <=29.9){
                    printf("Indice de massa corporal: SOBREPESO");
                }
                else if (imc >= 30 && imc <=34.9){
                    printf("Indice de massa corporal: OBESIDADE GRAU I");
                }
                else if (imc >= 35 && imc <=39.9){
                    printf("Indice de massa corporal: OBESIDADE GRAU II");
                }
                else {
                    printf("Indice de massa corporal: OBESIDADE GRAU III");
                }                 
                }
                break;
            case 21:
                {
                system("clear");
                printf("EXERCICIO 21\n");
                printf("\n");
                
                int temp1, temp2;
                double tempinicial, tempfinal;
                
                printf("Digite a temperatura atual: ");
                scanf("%lf", &tempinicial);
                printf("\n");
                printf("\nDigite: 1 = Celsius | 2 = Fahrenheit | 3 = Kelvin");
                printf("\n1º Digite o código da temperatura atual: ");
                scanf("%d", &temp1);
                printf("\n");
                printf("\nCódigo da temperatura a ser convertida: ");
                scanf("%d", &temp2);
                printf("\n");
                
                \
                if (temp1 == 1 && temp2 == 1){
                    printf("Ambas as temperaturas já estão na mesma escala.\n");
                    printf("%.2lf Graus Celsius", tempinicial);
                }
                else if (temp1 == 1 && temp2 == 2){
                    printf("Voce optou por converter de Celsius para Fahrenheit:\n");
                    tempfinal = (tempinicial * 9/5) + 32;
                    printf("Celsius: %.2lf -> Fahrenheit: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 1 && temp2 ==3){
                    printf("Voce optou por converter de Celsius para Kelvin:\n");
                    tempfinal = tempinicial + 273.15;
                    printf("Celsius: %.2lf -> Kelvin: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 2 && temp2 == 1){
                    printf("Voce optou por converter de Fahrenheit para Celsius:\n");
                    tempfinal = (tempinicial - 32) * 5/9;
                    printf("Fahrenheit: %.2lf -> Celsius: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 2 && temp2 == 2){
                    printf("Ambas as temperaturas já estão na mesma escala.\n");
                    printf("%.2lf Graus Fahrenheit", tempinicial);                
                }
                else if (temp1 == 2 && temp2 == 3){
                    printf("Voce optou por converter de Fahrenheit para Kelvin:\n");
                    tempfinal = (tempinicial - 32) * 5/9 + 273.15;
                    printf("Fahrenheit: %.2lf -> Kelvin: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 3 && temp2 == 1){
                    printf("Voce optou por converter de Kelvin para Celsius:\n");
                    tempfinal = tempinicial - 273.15;
                    printf("Kelvin: %.2lf -> Celsius: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 3 && temp2 ==2){
                    printf("Voce optou por converter de Kelvin para Fahrenheit:\n");
                    tempfinal = (tempinicial - 273.15) * 9/5 + 32;
                    printf("Kelvin: %.2lf -> Fahrenheit: %.2lf", tempinicial, tempfinal);
                }
                else if (temp1 == 3 && temp2 == 3){
                    printf("Ambas as temperaturas já estão na mesma escala.\n");
                    printf("%.2lf Graus Kelvin", tempinicial); 
                }
                else {
                    printf("Códigos inseridos estão incorretos.");
                }
                
                }
                break;
            case 22:
                {
                system("clear");
                printf("EXERCICIO 22\n");
                printf("\n");

                }
                break;                                                
            case 0:
                printf("Saindo...\n");
                menu = 0;
                break;

            default:
                printf("Opção inválida. Tente novamente.\n");
        }

        if (menu != 0) {
            printf("\nRETORNAR A LISTA?\n");
            printf("(1) Sim  |  (2) Não: ");
            scanf("%d", &menu);
            if (menu != 1) {
                printf("Saindo...\n");
                sleep(1);
                menu = 0;
            }
        }
    }
    return 0;
}
