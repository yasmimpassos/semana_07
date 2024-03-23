# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);

```
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado `false`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

**B) O código avalia a expressão booleana, imprime o resultado `true`, calcula a soma dos números de 1 a 5 e imprime o resultado no console.**

C) O código avalia a expressão booleana, imprime o resultado `true` e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado `false` e ordena a lista de números em ordem crescente.

Explicação: dentro da expressão booleana a primeira parte é falsa, mas a segunda é verdadeira, e como utilizamos o ||, que é o operador lógico "ou", é necessário que apenas uma parte seja verdadeira para que o resultado retorne verdadeiro. Após isso é realizado a soma de cade elemento da da listaDeNumeros, que são números de 1 a 5, e é armazenado na variável soma, que é impressa seu resultado no console.
______

**2)** Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

```javascript
//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

```javascript
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
```

Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

**B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'**

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

Explicação: 
Funcao calcularOrcamento: dentro do laço do/while vai ser feita a soma do total de gastos, que é 3600, mais o elemento 1 de gastos, que é 950, ficando 4550, e posteriormente é feita a verificação se o salario é maior ou igual ao totalGastos e se o i é menor do que o tamanho da array "gastos". Na primeira vez que roda a primeira condição já é falsa, desse modo rodando só uma vez e o totalGastos sendo igual a 4550. Depois é feito o calculo do saldo, que é salario menos totalGastos, e verifica se saldo é menor que zero, no caso esse afirmação está verdadeira,  se o salário é menor do que o total de gastos, assim modificando a variável statusSaldo para "negativo". Por fim é impresso seu saldo é negativo de -1050.

Funcao calcularOrcamento2: dentro do laço while vai ser feita a verificação se o salario é maior ou igual ao totalGastos e se o i é menor do que o tamanho da array "gastos", caso verdadeiro é feita a soma do total de gastos mais o elemento 1 de gastos, porém a primeira condição é falsa, desse modo não executando a soma. Depois é feito o calculo do saldo, que é salario(3500) menos totalGastos(3600), e verifica se saldo é menor que zero, no caso esse afirmação está verdadeira, se o salário é menor do que o total de gastos, assim modificando a variável statusSaldo para "negativo". Por fim é impresso seu saldo é negativo de -100.
______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
```

 Qual das seguintes alternativas é a descrição mais precisa do que o código faz?


A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

**D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".**

Explicação: Primeiro verifica se quando dividindo por 2 resta zero, logo par, e exibe a mensagem "O número é par!", caso não seja par, verifica se quando dividindo por 3 resta zero, e exibe a mensagem "O número é divisível por 3!" e caso nenhuma das afirmações sejam verdadeiras exibe a mensagem "O número é ímpar e não é divisível por 3!".
______

**4)** Qual será o resultado impresso no console após a execução desse código?
```javascript
//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200


B)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.


C)
Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.


**D)**

**Compra 1 aprovada. Saldo restante: 800**

**Compra 2 aprovada. Saldo restante: 0**

**Compra 3 aprovada com limite de crédito. Saldo restante: 200**

**Compra 4 negada. Saldo insuficiente e limite de crédito excedido.**

**Compra 5 negada. Saldo insuficiente e limite de crédito excedido.**

explicação: a primeira compra de 200 reais vai ser aprovada, porque ainda tem um saldo de 1000 reais, sobrando 800 reais. A segunda também vai ser aprovada, por ser de 800 reais, sobrando 0 reais. A terceira, de 300 reais, vai ter que usar o crédito, por não ter mais saldo, assim ficando 200 reais do crédito. A quarta não vai ser aprovada, porque ela é de 400 reais, mas só tem 200, no crédito. A última vai ser negada, poís ela é de 600 reais e o crédito é de 200.

______

**5)** Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

**B) Preload -> Create -> Update**

C) Load -> Initialize -> Render

D) Begin -> Play -> End

explicação: O principal ciclo de vida de um jogo Phaser.js, por padrão, é preload (que pré-carrega os ativos), o create (que cria a lógica inicial do jogo) e o update (que atualiza as informações do jogo).
______

**6)** Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

**B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.**

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

Explicação: Por padrão do Phaser.js o Arcade Physics, adiciona a física do jogo, assim simulando as interações físicas realistas, se aproximando mais a realidade.

______

# Questões dissertativas

**7)** Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem.
![Uma imagem](assets/image.png)

```
algoritmo "VerificaSeAPessoaPodeVotar"

inteiro idade
idade <- lerEntrada("Insira sua idade")

se (idade < 16) então:
    escreve("Não pode votar")
senão então:
    se (idade >= 16) && (idade < 18) então:
        escreve("Voto facultativo!")
    senão então:
        escreve("Voto obrigatório")
    fim do senão
fim do senão
```
______

**8)** Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

