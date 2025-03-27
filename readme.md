📌 Nome do Projeto

api-vendas-csv
📄 Descrição

Uma API simples feita com Flask que lê um arquivo CSV (advertise.csv) contendo dados de vendas e retorna o total de vendas via uma rota HTTP (/pegarvendas). Também inclui um exemplo de consumo da API com requests.
🚀 Funcionalidades

    GET /
    Verifica se a API está online. Retorna: "API está online".

    GET /pegarvendas
    Lê o arquivo advertise.csv e retorna a soma da coluna Vendas.

📂 Estrutura esperada do CSV

O arquivo advertise.csv deve conter, no mínimo, a seguinte coluna:
Vendas
1000
1500
2000
🧪 Exemplo de Requisição com Python

import requests

link = 'http://127.0.0.1:5000/pegarvendas'
resposta = requests.get(link)

print(resposta.json()) # {'total_vendas': 4500}

🛠️ Bibliotecas Utilizadas

    pandas: leitura e manipulação do CSV.

    flask: criação da API.

    requests: consumo da API (cliente).

▶️ Como Rodar

    Instale as dependências (pode usar um requirements.txt):

pip install flask pandas requests

Certifique-se de que o arquivo advertise.csv está na mesma pasta.

Execute o servidor:

python nome_do_arquivo.py

Em outro terminal (ou no mesmo, depois), execute o script de consumo da API.
