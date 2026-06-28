# Análise Histórica e de Correlação do Bitcoin 🪙📈

Este projeto foi desenvolvido como parte do trabalho de **Fundamentos em Ciência de Dados**, com o objetivo de analisar a cotação histórica do Bitcoin, sua volatilidade, drawdowns, e investigar suas correlações com diversos outros ativos financeiros relevantes do mercado global e nacional.

## 👥 Integrantes do Grupo
* **Pedro Henrique de Oliveira Covisi**
* **Lucca Teodoro Vaz**

---

## 📊 Origem dos Dados

Para a realização das análises e modelagens, o projeto utiliza duas fontes principais de dados:

1. **Yahoo Finance API (Coleta Dinâmica via biblioteca `yfinance`):**
   Os dados diários são extraídos em tempo real a partir de **01/01/2020** para os seguintes ativos e índices:
   * **Bitcoin (`BTC-USD`)**: Principal criptomoeda e foco central do estudo.
   * **Ethereum (`ETH-USD`)**: Segunda maior criptomoeda, utilizada para correlação intrassetorial.
   * **S&P 500 (`^GSPC`)**: Representação do mercado acionário americano das 500 maiores empresas.
   * **Nasdaq (`^IXIC`)**: Índice composto majoritariamente por empresas de tecnologia.
   * **Ibovespa (`^BVSP`)**: Principal índice do mercado de ações brasileiro.
   * **Ouro (`GC=F`)**: Contratos futuros de ouro (commodity de segurança/reserva de valor).
   * **Petróleo (`CL=F`)**: Contratos futuros de petróleo bruto (WTI), principal commodity energética.
   * **Índice Dólar (`DX-Y.NYB`)**: Índice DXY, medindo a força do dólar americano contra uma cesta de moedas fortes.

2. **Base de Dados Histórica do Bitcoin (Arquivo CSV):**
   * Armazenada localmente em `data/bitcoin_dataset.csv`.
   * Contém o histórico diário do preço do Bitcoin desde **17/09/2014**.
   * Variáveis inclusas: *Date*, *Open*, *High*, *Low*, *Close*, *Adj Close* e *Volume*.

---

## ⚙️ Pré-requisitos e Instalação

Siga os passos abaixo para preparar o ambiente e rodar o projeto localmente:

### 1. Criar e ativar um Ambiente Virtual (Recomendado)
Para evitar conflitos com outras bibliotecas Python instaladas em seu sistema, crie um ambiente virtual (`venv`):

* **No Linux/macOS:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```
* **No Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```
* **No Windows (Prompt de Comando):**
  ```cmd
  python -m venv venv
  .\venv\Scripts\activate.bat
  ```

### 2. Instalar as dependências pelo `requirements.txt`
Com o ambiente virtual ativo, instale todas as bibliotecas necessárias executando:
```bash
pip install -r requirements.txt
```

As principais bibliotecas instaladas incluem:
* `pandas` e `numpy` para manipulação de dados.
* `yfinance` para coleta de dados financeiros históricos do Yahoo Finance.
* `matplotlib` e `seaborn` para visualizações gráficas de alta qualidade.
* `jupyter` e `ipykernel` para executar o notebook interativo.

---

## 🚀 Como Rodar o Projeto

Com as dependências devidamente instaladas, você pode rodar as análises através do Jupyter Notebook.

### Opção 1: Via Jupyter Notebook no Navegador
1. Inicie o servidor do Jupyter:
   ```bash
   jupyter notebook
   ```
2. No seu navegador, abra a pasta `notebooks` e selecione o arquivo `BTC.ipynb`.
3. Execute as células sequencialmente para visualizar o pré-processamento, a análise exploratória e os gráficos gerados.

### Opção 2: Via Visual Studio Code (VS Code)
1. Abra a pasta do projeto no VS Code.
2. Certifique-se de que a extensão **Jupyter** está instalada no VS Code.
3. Abra o arquivo `notebooks/BTC.ipynb`.
4. No canto superior direito do editor do notebook, selecione o kernel correspondente ao seu ambiente virtual (`venv`).
5. Execute as células normalmente.

---

## 📈 Perguntas Investigadas no Projeto
O projeto busca responder e representar graficamente/matematicamente as seguintes questões:
1. Contextualização histórica do preço do Bitcoin.
2. Análise da volatilidade e períodos de drawdown da criptomoeda.
3. Impacto da sazonalidade (dias da semana) nos movimentos de preços.
4. Correlação histórica e contemporânea do Bitcoin com outros mercados (ações, commodities, moedas fiduciárias e ouro).
5. Tendências de comportamento de preço a longo prazo.
