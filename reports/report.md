# Relatório Inicial da Análise de Dados

1. Objetivo do Projeto

Plataformas de mobilidade urbana enfrentam desafios relacionados à oferta e demanda de motoristas, cancelamentos de corridas e variação de preços. A análise desses dados é fundamental para otimizar a operação e melhorar a experiência dos usuários.

O objetivo deste projeto é realizar uma análise exploratória de dados (EDA) em um dataset de corridas de transporte urbano (similar a serviços de ride-hailing), com o intuito de identificar padrões relacionados a:

- status das corridas
- cancelamentos
- comportamento dos usuários
- desempenho dos motoristas
- geração de receita

A análise permitirá compreender fatores que influenciam cancelamentos, avaliações e faturamento das corridas.

---

## 2. Descrição do Dataset

O dataset contém 150.000 registros e 21 variáveis, representando informações sobre corridas realizadas em uma plataforma de mobilidade.

Principais tipos de informação presentes no dataset:

- identificação da corrida
- horário e data
- tipo de veículo
- local de origem e destino
- status da corrida
- distância percorrida
- valor da corrida
- avaliações de clientes e motoristas
- motivos de cancelamento

---

## 3. Estrutura das Variáveis

As variáveis do dataset podem ser classificadas em quatro categorias principais:

### Variáveis temporais

- Date
- Time

### Variáveis identificadoras

- Booking ID
- Customer ID

### Variáveis categóricas

- Booking Status
- Vehicle Type
- Pickup Location
- Drop Location
- Payment Method
- Reason for cancelling by Customer
- Driver Cancellation Reason
- Incomplete Rides Reason

### Variáveis numéricas

- Avg VTAT
- Avg CTAT
- Cancelled Rides by Customer
- Cancelled Rides by Driver
- Incomplete Rides
- Booking Value
- Ride Distance
- Driver Ratings
- Customer Rating

---

## 4. Problemas identificados nos dados

Durante a inspeção inicial do dataset foram identificados:

- valores ausentes em múltiplas variáveis
- variáveis categóricas com valores faltantes
- valores numéricos ausentes associados a corridas não concluídas

Esses problemas exigiram um processo de limpeza e imputação de dados antes da realização da análise exploratória.

---

## 5. Estratégia de Tratamento de Dados Ausentes

Foram aplicadas diferentes estratégias de imputação conforme o tipo de variável:

- Média para variáveis contínuas relacionadas ao tempo

- Mediana para variáveis de avaliação

- Plataformas de mobilidade urbana enfrentam desafios relacionados à oferta e demanda de motoristas, cancelamentos de corridas e variação de preços. A análise desses dados é fundamental para otimizar a operação e melhorar a experiência dos usuários.

- Categoria "No Reason" para variáveis categóricas com ausência de motivo

Após o tratamento, o dataset ficou livre de valores ausentes.

### 5.1 Tratamento de Outliers

Foi realizada a análise de outliers nas variáveis numéricas, especialmente em `Booking Value` e `Ride distance`. Valores iguais a zero foram utilizados para variáveis associadas a corridas não concluídas, como Booking Value e Ride Distance, representando ausência de faturamento e deslocamento, respectivamente.

---

## 6. Estrutura Analítica do Projeto

A análise será conduzida nas seguintes etapas:

### 1. Entendimento dos dados

- estrutura do dataset

- tipos de variáveis

- identificação de valores ausentes

### 2. Limpeza e preparação dos dados

- tratamento de valores ausentes

- padronização de variáveis

- criação de novas variáveis se necessário

### 3. Análise exploratória

- distribuição das corridas por status

- análise de cancelamentos

- análise de receita

- análise por tipo de veículo

- análise por localização

- análise de avaliações

---

### 4. Identificação de insights

- padrões de cancelamento

- comportamento dos clientes

- fatores que impactam a receita

- avaliação dos motoristas

- avaliação dos clientes

- horarios de maior demanda

- dias da semana com maior demanda

- regioes com maior e menor demanda

- motivos de cancelamento

---

## 7. Próximos passos da análise

Após a etapa de preparação e tratamento dos dados, será realizada uma Análise Exploratória de Dados (EDA) com o objetivo de identificar padrões, tendências e possíveis problemas operacionais na plataforma de mobilidade.

As análises serão conduzidas para responder às seguintes questões:

### Comportamento das corridas

- Qual a taxa de cancelamento das corridas?

- Quais regiões apresentam maior número de corridas?

- Quais dias da semana possuem maior demanda?

- Quais horários concentram o maior volume de corridas?

### Oferta de motoristas

- Existem regiões onde faltam motoristas?

- Em quais locais ocorre maior frequência de corridas sem motorista disponível (No Driver Found)?

### Cancelamentos

- Qual percentual de corridas não são concluídas?

- Qual tipo de veículo tem maior taxa de cancelamento?

- Existe relação entre tempo de espera (Avg VTAT) e cancelamento?

- Quais são os principais motivos de cancelamento por parte dos clientes?

- Quais são os principais motivos de cancelamento por parte dos motoristas?

- Existe algum padrão de cancelamento associado a localização, horário ou tipo de veículo?

### Receita e desempenho da plataforma

- Quais tipos de veículos geram maior receita?

- Existe relação entre distância da corrida e valor pago?

- Existe relação entre o tipo de veículo e o valor da corida?

### Experiência do usuário

- Como estão distribuídas as avaliações dos motoristas?

- Existe relação entre tipo de corrida e avaliações recebidas?

### Características das corridas

- Corridas curtas são mais frequentes do que corridas longas?

- Qual a distância média das corridas?

- Qual dia da semana a distância das corridas são maiores?

- Qual horario do dia possui corridas mais curta e maior valor?

---

## Objetivo da análise

Responder a essas perguntas permitirá gerar insights relevantes sobre o funcionamento da plataforma, como:

- identificação de regiões com desequilíbrio entre oferta e demanda

- compreensão dos principais fatores que levam ao cancelamento de corridas

- análise dos padrões de demanda ao longo do tempo

- avaliação do impacto da distância e do tipo de veículo na geração de receita

Esses insights podem contribuir para melhorar a eficiência operacional da plataforma e a experiência dos usuários.

---

## 8. Ferramentas utilizadas

As principais ferramentas utilizadas no projeto incluem:

- Python (linguagem princiapla)

- Pandas (manipulação de dados)

- NumPy (Operações numéricas e estatisticas)

- Matplotlib e Seaborn (Visualização dos dados)

---

## Conclusão

Com os dados devidamente tratados e estruturados, o dataset encontra-se pronto para a realização da Análise Exploratória de Dados (EDA), etapa fundamental para identificar padrões, gerar insights e apoiar futuras análises ou modelos preditivos e tomada de decisão orientada a dados.