# banco-api-performance

Repositório de testes de performance utilizando [k6](https://k6.io/) com scripts escritos em JavaScript.

## 🧭 Introdução

Este projeto tem como objetivo realizar testes de carga e desempenho em APIs REST, com foco em simular usuários reais e validar tempo de resposta e estabilidade da aplicação.

## ⚙️ Tecnologias Utilizadas

- [k6](https://k6.io/) — Ferramenta de teste de performance de código aberto
- JavaScript — Linguagem para escrita dos testes
- Node.js — Utilizado para organização do ambiente de testes e utilitários

## 📁 Estrutura do Repositório

```
banco-api-performance/
├── config/               # Configurações de ambiente
├── fixtures/             # Arquivos de dados usados nos testes (ex: JSON de login)
├── helpers/              # Funções auxiliares (ex: autenticação)
├── tests/                # Scripts de testes organizados por endpoint
├── utils/                # Variáveis e configurações globais
└── README.md             # Documentação do projeto
```

## 🎯 Objetivo de Cada Grupo de Arquivos

- `config/`: Contém configurações específicas do ambiente local, como `config.local.json`.
- `fixtures/`: Armazena os dados que serão enviados durante os testes (por exemplo, corpo da requisição de login).
- `helpers/`: Contém funções auxiliares reutilizáveis, como a geração de token.
- `tests/`: Scripts de testes organizados por funcionalidades da API (login, transferências, etc).
- `utils/`: Funções e variáveis globais como `BASE_URL`.

## 🚀 Modo de Instalação

1. Clone o repositório:

```bash
git clone https://github.com/matheusalexan/banco-api-performance.git
cd banco-api-performance
```

2. Instale o [k6](https://k6.io/docs/getting-started/installation/).

## 🧪 Execução dos Testes

Antes de executar os testes, defina a variável de ambiente `BASE_URL`, apontando para a API a ser testada:

```bash
export BASE_URL=https://sua-api.com
```

### ✅ Execução simples

```bash
k6 run tests/login.test.js
```

### 📊 Execução com relatório web em tempo real

```bash
K6_WEB_DASHBOARD=true k6 run tests/login.test.js
```

### 💾 Exportar relatório para HTML

```bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/login.test.js
```

---

📁 Repositório: [https://github.com/matheusalexan/banco-api-performance](https://github.com/matheusalexan/banco-api-performance)
