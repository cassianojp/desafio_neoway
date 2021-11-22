# Desafio Neoway

<p><b>Cientista de Dados:</b> Cassiano J. Pereira</p>
<p><b>Data:</b> 22/11/2021</p>

![Estrutura do Projeto](estrutura.jpg?raw=true "Estrutura do Projeto")

O código foi todo desenvolvido em linguagem Python 3.7 dentro do ambiente Jupyter Notebook 6.3.0, bastando o usuário baixar todos os arquivos em algum diretório em sua máquina e executá-los neste mesmo ambiente.

O desafio começa em uma análise exploratória dos dados, no arquivo *desafio_neoway_eda.ipynb*, para entender melhor as variáveis do problema.
Nesta etapa é feita também o tratamento dos dados faltantes e a junção da tabela de conexões com os respectivos indivíduos pertencentes a tabela de individuos.
Este processo gera mais três bases de dados em formato csv: 
* *individuos_tratada.csv* (base de indivíduos com os dados faltantes tratados);
* *individuos_conexoes_v1* (junção da base de conexões com a base dos indivíduos tratada);
* *individuos_conexoes_v2* (junção da base de conexões com a base dos indivíduos, porém esta última com os registros faltantes completamente removidos).

A etapa seguinte, se concentra em criar um modelo que tenta prever as taxas de contágio do restante da população. Por se tratar da predição de uma variável independente contínua, optou-se pelo modelo de Regressão Linear. Nesta etapa, aplicou-se a Regressão, tanto na base individuos_conexoes_v1 (com os dados faltantes tratados), como na base individuos_conexoes_v2 (com os registros faltantes dos individuos completamente removidos). Como demonstrado no arquivo *desafio_neoway_model*, a base com os dados faltantes completamente removidos apresentou um modelo com uma melhor *performance* nas previsões. Após a predição das taxas de contágio do restante da população, foi gerado uma nova base de dados contendo agora a informação completa, tanto das taxas de contágio, conexões e informações sobre esses indivíduos relacionados: *individuos_conexoes_previstos.csv*


 