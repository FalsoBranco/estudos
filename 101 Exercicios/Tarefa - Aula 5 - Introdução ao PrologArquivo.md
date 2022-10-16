[[Inteligência Artificial]]  
tags::   
dates:: 2022-10-15    

---
#  Tarefa - Aula 5 - Introdução ao PrologArquivo

1. Permitir a digitação de quatro notas de um aluno e mostrar a média.
```prolog
main:- 
	write("Digite a primeira nota"), read(Nota1),nl,
	write("Digite a segunda nota"), read(Nota2),nl,
	write("Digite a terceira nota"), read(Nota3),nl,
	write("Digite a quarta nota"), read(Nota4),nl,

	Media is (Nota1 + Nota2 + Nota3 + Nota4)/4,

	format('~2f',[Media]),nl.

```
2. Permitir a digitação do lado de um quadrado, calcular e mostrar: área, perímetro e diagonal principal.
```prolog
main:- 
	write("Digite o tamanho do lado"), read(Lado),nl,
	Area is Lado ** 2,
    Perimetro is 4 * Lado,
    Diagonal_Principal is sqrt((Lado**2)+(Lado**2)),

	format('Area = ~2f\nPerimetro = ~2f\nDiagonal Principal = ~2f\n',[Area,Perimetro,Diagonal_Principal]),nl.


```
3. Permitir a digitação do raio de uma circunferência, calcular e mostrar diâmetro, perímetro e área do círculo.
```prolog
main:- 
    write("Digite o tamanho do raio"), read(Raio),nl,
	
    Pi is 3.14159,
    
	Diametro is 2 * Raio,
	Perimetro is 2 * Pi * Raio,
	Area is Pi * (Raio ** 2),
	
    format('Diametro = ~2f\nPerimetro = ~2f\nArea = ~2f',[Diametro,Perimetro,Area]),nl.
```
4. Permitir a digitação da 3 valores mostrar o tipo de triângulo que eles podem formar (equilátero, escaleno ou isósceles)
```prolog
triangulo(Lado1, Lado2, Lado3, _) :- Lado1 + Lado2 < Lado3, !, fail.
triangulo(Lado1, Lado2, Lado3, _) :- Lado2 + Lado3 < Lado1, !, fail.
triangulo(Lado1, Lado2, Lado3, _) :- Lado3 + Lado1 < Lado2, !, fail.

triangulo(Lado1, Lado2, Lado3, _) :- Lado1 = 0, Lado2 = 0, Lado3 = 0, !,	fail.

triangulo(Lado1, Lado2, Lado3, "equilatero") :- Lado1 = Lado2, Lado2 = Lado3, Lado2 = Lado1, !.
triangulo(Lado1, Lado2, Lado3, "escaleno") :- Lado1 \= Lado2, Lado2 \= Lado3, Lado2 \= Lado1, !.
triangulo(S, S, _, "isosceles") :- !.
triangulo(S, _, S, "isosceles") :- !.
triangulo(_, S, S, "isosceles") :- !.

main(Resposta):- 
	write("Digite o primeiro lado"), read(Lado1),nl,
	write("Digite o segundo lado"), read(Lado2),nl,
	write("Digite o terceiro lado"), read(Lado3),nl,
	
    triangulo(Lado1,Lado2,Lado3,Resposta).
```
5. Pesquisa: ler 3 números, coeficientes de uma equação do segundo grau, e determinar as raízes (caso existam)
```prolog
check_A_value(A):- A>0.
discriminante(A,B,Delta,X1,X1):- 
    Delta=0,
    X1 is -B/2/A,
    write('A equação possui duas raízes reais e iguais.').


discriminante(A,B,Delta,X1,X2):-
    Delta > 0,
    X1 is (-B+sqrt(Delta))/2/A,
    X2 is (-B-sqrt(Delta))/2/A,
    write('A equação possui duas raízes reais e distintas.').


discriminante(_,_,Delta,_,_):-
    Delta < 0,
    write('A equação não possui raízes reais.').
    


main(X1,X2):- 
	write("Digite o valor de A"), read(A),nl,
	check_A_value(A),
    write("Digite o valor de B"), read(B),nl,
    write("Digite o valor de C"), read(C),nl,
    
    Delta is (B**2 - (4*A*C)),
	discriminante(A,B,Delta,X1,X2),
	write('foi').
```