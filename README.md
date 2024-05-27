# Projeto: Análise e Transformação de Dados de Filmes e Avaliações com Apache Spark

Este repositório contém um projeto de análise de dados utilizando Apache Spark, com foco em ETL (Extração, Transformação e Carga) de dados de filmes e avaliações. O objetivo é limpar e transformar os dados, produzindo três resultados analíticos que respondem a casos de uso específicos.

## Dados Utilizados

Os dados utilizados no projeto consistem em dois conjuntos principais:
- **Filmes**: Contém informações sobre os filmes.
- **Avaliações**: Contém avaliações dos filmes realizadas pelos usuários.

Ambos os arquivos estão disponíveis no repositório para consulta e verificação.

## Objetivos e Casos de Uso

O projeto visa abordar três casos de uso principais:

1. **Top 10 Filmes Mais Votados**: Gerar uma tabela com os 10 filmes que receberam o maior número de votos.
2. **Top 10 Filmes Populares Não Lançados**: Gerar uma tabela com os 10 filmes mais populares que ainda não foram lançados.
3. **Distribuição de Avaliações**: Gerar uma tabela que conta o número de avaliações para cada nota.

## Processo de ETL

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

## Como Utilizar

Para reproduzir o projeto e visualizar os resultados, siga os passos abaixo:

1. Clone o repositório:
   ```sh
   git clone https://github.com/AnandaEllenmrs/USE_CASES_SPARK.git
   ```
2. Navegue até o diretório do projeto:
   ```sh
   cd USE_CASES_SPARK
   ```
3. Siga as instruções no arquivo README.md para configurar o ambiente e executar o pipeline de ETL.

## Conclusão

Este projeto demonstra como o Apache Spark pode ser utilizado para processar e analisar grandes volumes de dados de forma eficiente. Através das etapas de ETL, os dados brutos são transformados em informações valiosas, permitindo insights sobre os filmes mais votados, os filmes populares ainda não lançados e a distribuição das avaliações.

