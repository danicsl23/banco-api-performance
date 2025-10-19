# Banco API Performance - Testes com K6

## 🧩 Introdução

Este repositório tem como objetivo realizar **testes de performance** da API do projeto *Banco API*, utilizando o **K6**, uma ferramenta open-source para testes de carga e desempenho.  
Os testes foram desenvolvidos em **JavaScript** e organizados de forma modular para facilitar a manutenção, leitura e execução dos cenários.

---

## ⚙️ Tecnologias Utilizadas

- [K6](https://k6.io) — Ferramenta principal para execução dos testes de performance.  
- **JavaScript (ES6)** — Linguagem utilizada para escrever os scripts de teste.  
- **Node.js** — Utilizado para instalação e execução de dependências, caso necessário.  
- **Variáveis de Ambiente** — Controlam URLs e parâmetros dinâmicos de execução.

---

## 📁 Estrutura do Repositório

```
banco-api-performance/
├── fixtures/
│   ├── Dados de entrada para os testes (ex: usuários)
├── helpers/
│   ├── Funções utilitárias reutilizáveis para interação com API
├── tests/
│   ├── Casos de testes organizados por módulo API
├── config/
│   └── Arquivo de configuração de variárveis de ambiente
├── utils/
│   └── Funções utilitárias reutilizáveis
└── README.md
```

---

## 🎯 Objetivo de Cada Grupo de Arquivos

| Diretório/Arquivo | Descrição |
|--------------------|-----------|
| `fixtures/` | Dados de entrada para os testes (ex: usuários). |
| `helper/` | Funções utilitárias reutilizáveis para interação com API. |
| `tests/` | Casos de testes organizados por módulo API |
| `config/` | Arquivo de configuração de variárveis de ambiente|
| `utils/` | Funções utilitárias reutilizáveis |
| `README/` | Diretório destinado à exportação dos relatórios HTML ou JSON gerados pelo K6. |

---

## 🚀 Instalação e Execução

### 1. Clonar o repositório

```bash
git clone https://github.com/danicsl23/banco-api-performance.git
cd banco-api-performance
```

### 2. Instalar o K6

Siga as instruções oficiais: [https://k6.io/docs/getting-started/installation](https://k6.io/docs/getting-started/installation)

### 3. Definir variável de ambiente obrigatória

Antes de executar qualquer teste, é necessário definir a variável de ambiente `BASE_URL`, que representa a URL base da API alvo.

Exemplo (Linux/macOS):

```bash
export BASE_URL=http://localhost:3000

No Windows (PowerShell):

```powershell
$env:BASE_URL="http://localhost:3000"
```

### 4. Executar um teste

```bash
k6 run tests/login.test.js
```

### 5. Executar com acompanhamento em tempo real e exportação do relatório

O K6 permite visualizar métricas em tempo real via dashboard local e gerar um relatório HTML automaticamente.

```bash
k6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html BASE_URL=http://localhost:3000 k6 run tests/login.test.js
```

Após a execução, o relatório `html-report.html` será gerado no diretório atual.

---

## 🌐 Repositório Oficial

[GitHub - danicsl23/banco-api-performance](https://github.com/danicsl23/banco-api-performance)

---

**Autor:** Danielle Lopes  
<<<<<<< HEAD
📅 Última atualização: Outubro de 2025
=======
📅 Última atualização: Outubro de 2025
>>>>>>> 1ef0cb335ddb93afb67dc323c5475fc3f530e5b0
