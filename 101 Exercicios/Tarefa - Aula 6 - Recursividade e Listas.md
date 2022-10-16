[What is this most related to?]  
tags::   
dates:: 2022-10-15    

---
#  Tarefa - Aula 6 - Recursividade e Listas

1. Calcular $X^y$ – com uma função recursiva. 
```prolog
expo(_,0,1).
expo(X,Y,Resultado):-
    Y1 is Y-1,
    
    expo(X,Y1,Resultado1),
    
    Resultado is X*Resultado1.
```
2. Mostrar o Binário que representa um número natural qualquer. 
```prolog
binario(0,0).
binario(Decimal,Resultado):-
    Decimal1 is Decimal//2,
    binario(Decimal1,Resultado1),
    Resultado is Decimal mod 2 +10 * Resultado1.
```
3. Retornar a quantidade de elementos presentes em uma lista. 
```prolog
count_list([],0).
count_list([_|Y],Resultado):-
    count_list(Y,Resultado1),
    Resultado is Resultado1 + 1.
```
4. Retornar a soma de elementos de uma lista. 
```prolog
count_list([],0).
count_list([X|Y],Resultado):-
    count_list(Y,Resultado1),
    Resultado is Resultado1 + X.
```
5. Devolver o maior elemento de uma lista.
```prolog
max([],0).

max([X|Y],Resultado) :-
    max(Y,Maior),
    X > Maior,
    Resultado is X.

max([X|Y],Resultado) :-
    max(Y,Maior),
    X =< Maior,
    Resultado is Maior.
```
2. Criar uma estrutura de dados pilha (empilhar, desempilhar e pilhaVazia).
3. Criar uma estrutura de dados fila (enfileira, desenfileira e filaVazia).