# Data engineering capstone

## BigData Airlines

A X irá atender um novo cliente, a _BigData Airlines_, e você será o engenheiro de dados responsável por fazer a ingestão de dados e preparar algumas tabelas para os cientistas de dados e analistas de dados. 

### Capstone

- Carregar os dados de VRA
  - Normalizar o cabeçalho para snake case
  - Salvar estes dados
- Carregar dos dados de AIR_CIA
  - Normalizar o cabeçalho para snake case
  - Separar a coluna 'ICAO IATA' em duas colunas, seu conteúdo está separado por espaço e pode não conter o código IATA, caso não contenha o código IATA, deixe o valor nulo.
  - Salvar estes dados
- Criar nova tabela aerodromos
  - Através da API [https://rapidapi.com/Active-api/api/airport-info/]() trazer os aeródramos através do código ICAO presente nos dados de VRA.
  - Salvar estes dados
- Criar as seguintes views (Priorize o uso de SQL para esta parte):
  - Para cada companhia aérea trazer a rota mais utilizada com as seguintes informações:
    - Razão social da companhia aérea
    - Nome Aeroporto de Origem
    - ICAO do aeroporto de origem
    - Estado/UF do aeroporto de origem
    - Nome do Aeroporto de Destino
    - ICAO do Aeroporto de destino
    - Estado/UF do aeroporto de destino
  - Para cada aeroporto trazer a companhia aérea com maior atuação no ano com as seguintes informações:
    - Nome do Aeroporto
    - ICAO do Aeroporto
    - Razão social da Companhia Aérea
    - Quantidade de Rotas à partir daquele aeroporto
    - Quantidade de Rotas com destino àquele aeroporto
    - Quantidade total de pousos e decolagens naquele aeroporto

#### Extras:
  - Descrever qual estratégia você usaria para ingerir estes dados de forma incremental caso precise capturar esses dados a cada mes?
  - Justifique em cada etapa sobre a escalabilidade da tecnologia utilizada.
  - Justifique as camadas utilizadas durante o processo de ingestão até a disponibilização dos dados.

