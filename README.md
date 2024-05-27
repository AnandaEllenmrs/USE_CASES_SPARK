# Projeto: Análise e Transformação de Dados de Filmes e Avaliações com Apache Spark

Este repositório contém um projeto de análise de dados utilizando Apache Spark, com foco em ETL (Extração, Transformação e Carga) de dados de filmes e avaliações. O objetivo é limpar e transformar os dados, produzindo três resultados analíticos que respondem a casos de uso específicos.

## 📊 Dados Utilizados

Os dados utilizados no projeto consistem em dois conjuntos principais:
- **Filmes**: Contém informações sobre os filmes.
- **Avaliações**: Contém avaliações dos filmes realizadas pelos usuários.

Ambos os arquivos estão disponíveis no repositório para consulta e verificação.

## 🎯 Objetivos e Casos de Uso

O projeto visa abordar três casos de uso principais:

1. **Top 10 Filmes Mais Votados**: Gerar uma tabela com os 10 filmes que receberam o maior número de votos.
2. **Top 10 Filmes Populares Não Lançados**: Gerar uma tabela com os 10 filmes mais populares que ainda não foram lançados.
3. **Distribuição de Avaliações**: Gerar uma tabela que conta o número de avaliações para cada nota.

## 🛠️ Processo de ETL

O processo de ETL foi conduzido em várias etapas, detalhadas a seguir:

1. **Criação do Database**: Inicialmente, cria-se o database que será utilizado ao longo do processo.
2. **Listagem dos Arquivos Carregados**: Verificação e listagem dos arquivos de dados que foram carregados.
3. **Criação de DataFrames**: Leitura dos arquivos JSON e criação dos DataFrames correspondentes.
4. **Camada Bronze**: Formatação dos DataFrames para o formato Delta, criando a camada Bronze.
5. **Listagem da Camada Bronze**: Visualização dos dados formatados na camada Bronze.
6. **Início da Camada Silver**: Seleção das principais colunas a serem utilizadas para análises futuras.
7. **Camada Silver - Tabela Filmes**: Realização de alterações necessárias na tabela de filmes.
8. **Camada Silver - Tabela Avaliações**: Realização de alterações necessárias na tabela de avaliações.
9. **Camada Silver - Junção e Carregamento**: Criação da tabela combinada `avaliacao_filmes` através de JOIN.
10. **Camada Gold - Top 10 Filmes Mais Votados**: Criação da tabela com os 10 filmes mais votados.
11. **Camada Gold - Top 10 Filmes Populares Não Lançados**: Criação da tabela com os 10 filmes mais populares que ainda não foram lançados.
12. **Camada Gold - Distribuição de Avaliações**: Criação da tabela que conta o número de avaliações para cada nota.
13. **Acesso Fácil às Tabelas Gold**: Disponibilização das tabelas gold para acesso fácil e rápido.

## 🚀 Como Executar o Processo ETL

Para executar o processo ETL deste projeto, siga estas etapas:


1. Clone o repositório para sua máquina local:

   ```bash
   git clone https://github.com/AnandaEllenmrs/USE_CASES_PRONTO.dbc


## 🚀 Como Executar o Processo ETL

Para executar o processo ETL deste projeto, siga estas etapas:

1. **Instale e Configure o Apache Spark**:
   Certifique-se de ter o Apache Spark instalado e configurado.
   Instruções de instalação estão disponíveis [aqui](https://spark.apache.org/docs/latest/).

2. **Importe o Arquivo USE_CASES_PRONTO.dbc no Databricks**:
   - Acesse sua conta no Databricks.
   - Vá para "Workspace" e clique em "Import".
   - Selecione "File" e carregue o arquivo USE_CASES_PRONTO.dbc do repositório clonado.

3. **Execute os Notebooks**:
   Após a importação, execute os notebooks na ordem apresentada para garantir que o processo ETL seja realizado corretamente:
   - Notebook 1: Criação do Database e Listagem dos Arquivos Carregados.
   - Notebook 2: Criação dos DataFrames a partir dos arquivos JSON.
   - Notebook 3: Processamento e Armazenamento na Camada Bronze.
   - Notebook 4: Seleção e Transformação dos Dados na Camada Silver.
   - Notebook 5: Junção das Tabelas e Criação da Tabela avaliacao_filmes.
   - Notebook 6: Geração das Tabelas na Camada Gold com os resultados finais.

4. **Verifique os Resultados**:
   Verifique as tabelas geradas na camada Gold para obter insights como:
   - Os 10 filmes mais votados.
   - Os 10 filmes mais populares não lançados.
   - A contagem de avaliações por nota.


