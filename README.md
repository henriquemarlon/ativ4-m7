# Previsão de Faixa Etária Utilizando Linear Discriminant Analysis

- Este projeto desenvolve uma aplicação FastAPI para prever a faixa etária de uma pessoa com base em três variáveis: gênero, score bancário (de 1 a 100) e renda anual (em dólares/ano). O modelo de previsão é construído utilizando Linear Discriminant Analysis e é servido através de uma API criada com FastAPI.

### Demonstração em Vídeo:

https://youtu.be/8ICWlsHuSTg

### Estrutura do Projeto:

- Aqui está uma explicação detalhada da estrutura do diretório do projeto:

```
├── app.py                # Arquivo principal que contém o código FastAPI para servir o modelo
├── Dockerfile            # Arquivo Dockerfile para conteinerizar a aplicação
├── etl                   # Diretório com scripts e dados para ETL
│   ├── Exploracao_dados.ipynb  # Notebook Jupyter para a exploração de dados
│   ├── logs.log         # Arquivo de log
│   └── Mall_Customers.csv # Dados de entrada em formato CSV
├── .git                 # Diretório do sistema de controle de versão Git
├── Modelo.pkl           # Arquivo contendo o modelo treinado usando Linear Discriminant Analysis
├── README.md            # Este arquivo README com instruções e informações do projeto
├── requirements.txt     # Arquivo com as dependências necessárias para rodar o projeto
└── templates            # Diretório com templates HTML
    └── index.html      # Template HTML para a interface do usuário
```

### Dependências:

- O projeto requer as seguintes dependências, que podem ser instaladas manualmente ou através do Docker (veja instruções abaixo):

        pycaret==3.0.4
        uvicorn==0.23.2
        fastapi==0.103.1
        pydantic==2.3.0
        pandas==1.5.3

### Executando a Aplicação com Docker:

- ***Para rodar a aplicação usando Docker, siga as instruções abaixo:***


    Primeiro, faça o pull da imagem Docker com o seguinte comando:

    ```bash
    docker pull henriquemarlon/ativ4-m7:1.0.0
    ```

    Em seguida, rode a aplicação com o comando:

    ```bash
    docker run -p 8000:8000 henriquemarlon/ativ4-m7:1.0.0
    ```

### ***Agora, você pode acessar a aplicação através do navegador no endereço http://0.0.0.0:8000.***
### Como Usar

- Na interface web da aplicação, você encontrará um formulário onde poderá inserir os detalhes:



    Score Bancário (1-100)
    Renda Anual (em dólares/ano)
    Gênero (Feminino/Masculino)
    Após preencher os campos, clique em "Enviar" para obter a previsão da faixa etária, que é calculada pelo modelo Linear Discriminant Analysis e exibida na página.


### Contribuindo
- Estamos abertos a contribuições! Se deseja colaborar com o projeto, sinta-se à vontade para criar um pull request.

