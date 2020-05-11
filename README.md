# 
<h2 align="center">
    <img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/pandas.png" width="200px" /><br/>🐼 Dominando Pandas
</h2>

 <p align="justify">
    O Pandas é um framework python utilizado para <Strong>manipulação</Strong>, <Strong>leitura</Strong> e <strong>visualização de dados</strong>, oferecendo alto desempenho para pequenas quantidade de dados, quanto para enormes. por padrão o pandas faz a conversão de dados para um objeto chamado <strong>Dataframe</strong>, armazenando o conteúdo na memória RAM da sua máquina para que os dados possam ser manipulados sem sofrer alteração no arquivo/variável inicial.
 </p>
 <hr/>
 
  <p align="justify">
   Pandas é um framework robusto e de fácil adaptação, com destaque na conversão de dados, facilmente lêmos um arquivo e convertemos em um Dataframe, assim como facilmente o transformamos em um arquivo estático para armazenamento.
 </p>
 <hr/>
 
 <img alt="BeTheHero" title="#delicinha" src="https://pandas.pydata.org/docs/_images/02_io_readwrite1.svg"  />
 
    
## 💿Como Instalar?

Utilizando Pype:
```sh
pip install pandas
```
Utilizando o ambiente Anaconda:
```sh
conda install pandas 
```

## ⌨️ Iniciando com pandas:

Para iniciarmos, podemos criar nossos dataframes utilizando os tipos de variáveis que estamos habituados a utilizar, como é o caso de dicionários (representação de chave e valor similares à arquivos [JSON](https://www.json.org/json-pt.html)), assim como as famosas listas.

```sh
[01]: import pandas  as pd
```
```sh
[02]: data = {
'Estados': ['Pará', 'Rio de Janeiro', 'São Paulo'],
'Capital': ['Belém', 'Rio de Janeiro', 'São Paulo'],
'População': [143474, 12180000, 6320000]
}
```
```sh
[03]: df_estados = pd.DataFrame(data) # Transformará a variável "data" do tipo dict em um dataframe
      df_estados
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/demo.PNG"/>

```sh
[04]:  comidas = ["maçã","banana","abacate","uva","cereja","pêra"]
```
```sh
[05]:  df_comidas = pd.DataFrame(comidas, columns=["Comidas"]) # Atribuindo nome de colunas com o parâmetro "columns"
       df_comidas
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/comidas.PNG"/>

<hr/>

## 🔎 Análise de dados com Pandas:

Em geral, quando pegamos uma base de dados nova, precisamos verificar com que tipo de dados estamos lidando, para isto, iremos analizar uma base de dados famosa sobre passageiros do Titanic extraída da plataforma [Kaggle](https://www.kaggle.com/).

```sh
[06]: df = pd.read_csv("titanic_data.csv") # Certifique-se que o arquivo está no mesmo diretório que seu código
      df.head(5) # Retorna as primeiras linhas do dataframe (por padrão 5)
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/head.PNG"/>

Para começar nossa análise, usaremos o método describe que retorna dados estatísticos sobre o Dataframe

```sh
[07]: df.describe()
```

<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/describe.PNG"/>

- Para informações básicas: 
```sh
df.shape #Retorna uma tupla contendo a quantidade de linhas e colunas do DataFrame
df.index #Descrição do Index
df.columns #Colunas presentes no DataFrame
df.count() #Contagem de dados não-nulos
```
- Para resumo dos dados: 
```sh
df.sum() #Soma dos valores de um DataFrame
df.min() #Menor valor de um DataFrame
df.max() #Maior valor
df.mean() #Média dos valores
df.median() #Mediana dos valores
```
- Para Ordenação dos dados: 
```sh
df.sort_values() #Ordenando em ordem crescente
df.sort_values(ascending=False) #Ordenando em ordem decrescente
```
## 🖥️ Dataframe avançado:

Além de métodos para análise, o DataFrame possui um enorme leque de funcionalidades para quem deseja manipular dados.
Podemos criar uma função comum que receba um valor e divida pela sua metade e submeter ao nosso Dataframe

```sh
[08]: def dividir_população(quantidade):
        return quantidade/2
```
```sh
[09]: df["População"] = df["População"].apply(dividir_população)
      df
```


<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/função.PNG"/>

```sh
[10]: df["Estados"] = df["Estados"].apply((lambda x: x.lower()))
      df
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/lambda.PNG"/>

- Filtragem de dados com Pandas

```sh
df[df['População'] > 200000]  #Filtrando o DataFrame para mostrar apenas valores maiores que 200000
df.loc[0, 'Estados'] #Selecionando a primeira linha da coluna país 
```



## 📈 Visualização de dados com Pandas:

```sh
[11]: df = pd.read_csv("air_quality_no2.csv") # Base de dados da qualidade do Ar
      df.plot.area(figsize=(12, 4), subplots=True)
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/grafico.png"/>



## 🤝 Como contribuir

- Faça um fork desse repositório;
- Cria uma branch com a sua feature: `git checkout -b minha-feature`;
- Faça commit das suas alterações: `git commit -m 'feat: Minha nova feature'`;
- Faça push para a sua branch: `git push origin minha-feature`.

Depois que o merge da sua pull request for feito, você pode deletar a sua branch.

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

----

Made with ♥ by Luis Henriques :wave: [Get in touch!](https://www.linkedin.com/in/luis-eduardo-da-rocha-henriques-462714164/)
