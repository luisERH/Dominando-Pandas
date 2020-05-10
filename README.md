# 
<h2 align="center">
    <img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/pandas.png" width="200px" />
</h2>
<h2 align="center">
  🐼 Dominando Pandas
</h2>


 <p align="justify">
    O pandas é um framework python utilizado para <Strong>manipulação</Strong> <Strong>leitura</Strong> e <strong>visualização de dados</strong>, oferecento alto desempenho para pequenas quantidade de dados, quanto para enormes. por padrão o pandas faz a conversão de dados para um objeto chamado <strong>dataframe</strong>, armazendo o conteúdo na memória RAM da sua máquina para que os dados possam ser manipulados sem sofrer alteração no seu arquivo/variável inicial.
 </p><hr/>
    
<center/>
    <img alt="BeTheHero" title="#delicinha" src="https://pandas.pydata.org/docs/_images/02_io_readwrite1.svg"  />
 
    
## 💿Como Instalar?
</br>

Utilizando Pype:
```sh
pip install pandas
```
Utilizando o ambiente Anaconda:
```sh
conda install pandas 
```
</br>

## ⌨️ Iniciando com pandas:
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
       comidas
```
<img alt="BeTheHero" title="#delicinha" src="https://github.com/luisERH/Dominando-Pandas/blob/master/assets/comidas.PNG"/>




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
