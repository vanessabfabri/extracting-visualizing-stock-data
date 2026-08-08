# 📈 Extração e Visualização de Dados de Ações com Python

🌐 Idioma:
- 🇧🇷 Português
- 🇺🇸 [Inglês](README.en.md)

## Visão Geral

Este projeto demonstra o processo de extração, limpeza, análise e visualização de dados financeiros utilizando Python.

A análise combina dois métodos diferentes de coleta de dados:

- Dados do mercado financeiro extraídos por meio da API Yahoo Finance (`yfinance`)
- Dados de receita obtidos através de Web Scraping (`BeautifulSoup`)

O projeto compara o desempenho das ações e as informações de receita de duas empresas:

- Tesla (TSLA)
- GameStop (GME)

O resultado final inclui análises históricas dos preços das ações e visualizações de receita geradas com Matplotlib.

---

## Fonte

**Fonte:** IBM Data Analyst Professional Certificate (Coursera)

**Observação:** Este projeto foi desenvolvido como parte das atividades do curso e aprimorado com documentação e análises adicionais.

---

## Objetivos

Os principais objetivos deste projeto são:

- Extrair dados históricos de ações utilizando APIs
- Aplicar técnicas de Web Scraping para coletar dados financeiros
- Limpar e preparar dados para análise
- Criar visualizações de preços de ações e receitas
- Comparar o desempenho empresarial com o comportamento do mercado financeiro
- Praticar fluxos de trabalho utilizados em projetos reais de análise de dados

---

## Tecnologias Utilizadas

- Python
- Pandas
- yFinance
- Requests
- BeautifulSoup4
- Matplotlib
- Jupyter Notebook

---

## Fluxo do Projeto

### 1. Definição da Função de Visualização

Foi utilizada uma função personalizada chamada `make_graph` para criar visualizações comparando:

- Preços históricos das ações
- Receitas históricas das empresas

Os gráficos são gerados com Matplotlib e exibem ambas as métricas ao longo do tempo.

---

## Questão 1: Extração de Dados das Ações da Tesla

Os dados históricos das ações da Tesla foram obtidos utilizando a API Yahoo Finance.

### Ticker Utilizado

```python
TSLA
```

### Atividades Realizadas

- Criação do objeto ticker da Tesla
- Download do histórico completo disponível
- Armazenamento dos dados em um DataFrame chamado `tesla_data`
- Redefinição do índice do DataFrame
- Exibição das cinco primeiras linhas

### Principais Colunas

- Date
- Open
- High
- Low
- Close
- Volume
- Dividends
- Stock Splits

---

## Questão 2: Extração da Receita da Tesla com Web Scraping

Os dados de receita da Tesla foram extraídos de uma página HTML utilizando:

```python
requests
BeautifulSoup
```

### Fonte dos Dados

Os dados de receita foram obtidos a partir de uma página HTML disponibilizada pelo laboratório da IBM Skills Network.

### Atividades Realizadas

- Download do conteúdo HTML
- Processamento da página com BeautifulSoup
- Localização da tabela **Tesla Quarterly Revenue**
- Extração dos campos:
  - Date
  - Revenue
- Criação do DataFrame:

```python
tesla_revenue
```

### Limpeza dos Dados

As seguintes transformações foram aplicadas:

- Remoção do símbolo (`$`)
- Remoção de vírgulas (`,`)
- Remoção de valores vazios
- Remoção de valores nulos

Exemplo:

```text
$21,454
```

Transformado em:

```text
21454
```

---

## Questão 3: Extração de Dados das Ações da GameStop

Os dados históricos da GameStop foram extraídos utilizando Yahoo Finance.

### Ticker Utilizado

```python
GME
```

### Atividades Realizadas

- Criação do objeto ticker da GameStop
- Download do histórico completo disponível
- Armazenamento dos dados em:

```python
gme_data
```

- Redefinição do índice do DataFrame
- Exibição das cinco primeiras linhas

---

## Questão 4: Extração da Receita da GameStop com Web Scraping

Os dados trimestrais de receita da GameStop foram obtidos através de Web Scraping.

### Atividades Realizadas

- Download do conteúdo HTML
- Processamento da página com BeautifulSoup
- Localização da tabela de receita trimestral
- Extração dos campos:
  - Date
  - Revenue

### DataFrame Gerado

```python
gme_revenue
```

### Limpeza dos Dados

