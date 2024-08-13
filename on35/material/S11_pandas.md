<h1 align="center">
  <img src="assets/reprograma-fundos-claros.png" alt="logo reprograma" width="500">
</h1>

# Tratamento de dados utilizando pandas e numpy

Turma Online | Semana 11 | 2024 | Professora Daviny Letícia


### Resumo
O que veremos na aula de hoje?
* Analise
* Coleta e Tratamento
* Base de dados
* Instalando
* Series e Dataframes
* Pandas

## Conteúdo
### Analise
1. Pq usamos o python para analisar dados
### Coleta e Tratamento
1. Comos são os dados no mundo real
2. Indo no INMET para baixar os dados
   * Baixando os dados
   * Processando eles

### Base de dados
1. Conhecendo os dados da base
   * Temperatura
   * Posição
   * Tempo
   * Radiação
   * Vento
   * Pressão
   * Umidade

### Instalando
1. Interfaces
   * VS Code
   * Jupyter
   * Colab
2. Modulos
   * pandas
   * numpy
   * matplotlib
3. VS Code
   * instalando modulo
4. Jupyter
   * instalando o jupyter
   * instalando o notebook
   * abrindo o jupyter
   * instalando modulo
5. Colab

### Series e Dataframes
1. Series
2. Dataframes

### Pandas
1. função read_csv()
2. função head()
3. função tail()
4. função shape
5. função describe()
6. função dtypes
7. função sample() e reset_index()
8. reduzir o dataframe
9. função columns
10. Selecionar uma coluna
11. função min(), max(), sum() e mean()
12. função isnull()
13. função dropna()
14. função fillna()
15. função replace()
16. função drop_duplicates()
17. normalização

