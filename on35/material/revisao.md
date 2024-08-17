<h1 align="center">
  <img src="assets/reprograma-fundos-claros.png" alt="logo reprograma" width="500">
</h1>


Turma Online ON33, 34 E 35 | Revisão | 2024 | Professora [Jenifer Plácido](https://www.linkedin.com/in/jenifer-pl%C3%A1cido-00b5611ab/)


# Revisão On33, 34 e 35

## Git

Git é um sistema de controle de versão distribuído.

Criador: Linus Torvalds, 2005.

- **Git** é como um sistema de "salvar e recuperar" para o seu código.
- Quando você faz uma mudança e "salva" (nós chamamos isso de "commit"), o Git lembra o que você fez.
- Se algo der errado, você pode voltar para uma versão anterior, assim como desfazer mudanças em um documento de texto.

**Características:**

- Distribuído
- Rápido
- Integridade dos dados
- Suporte para branching e merging

**Comandos Básicos de git**

- **git init:** Inicia um novo repositório Git.
- **git clone <url>**: Clona um repositório remoto.
- **git add <arquivo> ou .** : Adiciona arquivos ao staging area.
- **git commit -m "mensagem"**: Cria um commit com as mudanças.
- **git status:** Verifica o status do repositório.
- **git push:** Envia mudanças para o repositório remoto.
- **git pull:** Atualiza o repositório local com mudanças do remoto.
- **git checkout -b <nome>**: Cria uma nova branch e muda pra ela.
- **git checkout <nome>:** Muda para uma branch específica.
- **git merge <branch>:** Faz merge de uma branch com outra.

## GitHub

Plataforma de hospedagem de código-fonte que usa Git.

**Usos:**

- Colaboração em projetos
- Controle de versão
- Hospedagem de repositórios públicos e privados

**Principais funcionalidades do GitHub**

- **Repositórios (Repositories):** Armazenamento e versionamento de código.
- **Branches (Ramificações):** Desenvolvimento isolado de novas funcionalidades ou correções de bugs.
- **Pull Requests:** Revisão e integração de mudanças no código.
- **Issues (Problemas):** Rastreamento de bugs, tarefas e funcionalidades.
- **GitHub Actions:** Automação de fluxos de trabalho (CI/CD).
- **Forks:** Cópia de repositórios para desenvolvimento independente.
- **Colaboração e Revisão de Código:** Comentários e discussões em pull requests e issues.

### Fork

**Fork** é uma cópia de um repositório que fica na sua conta do GitHub. Vamos imaginar uma situação da vida real para entender melhor:

### Exemplo Real de Fork

Imagine que você está em uma biblioteca e encontra um livro de receitas incrível. Você quer fazer algumas modificações nas receitas, talvez adicionar seus próprios ingredientes ou fazer anotações, mas você não pode escrever no livro da biblioteca. O que você faz? Tira uma cópia do livro para levar para casa.

- **Na programação**: Quando você encontra um projeto interessante no GitHub que quer modificar ou contribuir, você faz um "fork" do repositório. Isso cria uma cópia do projeto no seu próprio GitHub, onde você pode fazer todas as mudanças que quiser sem afetar o projeto original.

### Pull Request

**Pull Request** é como pedir ao dono do repositório original para dar uma olhada nas suas mudanças e, se gostar, incorporar essas mudanças no projeto original.

### Exemplo Real de Pull Request

Voltando ao exemplo da biblioteca, imagine que você fez várias modificações na sua cópia do livro de receitas em casa. Agora, você acha que suas mudanças tornaram as receitas melhores e quer compartilhar isso com a biblioteca para que todos os leitores possam se beneficiar.

- **Na programação**: Depois de fazer melhorias ou correções no projeto que você copiou (forked), você pode pedir ao dono do projeto original para considerar suas mudanças. Você faz isso criando um "pull request". O dono do projeto original revisa suas mudanças e, se concordar que elas são úteis, ele "merge" (integra) essas mudanças no projeto original.

### Para que Servem

- **Forks**: Permitem que você experimente e faça mudanças em um projeto sem afetar o original. É uma forma segura de desenvolver e melhorar código.
- **Pull Requests**: Facilitam a colaboração. Eles permitem que você contribua com projetos de outras pessoas e que outras pessoas contribuam com os seus. É uma maneira de melhorar projetos de código aberto de forma colaborativa.

### Exemplo de Uso de Fork e Pull Request

Vamos imaginar um cenário de desenvolvimento real:

1. **Você encontra um projeto interessante no GitHub**: Digamos que você encontrou um projeto de código aberto que é um aplicativo de receitas que te interessa.

2. **Você faz um fork do projeto**: Agora você tem uma cópia desse aplicativo de receitas no seu próprio GitHub. Você pode fazer mudanças e melhorias à vontade.

3. **Você melhora o aplicativo**: Você adiciona novas receitas, melhora a interface do usuário, ou corrige alguns bugs que encontrou.

4. **Você cria um pull request**: Você acha que suas mudanças tornam o aplicativo melhor. Então, você cria um pull request para o repositório original, explicando o que você mudou e por que isso é uma melhoria.

5. **Revisão e integração**: O dono do projeto original revisa seu pull request. Se ele gostar das suas mudanças, ele pode integrar (merge) suas melhorias ao projeto original. Agora, todos os usuários do aplicativo de receitas podem se beneficiar das suas contribuições.

Forks e pull requests são ferramentas no GitHub que permitem que desenvolvedores colaborem de forma eficaz em projetos de código aberto. Eles possibilitam a experimentação individual e a contribuição coletiva, tornando o desenvolvimento de software uma atividade verdadeiramente colaborativa. Então, sempre que você encontrar um projeto interessante, não hesite em fazer um fork e começar a contribuir!

## Terminal

Para interagir com Git e GitHub, muitas vezes usamos o **terminal**. O terminal é uma ferramenta que permite que você dê comandos para o seu computador usando texto.

- Pense no terminal como um telefone antigo, onde você disca números para falar com alguém. Aqui, você digita comandos para dizer ao seu computador o que fazer.
- Comandos como `ls` para listar arquivos ou `cd` para mudar de diretório ajudam você a navegar pelos arquivos e pastas do seu computador.

## Tipos de Variáveis

Quando programamos, usamos **variáveis** para armazenar informações. É como guardar coisas em diferentes tipos de caixas.

- **Inteiros (int)**: São como caixas que guardam números inteiros, como 1, 2, 3.
- **Decimais (float)**: São caixas que guardam números com pontos decimais, como 1.5, 2.75.
- **Texto (str)**: São caixas que guardam palavras ou frases, como "Olá, mundo!".
- **Booleanos (bool)**: São caixas que guardam verdadeiro ou falso, como sim ou não (True ou False).

Imagine que você está anotando a idade de várias pessoas:

- Idade de Maria: 25 (int)
- Altura de João: 1.75 metros (float)
- Nome do cachorro: "Rex" (str)
- Estudante? Sim (True)

## Operadores

Os **operadores** são como ferramentas que usamos para fazer cálculos ou comparações.

- **Operadores de adição (+), subtração (-), multiplicação (*) e divisão (/)**: São como calculadoras. Se você tem 5 maçãs e ganha mais 3, você usa o operador de adição para descobrir que agora tem 8 maçãs.
- **Operadores de comparação (==, !=, >, <)**: São como balanças que comparam coisas. Por exemplo, "Você tem mais de 18 anos?" é uma comparação.

- Claro! Vamos explicar o conceito de funções, funções com retorno, funções sem retorno e funções internas em Python com exemplos da vida real para facilitar o entendimento.

  ### Funções em Geral

  Uma **função** em programação é como uma receita que você segue para realizar uma tarefa específica. Em vez de repetir o mesmo código várias vezes, você define a função uma vez e a usa sempre que precisar. Vamos imaginar isso com um exemplo do cotidiano.

  **Na programação**: Você cria uma função para uma tarefa que precisa ser feita repetidamente. Por exemplo, calcular o total de uma compra.

  ### Funções Sem Retorno

  Uma **função sem retorno** faz alguma coisa, mas não envia nada de volta. Ela apenas executa uma ação.

  **Na programação**: Uma função sem retorno pode ser usada para imprimir uma mensagem na tela ou atualizar uma variável.

  ### Funções Com Retorno

  Uma **função com retorno** faz alguma coisa e envia um resultado de volta. Ela realiza uma ação e te dá uma resposta que você pode usar.

  **Na programação**: Uma função com retorno pode calcular um valor e retornar esse valor para que você possa usá-lo em outra parte do seu programa.

  ### Funções Internas em Python

  O Python vem com várias **funções internas** (built-in functions) que são como ferramentas prontas para usar. Elas são fornecidas pela linguagem e podem ser usadas diretamente.

  **Na programação**: Python tem funções internas como `print()`, que exibe uma mensagem na tela, `len()`, que retorna o comprimento de uma lista ou string, e `sum()`, que soma os valores em uma lista.

  ### Exemplos Reais

  **Função Sem Retorno**:

  - **Vida Real**: Você pede ao assistente para apagar as luzes.
  - **Programação**: Uma função que imprime "Olá, mundo!" na tela.

  **Função Com Retorno**:

  - **Vida Real**: Você pede ao assistente para contar as maçãs e te dizer o número.
  - **Programação**: Uma função que calcula o dobro de um número e retorna o resultado.

  **Funções Internas**:

  - **Vida Real**: Usar uma faca de chef ou uma colher de pau que já estão na cozinha.
  - **Programação**: Usar `print()` para exibir uma mensagem ou `len()` para obter o tamanho de uma lista.

  ### Exemplos Detalhados

  #### Função Sem Retorno (Vida Real)

  Você tem um cronômetro que apita a cada 30 minutos para lembrá-lo de se alongar. Ele não te dá mais nenhuma informação, apenas faz um som para lembrá-lo.

  #### Função Sem Retorno (Programação)

  Uma função que imprime uma mensagem de boas-vindas na tela. Ela não retorna nenhum valor, apenas exibe a mensagem.

  #### Função Com Retorno (Vida Real)

  Você pede ao seu assistente para calcular a quantidade total de dinheiro que você tem depois de contar todas as suas moedas e te informar o valor.

  #### Função Com Retorno (Programação)

  Uma função que calcula a média de uma lista de números e retorna esse valor. Você pode então usar essa média em outro cálculo ou exibi-la na tela.

  #### Funções Internas (Vida Real)

  Ao cozinhar, você usa ferramentas básicas que sempre estão à mão, como uma faca ou uma colher. Você não precisa reinventar essas ferramentas cada vez que cozinha.

  #### Funções Internas (Programação)

  Funções como `max()` que retorna o maior valor de uma lista, ou `sorted()` que ordena os itens de uma lista. Essas funções são prontas para uso, assim como as ferramentas básicas na sua cozinha.

  Entender funções e como elas operam ajuda a organizar e reutilizar o código eficientemente. As funções sem retorno realizam ações, as funções com retorno fornecem resultados utilizáveis, e as funções internas do Python são ferramentas prontas que tornam a programação mais fácil e rápida. Com essas ferramentas, você pode começar a construir programas mais complexos e funcionais!

### Condicionais

**Condicionais** são instruções que permitem ao programa tomar decisões diferentes com base em certas condições. Elas são como bifurcações na estrada: "Se for por esse caminho, faça isso; se for por aquele caminho, faça aquilo."

### Exemplo Real de Condicionais

Imagine que você está decidindo o que vestir com base no clima:

1. **Se estiver frio**, você veste um casaco.
2. **Se estiver quente**, você veste uma camiseta.
3. **Se estiver chovendo**, você leva um guarda-chuva.

### Condicionais em Programação

Em programação, usamos condicionais para fazer decisões semelhantes. O Python tem a estrutura `if`, `elif` (else if), e `else` para isso.

### Estrutura de Condicionais

- **If**: Se uma condição é verdadeira, execute um bloco de código.
- **Elif**: Se a condição anterior não for verdadeira, mas esta condição for, execute outro bloco de código.
- **Else**: Se nenhuma das condições anteriores for verdadeira, execute este bloco de código.

Vamos aprofundar no exemplo do clima para entender como isso funciona na vida real e depois em programação:

1. **Se estiver frio** (condição verdadeira), você decide vestir um casaco (ação).
2. **Senão, se estiver quente** (segunda condição verdadeira), você decide vestir uma camiseta (outra ação).
3. **Senão** (nenhuma das condições anteriores é verdadeira), você decide que vai vestir algo apropriado para o clima indefinido, como roupas confortáveis (ação padrão).

### Exemplo de Condicionais em Programação

Vamos transformar o exemplo da vida real em uma explicação de como isso funcionaria em um programa.

#### Vida Real

Imagine que você tem uma lista de condições do tempo e ações correspondentes:

- **Condição**: Está frio?
  - **Ação**: Vestir um casaco.
- **Condição**: Está quente?
  - **Ação**: Vestir uma camiseta.
- **Condição**: Está chovendo?
  - **Ação**: Levar um guarda-chuva.
- **Se nenhuma condição for verdadeira**:
  - **Ação**: Vestir roupas confortáveis.

#### Programação

Pense nisso como um conjunto de instruções que o computador segue para tomar decisões:

1. **Se** (if) a temperatura está abaixo de 15 graus:
   - Ação: Vestir um casaco.
2. **Senão, se** (elif) a temperatura está acima de 25 graus:
   - Ação: Vestir uma camiseta.
3. **Senão, se** (elif) está chovendo:
   - Ação: Levar um guarda-chuva.
4. **Senão** (else):
   - Ação: Vestir roupas confortáveis.

### Exemplo Detalhado

#### Vida Real

Você acorda e olha pela janela para verificar o clima. Com base no que você vê e sente, você decide o que vestir:

- **Se está frio (abaixo de 15 graus)**: Você pega seu casaco grosso do armário e se veste.
- **Se está quente (acima de 25 graus)**: Você escolhe uma camiseta leve.
- **Se está chovendo**: Você pega seu guarda-chuva.
- **Se nenhuma dessas condições se aplica**: Você escolhe roupas que são confortáveis para um clima moderado.

#### Programação

Vamos traduzir isso em uma estrutura condicional que um computador possa entender:

- **If**: Se a temperatura < 15:
  - Ação: Vestir um casaco.
- **Elif**: Se a temperatura > 25:
  - Ação: Vestir uma camiseta.
- **Elif**: Se está chovendo:
  - Ação: Levar um guarda-chuva.
- **Else**: Para qualquer outro caso:
  - Ação: Vestir roupas confortáveis.

### Condições Compostas

Às vezes, você precisa checar mais de uma condição ao mesmo tempo. Vamos ver um exemplo da vida real e como isso se traduz na programação:

#### Vida Real

- **Se está frio e chovendo**: Você veste um casaco e leva um guarda-chuva.
- **Se está quente e ensolarado**: Você veste uma camiseta e coloca óculos de sol.

#### Programação

Usamos operadores lógicos como **and** (e) e **or** (ou) para combinar condições:

- **If**: Se (temperatura < 15 **and** está chovendo):

  - Ação: Vestir um casaco e levar um guarda-chuva.

- **Elif**: Se (temperatura > 25 **and** está ensolarado):

  - Ação: Vestir uma camiseta e colocar óculos de sol.

  

**Condicionais** permitem que o programa tome decisões baseadas em condições específicas.

**If** é usado para verificar se uma condição é verdadeira.

**Elif** (else if) permite checar outra condição se a primeira for falsa.

**Else** define o que fazer se nenhuma das condições anteriores for verdadeira.

**Condições compostas** permitem verificar múltiplas condições ao mesmo tempo usando operadores lógicos.

Condicionais são fundamentais para criar programas que possam reagir de maneira inteligente a diferentes situações. Assim como na vida real, onde você toma decisões com base nas condições ao seu redor, em programação, as condicionais permitem que seu código tome decisões e se comporte de maneiras diferentes dependendo das circunstâncias.

### Erros e Exceções

Na programação, **erros** são inevitáveis. Eles ocorrem quando algo dá errado durante a execução do programa. **Exceções** são um tipo específico de erro que pode ser previsto e tratado para evitar que o programa pare de funcionar abruptamente.

### Exemplo Real de Erros

Imagine que você está tentando abrir uma porta com uma chave. Se a chave não for a correta, você não consegue abrir a porta. Esse é um erro.

### Exceções em Programação

Na programação, exceções são como sinais de alerta que indicam que algo deu errado. Em vez de simplesmente parar, o programa pode lidar com a situação e tentar continuar.

### Exemplo Real de Exceções

Vamos usar um exemplo do cotidiano:

1. **Erro**: Você tenta ligar o carro, mas a bateria está descarregada.
2. **Exceção**: Você percebe que a bateria está descarregada e decide usar cabos de emergência para recarregá-la.

### Lidando com Exceções em Programação

Em Python, usamos `try` e `except` para lidar com exceções. Vamos explorar isso com exemplos da vida real e na programação.

### Vida Real: Erros e Exceções

1. **Erro Comum**: Você tenta usar uma chave errada para abrir a porta.
   - **Exceção**: Você percebe o erro e procura a chave correta.

2. **Erro Comum**: Você coloca um endereço errado no GPS.
   - **Exceção**: O GPS avisa que o endereço não existe e pede para você inserir um novo endereço.

### Programação: Erros e Exceções

1. **Erro Comum**: Tentar dividir um número por zero.
   - **Exceção**: Capturar o erro e exibir uma mensagem informando que a divisão por zero não é permitida.

2. **Erro Comum**: Tentar abrir um arquivo que não existe.
   - **Exceção**: Capturar o erro e informar que o arquivo não foi encontrado.

### Estrutura de `try` e `except`

- **try**: Tentar executar um bloco de código.
- **except**: Executar um bloco de código alternativo se ocorrer um erro.

### Exemplo Detalhado

#### Vida Real

Imagine que você está tentando assar um bolo, mas pode haver vários problemas (exceções) que você precisa lidar:

1. **Tentar assar o bolo**: Você segue a receita e coloca o bolo no forno.
2. **Erro potencial**: O forno não liga.
   - **Exceção**: Verificar se o forno está conectado e tentar novamente.
3. **Erro potencial**: Você esquece de adicionar açúcar.
   - **Exceção**: Perceber o erro, tirar o bolo do forno, adicionar açúcar e tentar assar novamente.

#### Programação

Vamos traduzir isso em um exemplo de programação:

1. **Tentar executar o código**:

   ```python
   try:
       # Tentar abrir um arquivo e ler o conteúdo
       arquivo = open('meuarquivo.txt', 'r')
       conteudo = arquivo.read()
   ```

2. **Erro potencial**: O arquivo não existe.

   - **Exceção**:

     ```python
     except FileNotFoundError:
         print("Arquivo não encontrado. Verifique o nome do arquivo e tente novamente.")
     ```

### Exemplo

#### Vida Real

Você está tentando preparar uma refeição e encontra problemas ao longo do processo:

1. **Tentar preparar a refeição**: Seguir a receita.
2. **Erro potencial**: Faltam ingredientes.
   - **Exceção**: Ir ao mercado comprar os ingredientes que faltam.
3. **Erro potencial**: O fogão não acende.
   - **Exceção**: Verificar o fornecimento de gás ou usar um fogão elétrico.

#### Programação

Vamos usar um exemplo em Python para explicar como lidar com diferentes tipos de erros:

```python
try:
    # Tentar abrir um arquivo e ler o conteúdo
    arquivo = open('meuarquivo.txt', 'r')
    conteudo = arquivo.read()
    
    # Tentar dividir um número por outro
    resultado = 10 / 0

except FileNotFoundError:
    # Exceção se o arquivo não for encontrado
    print("Arquivo não encontrado. Verifique o nome do arquivo e tente novamente.")

except ZeroDivisionError:
    # Exceção se houver uma divisão por zero
    print("Erro: Divisão por zero não é permitida.")

finally:
    # Código que será executado independentemente de haver uma exceção ou não
    print("Finalizando a tentativa de execução.")
```

Erros e exceções são parte do processo de programação. Compreender como prever e tratar exceções permite que seus programas sejam mais robustos e menos propensos a falhas. Usar `try` e `except` é como ter um plano de contingência: você espera pelo melhor, mas está preparado para lidar com problemas se eles surgirem.

### Debugger

Um **debugger** é uma ferramenta que os programadores usam para encontrar e corrigir erros (bugs) em seus programas. É como ter um detetive que ajuda a investigar e resolver problemas no código.

### Exemplo Real de Debugger

Imagine que você está construindo uma casa e percebe que a luz de um dos quartos não está funcionando. Você chama um eletricista para encontrar e consertar o problema. O eletricista é como um debugger, ele identifica onde está o problema na fiação e o resolve.

### Debugger em Programação

No desenvolvimento de software, usamos um debugger para examinar o código passo a passo e entender o que está acontecendo em cada etapa da execução do programa.

### Funcionalidades do Debugger

1. **Pontos de Interrupção**: Você pode definir pontos no código onde o debugger deve parar a execução para que você possa inspecionar variáveis e o estado do programa.

2. **Execução Passo a Passo**: Você pode executar o programa linha por linha para ver como as variáveis mudam em cada etapa.

3. **Inspeção de Variáveis**: Você pode verificar o valor das variáveis em diferentes momentos para entender o comportamento do programa.

4. **Análise de Pilha**: O debugger mostra a hierarquia das funções que estão sendo chamadas, o que ajuda a rastrear a origem de um erro.

### Exemplo 

Imagine um programa simples em Python que calcula a média de uma lista de números:

```python
def calcular_media(lista_numeros):
    total = 0
    for numero in lista_numeros:
        total += numero
    media = total / len(lista_numeros)
    return media

# Lista de números para calcular a média
numeros = [10, 20, 30, 40, 50]

# Chamada da função para calcular a média
resultado = calcular_media(numeros)

# Exibir o resultado
print("A média dos números é:", resultado)
```

Suponha que você encontre um erro na média calculada e deseja usar um debugger para investigar:

1. **Pontos de Interrupção**: Você define um ponto de interrupção na linha `media = total / len(lista_numeros)` para ver o valor das variáveis `total`, `len(lista_numeros)` e `media` antes e depois dessa operação.

2. **Execução Passo a Passo**: Você inicia o debugger e observa como as variáveis mudam à medida que o programa é executado linha por linha.

3. **Inspeção de Variáveis**: Você verifica os valores das variáveis `total`, `len(lista_numeros)` e `media` em diferentes etapas para entender como o cálculo da média está sendo feito.

4. **Análise de Pilha**: O debugger mostra a hierarquia das chamadas de função, mostrando de onde veio a chamada para `calcular_media` e ajudando a identificar possíveis erros na lógica do programa.

O debugger ajuda a identificar e corrigir problemas no código de maneira eficiente. Assim como um detetive que investiga um caso, o debugger ajuda a investigar e resolver os "mistérios" que podem surgir durante o desenvolvimento de software.

<p align="center">
Desenvolvido com :purple_heart:  
</p>
