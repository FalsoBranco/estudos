**Exercício salvação IA E CA

INTELIGÊNCIA ARTIFICIAL

  
  

1.  Defina Sistemas especialistas (SE):
> Sistema que representa o conhecimento de um especialista
1.  Quais são as fases do desenvolvimento de um S.E.?
> Passos para seu desenvolvimento:
> 	▶ Levantamento de informações
> 	▶ Engenharia do conhecimento
> 	▶ Representação do conhecimento
> 	▶ Codificação
1.  O que significa PROLOG?
> Prolog, Programação lógica, é uma linguagem que se enquadra no paradigma de Programação em Lógica Matemática. Sendo uma linguagem declarativa que permite a implementação de programas utilizando lógica de predicados.
2.  Para as chamadas: `q4(0,1,w)` , `q4(1,1,w)`,  `q4(0,0,w)`, quais os valores de w?
```prolog
q4(0,0,0).
q4(1,0,0).
q4(0,1,0).
q4(1,1,1).
```

>```prolog
> ?q(0,1,W)
> W=0
>
> ?q(1,1,W)
> W=1
>
> ?q(0,0,W)
> W=0
>``` 

O que foi o predicado de q4?

> Foi uma Tabela verdade "e", conjunção

5.  Qual é o resultado do predicado q5 para a chamada: `q5([1,3,6,1,2,9], W)`
```prolog
q5([], 0).
q5([X|Y], Z):-
	q5(Y, K),
	Z is K+1.  
```
> W = 6. O predicado q5 conta quantos elementos há em uma lista.

6. Cite 4 problemas reais que podem ser resolvidos utilizando-se S.E.:
> Exemplos de áreas de aplicação de Sistemas Especialistas:
> ▶ Diagnose médica
> ▶ Tomada de decisões financeiras
> ▶ Estratégias militares
> ▶ Detecção de Fraudes
1. Defina Aprendizado de Máquina: 
> Aprendizado de máquina se preocupa com a construção de programas de computador que melhoram seu desempenho por meio de experiência, ou, campo de estudo que dá aos computadores a habilidade de aprender sem serem explicitamente programados.
8. Cite 4 estratégias de aprendizado utilizadas em M.L.:
> Exemplos de estratégias:
> ▶ **Supervisionado**: Quando há entrada e saida de dados ditando como o seu treinamento deve seguir
> ▶ **Reforço**: Quando há entrada mas não uma saida precisa, apenas reforços positivos e negativos.
> ▶ **Não supervisionado**: Quando não há mecanismos que determinam a qualidade das saídas que dão apoio ao treinamento.
> ▶ **Semi-supervisionado**: Utiliza um numero menor de dados de saida para orientar o aprendizado.
> 
1. O que é o método ID3? Descreva o seu funcionamento.
> Metodo ID3 é um algoritmo que constroi uma arvore de decisão de forma descendente ("Cima-baixo"), a cada nó seleciona-se o atributo que melhor classifica os exemplos de treinamento locais, continuando perfeitamente até que a arvoce classifique os exemplos de treinamentos, ou até que todos os atributos sejam usados.
3.  Explique o funcionamento de um problema de classificação.
> Esse metodo define um valor de classe com base nos dados de entrada
1.  Dada a planilha de treinamento abaixo, construa de maneira intuitiva uma árvore de decisão, sob a variável aprovado: Explique

| Sexo | +10 horas | Dificil | Aprovado |
| ---- | --------- | ------- | -------- |
| M    | TRUE      | TRUE    | SIM      |
| F    | FALSE     | TRUE    | SIM      |
| M    | FALSE     | TRUE    | SIM      |
| F    | FALSE     | FALSE   | NÃO      |
| M    | FALSE     | FALSE   | NÃO      |
| F    | TRUE      | TRUE    | SIM      |
| F    | TRUE      | FALSE   | SIM      |
![[DT_alunos.png]]
> O atributo `Dificil` foi o melhor encontrado, pois é o que melhor separa as decisões.

12. Defina Redes Neurais (RNA):
> RNA, Redes Neurais Artificiais são modelos computacionais inspirados pelo sistema nervoso central de um animal (cérebro) que são capazes de realizar o aprendizado de máquina. São apresentadas como sistemas de neurônios interconectados, que podem computar valores de entradas, retornando uma saída.
13. Qual o problema com as redes Perceptron ?
> Por ser um classificador linear, os problemas  solucionados por ele devem ser linearmente separaveis.
> 
14. Explique o Multilayer Perceptron e o algoritmo Backpropagation
> **Multilayer Perceptron**: é uma rede neural com uma ou mais camadas ocultas com um número indeterminados de neurônios. A cama oculta possui esse nome porque não é possível prever a saída desejada nas camadas intermediarias.
> **O backpropagation** é o algoritmo-chave que faz o treinamento de modelos profundos algo computacionalmente tratável. Para as redes neurais modernas, ele pode tornar o treinamento com gradiente descendente até dez milhões de vezes mais rápido, em relação a uma implementação ingênua.
15. Cite 4 problemas reais que podem ser resolvidos utilizando-se RNA:
> ▶ Identificação de alvos militares
> ▶ Autenticação de usuário
> ▶ Controle de navegação
> ▶ Predição do mercado financeiro