# Projeto: Manutenção Preditiva de Zero-Downtime: previsão de falhas em sistemas críticos antes que elas ocorram, utilizando dados de sensores e modelos analíticos para evitar paradas não planejadas.

### 1. Identificação do Grupo
* **Instituição:** Faculdade Engenheiro Salvador Arena (FESA) / UNICID
* **Curso:** Engenharia de Controle e Automação - ECA10
* **Grupo:** Manutenção Preditiva de Zero-Downtime: previsão de falhas em sistemas críticos antes que elas ocorram, utilizando dados de sensores e modelos analíticos para evitar paradas não planejadas.
* **Integrantes:**
    * Carlos Eduardo Gatto - RA: 062210029
    * Luiz Felipe Farias Mota - RA: 062210027
    * Raphaella Souza de Moraes - RA: 062210010
    * Vinicius Makimoto de Freitas - RA: 062210026
    * Yago Patrick Gomide Oliveira Ortolan - RA: 062210028

---

### 2. Área Problema Selecionada
O grupo seleciona uma das áreas norteadoras abaixo para o desenvolvimento do projeto:
* [x] Manutenção Preditiva de Zero-Downtime
* [ ] Eficiência Energética e Descarbonização via Smart Grids
* [ ] Controle de Qualidade Autônomo com Visão Computacional
* [ ] Gêmeos Digitais (Digital Twins) e Analytics em Tempo Real

---

### 3. Diagnóstico e Definição do Problema
Esta seção apresenta a fundamentação do desafio. O grupo descreve o cenário de atuação e justifica a importância da solução proposta.
* **Contexto:** O projeto aborda o cenário da indústria 4.0 e da manutenção preditiva em máquinas industriais, no qual dados operacionais de sensores são utilizados para monitorar o desempenho dos equipamentos e apoiar decisões mais inteligentes de manutenção..
* **Problema:** A dificuldade central reside em identificar, com antecedência, padrões de operação que indiquem risco de falha, já que muitas vezes defeitos mecânicos ou operacionais só são percebidos quando a máquina já apresenta perda de desempenho ou parada não planejada.
* **Impacto:** A solução visa otimizar a confiabilidade operacional, a disponibilidade dos equipamentos e o planejamento da manutenção, contribuindo para a redução de custos, diminuição de paradas inesperadas e aumento da eficiência do processo industrial.

---

### 4. Arquitetura de Dados (Fonte e Dataset)
O projeto utiliza dados estruturados para alimentar os modelos preditivos.
* **Origem dos Dados:** https://www.kaggle.com/datasets/nair26/predictive-maintenance-of-machines?resource=download
* **Características:** O conjunto de dados apresenta variáveis como UDI (identificador único), Product ID, Type (tipo da máquina), Air Temperature (K), Process Temperature (K), Rotational Speed (rpm), Torque (Nm), Vibration Levels, Operational Hours e Failure Type (tipo de falha). Trata-se, portanto, de uma base com variáveis numéricas e categóricas voltadas ao monitoramento operacional e à análise de falhas em máquinas.
* **Volume:** O dataset conta com 500 registros e 10 atributos técnicos.

---

### 5. Plano de Tratamento de Dados (ETL)
O pipeline de dados segue as seguintes etapas de processamento:
1. **Extração:** A ingestão ocorre por meio de arquivo CSV obtido a partir do dataset selecionado no Kaggle e importado para o ambiente Google Colab para leitura com Python.
2. **Transformação:** O grupo realiza a inspeção e limpeza dos dados, incluindo verificação de valores ausentes, identificação de registros duplicados, análise de outliers e padronização dos nomes das colunas. Também podem ser aplicadas transformações complementares, como criação de variáveis derivadas e organização dos tipos de dados para análise.
3. **Carga:** Os dados tratados são disponibilizados na pasta `/data/processed` para consumo dos modelos de Machine Learning.

---

### 6. Estrutura do Repositório
A organização das pastas facilita a manutenção e o versionamento do projeto:
* `/docs`: Contém os diagramas de fluxo de dados e a documentação técnica.
* `/data/raw`: Armazena os arquivos de dados originais (não modificados).
* `/data/processed`: Armazena os dados após a execução do script de ETL.
* `/scripts`: Contém os códigos Python responsáveis pelo tratamento dos dados.
* `requirements.txt`: Lista todas as bibliotecas necessárias para a execução do projeto.

---

### 7. Instruções para Execução
Para reproduzir o ambiente de dados e executar o pipeline de ETL:
1. Clona-se este repositório.
2. Instalam-se as dependências através do comando:
   ```bash
   pip install -r requirements.txt