```
resposta:
```
Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        # Define o valor do atributo cor com o valor passado como parâmetro.
        cor <- cor

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

Classe Retangulo herda de FormaGeometrica:
    Atributos:
        - cor
        - largura
        - altura
    
    Método Construtor(cor, largura, altura):
        ConstructorDePai(cor)
        # Define o valor do atributo cor, largura e altura com o valor passado pelos respectivos parâmetros: cor, largura e altura.
        cor <- cor
        largura <- largura
        altura <- altura

    Método CalcularArea():
        # Faz o calculo da área
        area <- (largura x altura)
        escreve(area)

Classe Circulo herda de FormaGeometrica:
    Atributos:
        - cor
        - raio
        - pi <- 3,14
    
    Método Construtor(cor, raio):
        ConstructorDePai(cor)
        # Define o valor do atributo cor e raio com o valor passado pelos respectivos parâmetros: cor e raio.
        cor <- cor
        raio <- raio

    Método CalcularArea():
        # Faz o calculo da area
        area <- (pi x (raio)^2)
        escreve(area)


```

______

**9)** Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

```
Algoritmo "desempenhoCarroElétrico"

# faz uma função de desempenho do carro elétrico
Função DesempenhoCarroElétrico(velocidadeInicial, aceleracao, distância, velocidadeMaxima, tempoMaximo):
    tempoPassado <- 0
    velocidadeDoCarro <- velocidadeInicial
    # faz o calculo para descobrir qual é o tempo necessário para a velocidade chegar no maximo
    tempoParaChegarNaVelocidadeMaxima <- (velocidadeMaxima - velocidadeInicial)/aceleracao

    # executa enquanto a distancia que precisa percorrer for maior do que a percorrida e o tempo passado for menor do que o tempo maximo
    Enquanto (distancia > distanciaPercorrida e tempoPassado < tempoMaximo):
        # a velocidade do carro é atualizada
        velocidadeDoCarro <- velocidadeInicial + aceleracao * tempoPassado
        # o tempo passado é atualizado
        tempoPassado = tempoPassado + 1

        # verifica se a velocidade do carro é maior ou igual a da velocidade maxima
        Se velocidadeDoCarro >= velocidadeMaxima:
            velocidadeDoCarro <- velocidadeMaxima
            # atualiza a distância percorrida, fazendo o calculo da parte em movimento uniformemente variado (MUV) e da parte em movimento uniforme (MU)
            distânciaPercorrida <- velocidadeInicial * tempoParaChegarNaVelocidadeMaxima + (1/2) * aceleracao * tempoParaChegarNaVelocidadeMaxima^2 + velocidadeMaxima * (tempoPassado - tempoParaChegarNaVelocidadeMaxima)
        else:
            # atualiza a ditância percorrida considerando apenas o movimento uniformemente variado (MUV)
            distânciaPercorrida <- velocidadeInicial * tempoPassado + (1/2) * aceleracao * tempoPassado^2
        
    # Após o loop parar verifica se a distancia a ser percorrida é  menor ou igual a distanciaPercorrida
    Se distancia <= distanciaPercorrida:
        Retorne tempoPassado
    Senão:
        # Caso contrário informa que o tempo acabou
        Retorne "Não foi possível completar a corrida dentro do tempo máximo."
```

______

**10)** Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

```
Função SomaDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."
    Senão:
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0]) # Considerando que todas as linhas têm o mesmo número de colunas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a soma
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizSoma <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Soma das matrizes:")
ImprimirMatriz(matrizSoma)
```
resposta:
```
Função MultiplicacaoDeMatrizes(matrizA, matrizB):
    # Verifica se a quantidade de colunas da matrizA é igual ao de linhas da matrizB

    Se tamanho(matrizA[0]) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas, a quantidade de colunas da matrizA precisa ser igual ao de linhas da matrizB"
    Senão:
        linhas <- tamanho(matrizA) # quantidade de linhas igual a da matrizA
        colunas <- tamanho(matrizB[0]) # quantidade de colunas igual a da matrizB

        # matrizResultado recebe a novaMatriz, com a quantidade de linhas e colunas já calculadas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a multiplicação
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                somaDeElemento <- 0  # Inicializa somaDeElemento para cada elemento da matriz resultante
                Para k de 0 até tamanho(matrizA[0]) - 1 faça:
                    #faz a soma das multiplicações para cada elemento
                    somaDeElemento += matrizA[i][k] * matrizB[k][j]
                # matrizResultado recebe o elemento correspondente
                matrizResultado[i][j] <- somaDeElemento
        Retornar matrizResultado
        

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizMultiplicada <- MultiplicacaoDeMatrizes(matrizA, matrizB)
Escrever("Multiplicação das matrizes:")
ImprimirMatriz(matrizMultiplicada)
```