- Remoção de vírgulas
- Remoção de símbolos monetários
- Remoção de registros nulos
- Remoção de valores vazios

---

## Questão 5: Visualização dos Dados da Tesla

A função personalizada de visualização foi utilizada para comparar:

- Histórico do preço das ações da Tesla
- Receita trimestral da Tesla

### Gráfico Gerado

```python
make_graph(tesla_data, tesla_revenue, "Tesla")
```

O gráfico permite visualizar a evolução da receita da empresa ao lado do comportamento de suas ações ao longo do tempo.
![Tesla](tesla_stock_graph.png)

---

## Questão 6: Visualização dos Dados da GameStop

A mesma metodologia foi aplicada aos dados da GameStop.

### Gráfico Gerado

```python
make_graph(gme_data, gme_revenue, "GameStop")
```

A visualização destaca a relação entre o desempenho financeiro da empresa e o comportamento do mercado.
![Results](gamestop_stock_graph.png)

---

## Competências Demonstradas

### Coleta de Dados

- Consumo de APIs
- Extração de Dados Financeiros
- Web Scraping

### Tratamento de Dados

- Limpeza de Dados
- Transformação de Dados
- Tratamento de Valores Ausentes

### Análise de Dados

- Análise Financeira
- Séries Temporais
- Avaliação de Indicadores de Negócio

### Visualização de Dados

- Matplotlib
- Gráficos Comparativos
- Análise de Tendências

---

## Principais Insights

### Tesla

- A Tesla apresentou crescimento significativo de receita ao longo do período analisado.
- O aumento da receita foi acompanhado por uma valorização expressiva das ações no longo prazo.
- Os dados evidenciam a rápida expansão da companhia e sua consolidação no mercado.

### GameStop

- A GameStop apresentou períodos de grande volatilidade no preço das ações.
- O comportamento das ações nem sempre acompanhou diretamente a evolução da receita.
- O caso demonstra como o sentimento do mercado pode influenciar a valorização de uma empresa além de seus fundamentos financeiros.

---

## Estrutura do Projeto

```text
.
├── Extracting_and_Visualizing_Stock_Data.ipynb
├── README.md
├── README.pt-BR.md
├── images
│   ├── tesla_stock_graph.png
│   └── gamestop_stock_graph.png
```

---

## Instalação

Clone este repositório:

```bash
git clone https://github.com/seu-usuario/extracting-visualizing-stock-data.git
```

Acesse a pasta do projeto:

```bash
cd extracting-visualizing-stock-data
```

Instale as dependências:

```bash
pip install pandas
pip install yfinance
pip install requests
pip install beautifulsoup4
pip install matplotlib
```

Ou execute:

```bash
pip install pandas yfinance requests beautifulsoup4 matplotlib
```

---

## Executando o Notebook

Abra o Jupyter Notebook:

```bash
jupyter notebook
```

Execute todas as células sequencialmente para:

1. Extrair os dados de mercado
2. Realizar o Web Scraping das receitas
3. Limpar os conjuntos de dados
4. Gerar as visualizações

---

## Melhorias Futuras

Possíveis evoluções deste projeto incluem:

- Dashboards interativos com Plotly
- Modelos de previsão de receita
- Comparação entre múltiplas empresas
- Análise de indicadores financeiros
- Automatização da coleta de dados
- Monitoramento em tempo real do mercado

---

## Sobre o IBM Data Analyst Professional Certificate

Este projeto foi desenvolvido durante o programa **IBM Data Analyst Professional Certificate**, disponibilizado na plataforma Coursera.

Entre os tópicos abordados na certificação estão:

- Python para Análise de Dados
- Visualização de Dados
- Bancos de Dados e SQL
- Data Wrangling
- Estatística Aplicada
- Dashboards
- Projetos de Análise de Dados

---

## Autora

**Vanessa Batista Fabri**

Projeto de Portfólio em Análise de Dados

📌 LinkedIn: [linkedin.com/in/vanessafabri](https://www.linkedin.com/in/vanessafabri/)

📌 GitHub: [vanessabfabri](https://github.com/vanessabfabri)

---

## Aviso

Este repositório contém um projeto educacional desenvolvido como parte do programa IBM Data Analyst Professional Certificate. O notebook foi documentado e organizado para fins de portfólio, com o objetivo de demonstrar competências em extração de dados, Web Scraping, limpeza de dados, análise exploratória e visualização utilizando Python.
