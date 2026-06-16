# README - Diretório `data`

Este diretório contém os artefatos e a documentação técnica detalhada do projeto de **Análise de Vendas de E-commerce com SQL e Python**. Aqui, você encontrará as instruções para replicar a análise, entender a lógica por trás das consultas SQL e do processamento em Python, e interpretar os insights de negócio gerados.

## Visão Geral
O objetivo deste projeto é demonstrar a capacidade de transformar dados brutos de vendas de e-commerce em informações estratégicas e acionáveis. Através da integração de SQL para consultas robustas e Python para manipulação e visualização, o projeto simula um cenário real de análise de dados, focando na resolução de problemas de negócio e na geração de valor.

## Estrutura do Projeto
O diretório `data` é o coração analítico do projeto, contendo os scripts e os resultados intermediários que alimentam as análises. Embora o arquivo CSV original não esteja incluído por questões de tamanho ou privacidade, os outputs gerados a partir dele são a base para a compreensão do fluxo de trabalho.

## Parte 1: Análise de Dados com SQL
Nesta etapa, utilizamos **SQL** para realizar consultas e agregações diretamente sobre os dados de vendas. Para simular um ambiente de banco de dados leve e reprodutível, os dados foram carregados em um banco de dados **SQLite em memória** via Python. As queries foram projetadas para responder a perguntas de negócio fundamentais:

### Perguntas de Negócio e Queries SQL:

1.  **Faturamento Total por Produto:**
    ```sql
    SELECT 
        produto, 
        ROUND(SUM(quantidade * preco_unitario), 2) AS faturamento_total
    FROM vendas
    GROUP BY produto
    ORDER BY faturamento_total DESC;
    ```
    *   **Objetivo:** Identificar os produtos mais rentáveis para otimização de estoque e estratégias de marketing.

2.  **Faturamento Total por Categoria:**
    ```sql
    SELECT 
        categoria, 
        ROUND(SUM(quantidade * preco_unitario), 2) AS Fat_total_Cat
    FROM vendas
    GROUP BY categoria
    ORDER BY Fat_total_Cat DESC;
    ```
    *   **Objetivo:** Entender quais categorias de produtos geram mais receita e direcionar investimentos.

3.  **Ticket Médio por Cliente:**
    ```sql
    SELECT 
        cliente,
        COUNT(id_venda) AS total_compras,
        ROUND(SUM(quantidade * preco_unitario), 2) AS faturamento_total,
        ROUND(SUM(quantidade * preco_unitario) / COUNT(*), 2) AS ticket_medio
    FROM vendas
    GROUP BY cliente
    ORDER BY ticket_medio DESC
    LIMIT 10;
    ```
    *   **Objetivo:** Identificar clientes de alto valor para programas de fidelidade e ofertas personalizadas.

4.  **Faturamento Total por Vendedor:**
    ```sql
    SELECT 
        vendedor,
        ROUND(SUM(quantidade * preco_unitario), 2) AS faturamento_total
    FROM vendas
    GROUP BY vendedor
    ORDER BY faturamento_total DESC;
    ```
    *   **Objetivo:** Avaliar a performance individual dos vendedores e identificar oportunidades de treinamento.

5.  **Faturamento por Mês:**
    ```sql
    SELECT 
        STRFTIME('%Y-%m', data_venda) AS mes_ano,
        ROUND(SUM(quantidade * preco_unitario), 2) AS faturamento_total
    FROM vendas
    GROUP BY mes_ano
    ORDER BY mes_ano;
    ```
    *   **Objetivo:** Analisar tendências sazonais e o desempenho de vendas ao longo do tempo.

## Parte 2: Processamento e Visualização com Python
Após as consultas SQL, a análise prossegue com **Python**, utilizando a biblioteca `pandas` para manipulação de dados e `matplotlib`/`seaborn` para visualização. Esta etapa valida os resultados do SQL e os transforma em gráficos compreensíveis.

### Tarefas em Python:

1.  **Criação da Coluna de Faturamento:**
    *   Uma nova coluna `faturamento` é calculada como `quantidade * preco_unitario` para cada transação.

2.  **Agrupamento e Agregação:**
    *   Os dados são agrupados por `produto`, `categoria` e `cliente` para consolidar o faturamento total e outras métricas, replicando e expandindo as análises SQL.

3.  **Visualização de Dados:**
    *   Gráficos de barras são gerados para ilustrar o faturamento por produto, a performance de vendedores e o ticket médio dos clientes. Essas visualizações facilitam a interpretação dos dados e a comunicação dos insights.

4.  **Exportação de Tabela Resumo:**
    *   Uma tabela resumo de vendas é exportada para um arquivo CSV, pronta para ser integrada a outras ferramentas de BI ou para relatórios gerenciais.

## Parte 3: Insights de Negócio
Os insights gerados a partir desta análise são cruciais para a tomada de decisões estratégicas:

*   **Concentração de Receita:** Produtos como 
Notebook, Mesa e Monitor são os principais motores de faturamento, exigindo atenção especial na gestão de estoque e marketing.
*   **Categorias de Alta Performance:** Eletrônicos e Móveis dominam o faturamento, indicando onde os esforços de expansão e otimização de portfólio devem ser concentrados.
*   **Clientes de Alto Valor:** A identificação dos clientes com maior ticket médio permite a criação de estratégias de fidelização e ofertas personalizadas para maximizar o Lifetime Value (LTV).
*   **Performance de Vendedores:** A análise individual dos vendedores pode subsidiar programas de incentivo, treinamento e realinhamento de metas.

## Como Replicar
Para replicar este projeto, você precisará de um ambiente Python com as bibliotecas `pandas`, `matplotlib` e `seaborn` instaladas. O código original foi desenvolvido em um Jupyter Notebook e pode ser executado em um ambiente como o Visual Studio Code.

1.  **Instale as dependências:**
    ```bash
    pip install pandas matplotlib seaborn
    ```
2.  **Execute o notebook:** Abra o arquivo `analise_ecommerce.ipynb` em um ambiente compatível (e.g., VS Code com extensão Jupyter) e execute as células sequencialmente.
3.  **Gere os dados de resumo:** O script `recreate_data.py` pode ser usado para gerar os arquivos CSV de resumo (`faturamento_produto.csv`, `faturamento_vendedor.csv`, `ticket_medio_cliente.csv`) que são utilizados para a geração dos gráficos e relatórios.
    ```bash
    python recreate_data.py
    ```
4.  **Gere os gráficos:** O script `generate_charts.py` irá gerar os arquivos de imagem dos gráficos (`chart_faturamento_produto.png`, `chart_faturamento_vendedor.png`, `chart_ticket_medio_cliente.png`).
    ```bash
    python generate_charts.py
    ```

Este README.md serve como um guia técnico para entender e replicar as análises, além de fornecer o contexto de negócio e os insights derivados do projeto.
