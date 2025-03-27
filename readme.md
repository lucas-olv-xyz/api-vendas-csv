# 📊 api-vendas-csv

Uma API simples feita com Flask que lê um arquivo CSV (`advertise.csv`) contendo dados de vendas e retorna o total de vendas via uma rota HTTP (`/pegarvendas`). Também inclui um exemplo de consumo da API com `requests`.

---

## 🚀 Funcionalidades

### `GET /`

Verifica se a API está online.  
**Resposta:**
API está online

### `GET /pegarvendas`

Lê o arquivo `advertise.csv` e retorna a soma da coluna `Vendas`.  
**Resposta:**

```json
{
  "total_vendas": 4500
}
```

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

    pandas: para leitura e manipulação do CSV

    flask: para criação da API

    requests: para consumo da API (cliente)

▶️ Como Rodar

    Instale as dependências:

pip install flask pandas requests

Certifique-se de que o arquivo advertise.csv está na mesma pasta do script.

Execute o servidor:

    python nome_do_arquivo.py

    Em outro terminal (ou depois), execute o script de consumo da API.

✅ Melhorias Futuras

    Adicionar tratamento de erros (arquivo não encontrado, CSV mal formatado, etc.)

    Organizar o projeto com Flask Blueprints

    Adicionar documentação automática com Swagger (flasgger ou apispec)

    Tornar o caminho do CSV configurável via variável de ambiente

    Adicionar suporte a Docker
