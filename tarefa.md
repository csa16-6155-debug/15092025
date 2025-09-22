# Tarefa 1 - 3ª etapa 2025

Implemente cada questão **no arquivo indicado** (`q1.py`…`q4.py`).
Cada arquivo deve **imprimir o resultado final** quando executado:
```bash
python q1.py

#### Comece aqui a questão ####
p

#### Termine aqui a questão ####

```

## O que fazer
- Abra o arquivo da questão indicada `qn.py` e coloque seu código nas questões nos espaços corretos.
- O print deve ser exatamente como o solicitado.
- Como vamos tratar de aleatoriedade, em todas as questões, importe a bibloteca `random` com `import random` e selecione a semente 2 com `random.seed(2)`.
##

## Contexto
A mega-sena, famoso concurso de loteria no Brasil, é um jogo em que seis números diferentes entre 1 e 60 são sorteados e o vencedor é o apostador que selecionou esses seis números em sua aposta. Por se tratar de um sorteio auditado e verificado, sabemos que qualquer conjunto de seis números tem a mesma probabiliade de $\frac{1}{50.063.860}$ de ser sorteado, mesmo os mais banais como [1, 2, 3, 4, 5, 6].
##

### QUESTÃO 1
Suponha um sorteio de um número qualquer entre 1 e 60. Teste quantos sorteios serão necessários na semente 2 para que o número 1 seja sorteado.
#### Dicas
* Crie uma variável `contador = 0`;
* crie uma variável de controle com `fim = False`;
* crie um `while` cuja a condição seja que `fim == False`. Dentro do `while` sorteie um número `x` com `random.randint(1,60)` e verifique se ele é 1. Se for 1, troque `fim` para `True`;
* dentro do `while`, lembre sempre de adicionar 1 ao seu `contador`, que, no fim do código, será impresso como sua resposta.
##
### QUESTÃO 2 
Suponha uma outra modalidade de sorteio de dois números quaisquer entre 1 e 60. Teste quantos sorteios serão necessários na semente 2 para que os números 1 e 2 sejam os sorteados.
#### Dicas (além das que estão na questão 1)
* Crie uma lista `alvo = [1,2]` que serão os números que você quer que sejam sorteados;
* dentro do `while`, crie uma lista `sorteio = []` que armazenará os números sorteados;
* ainda dentro do `while`, crie um outro `while` cuja condição seja que o número de elementos da lista `sorteio` seja menor do que 2 (na prática, esse `while` vai funcionar enquanto você não sortear dois números).
* dentro desse segundo `while`, sorteie um número `x` com `random.randint(1,60)` e verifique se ele já não está entre os sorteados usando `if`. Construa sua condição com os operadores `not` e `in` (faça como se você estivesse falando em inglês `se x não está nos sorteados`), se não estiver, adicione-o aos sorteados com `append`;
* quando sua lista de sorteados estiver completa, saia do segundo `while`, ordene-a com `sorteados_ordenados = sorted(sorteados)` e verifique se essa nova lista é igual à sua lista `alvo`;
* se `sorteados_ordenados == alvo`, troque `fim` para `True`;
##
### QUESTÃO 3
Suponha uma outra modalidade de sorteio de três números quaisquer entre 1 e 60. Teste quantos sorteios serão necessários na semente 2 para que os números 1, 2 e 3 sejam os sorteados.
##
### QUESTÃO 4
Por fim, suponha uma modalidade de sorteio de `n` números quaisquer entre 1 e 60. Teste quantos sorteios serão necessários na semente 2 para que os números naturais entre `1` e `n` sejam os sorteados. Sua variável `n` será colhida com `n = input()`, nesse caso `n` virá como string, converta-o.
A maior diferença dessa questão é para criar a lista `alvo`, que deve começar vazia. Use um `for` com um `range(n)` adicionando elementos à `alvo` com `append`.
Depois lembre de alterar a codição do segundo `while`.


Boa trabalho!

## Curiosidade
Baixe seu código e simule com valores diferentes de n e da semente para entender a dificuldade de sair um valor específico em que não haja sorte envolvida. Com a semente 2, o programa demorou mais de 18 minutos e 90 milhões de sorteios para sortear 1, 2, 3, 4, 5 e 6. A título de comparação, em setembro de 2025, ainda não chegamos ao sorteio 3000 da história da mega-sena.
