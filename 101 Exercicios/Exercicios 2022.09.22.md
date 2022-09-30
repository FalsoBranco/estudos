[[Inteligência Artificial]]  
tags::  #Faculdade #Exercicio #Terminar  
dates:: 2022-09-23    

---
# Exercícios 2022.09.22  
1. De duas definições de [[Inteligência Artificial]]
	> Inteligência computacional é o estudo sobre o desenvolvimento de agentes inteligentes  
	
	> O Estudo de métodos computacionais que torna possível a percepção, o pensamento e o agir.
2. Quando foi escrito o primeiro trabalho de Inteligência Artificial?
	> Em 1943 foi apresentado o primeiro artigo que fala pela primeira vez de redes neurais.
3. Defina Agente
	> Agente é a entidade que percebe o mundo à sua volta (através de sensores) e atua neste mundo (através de atuadores)
4. O que é a descrição PAGE
	> É a decomposição de um problema em : percepções, ações, objetivos e ambientes
5. Um algoritmo de busca pode ser avaliado em 4 aspectos. Explique essas características.
	1. Completude
		> a solução (quando existe) é sempre encontrada?
	2. Otimalidade
		> a solução encontrada é de custo mínimo?
	3. Complexidade de Tempo
		> Número de nós gerados ou expandidos
	4. Complexidade de Espaço
		> Número máximo de nós na memória.
		```ad-note
	 
		 Complexidade no tempo e no espação são meidas em temos de:  
		 ▶ b - fator de ramificação máximo da árvore de busca(quantidade máxima de estaos gerados após a expansão de um estado)  
		 ▶ d - Profunidade da solução de custo mínimo  
		 ▶ m - Profundidade máxima do espaço de busca (poe ser infinito) 
		 ```
1. Com base nas características dadas no exercício 5, descreva os algoritmos:
	1. Busca em Largura
		> Completo: Sim  
		> Otimo: Sim  
		> Tempo: $\mathcal{O}(b^d)$  
		> Espaço: $\mathcal{O}(b^d)$  
		> Estrutura de dados: Fila
	1. Busca em Profundidade
		> Completo: Não  
		> Otimo: Não  
		> Tempo: $\mathcal{O}(b^d)$  
		> Espaço: $\mathcal{O}(bm)$  
		> Estrutura de dados: Pilha  
	1. Busca em Profundidade Iterativo
		> Completo: Sim  
		> Otimo: Sim  
		> Tempo: $\mathcal{O}(b^d)$  
		> Espaço: $\mathcal{O}(bd)$  
		> Estrutura de dados: Pilha
	
	Determinado cada a estrutura de dados utilizada por cada um destes.

1. Qual é a principal características dos métodos de busca por melhoria iterativa
	> Não gera árvore
1. Qual é a estrutura de dados utilizada pelos algoritmos:
	1. Busca de custo uniforme
	2. Busca gulosa
	3. A*
2. Ordene os operadores (Polução inicial, cruzamento, mutação, pré-seleção, seleção) dos algoritmos genéricos.
	> População Inicicial > cruzamento > mutação > pré-seleção > seleção
1. Diferencia subida de encosta e simulated anniling