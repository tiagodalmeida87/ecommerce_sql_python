# 🚀 **Análise de Vendas de E-commerce com SQL e Python: Do Dado Bruto ao Insight de Negócio**

![Capa do Projeto](https://github.com/tiagodalmeida87/ecommerce_sql_python/blob/main/result/dashboard_final_pro.jpg)

# 🎯 Problema de Negócio
No cenário altamente competitivo do comércio eletrônico, a capacidade de transformar dados brutos de transações em informações estratégicas é um diferencial decisivo. Uma empresa de e-commerce possuía uma base de dados com 10.000 registros de vendas, contendo informações sobre clientes, produtos, categorias, quantidades, preços, vendedores e localizações. O desafio consistia em estruturar esses dados, que estavam dispersos em um arquivo CSV, para responder a perguntas cruciais de negócio, como a identificação dos produtos mais rentáveis, o desempenho por categoria, o ticket médio dos clientes e a performance individual dos vendedores. A ausência de uma visão consolidada impedia a tomada de decisão ágil e baseada em evidências, limitando o potencial de crescimento e a otimização das estratégias de vendas.

# 📌 Objetivo do Projeto
O objetivo principal deste projeto é desenvolver uma solução analítica ponta a ponta, utilizando SQL e Python, para extrair, transformar e analisar os dados de vendas do e-commerce. A intenção é demonstrar a capacidade de responder a perguntas de negócio complexas por meio de consultas estruturadas e manipulação de dados, gerando insights acionáveis. Ao resolver esse problema, o projeto visa fornecer uma base sólida para a tomada de decisão gerencial, permitindo a identificação de oportunidades de aumento de receita, otimização de portfólio de produtos e direcionamento de campanhas de marketing. O retorno financeiro esperado inclui o aumento do ticket médio e a maximização do faturamento por meio do foco nos produtos e categorias de maior rentabilidade.

# 💡 Estratégia da Solução
A estratégia adotada para solucionar o problema de negócio baseou-se em uma abordagem de engenharia analítica e análise exploratória de dados. O plano de desenvolvimento foi estruturado nas seguintes etapas:
1.  **Configuração do Ambiente:** Criação de um ambiente virtual isolado (`venv`) e utilização do Jupyter Notebook integrado ao Visual Studio Code para garantir a reprodutibilidade e organização do código.
2.  **Extração e Preparação de Dados (Python):** Leitura do arquivo CSV bruto utilizando a biblioteca `pandas`, com tratamento adequado de tipos de dados, como a conversão de datas (`parse_dates`).
3.  **Modelagem e Consultas (SQL):** Criação de um banco de dados SQLite em memória para simular um ambiente relacional leve e rápido. Os dados foram importados para o banco e consultas SQL foram elaboradas para calcular métricas-chave, como faturamento total, ticket médio e rankings de vendas.
4.  **Análise e Visualização (Python):** Retorno aos dados em Python para realizar agrupamentos (`groupby`), agregações e ordenações, validando os resultados do SQL. Geração de visualizações gráficas utilizando `matplotlib` para facilitar a interpretação dos insights.
5.  **Consolidação de Resultados:** Exportação de uma tabela resumo de vendas em formato CSV, pronta para ser consumida por ferramentas de Business Intelligence (BI) ou relatórios gerenciais.

# 🛠️ Tecnologias Utilizadas
As ferramentas e tecnologias empregadas neste projeto foram selecionadas para demonstrar proficiência em análise de dados e engenharia de dados júnior, alinhadas com as demandas do mercado:
*   **Linguagens de Programação:** Python, SQL
*   **Bibliotecas de Manipulação de Dados:** pandas
*   **Bibliotecas de Visualização:** matplotlib
*   **Banco de Dados:** SQLite (em memória)
*   **Ambiente de Desenvolvimento:** Visual Studio Code (VS Code), Jupyter Notebook
*   **Gerenciamento de Ambiente:** venv, pip

# ⚙️ Etapas do Projeto
*   **Etapa 1: Configuração e Ingestão de Dados:** Preparação do ambiente de desenvolvimento, leitura do dataset bruto (CSV) com `pandas` e inspeção inicial da estrutura e qualidade dos dados.
*   **Etapa 2: Integração Python-SQL:** Criação de um banco de dados SQLite em memória e transferência dos dados do DataFrame para uma tabela relacional, estabelecendo a base para as consultas analíticas.
*   **Etapa 3: Análise de Faturamento com SQL:** Desenvolvimento de queries SQL para responder às perguntas de negócio, calculando o faturamento por produto, categoria, vendedor e mês, além de identificar o ticket médio por cliente e as cidades com maior volume de vendas.
*   **Etapa 4: Análise Exploratória com Python:** Utilização do `pandas` para replicar e expandir as análises feitas em SQL, aplicando funções de agrupamento (`groupby`) e agregação para consolidar as métricas.
*   **Etapa 5: Visualização e Exportação:** Criação de gráficos com `matplotlib` para ilustrar os principais achados e exportação de uma tabela resumo de vendas consolidada para uso futuro.

# 🧠 Principais Insights
Durante o desenvolvimento do projeto, as seguintes hipóteses foram avaliadas e insights foram gerados:
*   **Concentração de Receita:** A análise revelou que uma pequena parcela dos produtos (Top 5) é responsável por uma fatia desproporcional do faturamento total, indicando a necessidade de garantir o estoque e focar o marketing nesses itens "curva A".
*   **Desempenho por Categoria:** Identificou-se que determinadas categorias de produtos possuem um ticket médio significativamente superior, sugerindo oportunidades para campanhas de *cross-selling* e *up-selling*.
*   **Performance de Vendas:** A avaliação do faturamento por vendedor destacou disparidades de desempenho, fornecendo dados concretos para programas de treinamento ou reestruturação de metas e comissões.
*   **Geografia das Vendas:** A análise por cidade permitiu mapear as regiões com maior volume de faturamento, direcionando potenciais investimentos em logística e campanhas regionais.

# 📈 Resultados
Os resultados alcançados superaram as expectativas iniciais do projeto. A solução desenvolvida não apenas respondeu a todas as perguntas de negócio propostas de forma eficiente, mas também estabeleceu um pipeline de dados reprodutível e bem documentado. A integração fluida entre Python e SQL demonstrou a capacidade de utilizar a ferramenta certa para cada etapa do processo analítico. A geração da tabela resumo de vendas e das visualizações gráficas forneceu artefatos tangíveis e de alto valor agregado para a tomada de decisão gerencial.

# 📌 Conclusão
A conclusão deste projeto é altamente positiva. A aplicação conjunta de SQL e Python provou ser uma abordagem robusta e flexível para a análise de dados de e-commerce. O projeto demonstrou com sucesso a capacidade de extrair valor de dados brutos, transformando-os em insights estratégicos por meio de técnicas de manipulação, agregação e visualização. A estruturação do código em um Jupyter Notebook, aliada ao uso de um banco de dados em memória, evidenciou boas práticas de engenharia analítica, tornando o projeto um excelente caso de uso para portfólio nas áreas de Análise e Engenharia de Dados.

# 🔗 Próximos Passos
Caso houvesse mais tempo para aprimorar e expandir este projeto, as seguintes iniciativas seriam priorizadas:
*   **Automação do Pipeline:** Implementar um script de automação (ex: Apache Airflow ou cron jobs) para executar a ingestão e processamento dos dados periodicamente.
*   **Modelagem de Dados Avançada:** Estruturar o banco de dados em um modelo dimensional (Star Schema), separando tabelas de fatos (vendas) e dimensões (clientes, produtos, tempo) para otimizar consultas complexas.
*   **Dashboard Interativo:** Conectar a tabela resumo exportada a uma ferramenta de BI (como Power BI, Tableau ou Metabase) para criar um painel gerencial dinâmico e interativo.
*   **Análise Preditiva:** Aplicar algoritmos de Machine Learning (ex: regressão linear ou séries temporais) para prever o faturamento futuro com base no histórico de vendas.
*   **Análise de Cohort:** Desenvolver análises de retenção de clientes (cohort) para entender o comportamento de recompra ao longo do tempo.

---

# 👨‍💻 Autor

[Tiago Almeida](https://github.com/tiagodalmeida87)

Desenvolvido como **projeto de portfólio de Análise de Dados e Business Intelligence**.

📧 Entre em contato via [LinkedIn](https://www.linkedin.com/in/tiago-l-almeida)

---

# 📜 Licença

Este projeto é de uso livre para fins educacionais e de portfólio.  