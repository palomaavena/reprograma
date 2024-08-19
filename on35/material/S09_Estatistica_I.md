<h1 align="center">
  <img src="assets/reprograma-fundos-claros.png" alt="logo reprograma" width="500">
</h1>

<h1 align="center">  Estatística com Python: Probabilidade e Amostragem 📊 </h1>
<h3 align="center">  Turma ON35 | Python | Semana 09 | 2024 | Professora Deborah Foroni  </h3>

<br>


## 1.	Importância da Estatística para Analistas de Dados

    •	Interpretar e analisar dados
    •	Entender padrões, testar hipóteses e fazer previsões

## 2.	Razões para Aprender Estatística

    1.	Estatística Descritiva: Descreve e resume dados.
    2.	Inferência: Faz inferências sobre uma população a partir de uma amostra.
    3.	Modelagem: Constrói modelos para prever comportamentos futuros.
    4.	Teste de Hipóteses: Testa suposições e verifica teorias.
    5.	Identificação de Anomalias: Detecta outliers ou anomalias nos dados.

## 3.	Tipos de Dados

    o	Quantitativos (Numéricos)
         Contínuos: Valores em um intervalo contínuo (altura, distância)
        Discretos: Valores em um conjunto especificado (contagem de eventos)
        
    o	Qualitativos (Categóricos)
        Nominal: Sem ordem (estado de residência)
        Ordinal: Com ordem (avaliação de desempenho)
        Binário: Apenas duas categorias (Verdadeiro/Falso)

## 4.	Medidas de Tendência Central e Medidas de Dispersão

    Média
        o	Valor central dos dados.
        o	Fórmula: Soma dos valores / Número de observações
        o	Exemplo: Média das idades = (35 + 45 + 23 + 25 + 37)/5 = 33.0

    Mediana
        o	Valor que divide um conjunto ordenado em duas partes iguais.
        o	Fórmula: Mediana = valor central (número ímpar) ou média dos dois valores centrais (número par)
        o	Exemplo: Mediana das idades = 35
    Moda
        o	Valor mais frequente.
        o	Exemplo: Moda da escolaridade = 5

    Variância
        o	Mede a dispersão dos dados em relação à média.
        o	Fórmula: Soma das diferenças ao quadrado / Número de observações
        o	Exemplo: Variância das idades = 82

    Desvio Padrão
        o	Raiz quadrada da variância.
        o	Exemplo: Desvio padrão das idades = 9.06

    Função describe do Pandas
        •	Retorna estatísticas descritivas resumidas para um dataframe.
            o	Para colunas numéricas: count, mean, std, min, 25%, 50%, 75%, max
            o	Para colunas de objetos: count, unique, top, freq

## 5. Probabilidade

    Definição
        o	Medida da chance de um evento ocorrer (0 a 1).
        o	Evento: Resultado específico ou conjunto de resultados possíveis.
    
    Tipos de Probabilidade
        o	Clássica: Razão entre resultados favoráveis e total de resultados.
        o	Frequentista: Frequência relativa de um evento em um grande número de repetições.
        o	Subjetiva: Baseada na opinião ou experiência pessoal.

    Regras de Probabilidade
        o	Soma: Probabilidade da união de eventos mutuamente exclusivos.
        o	Multiplicação: Probabilidade da interseção de eventos independentes.
        o	Condicional: Probabilidade de um evento ocorrer dado que outro evento já ocorreu.

## 6. Amostragem


    Amostragem Aleatória Simples:
    Cada elemento da população tem a mesma chance de ser selecionado.

    Amostragem Estratificada:
    Divisão da população em subgrupos homogêneos (estratos) e seleção aleatória dentro de cada estrato.

    Amostragem por Conglomerados:
    Divisão da população em grupos naturais (conglomerados) e seleção aleatória de alguns conglomerados para análise completa.

    Amostragem Sistemática:
    Seleção do primeiro elemento aleatoriamente e dos demais a intervalos regulares.

---

### 🔗 Links Úteis

1. **[Doc Numpy](https://numpy-org.translate.goog/devdocs/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt-BR&_x_tr_pto=sc)** :  A base para cálculos numéricos com arrays multidimensionais, fornecendo funções para média, mediana, moda, variância e desvio padrão.
2. **[Doc Pandas](https://pandas-pydata-org.translate.goog/docs/?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt-BR&_x_tr_pto=sc)** : Permite manipular e analisar dados estruturados em forma tabular, facilitando cálculos e visualização.
3. **[Doc Random](https://docs.python.org/pt-br/3/library/random.html)** : Usada para gerar números aleatórios e simular eventos aleatórios, como o lançamento de uma moeda.
4. **[Doc Scipy.stats](https://docs-scipy-org.translate.goog/doc/scipy/reference/stats.html?_x_tr_sl=en&_x_tr_tl=pt&_x_tr_hl=pt-BR&_x_tr_pto=sc)** : Usada para cálculos estatísticos mais avançados, incluindo a função mode() para encontrar a moda e o cálculo de intervalos de confiança.


<br>


<p align="center">
Desenvolvido com :purple_heart:  
</p>
