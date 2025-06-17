# Monitoramento de Gasto de Insumos (Água, Energia e Produtos de Higiene)

> Projeto em Python para monitorar o consumo doméstico de insumos essenciais, com dashboards interativos e API local.

---

## Objetivo

Este projeto tem como finalidade **ajudar usuários a acompanharem e visualizarem seus gastos com água, energia elétrica e produtos de higiene pessoal**. Através de uma interface interativa e uma API local, o sistema permite registrar, consultar e analisar os dados de consumo ao longo do tempo.

---

## Funcionalidades

- 📊 Dashboards interativos com gráficos de consumo em R$ e por categoria (água, energia, higiene)
- ✍️ Tela para inserção manual de dados de consumo
- 🔌 API local desenvolvida com **FastAPI**, com endpoints para envio e recuperação de dados
- 📁 Banco de dados local persistente com **SQLite**

---

## Tecnologias Utilizadas

| Tecnologia    | Descrição                                             |
|---------------|-------------------------------------------------------|
| `Streamlit`   | UI interativa e dashboards + hospedagem gratuita      |
| `FastAPI`     | Criação da API REST para endpoints de consumo         |
| `SQLite`      | Banco de dados leve e local                           |
| `SQLAlchemy`  | ORM para manipulação e serialização de tabelas        |
| `Pandas`      | Manipulação de DataFrames e consulta ao banco         |
| `Matplotlib`  | Geração de gráficos personalizados                    |
| `Plotly`      | Visualizações interativas nos dashboards              |

---

## Estrutura do Projeto

```plaintext
/
├── ui/                         # Interface com Streamlit
│   ├── PaginaCentral/         # Página principal do app
│   ├── pages/                 # Subpáginas dos dashboards
│   │   ├── Agua.py            # Dashboard de água
│   │   ├── Energia.py         # Dashboard de energia
│   │   ├── ProdHigiene.py     # Dashboard de higiene
│   │   ├── InserirDados.py    # Formulário de inserção de dados
│   ├── db.py                  # Conexão e criação do banco
│   ├── util.py                # Funções auxiliares
├── api/                       # Backend FastAPI
│   ├── app/                   # Arquivos principais da API
│   ├── models/                # Schemas / modelos de dados
│   ├── tables/                # Definições de tabelas SQLAlchemy
├── consumo.db                 # Banco de dados local (SQLite)
├── requirements.txt           # Dependências do projeto
├── README.md                  # Este documento
