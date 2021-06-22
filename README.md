# Trabalho-Lacos-de-Repetcao
Trabalho em C++ para laços de Repetição
Questão 01: Conversão de Polegadas. 
#include <iostream>
#include <iomanip>
#include <locale.h>
using namespace std;
int main(){
	float pol;
	setlocale(LC_ALL,"Portuguese");
	cout << fixed << setprecision(2);
	cout << "\n|----------------TABELA----------------|\n";
	cout << "\nConversão de Polegadas para Centímetros.\n";	
	for (pol=1;pol<=20;pol++){
			cout << "\n" << pol << "  polegada(s) é igual a " << pol*2.54 << " centímetros";
	}
	cout << "\n|--------------------------------------|\n";
	return 0;		
	}
 
Questão 02: Pessoas com menos de 21 anos e mais de 50 anos.
#include <iostream>
#include <locale.h>
using namespace std;
int main(){
	int idade,contador21=0, contador50=0;	
		while(idade !=71){
	cout << "\nDigite sua idade ou digite 71 para sair: ";
	cin >> idade;
			if(idade<21){
			contador21++;
			}
			if(idade>50){
			contador50++;
			}
		}
	cout << "\nTotal de pessoas com menos de 21 anos: " << contador21;
	cout << "\nTotal de pessoas com  mais de 50 anos: " << contador50;
	return 0;
}
 

Questão 03: Estatística de Sexo e Altura.
#include <iostream>
#include <iomanip>
using namespace std;
int main(){
	char sexo;
	float menorAltura=999, maiorAltura=0, altura, mediaAltura=0;
	int i, numHomens, numMulheres, numM;	
	for(i=0;i<5;i++){
		cout<<fixed<<setprecision(2)<<"\nEscreva a altura: ";
		cin>>altura;
		cout<<"\nEscreva o sexo: ";
		cin>>sexo;
		if(menorAltura>altura){
			menorAltura=altura;
		}
		if(maiorAltura<altura){
			maiorAltura=altura;
		}
		if(sexo=='F' || sexo=='f'){
			mediaAltura+=altura;
			numMulheres++;		
			numM++;
		}
if(sexo=='m' || sexo=='M'){
			numHomens++;
		}
		}
	cout<<"\nA Menor altura: "<<menorAltura;
	cout<<"\nA Maior altura: "<<maiorAltura;
	cout<<"\nA media de altura das mulheres: "<<mediaAltura/numM; 
	cout<<"\nO numero de homens: "<<numHomens;
	return 0;
}

 


Questão 04: Massa de acordo com o Tempo.
#include<iostream>
#include<math.h>
using namespace std;
int main (){
    float massa; 
	int tempo = 0, tempo1, tempo2, tempo3;
    cout << " Digite a massa do material em gramas: ";
    cin >> massa;    
    while(massa >= 0.5){
        massa = massa / 2.0;
        tempo++;
    }    
    tempo1 = (tempo*50)/3600;
    tempo2 = ((tempo*50) % 3600) / 60;
    tempo3 = ((tempo*50) % 3600) % 60;
    
    cout << " Massa final: " << massa; 
    cout << "\n Tempo em Horas   : " << tempo1 << " horas";
    cout << "\n Tempo em Minutos : " << tempo2 << " minutos";
    cout << "\n Tempo em Segundos: " << tempo3 << " segundos";
	return 0;
	}
 
Questão 05: Alunos e Notas.
#include <iostream>
#include <locale.h>
#include <iomanip>
using namespace std;
int main(){	
	int ca, aux=0;
	float nota1, nota2, nota3, nota4, nota5, media;
	string aluno;
	setlocale(LC_ALL,"Portuguese");
	for(ca=0;ca<3;ca++){
		cout << "\n Digite o nome do aluno e suas Cinco Notas: ";
		cin >> aluno;		
			cout << "notas: \n";
				cin >> nota1; 
				cin >> nota2;
				cin >> nota3;
				cin >> nota4; 
				cin >> nota5;						
		if (nota1>=7&&nota2>=7&&nota3>=7&&nota4>=7&&nota5>=7){
			cout << "\n Aluno(a) " << aluno << " foi aprovado(a) em todas as matérias!\n"; 
		}
		if (nota1>=7&&nota4>=7){
			cout << "\n Aluno(a) " << aluno << " foi aprovado(a) na matéria 1 e 4!\n";	
		}
		if (nota3>=7){
			aux=aux+1;
		}
	}
		if(aux==1){
			cout << "\n 33% dos alunos foram aprovados na matéria 3.";
			}
			if(aux==2){
				cout << "\n 66% dos alunos foram aprovados na matéria 3.";
			}
			if(aux==3){
				cout << "\n 100% dos alunos foram aprovados na matéria 3.";			
			}
	return 0;
	}
 

DESAFIO: Fibonacci.
#include <iostream>
using namespace std;
int main (){
int num, ant = 1, at = 1, pr;
cout << "Digite o numero de termos Fibonacci: ";
cin >> num;
for (int i = 1; i <= num; i++)
{
if (i == 1) cout << "0 ";
else if (i == 2 || i == 3) cout << "1 ";
else{
pr = ant + at;
ant = at;
at = pr;
cout << " " << pr;
}
}
return 0;
}

 