***
### Exercícios 
* [Exercicio para sala](https://docs.google.com/spreadsheets/d/1PUtJ7kFL3YuzfPVdtaa4e-WuL8tbD1UOGELFwa4xgsg/edit?usp=sharing)
* [Exercicio para casa](https://github.com/mflilian/repo-example/tree/main/exercicios/para-casa)

### Material da aula 

### Links Úteis
- [INMET](https://portal.inmet.gov.br/)
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://numpy.org/)
- [Matplotlib](https://matplotlib.org/)
- [Jupyter](https://jupyter.org/)
- [Colab](https://colab.research.google.com/)

<p align="center">
Desenvolvido com :purple_heart:  
</p>

.

# Pandas

### 1. `read_csv()`
A função `read_csv()` é usada para ler um arquivo CSV e convertê-lo em um DataFrame do pandas.

```python
import pandas as pd

# Lê o arquivo CSV e cria um DataFrame
df = pd.read_csv('caminho/para/seu_arquivo.csv')
```

### 2. `head()`
Exibe as primeiras linhas do DataFrame. Por padrão, mostra as 5 primeiras linhas.

```python
# Exibe as 5 primeiras linhas
print(df.head())
#ou
df.head()

# Exibe as 10 primeiras linhas

print(df.head(10))
#ou
df.head(10)
```

### 3. `tail()`
Exibe as últimas linhas do DataFrame. Por padrão, mostra as 5 últimas linhas.

```python
# Exibe as 5 últimas linhas
print(df.tail())

# Exibe as 10 últimas linhas
print(df.tail(10))
```

### 4. `shape`
Retorna a quantidade de linhas e colunas do DataFrame em formato de tupla `(linhas, colunas)`.

```python
# Exibe o formato do DataFrame
print(df.shape)
```

### 5. `describe()`
Gera estatísticas descritivas para colunas numéricas, como contagem, média, desvio padrão, valores mínimo e máximo, e quartis.

```python
# Exibe estatísticas descritivas
print(df.describe())
```

### 6. `dtypes`
Retorna os tipos de dados de cada coluna no DataFrame.

```python
# Exibe os tipos de dados das colunas
print(df.dtypes)
```

### 7. `sample()` e `reset_index()`
- `sample()`: Seleciona uma amostra aleatória de linhas do DataFrame.
- `reset_index()`: Reseta o índice do DataFrame, útil após filtragens ou amostragens.

```python
# Seleciona 5 linhas aleatórias
amostra = df.sample(n=5)
#ou

df.sample(n=5)

# Reseta o índice do DataFrame amostrado
amostra_resetada = amostra.reset_index(drop=True)

print(amostra_resetada)
```

### 8. Reduzir o DataFrame
Selecionar um subconjunto de colunas e/ou linhas.

```python
# Selecionar 3 colunas específicas
df_reduzido = df[['Coluna1', 'Coluna2', 'Coluna3']]

# Selecionar 1000 linhas aleatórias
df_reduzido = df_reduzido.sample(n=1000, random_state=42)
```

### 9. `columns`
Exibe ou altera os nomes das colunas.

```python
# Exibe os nomes das colunas
print(df.columns)

# Altera os nomes das colunas
df.columns = ['NovoNome1', 'NovoNome2', 'NovoNome3']
```

### 10. Selecionar uma coluna
Você pode selecionar uma coluna específica utilizando a notação de colchetes.

```python
# Seleciona a coluna 'Coluna1'
coluna1 = df['Coluna1']
print(coluna1)
```

### 11. `min()`, `max()`, `sum()` e `mean()`
Funções para calcular o valor mínimo, máximo, soma e média, respectivamente.
Ex: 
coluna_temperatura = df['TEMPERATURA DO AR - BULBO SECO, HORARIA (°C)']
coluna_temperatura = pd.to_numeric(df('TEMPERATURA DO AR - BULBO SECO, HORARIA (°C)'), errors='coerce')
coluna_temperatura.min()
coluna_temparatura.max()
coluna_temperatura.sum()
coluna_temperatura.mean()

```python
# Valor mínimo
minimo = df['Coluna1'].min()

# Valor máximo
maximo = df['Coluna1'].max()

# Soma dos valores
soma = df['Coluna1'].sum()

# Média dos valores
media = df['Coluna1'].mean()

print(f"Mínimo: {minimo}, Máximo: {maximo}, Soma: {soma}, Média: {media}")
```

### 12. `isnull()`
Identifica valores nulos no DataFrame, retornando um DataFrame booleano.
df.isnull().sum()

```python
# Verifica valores nulos
nulos = df.isnull()
print(nulos)

# Contagem de valores nulos em cada coluna
nulos_por_coluna = df.isnull().sum()
print(nulos_por_coluna)
```

### 13. `dropna()`
Remove linhas ou colunas que contenham valores nulos.

```python
# Remove linhas com qualquer valor nulo
df_sem_nulos = df.dropna()

# Remove colunas que contenham valores nulos
df_sem_nulos_colunas = df.dropna(axis=1)
```

### 14. `fillna()`
Preenche valores nulos com um valor específico.

```python
# Preenche valores nulos com 0
df_preenchido = df.fillna(0)

# Preenche valores nulos com a média da coluna
df_preenchido_media = df.fillna(df.mean())
```

### 15. `replace()`
Substitui valores específicos no DataFrame.

```python
# Substitui todos os valores 0 por NaN
df_substituido = df.replace(0, np.nan)

# Substitui um valor específico em uma coluna
df['Coluna1'] = df['Coluna1'].replace('ValorAntigo', 'ValorNovo')

# Substitui virgula por ponto
df_amostra['PRECIPITAÇÃO TOTAL, HORÁRIO (mm)'] = df_amostra['PRECIPITAÇÃO TOTAL, HORÁRIO (mm)'].replace(',', '.', regex=True)

```

### 16. `drop_duplicates()`
Remove linhas duplicadas do DataFrame.

```python
# Remove linhas duplicadas
df_sem_duplicatas = df.drop_duplicates()

# Remove duplicatas com base em colunas específicas
df_sem_duplicatas_colunas = df.drop_duplicates(subset=['Coluna1', 'Coluna2'])
```

### 17. Normalização
A normalização é o processo de ajustar os valores das colunas para um mesmo intervalo, geralmente entre 0 e 1.
df['Coluna1_normalizada'] = (df['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'] - df['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'].min()) / (df['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'].max() - df['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'].min())

```python
# Normaliza os valores de uma coluna para o intervalo [0, 1]
df['Coluna1_normalizada'] = (df['Coluna1'] - df['Coluna1'].min()) / (df['Coluna1'].max() - df['Coluna1'].min())

# Outra forma de normalização usando o método z-score (normalização padrão)
df['Coluna1_zscore'] = (df['Coluna1'] - df['Coluna1'].mean()) / df['Coluna1'].std()
```

### 18. Outros

```python
data = {
    'A': [1, 2, 3],
    'B': [4, 5, 6],
    'C': [7, 8, 9]
}
```

```python
df_data = pd.DataFrame(data)
```

```python
df_data['A+B'] = df_data['A'] * df_data['B']
```
  
```python
df_data.head()
```



# Matplotlib

```python
pip install matplotlib
```

```python
import matplotlib.pyplot as plt
```

```python
df.head()
```

```python
df_20 = df.head(20)
```

```python
plt.figure(figsize=(12, 6))
plt.plot(df_20['Hora UTC'], df_20['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'], marker='o', linestyle='-', color='g')
plt.xlabel('Hora UTC')
plt.ylabel('Umidade (%)')
plt.title('Umidade ao Longo do Tempo')
plt.xticks(rotation=90)
plt.tight_layout()
plt.show()
```

```python
# Gráfico de Dispersão
plt.figure(figsize=(12, 6))
plt.scatter(df_20['TEMPERATURA DO AR - BULBO SECO, HORARIA (°C)'], df_20['UMIDADE REL. MAX. NA HORA ANT. (AUT) (%)'], color='y')
plt.xlabel('Temperatura (°C)')
plt.ylabel('Umidade (%)')
plt.title('Temperatura x Umidade')
plt.tight_layout()
plt.show()
```


```python
plt.figure(figsize=(12, 6))
plt.bar(df_20['Hora UTC'], df_20['PRECIPITAÇÃO TOTAL, HORÁRIO (mm)'], color='r')
plt.xlabel('Hora UTC')
plt.ylabel('Precipitação (mm)')
plt.title('Precipitação ao Longo do Tempo')
plt.xticks(rotation=90)
plt.tight_layout()
plt.show()
```



```python

```

