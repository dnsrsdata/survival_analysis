### Sobre o problema

Serviços por assinatura estão cada vez mais presentes no nosso dia a dia. Com
isso, é necessário que as empresas que oferecem esses serviços tenham uma
preocupação maior com a retenção de clientes. Uma das formas de se fazer isso é
através da análise de dados. Com isso, é possível identificar padrões de
comportamento que podem indicar a saída de um cliente. Com essa informação, a
empresa pode tomar ações para evitar a saída do cliente.

### Objetivo

O objetivo desse projeto é criar um modelo que seja capaz de prever quando um
cliente irá cancelar o serviço. Após a criação do modelo e projeção do tempo
de vida do cliente, será criado um relatório em PDF contendo as informações
obtidas através da análise dos dados.

### Sobre os dados

Os dados utilizados foram obtidos através do Kaggle. Os dados são referentes a
um serviço de telecomunicações. O dataset contém 7043 linhas e 21 colunas.

### Métricas de avaliação

Para avaliar o nosso modelo, iremos usar o **c-index**. Essa métrica vai de 0 a 
1, onde quanto mais próximo de 1, melhor. O c-index é uma métrica que avalia a
capacidade do modelo de prever a ordem de ocorrência dos eventos. Por exemplo,
se o modelo previu que o cliente A irá cancelar o serviço antes do cliente B,
e isso realmente aconteceu, o modelo ganha pontos. Caso contrário, ele perde.

### Melhorias

[⌛] Criar uma interface Streamlit para facilitar o entendimento do retorno
financeiro do modelo dado diferentes taxas de retenção.

### Instruções para execução do projeto

Esse projeto foi desenvolvido usando o Python 3.10.12. Para executar o projeto,
siga os passos abaixo:

1. Clone o repositório:
```sh
git clone https://github.com/dnsrsdata/survival_analysis
```
2. Instale o poetry:
```sh
pip install poetry
```
3. Instale as dependências do projeto:
```sh
poetry install
```
4. Execute os notebooks

### Descrição dos arquivos

    - data
    |- processed
    | |- Processed_Telecom_Data.csv  # Dados transformados e limpos
    |- raw
    | |- WA_Fn-UseC_-Telco-Customer-Churn.xls  # Dados brutos referentes ao churn de clientes
    |
    - images
    |- distribuicaoExpectativas.png  # Imagem contendo a distribuição das expectativas de permanência de cada cliente
    |- kaplanmeiercontratos.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo dado os tipos de contrato
    |- kaplanmeierdependentes.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo dado se o cliente tem dependentes ou não
    |- kaplanmeiergeneros.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo dado o gênero do cliente
    |- kaplanmeierparceiros.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo dado se o cliente tem parceiros ou não
    |- kaplanmeierpsenior.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo dado se o cliente é sênior ou não
    |- probabilidadesdesobrevidageral.png  # Gráfico de linhas contendo a probabilidade de permanência dos clientes ao longo do tempo
    |
    - models
    |- modelo_cox.pkl  # Modelo treinado
    |
    - notebooks
    |- EDA.ipynb  # Notebook contendo a preparação dos dados
    |- Survival_Analysis.ipynb  # Notebook contendo a experimentação dos modelos
    |
    - Relatório
    |- Analise_de_sobrevivencia.pdf  # Apresentação ppt contendo partes da análise de sobrevivência e EDA
    |
    - .gitignore  # Arquivo contendo as folders para o git ignorar
    - poetry.lock # Arquivo contendo as versões dos pacotes e suas dependências
    - pyproject.toml  # Arquivo contendo as dependências do projeto
    - README.md  # Arquivo contando informações do projeto

### Resultados

Foi criado um modelo que prevê a expectativa de permanência do cliente. Além disso,
soluções para os problemas encontrados foram propostas. O resumo dos resultados pode
ser acessado no relatório em PDF na folder **Relatórios**.